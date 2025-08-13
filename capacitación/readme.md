# Lineamientos de trabajo

- [1. Fundamentos](#fundamentos)
- [2. Herramientas de visualización](#herramientas)
- [3. Introducción a Apache Superset](#intro)
- [4. Base de datos](#bd)
  - [4.1. Creación de una tabla](#bd1) 
  - [4.2. Datasets y gráficos](#bd2) 
    - [4.2.1. Nomenclatura](#bd21) 
    - [4.2.2. Filtros](#bd22) 
    - [4.2.3. Tabla virtual](#bd23) 
      - [4.2.3.1. Nuevo conjunto de datos desde consultas](#bd231) 
      - [4.2.3.2. Columnas calculadas](#bd232) 
- [5. Tableros (Dashboards)](#tableros)
  - [5.1. Filtros](#tableros1)
  - [5.2. Plantillas CSS](#tableros2)
- [6. Recomendaciones clave](#reco)
- [7. Referencias bibliográficas](#ref)


<h1 id="fundamentos">1. Fundamentos</h1>

Este documento pretende sentar bases generales, delimitar y guiar determinadas prácticas en pro de optimizar, garantizar la calidad, disponibilidad, integridad y seguridad de los datos de manera efectiva y responsable.

Entendiendo los datos como el principal insumo y activo dentro de una organización, donde se constituyen como el principal recurso a la hora de una toma de decisiones más informada y más eficiente para ofrecer mejores servicios, guiar actividades operacionales, tácticas y estratégicas; el valor comercial que adquieren es evidentemente significativo. En este sentido, toma una especial relevancia la manipulación y resguardo de los mismos, gestión que no debería ser externalizada al ámbito municipal. 

Cuando un programa, instrucciones y reglas informáticas para ejecutar ciertas tareas en una computadora (software) ingresa a las actividades sustantivas del Estado, adquiere una especificidad respecto de la política tecnológica tradicional dado el tenor y grado de importancia sobre lo que opera, ya que puede tratarse de información sobre la población y el territorio o transparencia de la gestión de gobierno, etc. En este sentido, el software implementado en la gestión estatal no puede tener restricciones sobre el acceso a su diseño, inspección exhaustiva de los mecanismos de funcionamiento, así como tampoco de la posibilidad de estudiarlo y poder adaptarlo a las necesidades propias. El tipo de software que se adapta a estas particularidades es el denominado Software Libre, el cual no solo se encuentra licenciado para ofrecer estas libertades, sino que expone de manera explícita las restricciones y decisiones tecnológicas, científicas y sociales que ese diseño busca regular en determinadas maneras de actuar en la realidad y de organizar la acción de los agentes humanos.

<h1 id="herramientas"> 2. Herramientas de visualización</h1>

Existen diversas y variadas herramientas diseñadas para crear tableros interactivos. Entre ellas podemos encontrar como las más populares, a saber: Tableu, Power BI, Looker Studio, que, como principal impedimento a la hora de implementarlas en nuestro ámbito laboral, tienen la condición de no ser Software Libre, forman parte de lo que se denomina software propietario. Esto implica que, además de requerir una licencia para acceder a sus versiones completas, los datos que trabajemos serán alojados en servidores de la empresa propietaria del software, con las consecuencias que esto conlleva.
Dados estos fundamentos y, principalmente, que rige una ordenanza con número 11063 que
>*“(…) tiene por objeto establecer los lineamientos de las políticas de incorporación y gestión de software, que garanticen la debida protección de la integridad, confidencialidad, accesibilidad, interoperabilidad y compatibilidad de la información y la auditabilidad de su procesamiento, en la Administración Municipal; el libre acceso ciudadano a la información pública ofrecida en formatos digitales; y la accesibilidad de los servicios que la administración preste al público empleando medios informáticos.”* (Ordenanza nro 11063, 2004, Artículo 1)

desde la Subdirección de Gobernanza de Datos es que se decide utilizar herramientas libres, particularmente Metabase, Grafana y Superset.
Si bien se pretende generalizar sobre ciertas prácticas, se brindarán ejemplos particulares sobre Superset.

<h1 id="intro"> 3. Introducción a Apache Superset </h1>

Ingresando a [Superset](https://superset.santafeciudad.gov.ar/), podrán encontrarse con la pantalla de inicio de sesión de Superset, el usuario de la imagen es solo un ejemplo. Es importante que cada persona que va a utilizar la herramienta tenga su propio usuario y por motivos de seguridad, sea de exclusivo uso personal.
<p style="width:800px; display: block; margin: 0 auto;">
   <img src="./img/1.png">
</p>

La siguiente es la pantalla de inicio, en la misma contamos con una *barra de menú*, una lista desplegable de elementos **Recientes, Dashboards, Gráficos y Consultas guardadas**:

<p style="width:800px;display: block; margin: 0 auto;">
   <img src="./img/2.png">
</p>

Este usuario no tiene aún ningún elemento a disposición, a medida que vaya creando cosas, se irán agregando a la sección correspondiente.
<p style="width:800px;display: block; margin: 0 auto;">
   <img src="./img/3.png">
</p>

Tenemos también en la esquina superior derecha opciones de **idioma**, de **Configuración** y un acceso rápido a crear los siguientes elementos:
<p style="width:200px;display: block; margin: 0 auto;">
   <img src="./img/4.png">
</p>

Si bien los nombres son descriptivos, hacemos una breve descripción de cada uno a modo de glosario:

**Conjunto de datos (dataset):** tabla o vista de base de datos.

**Datos:** desde este apartado podemos crear datasets desde bases de datos conectadas o desde un archivo con formato *.csv* o *.xlsx*.
<p style="width:300px;display: block; margin: 0 auto;">
   <img src="./img/5.png">
</p>


**Gráfico (chart):** representación visual de datos (ej: gráfico de barras, línea, mapa, tabla, etc.). En este caso, se crean a partir de un dataset y permite personalizar métricas, filtros y estilos.

**SQL:** si bien SQL es el Lenguaje de Consulta Estructurado (Structured Query Language), aquí lo utilizan en el menú para dirigir a un apartado donde se pueden realizar consultas, modificar y eliminar datos en las bases de datos, así como también guardar esas consultas y acceder al historial.
<p style="width:200px;display: block; margin: 0 auto;">
   <img src="./img/6.png">
</p>

**Tablero (Dashboard):** panel interactivo que agrupa múltiples gráficos en una sola vista. Permite analizar datos desde diferentes perspectivas y compartir el conocimiento que de allí surge.

Luego de familiarizarse con la herramienta, para comenzar a trabajar vamos a necesitar importar nuestros datos.
<h1 id="bd"> 4. Base de datos </h1>

Siendo el objetivo principal la realización de análisis exploratorios, es primordial constituir una agregación consistente de datos donde se evite la redundancia e inconsistencia, se facilite la accesibilidad y se eviten problemas de seguridad e integridad, para ello se recomienda constituir bases de datos relacionales bajo la que es hasta hoy día, la manera más efectiva de reflejo de la realidad para estos análisis: el modelado dimensional.

La Base de Datos será alojada en servidores propios sobre el motor PostgreSQL, también de licencia abierta y libre. No se tendrá vínculo directo con el motor, sino que, en este caso, utilizaremos como intermediario o “sistema de manejo” al mismo Superset.
<h2 id="bd1"> 4.1 Creación de una tabla </h2> 
Independientemente del modelado de la información, se mostrará a continuación cómo realizar la ingesta de datos para ponerlas a disposición de la herramienta.

Como recomendaciones generales, se sugiere nombrar las tablas en singular con denominaciones representativas y claras.

Se intentará ejemplificar utilizando datos brindados por el sector.

A fines prácticos, asumiremos cada archivo como una tabla. Como se indicó anteriormente, lo ideal es contar con la información modelada, pero se tiene en cuenta también que este es el último paso antes de la creación de tableros, por lo que puede considerarse esta presentación de datos como primitiva para un posterior refinamiento y modelado.

Como mencionamos previamente, desde el botón **+** accedemos a `Datos → Upload Excel to Dataset` desde donde se nos presentará el siguiente cuadro:

<p align="center" style="height:450px">
   <img src="./img/7.png">
</p>

Desde el botón `SELECT`, elegimos el archivo, en este caso seleccionamos SISA_SALA_DENGUE.xlsx. Teniendo seleccionado `Preview uploaded file`, podemos ver una vista previa de las columnas que se van a cargar, lo que sirve para comprobar que la herramienta está leyendo correctamente el archivo.
A continuación, se puede observar lo que debería quedar seleccionado siempre para los campos `BASE DE DATOS` y `ESQUEMA`. Con un conocimiento mayor sobre el conjunto de datos, se podrá elegir un nombre más adecuado para la tabla, en este caso, a fines ejemplificadores, elegimos el que se observa en la imagen 8. Se recomienda no utilizar caracteres especiales, si es necesario utilizar más de una palabra, se deberán separar por guion bajo (_).
<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin: 0 auto;">
  <div style="text-align: center;">
    <img src="./img/8.png" style="height: 500px;"><br>
    <span>Imagen 8</span>
  </div>
  <div style="text-align: center;">
    <img src="./img/9.png" style="height: 500px;"><br>
    <span>Imagen 9</span>
  </div>
</div>

Para archivos *.xlsx* se puede elegir en `SHEET NAME` el nombre de la hoja de trabajo.

En el apartado `File Settings` se puede configurar cómo debe actuar el sistema ante tablas que ya existen y valores nulos. (Imagen 9)

En `Columnas` se pueden seleccionar las mismas de manera personalizada. (Imagen 10)

Finalmente, se puede determinar si se cuenta con un encabezado, la cantidad de filas a leer y si se quieren omitir. (Imagen 11)

<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin: 0 auto;">
  <div style="text-align: center;">
    <img src="./img/10.png" style="height: 500px;"><br>
    <span>Imagen 10</span>
  </div>
  <div style="text-align: center;">
    <img src="./img/11.png" style="height: 500px;"><br>
    <span>Imagen 11</span>
  </div>
</div>

Cuando finalmente seleccionemos `UPLOAD`, tendremos nuestra tabla para comenzar nuestros análisis.
<h2 id="bd2"> 4.2 Datasets y gráficos </h2>

Ahora en el menú `Conjuntos de datos`, ya podremos ver nuestra tabla:
<p style="width:800px;display: block; margin: 0 auto;">
   <img src="./img/12.png">
</p>

Como acciones, puede editarse el conjunto y definir `MÉTRICAS` como funciones de agregación, por ejemplo, personalizar las columnas redefiniendo el tipo de dato o señalando si es un dato temporal o, definir columnas calculadas.
<p style="width:600px;display: block; margin: 0 auto;">
   <img src="./img/13.png">
</p>
Si hacemos clic directamente sobre el nombre de la tabla, accedemos a la creación de un gráfico.
<p style="width:600px;display: block; margin: 0 auto;">
   <img src="./img/14.png">
</p>
La pantalla se divide en 3 partes, la primera sección nos muestra el detalle de la tabla seleccionada, sus columnas y métricas que hayamos definido. La segunda, la configuración del gráfico que deseemos realizar.

En la parte superior de esta segunda sección, tenemos algunos de los gráficos más comunes, pero si hacemos clic en `View all charts` podremos acceder a una inmensa variedad de gráficos que Superset tiene a disposición.
<p style="width:600px;display: block; margin: 0 auto;">
   <img src="./img/15.png">
</p>
El gráfico que seleccionemos va a depender pura y exclusivamente de lo que queramos representar. Mostraremos solo a fines ilustrativos, la creación de un gráfico de barras y uno de torta.
En el mismo sentido que la elección depende de lo que se quiera representar, cada gráfico tendrá su requerimiento particular de tipo y formato de datos, por ejemplo, con este conjunto de datos no podríamos generar ningún tipo de mapa ya que no contamos con información georefenciada y/o datos espaciales.

Vamos a replicar el gráfico **CASOS NOTIFICADOS A SISA POR SEXO Y GRUPO ETARIO** de la hoja *DENGUE SISA* del reporte `REPORTE SALA DE SITUACIÓN MUNICIPALIDAD DE SANTA FE`.
<h3 id="bd21"> 4.2.1 Nomenclatura </h3>

Ya que existe un apartado desde donde acceder a todos los gráficos, para mantener una consistencia en el formato de nombres a fin de identificar rápidamente el tipo de visualización, entender su propósito sin necesidad de accederlo y facilitar la lectura y comprensión del elemento, se recomienda seguir la siguiente convención para nombres de gráficos:
- Utilizar nombres en minúsculas.
- Utilizar guiones para separar palabras en los nombres de visualizaciones.
- Utilizar nombres descriptivos para las visualizaciones.
- En caso de existir varias pestañas, utilizar como prefijo el nombre de la pestaña.
- Continuar con el tipo de visualización.
- Finalmente, nombre descriptivo y significativo de la visualización.

<span style="text-decoration: underline;">Modelo de formato de nombres</span>

\<tablero>\_<pestaña>\_<tipo-visualización>\_\<identificador>

Si utilizamos como nombre del tablero **DENGUE SISA**, el nombre de nuestro gráfico sería: *dengue-sisa_barra_casos-notificados-por-sexo-grupo-etario*, por ejemplo.
<p style="width:500px;display: block; margin: 0 auto;">
   <img src="./img/16.png">
</p>

En el apartado `Personalizar`, encontramos configuraciones propias del tipo de gráfico, en este caso: orientación de las barras y si queremos que estén apiladas, por ejemplo, títulos de los ejes, colores, etc.
<p style="width:500px;display: block; margin: 0 auto;">
   <img src="./img/17.png">
</p>

Finalmente, guardamos el gráfico y Superset nos da la opción de agregarlo a un tablero ya creado, como aún no lo tenemos, simplemente lo guardamos.
Ya tenemos nuestro primer gráfico.

<p style="width:700px;display: block; margin: 0 auto;">
   <img src="./img/18.png">
</p>

Para hacer otro, procedemos de la misma manera, seleccionando ahora el nuevo tipo y datos.
Supongamos que queremos representar ahora la columna `Ficha`

<p style="width:700px;display: block; margin: 0 auto;">
   <img src="./img/19.png">
</p>

Observamos que hay un número significativo de valores nulos. La manera de actuar ante esto dependerá de los objetivos de nuestro análisis, pero aquí lo usaremos para ejemplificar algunos procedimientos.

<h3 id="bd22"> 4.2.2 Filtros </h3>

Podemos simplemente ignorar los valores nulos, para esto, en la sección `DATOS` del gráfico, vamos hasta `FILTROS` y podemos observar que por defecto selecciona un campo de fecha, esto será explicado más adelante, lo que haremos ahora, será seleccionar nuestra dimensión `FICHA` en el cuadro de diálogo, y la condición a filtrar, en este caso, queremos que ignore los valores nulos:

<p style="width:250px;display: block; margin: 0 auto;">
   <img src="./img/20.png">
</p>


Actualizamos nuestro gráfico y solo veremos datos no nulos

<p style="width:700px;display: block; margin: 0 auto;">
   <img src="./img/21.png">
</p>

Pueden encontrarse como opciones de filtro 12 diferentes operadores, como pueden ser los numéricos (<,>, =, etc.), de lista (in, not in) o de comparación de cadenas de texto (like), los que la herramienta considera `SIMPLES`; así como también `SQL PERSONALIZADO`, donde podemos escribir directamente sentencias con cláusulas `WHERE` o `HAVING`, dejando en claro, que no es la única funcionalidad ignorar valores nulos.
<h3 id="bd23"> 4.2.3 Tabla virtual</h3>

La solución anterior solo tendrá efecto en cada gráfico que lo apliquemos, si en cambio, queremos mantener esta condición para todas las ocasiones donde se utilice este set de datos, tenemos dos maneras de proceder.
<h4 id="bd231"> 4.2.3.1 Nuevo conjunto de datos desde consultas</h4>

Desde el menú `SQL`, accedemos a `Laboratorio SQL`

<p style="width:700px;display: block; margin: 0 auto;">
   <img src="./img/22.png">
</p>

Seleccionamos principalmente Base y Esquema.
Si nuestra intención es que no aparezcan los datos con la columna FICHA vacía, nuestra consulta puede ser:
```SQL
SELECT *
FROM sisa_dengue sd
WHERE sd."FICHA" is not NULL
```
De esta manera obtenemos un recorte de nuestro conjunto de datos, el que vamos a poder utilizar guardándolo como un nuevo dataset.

<p style="width:700px;display: block; margin: 0 auto;">
   <img src="./img/23.png">
</p>

Como puede observarse, esto define un nuevo tipo de conjunto de datos, una tabla de tipo virtual.
<p style="width:600px;display: block; margin: 0 auto;">
   <img src="./img/24.png">
</p>

<h3 id="bd231"> 4.2.3.2 Columnas calculadas</h3>
Otra manera de manejar este tipo de situaciones es no ignorando las filas con valores nulos, sino, asignando un valor a estos casos.
A esto también podemos hacerlo con una consulta `SQL` como la siguiente:

```SQL
SELECT *,
    CASE WHEN "FICHA" IS NULL THEN 'SIN DATOS'
        ELSE "FICHA"
    END AS "FICHA_NEW"
FROM sisa_dengue
```

que, como podemos observar, crea una nueva columna con el nuevo valor que creamos conveniente.

<p style="width:600px;display: block; margin: 0 auto;">
   <img src="./img/25.png">
</p>

Nótese que estamos creando nuevos conjuntos de datos con cada modificación.
Si consideramos que el cambio que estamos haciendo debería ser definitivo para nuestro conjunto, y no debería haber más de un conjunto con diferencias menores, nuevamente seleccionando la acción *Editar*

<p style="width:700px;display: block; margin: 0 auto;">
   <img src="./img/26.png">
</p>

accedemos a la ventana de edición, nos dirigimos a la sección `COLUMNAS CALCULADAS`, allí, el botón `AÑADIR ELEMENTO` nos permitirá definir nuestra columna nueva con la sentencia CASE que usamos en las consultas anteriores.

<p style="width:550px;display: block; margin: 0 auto;">
   <img src="./img/27.png">
</p>

Ahora, tendremos a disposición esta columna para utilizarla donde la necesitemos.

<p style="width:400px;display: block; margin: 0 auto;">
   <img src="./img/28.png">
</p>

<h1 id="tableros"> 5. Tableros (Dashboards)</h1>
Para crear un tablero, simplemente nos dirigimos a la sección Dashboards y pulsamos el botón con el mismo nombre.
<p style="width:600px;display: block; margin: 0 auto;">
   <img src="./img/29.png">
</p>

Ya aquí, podemos agregar gráficos y elementos como pestañas, filas, columnas, encabezados, texto -el cual puede ser en formato Markdown o etiquetas HTML-.
<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin: 0 auto;">
  <div style="text-align: center;">
    <img src="./img/30.png" style="height: 400px;"><br>
    
  </div>
  <div style="text-align: center;">
    <img src="./img/31.png" style="height: 250px;"><br>
    
  </div>
</div>


Superset maneja el denominado sistema *Drag and drop*, se selecciona el elemento, se arrastra y se suelta en la ubicación donde se desee colocar.
Ya insertado el gráfico, podemos definir las propiedades con las que queremos que se visualice finalmente en el tablero.
<p style="width:550px;display: block; margin: 0 auto;">
   <img src="./img/32.png">
</p>
<p style="width:550px;display: block; margin: 0 auto;">
   <img src="./img/33.png">
</p>

Superset organiza la disposición de elementos por bloques que a su vez se separan en columnas. Cada bloque es independiente, se pueden agregar todos los elementos que se deseen, como por ejemplo separar en pestañas.

<p style="width:500px;display: block; margin: 0 auto;">
   <img src="./img/34.png">
</p>

<h2 id="tableros1">5.1 Filtros </h2>

<div style="display: flex; align-items: center; justify-content: left; gap: 20px; margin: 0 auto;">
  <span>La flecha ubicada a la izquierda del tablero</span>
  <img src="./img/35.png" style="width:20px;">
</div>

despliega la sección de filtros:
<p style="width:250px;display: block; margin: 0 auto;">
    <span></span>
    <img src="./img/36.png">
</p>

`ADD/EDIT FILTERS` despliega la siguiente ventana

<p style="width:450px;display: block; margin: 0 auto;">
    <img src="./img/37.png">
</p>

Supongamos que queremos definir un filtro por “Sexo Legal”, seleccionamos el tipo correspondiente, que en este caso es `Valor`, tipo que se corresponde con los campos de tipo texto o string.
Las otras opciones son:

<p style="width:200px;display: block; margin: 0 auto;">
    <img src="./img/38.png">
</p>


**Valor:** El filtro de valor crea un menú desplegable con todos los valores únicos disponibles para esa columna.

**Rango numérico (Numerical range):** Este filtro crea un control deslizante con dos puntos de selección para definir un rango. El punto más a la izquierda del control deslizante representa el valor más bajo disponible en esa columna, mientras que el más a la derecha representa el valor más alto.
Así es como se ve el filtro en el tablero:
<p style="width:200px;display: block; margin: 0 auto;">
    <img src="./img/39.png">
</p>

Finalmente, tenemos 3 tipos de filtros relacionados con fechas: **Período de tiempo, Columna de tiempo** y **Granularidad temporal**.

**Período de tiempo (Time Range):** aquí se despliegan diferentes opciones y formatos de fechas dentro de una amplia gama de configuraciones genéricas (como Último día, Semana pasada, Día anterior, Semana anterior, Día actual, Semana actual, etc.) disponibles para este filtro. Permitiendo también seleccionar un intervalo de tiempo personalizado. Se aplicará por igual a todos los campos tipo fecha que hayamos cargado en cada elemento o gráfico del tablero como fue explicado en la sección 3.2.2, si no indicamos ninguno, el filtro no tendrá ningún efecto.

**Granularidad temporal (Time Grain):** En éste se puede definir la granularidad, como su título lo indica, de la siguiente manera:
<p style="width:150px;display: block; margin: 0 auto;">
    <img src="./img/40.png">
</p>

**Columna de tiempo (Time Column):** Con éste, seleccionamos una columna del dataset sobre el que estamos trabajando, por ejemplo:
<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin: 0 auto;">
  <div style="text-align: center;">
    <img src="./img/41.png" style="height: 150px;"><br>
    
  </div>
  <div style="text-align: center;">
    <img src="./img/42.png" style="height:150px;"><br>
    
  </div>
</div>

El cual nos trae un solo valor, ya que es la única columna de tipo fecha que tenemos.
Para este filtro, no necesitamos cargar previamente el campo en el gráfico, el uso común y recomendado es cuando se tienen múltiples columnas de fecha, se selecciona una con este filtro y luego se define la temporalidad con el **Período de tiempo**, pero solo podremos filtrar sobre esa columna.
En general, los filtros pueden configurarse con valores por defecto, dependientes de otros filtros o que si despliegan un menú, se muestre ordenado, aunque esta última opción no se recomienda ya que exige mayor esfuerzo a la herramienta.
<p style="width:300px;display: block; margin: 0 auto;">
    <img src="./img/43.png">
</p>

Para finalizar, en la siguiente imagen puede observarse cómo los filtros pueden aplicarse solo a determinados gráficos y no a todos.
<p style="width:450px;display: block; margin: 0 auto;">
    <img src="./img/44.png">
</p>

<h2 id="tableros2">5.2 Plantillas CSS </h2>
Otra de las grandes ventajas de esta herramienta es la de poder personalizar los estilos con código CSS.
Se establece una plantilla con el código deseado accediendo desde `Configuración → Plantilla CSS`.

<p style="width:400px;display: block; margin: 0 auto;">
    <img src="./img/45.png">
</p>

Luego, editando el tablero, seleccionamos la opción `Editar CSS` y cargamos nuestro estilo personalizado:
<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin: 0 auto;">
  <div style="text-align: center;">
    <img src="./img/46.png" style="height: 200px;"><br>
    
  </div>
  <div style="text-align: center;">
    <img src="./img/47.png" style="height: 200px;"><br>
    
  </div>
</div>

Donde finalmente podemos obtener nuestro tablero totalmente personalizado
<p style="width:750px;display: block; margin: 0 auto;">
    <img src="./img/48.png">
</p>

<h1 id="reco"> 6. Recomendaciones clave </h1>


**1) Cuándo usar gráficos:**
El uso de gráficos es esencial cuando el objetivo es revelar patrones, relaciones, tendencias o excepciones en los datos. Mientras que el texto o las tablas pueden ser útiles para comunicar valores exactos o facilitar la búsqueda puntual, los gráficos permiten obtener una visión general y captar rápidamente el significado subyacente. La  visualización convierte la información numérica en formas que el ojo humano puede captar de inmediato, lo cual resulta crucial en contextos donde la comprensión rápida y global es necesaria. La clave está en que los datos adquieren forma visual, lo que posibilita una percepción más ágil y significativa que una serie de números sin contexto visual.

**2) Cómo diseñar visualizaciones efectivas:**
Diseñar buenas visualizaciones implica mucho más que simplemente generar gráficos con herramientas digitales. Aunque hoy es técnicamente sencillo crearlos, lo importante es diseñarlos teniendo en cuenta la percepción humana. La percepción visual tiene sus propias reglas, y una visualización efectiva debe apoyarse en éstas para ser comprensible. El diseño debe enfocarse en la **claridad, precisión y relevancia del mensaje**.
Es fundamental utilizar representaciones visuales que permitan comparaciones fáciles, como longitudes en lugar de áreas, debido a que el ojo humano es más competente para interpretar la primera. La elección del tipo de gráfico, la escala, los colores y las etiquetas deben hacerse con criterios comunicativos, **no decorativos**. Toda decisión de diseño debe responder a la pregunta: ¿esto mejora la comprensión del mensaje?

**3) Evitar errores comunes:**
Un gran número de visualizaciones fracasan no por falta de tecnología, sino por deficiencias en el diseño y la comprensión de los principios básicos. Uno de los errores más extendidos es el uso excesivo de gráficos circulares o 3D, que dificultan la comparación precisa y generan confusión visual. Otro fallo frecuente es la manipulación de escalas, como no iniciar en cero en gráficos de barras, lo que distorsiona la percepción de las diferencias entre valores.
Además, el uso de colores chillones, sombras, degradados o efectos tridimensionales puede parecer atractivo, pero en este tipo de representaciones, interfiere con la claridad del mensaje. Estos elementos, en lugar de facilitar la interpretación, actúan como distracciones que restan eficacia al propósito informativo, ya que no tienen un objetivo en sí como pueden ser los *mapas topográficos* o *gráficos de contorno* donde los diferentes tonos, representan diferencias de niveles o intensidades de una variable. La simplicidad y la sobriedad son mucho más efectivas para comunicar datos de manera convincente.

El siguiente diagrama de flujo desarrolla con mayor profundidad la elección de paletas de colores:

![49.png](/datos/lineamientos/49.png)

**4) Diseño de dashboards:**
Los dashboards son herramientas clave en la visualización analítica, ya que consolidan la información más relevante en una sola pantalla para su monitoreo inmediato. Sin embargo, su eficacia depende completamente del diseño. Un buen dashboard debe estar estructurado para permitir una lectura rápida y clara de lo que está ocurriendo, facilitando tanto la detección de problemas como la toma de decisiones informadas.
El proceso de monitoreo visual que debe permitir un dashboard consta de tres etapas: escaneo general para identificar áreas de interés, enfoque en detalles importantes, y acceso a información adicional para profundizar si es necesario. Para esto, es crucial que el diseño facilite una navegación visual intuitiva, sin distracciones ni sobrecarga visual.
La elección de elementos visuales debe responder a su capacidad de mostrar información rica en poco espacio, sin sacrificar claridad. Asimismo, el uso del color debe ser estratégico y moderado. El objetivo es lograr un balance entre densidad informativa y legibilidad, donde cada elemento visual contribuya al entendimiento general sin necesidad de explicaciones adicionales.

**5) Cultura visual y responsabilidad:**
Presentar datos de manera efectiva no es solo una cuestión técnica, sino también ética y cultural. En una era inundada de información, comunicar con precisión, claridad y responsabilidad se vuelve esencial. Muchas veces, la información se distorsiona no por malicia, sino por desconocimiento. Por eso, es necesario desarrollar una cultura visual que valore la integridad del mensaje y la eficacia comunicativa.
Aprender a contar historias con datos implica entender cómo vemos, cómo pensamos y cómo tomamos decisiones. La percepción visual, la cognición y la memoria están profundamente conectadas. Una buena visualización no solo muestra datos: los transforma en conocimiento útil. Para lograrlo, es indispensable comprometerse con el aprendizaje y aplicación de principios sólidos de diseño visual, que permitan que los datos cumplan su verdadero propósito: ayudar a comprender el mundo y actuar con inteligencia.


<h1 id="ref"> 7. Referencias bibliográficas</h1>

- Bayo, M & otros. (Septiembre 2014) Aplicación de la Ley de Software Libre en la Provincia de Santa Fe. 43 Jornadas Argentinas de Informática. Simposio Argentino sobre Tecnología y Sociedad. Universidad de Palermo, Buenos Aires, Argentina.
- Crameri, F., Shephard, G. E., & Heron, P. J. (2020). The misuse of colour in science communication. Nature Communications, 11(5444), https://doi.org/10.1038/s41467-020-19160-7
- Ordenanza nro 11063 de 2004. Santa Fe. Argentina. Disponible en: https://www.concejosantafe.gov.ar/wp-content/uploads/Ordenanza/Ordenanza_11063.pdf 