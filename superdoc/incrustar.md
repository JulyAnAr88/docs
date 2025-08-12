Edit superset_config.py 

Using nano superset_config.py and put following code in it

# This is merely a default.
FEATURE_FLAGS: dict[str, bool] = {
    'DRILL_BY': True,
    'DASHBOARD_CROSS_FILTERS': True,
    "EMBEDDABLE_CHARTS": True,
    "EMBEDDED_SUPERSET": True,
    "DASHBOARD_NATIVE_FILTERS": True,
    "DRILL_TO_DETAIL": True,
    "ENABLE_TEMPLATE_PROCESSING": True,
    "HORIZONTAL_FILTER_BAR": True,
    #"DASHBOARD_RBAC": True,
    "DASHBOARD_VIRTUALIZATION": True,
    "ALERT_REPORTS_NOTIFICATION_DRY_RUN": True,
    "ALERT_REPORTS": True,
    "TAGGING_SYSTEM": True,
    "ENABLE_JAVASCRIPT_CONTROLS":True
}

# Forzar todas las URLs a HTTPS
PREFERRED_URL_SCHEME = 'https'
ENABLE_PROXY_FIX = True
ENFORCE_SSL = False

PUBLIC_ROLE_LIKE_GAMMA = True

# Dashboard embed
GUEST_ROLE_NAME = "Gamma"
GUEST_TOKEN_JWT_SECRET = "3c7c2f380ee1e034889c7bb263d2f6850cde8a8a4151c0c4f8b2ef1f30e897e2"
GUEST_TOKEN_JWT_ALGO = "HS256"
GUEST_TOKEN_HEADER_NAME = "X-GuestToken"
GUEST_TOKEN_JWT_EXP_SECONDS = 3000 # 50 minutes

class CustomSecurityManager(SupersetSecurityManager):
	def __init__(self, appbuilder):
		super(CustomSecurityManager, self).__init__(appbuilder)
		self.ensure_roles_exist()

	def ensure_roles_exist(self):
		# Crear o obtener rol Public
		public_role = self.find_role("Public")
		if not public_role:
			public_role = self.add_role("Public")

			# Asignar permisos básicos
			permissions = [
			('read', 'DashboardModelView'),
			('dashboard', 'Superset'),
			('explore', 'Superset'),
			('can_read', 'Dashboard'), # Permiso adicional en algunas versiones
			('can_show', 'Dashboard') # Necesario en Superset 1.5+
			]

			for permission in permissions:
				try:
					self.add_permission_view(public_role, *permission)
				except Exception as e:
					print(f"Error asignando permiso {permission}: {str(e)}")

# Uncomment to setup Public role name, no authentication needed
AUTH_ROLE_PUBLIC = 'Public'

# Will allow user self registration
AUTH_USER_REGISTRATION = False

# The default user self registration role
AUTH_USER_REGISTRATION_ROLE = "Gamma"

CUSTOM_SECURITY_MANAGER = CustomSecurityManager

Adding Dataset Permissions

To add dashboard permissions, you need to add dataset permissions to the public role. Type id in the search bar in permissions to get a list of all datasets. See the screenshot below:



Once the permissions are added, open the dashboard, click on the three horizontal dots adjacent to "Edit Dashboard", click on "Share", and "Copy permalink to clipboard".

Embedding the Dashboard

Create an index.html file in a folder and copy the following code, replacing the URL with the one copied in the previous step:

<iframe src="REPLACE_YOUR_URL_HERE" height="90%" width="90%" title="Iframe Example"></iframe>

Adjust the height and width as needed. Open the HTML page in a browser, and you should see Superset loading. If you encounter any issues, feel free to contact me on LinkedIn, via email, or any other means you find comfortable.



