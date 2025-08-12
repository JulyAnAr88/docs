How to enable Superset language selection

Background Info: as of 2022-Feb-17, Superset version 1.4.1

Language Selection are disable by default, you can see that in file superset/config.py

image

So, How to enable that?

Step 1: Create a superset_config.py file

in your case you need Spanish

LANGUAGES = {
    'en': {'flag': 'us', 'name': 'English'},
    "es": {"flag": "es", "name": "Spanish"},
}

Important: You have to config AT LEAST 2 Language to enable language selection

Step 2: add superset_config.py to proper PYTHONPATH location

Like this:

image

This line put superset_config.py into proper location.

COPY superset_config.py /app/pythonpath/superset_config.py

Why /app/pythonpath/?because in Docker Image apache/superset, it set default PYTHONPATH to /app/pythonpath/

image

The result look like this

image

Habilitar Celery y Redis

Environment

1.  Python and Python-venv (Version 3.10)

2.  Postgres (Metadata db)

3.  Redis

Process is going to be same as normal installation we saw with few changes. Let's start.

sudo apt update -y & sudo apt upgrade -y

Installing Redis

sudo apt install redis-server

Install dependencies

Activate python environment

   .  superset_env/bin/activate
   pip install --upgrade setuptools pip   ```

Install python dependencies  

   pip install pillow
   pip install gunicorn
   pip install celery
   pip install geven

Edit superset_config.py using nano superset_config.py and put following code in it

 # Configuración de Redis
REDIS_HOST = 'localhost'
REDIS_PORT = 6379
REDIS_DB = 0
REDIS_PASSWORD = None # Configura si necesitas autenticación
REDIS_URL = f"redis://{f':{REDIS_PASSWORD}@' if REDIS_PASSWORD else ''}{REDIS_HOST}:{REDIS_PORT}/{REDIS_DB}"
RATELIMIT_STORAGE_URI = f"redis://{f':{REDIS_PASSWORD}@' if REDIS_PASSWORD else ''}{REDIS_HOST}:{REDIS_PORT}/{REDIS_DB}"
REDIS_RESULTS_DB = f"redis://{f':{REDIS_PASSWORD}@' if REDIS_PASSWORD else ''}{REDIS_HOST}:{REDIS_PORT}/1"

# Configuración de Celery
class CeleryConfig:
broker_url = REDIS_URL
imports = ("superset.sql_lab",
	"superset.tasks.scheduler",
	"superset.tasks.thumbnails",
	"superset.tasks.cache",)
result_backend = REDIS_RESULTS_DB
worker_prefetch_multiplier = 1
task_acks_late = False
beat_schedule = {
	"reports.scheduler": {
	"task": "reports.scheduler",
	"schedule": crontab(minute="*"),
},
"reports.prune_log": {
	"task": "reports.prune_log",
	"schedule": crontab(minute=10, hour=0),
	},
}
RESULTS_BACKEND = FileSystemCache("/app/superset_home/sqllab")
 
CACHE_CONFIG = {
	"CACHE_TYPE": "RedisCache",
	"CACHE_DEFAULT_TIMEOUT": 86400,
	"CACHE_KEY_PREFIX": "superset_",
	"CACHE_REDIS_HOST": REDIS_HOST,
	"CACHE_REDIS_PORT": REDIS_PORT,
	"CACHE_REDIS_DB": 1,
}
DATA_CACHE_CONFIG = CACHE_CONFIG
 
FILTER_STATE_CACHE_CONFIG = {
	'CACHE_TYPE': 'RedisCache',
	'CACHE_DEFAULT_TIMEOUT': 86400, # 24 horas
	'CACHE_KEY_PREFIX': 'superset_filter_cache_',
	"CACHE_REDIS_URL": f"redis://{f':{REDIS_PASSWORD}@' if REDIS_PASSWORD else ''}{REDIS_HOST}:{REDIS_PORT}/2", #"redis://localhost:6379/2", URL del servidor Redis (ajustar según tu configuración)
	"CACHE_OPTIONS": { # Opciones adicionales para Redis
		"MAX_ENTRIES": 5000, # Número máximo de entradas en la caché (opcional)
		"CULL_FREQUENCY": 3, # Frecuencia con la que Redis eliminará entradas más viejas (opcional)
	},
# Serialización de los elementos de la caché
"CODEC": "json", # Usamos JSON para serializar los datos almacenados en Redis
}
 
CELERY_CONFIG = CeleryConfig

Once Done let us initialize database with following commands

   # Create an admin user in your metadata database (use `admin` as username to be able to load the examples)
   export FLASK_APP=superset

   superset db upgrade

   # Create default roles and permissions
   superset init

Run and Test Celery

To run celery I have created a sh script that you can run in order to run the server. To create create script using following command.

   nano run_celery.sh

   and paste following code in it.

   #!/bin/bash
   export SUPERSET_CONFIG_PATH=/app/superset/superset_config.py
   . /app/superset/superset_env/bin/activate
   celery --app=superset.tasks.celery_app:app worker --pool=prefork -O fair -c 4 &
   celery --app=superset.tasks.celery_app:app beat

In above script -c 4 represents how many worker processes should run in a worker.

In order to run it we need to grant it run permission. To do that lets run following command.

   chmod +x run_celery.sh

  Lets run and test if it works?

   sh run_celery.sh

Create Celery service edit/create file `sudo nano /etc/systemd/system/celery.service` and paste following code in it

   [Unit]
   Description = Apache Celery worker Daemon
   After = network.target

   [Service]
   PIDFile = /app/superset/celery.PIDFile
   Environment=SUPERSET_HOME=/app/superset
   Environment=PYTHONPATH=/app/superset
   WorkingDirectory = /app/superset
   ExecStart = /app/superset/run_celery.sh
   ExecStop = /bin/kill -s TERM $MAINPID


   [Install]
   WantedBy=multi-user.target

once copied run following command to enable and start service

   systemctl daemon-reload
   sudo systemctl enable celery.service
   sudo systemctl start celery.service