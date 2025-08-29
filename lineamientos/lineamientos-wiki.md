<h1 id="fundamentos">1. Fundamentos</h1>

Este documento pretende sentar bases generales, delimitar y guiar determinadas prácticas en pro de optimizar, garantizar la calidad, disponibilidad, integridad y seguridad de los datos de manera efectiva y responsable.

Entendiendo los datos como el principal insumo y activo dentro de una organización, donde se constituyen como el principal recurso a la hora de una toma de decisiones más informada y más eficiente para ofrecer mejores servicios, guiar actividades operacionales, tácticas y estratégicas; el valor comercial que adquieren es evidentemente significativo. En este sentido, toma una especial relevancia la manipulación y resguardo de los mismos, gestión que no debería ser externalizada al ámbito municipal. 

Cuando un programa, instrucciones y reglas informáticas para ejecutar ciertas tareas en una computadora (software) ingresa a las actividades sustantivas del Estado, adquiere una especificidad respecto de la política tecnológica tradicional dado el tenor y grado de importancia sobre lo que opera, ya que puede tratarse de información sobre la población y el territorio o transparencia de la gestión de gobierno, etc. En este sentido, el software implementado en la gestión estatal no puede tener restricciones sobre el acceso a su diseño, inspección exhaustiva de los mecanismos de funcionamiento, así como tampoco de la posibilidad de estudiarlo y poder adaptarlo a las necesidades propias. El tipo de software que se adapta a estas particularidades es el denominado Software Libre, el cual no solo se encuentra licenciado para ofrecer estas libertades, sino que expone de manera explícita las restricciones y decisiones tecnológicas, científicas y sociales que ese diseño busca regular en determinadas maneras de actuar en la realidad y de organizar la acción de los agentes humanos.

<h1 id="analisis"> 2. Análisis y visualización de datos</h1>

En esta instancia definimos nuestro objetivo en términos comunicacionales, queremos contar una historia específica basada en hallazgos ya identificados. La visualización, debe basarse en estos hallazgos y no abrumar a la audiencia con todos los detalles brutos de la exploración o del sistema de gestión en general. Knaflic (2015) señala como contraproducente el querer mostrar todo el análisis realizado, el público no necesita (ni desea) revisar cada paso exploratorio, sino comprender los hallazgos más importantes; ni mencionemos la inutilidad de exponer las bases de datos del sistema de gestión completa disfrazada de gráficos. Se debe filtrar y dar contexto a los resultados, entrando así al terreno de la **narrativa de datos**.

<h2 id="principios"> 2.1 Principios de diseño y narrativa visual para comunicar patrones, tendencias y anomalías.</h2> 

El diseño efectivo de visualizaciones y la construcción de una narrativa visual clara, son cruciales para comunicar los hallazgos de forma comprensible y persuasiva. Una visualización bien diseñada puede revelar rápidamente patrones de comportamiento, tendencias temporales o valores atípicos que de otro modo pasarían inadvertidos en tablas de números. Una comunicación efectiva de hallazgos no consiste solo en mostrar datos, sino en contar una historia convincente con ellos. Para ello es necesario aplicar principios de diseño visual y construir una narrativa que permita a la audiencia comprender estos patrones, tendencias y anomalías en los datos de forma clara. Cole Nussbaumer Knaflic (2015) propone seis lecciones fundamentales para lograr este objetivo, que sirven como guía para transformar descubrimientos del análisis exploratorio en mensajes impactantes.
A continuación, resumimos los principios fundamentales de diseño y narrativa visual, basándonos principalmente en sus lecciones:

<h3 id="principios1"> 2.1.1. Comprender el contexto</h3>

El punto de partida de la visualización de datos es la comprensión profunda del contexto de la comunicación. Antes de visualizar cualquier dato, es fundamental tener claridad sobre quién, qué y cómo se va a comunicar.
- **Quién (Su Audiencia)**: Es esencial ser lo más específico posible sobre la audiencia. Evitar “audiencias generales” permite una comunicación más efectiva. Se debe considerar la relación con la audiencia y si ya existe confianza.
- **Qué (Acción)**: Se debe definir claramente qué se quiere que la audiencia sepa o haga. El/la comunicador/a, como experto/a en la materia, debe interpretar los datos y guiar a la audiencia hacia la comprensión y la acción, incluso si esto implica salir de la zona de confort. No basta con presentar datos; se debe pedir una acción clara.
- **Cómo (Mecanismo y Tono)**: El método de comunicación impacta el control sobre cómo la audiencia consume la información y el nivel de detalle necesario.
   – Una **presentación en vivo** permite a quien presenta controlar la atención de la audiencia, requiriendo diapositivas más concisas y una buena preparación.
   – Un documento escrito o correo electrónico otorga menos control a quien creó, por lo que exige mayor detalle explícito y autoexplicación.
   – El término “slideument” se refiere a documentos que intentan satisfacer ambas necesidades, lo cual presenta desafíos.
   – El tono deseado (celebratorio, urgente, serio) también influye en las decisiones de diseño.

<p style="width:600px;display: block; margin: 0 auto;">
<img src="/datos/lineamientos/2.1.jpeg">
</p>

La autora recomienda algunas herramientas para resumir el “qué sigue”, como maneras para lograr mayor claridad y concisión:
- **La historia de 3 minutos:** comunicar lo esencial en tres minutos para asegurar que se tiene claridad sobre el mensaje principal en un párrafo y, en última instancia, en una sola declaración concisa. Para esto, es necesario conocer realmente el dominio: saber cuáles son las piezas más importantes y cuáles no son esenciales en la versión más reducida. Si bien suena fácil, ser conciso suele ser más desafiante que ser prolijo. El matemático y filósofo Blaise Pascal reconoció esto en su francés nativo, con una declaración que se traduce aproximadamente como “Hubiera escrito una carta más corta, pero no tuve tiempo” (un sentimiento que a menudo se atribuye a Mark Twain).
- **La Gran idea:** reduce el “qué sigue” a una sola oración. Tiene tres componentes:
	1. Debe articular su punto de vista único;
	2. Debe transmitir lo que está en juego; y
	3. Debe ser una oración completa.
- **Storyboarding:** El guión gráfico es la herramienta más importante desde el inicio para garantizar que una comunicación sea precisa y efectiva. Actúa como un esquema visual que establece la estructura del contenido, aunque puede evolucionar.
	1. Validación temprana: Buscar la aprobación del cliente o stakeholder en esta etapa asegura que el plan esté alineado con sus necesidades.
	2. Comienza con baja tecnología: Es crucial evitar software de presentaciones al principio, para no generar un apego emocional al trabajo que dificulte hacer cambios posteriores.
	3. Métodos ágiles: Usar pizarras, notas adhesivas (Post-it) o papel facilita la reorganización de ideas y la experimentación con diferentes flujos narrativos sin la resistencia a descartar trabajo ya hecho.
	4. Enfoque en la audiencia: La estructura debe asegurarse de que el punto principal sea claro desde el principio, explicando por qué la comunicación es relevante para el público.

<h3 id="principios2"> 2.1.2. Elegir una visualización efectiva</h3>

Seleccionar la mejor manera de presentar los datos, destacando que un puñado de tipos de visualizaciones satisfacen la mayoría de las necesidades. Los gráficos interactúan con nuestro sistema visual, lo que permite un procesamiento más rápido de la información que las tablas.
- **Texto Simple:** Ideal cuando solo se tienen uno o dos números que comunicar, permitiendo que destaquen con
“fuerza”.
- **Tablas:** Interactúan con nuestro sistema verbal (las leemos) y son excelentes para audiencias mixtas que buscan filas específicas o para comunicar múltiples unidades de medida. Sin embargo, raramente son una buena idea en presentaciones en vivo porque la audiencia leerá en lugar de escuchar. El diseño de la tabla debe “desvanecerse” para que los datos sean el foco, utilizando bordes ligeros o espacio en blanco.
- **Heatmaps:** Visualizan datos tabulares usando celdas coloreadas para transmitir la magnitud relativa de los números, lo que ayuda a identificar rápidamente los puntos de interés.
- **Gráficos de Puntos (Scatterplots):** Útiles para mostrar la relación entre dos cosas, codificando datos en ejes X e Y.
- **Gráficos de Líneas:** Comúnmente usados para graficar datos continuos, a menudo en unidades de tiempo. Incluyen gráficos de líneas estándar y gráficos de pendiente (slopegraphs), que son útiles para comparar dos períodos de tiempo o puntos de comparación, mostrando rápidamente aumentos y disminuciones relativas.
- **Gráficos de Barras:** Son el tipo de gráfico preferido por la autora para datos categóricos debido a su facilidad de lectura. Los ojos comparan los puntos finales de las barras, facilitando la visualización de las diferencias. Es crucial que los gráficos de barras siempre tengan una línea base cero para evitar comparaciones visuales falsas. Incluyen barras verticales, barras apiladas verticales (con usos más limitados para comparar subcomponentes), gráficos de cascada para mostrar la composición de cambios, y barras horizontales (preferidas para nombres de categorías largos). El orden lógico de las categorías es importante.
- **Gráficos de Área:** La autora los evita en su mayoría porque los ojos humanos no son buenos atribuyendo valor cuantitativo al espacio bidimensional, con la excepción del gráfico de área cuadrada para magnitudes muy diferentes.

Visualizaciones a evitar: 
- **Gráficos de pastel (pie charts):** Considerados “malvados,” son difíciles de interpretar con precisión debido a la dificultad de comparar ángulos y áreas.
- **Gráficos de donas o anillos:** También difíciles de interpretar ya que requieren comparar longitudes de arco.
- **Gráficos 3D:** La regla de oro es “Nunca uses 3D” a menos que se grafique una tercera dimensión real, ya que distorsionan los números y añaden elementos innecesarios.
- **Ejes Y secundarios:** Generalmente no son una buena idea porque requieren tiempo para entender qué datos se relacionan con qué eje, confundiendo la interpretación.

<h3 id="principios3"> 2.1.3. Eliminar el desorden</h3>

Cada elemento en una página o pantalla nos requiere un cierto esfuerzo mental por comprender esa nueva información, esto se denomina “carga cognitiva”. Cuando le pedimos a nuestra audiencia que trabaje observando, estamos aprovechando su poder de procesamiento mental. Los cerebros de los humanos tienen una cantidad finita de este poder de procesamiento mental. Como diseñadores de información, queremos aprovechar al máximo la capacidad intelectual de nuestra audiencia. Incorporar elementos visuales que ocupen espacio pero no aumentan la comprensión, es lo que la autora denomina *desorden*. El desorden agrega una complejidad innecesaria ya que hace que los diseños se vean más complicados de lo que realmente son; proporciona una mala experiencia al usuaria/o ya que provoca una sensación de incomodidad en la audiencia y; si el público percibe la información como complicada, puede rendirse y dejar de intentar entenderla, lo que produce una total pérdida de atención y significa que hemos perdido la oportunidad de comunicarnos efectivamente.

Cuando se trata de identificar qué elementos de nuestras imágenes son señales (la información que queremos comunicar) y cuáles podrían ser ruido (desorden), se podrían considerar los **Principios Gestalt de la percepción visual**. 

- Proximidad: Objetos cercanos se perciben como parte de un grupo. En la siguiente imagen, los puntos se ven como tres grupos distintos debido a su relativa proximidad entre sí.
  
<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin: 0 auto;">
  <div style="text-align: center;">
    <img src="/datos/lineamientos/2.2.png" style="width:150px;"><br>
    <span><strong>Imagen 2</strong></span>
  </div>
</div>

En la imagen 3, simplemente en virtud de diferenciar el espacio entre los puntos, sus ojos se dibujan hacia abajo de las columnas en el primer caso o a través de las filas en el segundo caso.

<p style="width:400px;display: block; margin: 0 auto;">
   <img src="/datos/lineamientos/2.3.png">
</p> 
<span><strong>Imagen 3</strong> Se observan columnas y filas, simplemente debido al espacio de puntos.</span>

- Similitud: Objetos con características similares (color, forma, tamaño) se perciben como relacionados.
  
<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin: 0 auto;">
  <div style="text-align: center;">
    <img src="/datos/lineamientos/2.4.png" style="width:300px;"><br>
    <span><strong>Imagen 4</strong></span>
  </div>
</div>


Esto se puede aprovechar en las tablas para ayudar a atraer los ojos de nuestra audiencia en la dirección en la que queremos que se enfoquen. En la imagen 5, la similitud de color es una señal para que nuestros ojos lean en las filas (en lugar de en las columnas). Esto elimina la necesidad de elementos adicionales como bordes para ayudar a dirigir nuestra atención.

<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin: 0 auto;">
  <div style="text-align: center;">
    <img src="/datos/lineamientos/2.5.png" style="width:250px;"><br>
    <span><strong>Imagen 5</strong></span>
  </div>
</div>

Una forma en que podemos aprovechar el principio del recinto es trazar una distinción visual dentro de nuestros datos, como se hace en el gráfico de la imagen 6.

<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin: 0 auto;">
  <div style="text-align: center;">
    <img src="/datos/lineamientos/2.6.png" style="width:350px;"><br>
    <span><strong>Imagen 6</strong> El área sombreada separa el pronóstico de los datos reales</span>
  </div>
</div>

- Cerramiento o recinto (Enclosure): Objetos físicamente encerrados se perciben como parte de un grupo.
No se necesita un recinto muy fuerte para hacer esto: el sombreado de fondo claro suele ser suficiente, como se muestra en la imagen 6.

<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin: 0 auto;">
  <div style="text-align: center;">
    <img src="/datos/lineamientos/2.7.png" style="width:150px;"><br>
    <span><strong>Imagen 7</strong></span>
  </div>
</div>

- Cierre (Closure): El concepto de cierre dice que a la gente le gusta que las cosas sean simples y que encajen en las construcciones que ya están en nuestras cabezas. Debido a esto, las personas tienden a percibir un conjunto de elementos individuales como una forma única y reconocible cuando pueden; cuando faltan partes de un todo, nuestros ojos llenan el vacío. Por ejemplo, los elementos de la imagen 7 tenderán a percibirse como un círculo primero y solo después como elementos individuales.

<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin: 0 auto;">
  <div style="text-align: center;">
    <img src="/datos/lineamientos/2.8.png" style="width:150px;"><br>
    <span><strong>Imagen 8</strong></span>
  </div>
</div>

Es común que las aplicaciones de gráficos (por ejemplo, Excel) tengan configuraciones predeterminadas que incluyan elementos como bordes de gráficos y sombreado de fondo. El principio de cierre nos dice que estos son innecesarios; podemos eliminarlos y nuestro gráfico sigue apareciendo como una entidad cohesiva. 
Cuando quitamos esos elementos innecesarios, nuestros datos se destacan más, como se muestra en la imagen 9.

<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin: 0 auto;">
  <div style="text-align: center;">
    <img src="/datos/lineamientos/2.9.png" style="width:350px;"><br>
    <span><strong>Imagen 9</strong></span>
  </div>
</div>

- Continuidad: El principio de continuidad es similar al cierre: cuando miramos objetos, nuestros
ojos buscan el camino más suave y, naturalmente, crean continuidad en lo que vemos, incluso donde puede que no exista explícitamente. A modo de ejemplo, en la imagen 9, si tomo los objetos (1) y los separo, la mayoría de la gente esperará ver lo que se muestra a continuación (2), mientras que podría ser fácilmente lo que se muestra a continuación (3) .

<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin: 0 auto;">
  <div style="text-align: center;">
    <img src="/datos/lineamientos/2.10.png" style="width:250px;"><br>
    <span><strong>Imagen 10</strong></span>
  </div>
</div>

En la aplicación de este principio, eliminamos la línea vertical de eje *y* de la gráfica de la imagen 10. Sus ojos todavía ven que las barras están alineadas en el mismo punto debido al espacio en blanco consistente (la ruta más suave) entre las etiquetas de la izquierda y los datos de la derecha. Como vimos con el principio de cierre en aplicación, eliminar elementos innecesarios permite que nuestros datos se destaquen más.

<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin: 0 auto;">
  <div style="text-align: center;">
    <img src="/datos/lineamientos/2.11.png" style="width:150px;"><br>
    <span><strong>Imagen 11</strong></span>
  </div>
</div>

- Conexión: Tendemos a pensar en objetos que están conectados físicamente como parte de un grupo. La propiedad conectiva normalmente tiene un valor asociativo más fuerte que un color, tamaño o forma similar. Tenga en cuenta que al mirar la imagen 11, sus ojos probablemente emparejen las formas conectadas por líneas (en lugar de colores, tamaños o formas similares): ese es el principio de conexión en acción. La propiedad conectiva **no es** normalmente más fuerte que el cerramiento, pero puede influir en esta relación mediante el grosor y la oscuridad de las líneas para crear la jerarquía visual deseada.

<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin: 0 auto;">
  <div style="text-align: center;">
    <img src="/datos/lineamientos/2.12.png" style="width:350px;"><br>
    <span><strong>Imagen 12</strong></span>
  </div>
</div>

Una forma en que usamos frecuentemente el principio de conexión es en gráficos de líneas, para ayudar a nuestros ojos a ver el orden en los datos, como se muestra en la imagen 12.

<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin: 0 auto;">
  <div style="text-align: center;">
    <img src="/datos/lineamientos/2.13.png" style="width:350px;"><br>
    <span><strong>Imagen 13</strong></span>
  </div>
</div>

Otros tipos de desorden visual

- **Falta de Orden Visual:** Un diseño bien pensado se “desvanece” en el fondo. 
La *alineación* (ej., texto justificado a la izquierda) es clave para crear líneas limpias y un diseño ordenado, evitando elementos diagonales que son difíciles de leer. 
El *espacio en blanco* es crucial para enfatizar y crear pausas visuales.

- **Uso no estratégico del contraste:** Si demasiadas cosas son diferentes, ninguna sobresale. Se debe usar el contraste estratégicamente para que lo importante se destaque.

<h3 id="principios4"> 2.1.4. Enfocar la atención de la audiencia</h3>

Al comprender cómo nuestra audiencia ve y procesa la información, nos colocamos en una mejor posición para poder comunicarnos de manera efectiva.

- Usted ve con su cerebro: La visión implica un procesamiento significativo en el cerebro, no solo en los ojos. Se distinguen tres tipos de memoria relevantes para el diseño visual:
   - Memoria Icónica: Súper rápida, inconsciente, sintonizada con los atributos preatentivos. Es un mecanismo de supervivencia que permite detectar rápidamente diferencias.
   - Memoria a Corto Plazo: Limitada a unos cuatro “fragmentos” de información visual a la vez. El exceso de información sobrecarga esta memoria.
   - Memoria a Largo Plazo: Construida a lo largo de la vida, vital para el reconocimiento de patrones. Las imágenes pueden ayudar a recordar información almacenada en la memoria verbal a largo plazo.
- Los atributos preatentivos son herramientas poderosas que permiten que la audiencia vea lo que se quiere que vean incluso antes de que sepan que lo están viendo. Incluyen *movimiento, posición espacial, intensidad, tonalidad (hue), ancho y longitud de línea, forma, orientación, cerramiento, marcas añadidas, curvatura y tamaño.*
  - Usados con moderación, son útiles para dirigir la atención rápidamente y crear una jerarquía visual de información.
  - Tamaño: Denota importancia; los elementos importantes deben ser grandes.
  - Color: Una de las herramientas más poderosas cuando se usa con moderación, siempre debe ser una decisión intencional.
      * Usar con moderación (demasiada variedad diluye su valor).
      * Usar de forma consistente (la historia debe mantener la atención, no los colores; los cambios de color deben señalar cambios de tema o tono).
    * Diseñar pensando en los daltónicos (evitar rojo/verde juntos, usar señales visuales adicionales).
    * Considerar el tono que transmite el color (evoca emociones).
    * Integrar colores de marca, pero asegurar que resalten.
    * Para profundizar sobre el mal uso de colores en la comunicación, seguir las recomendaciones de Crameri (2020).

- Posición en la página: La parte superior izquierda es un “bien inmueble precioso”; colocar lo más importante allí.

<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin: 0 auto;">
  <div style="text-align: center;">
    <img src="/datos/lineamientos/2.14.png" style="width:450px;"><br>
    <span><strong>Imagen 14</strong> Las marcas añadidas funcionan como una señal de «mirá acá», atrayendo la atención de la audiencia más rápidamente hacia el lado derecho del gráfico.</span>
  </div>
</div>

<h3 id="principios5"> 2.1.5. Pensar como un/a Diseñador/a</h3>

Se recomienda aplicar conceptos de diseño tradicional a la comunicación de datos, enfatizando la máxima **“La forma sigue a la función”**. El diseño debe permitir que la audiencia interactúe con los datos con facilidad.
- **Affordances (Sugerencias de Uso)**: Aspectos del diseño que hacen obvio cómo usar un producto. En visualización de datos, se trata de usar señales visuales para indicar cómo interactuar.
   - **Resaltar lo importante**: Usar atributos preatentivos para dirigir la atención, pero solo resaltar una fracción (máximo 10%) del total para no diluir el efecto. Técnicas incluyen **negrita**, *cursiva*, <span style="text-decoration: underline;">subrayado</span>, MAYÚSCULAS, <span><span style="color: #ff6b6b;">c</span><span style="color: #4ecdc4;">o</span><span style="color: #ffe66d;">l</span><span style="color: #1a535c;">o</span><span style="color: #ff9f1c;">r</span></span>, inversión de elementos y tamaño.

  - **Eliminar distracciones**: Inspirado en la frase de Antoine de Saint-Exupéry, “La perfección se logra (...) cuando no hay nada más que quitar”. Implica eliminar datos no críticos, resumir cuando no se necesita detalle y relegar elementos necesarios pero no esenciales al fondo (ej., con color gris claro).
  - **Crear una jerarquía visual clara de la información**: Utilizar los mismos atributos preatentivos para guiar a la audiencia sobre el orden en que deben procesar la información, empujando algunos elementos al frente y otros al fondo.
- **Accesibilidad**: Diseños utilizables por personas con diversas habilidades, incluyendo habilidades técnicas.
   - **No sobrecomplicar**: Un diseño que parece complicado disuade a la audiencia. Esto implica usar una fuente legible y consistente, mantener el diseño limpio, usar un lenguaje sencillo y eliminar la complejidad innecesaria.
   - **El texto es tu amigo**: El texto es fundamental para etiquetar, introducir, explicar, reforzar, resaltar, recomendar y contar una historia. Cada gráfico necesita un título y cada eje debe tener un título. Los **títulos de acción** en las diapositivas son un “bien inmueble precioso” para comunicar la idea principal. La **anotación directa** en el gráfico es útil.
- **Estética**: Hacer los diseños “bonitos” es necesario porque los diseños más estéticos se perciben como más fáciles de usar, se aceptan mejor y fomentan el pensamiento creativo. Se enfatiza el uso inteligente del color, la atención a la alineación y el aprovechamiento del espacio en blanco para lograr un diseño estético y organizado.
- **Aceptación**: Un diseño debe ser aceptado por su audiencia. Se ofrecen estrategias como articular los beneficios, mostrar el “lado a lado” (antes y después), proporcionar múltiples opciones,involucrar a un miembro influyente y buscar comentarios imparciales.

La siguiente imagen muestra el antes y después de una visualización donde se eliminaron las distracciones y resaltan las cosas importantes, mejorándola notablemente.

<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin: 0 auto;">
  <div style="text-align: center;">
    <img src="/datos/lineamientos/2.15.png" style="width:550px;"><br>
    <span><strong>Imagen 15</strong></span>
  </div>
</div>

<h3 id="principios6"> 2.1.6. Contar una historia.</h3>

Una buena historia capta tu atención y te lleva a un viaje, provocando una respuesta emocional. En medio de eso, te das cuenta de que no quieres darle la espalda ni dejarlo. Después de terminarlo, un día, una semana o incluso un mes después, podrías describírselo fácilmente a cualquiera. A través de la **fuerza de la repetición** y la **estructura de principio, nudo y desenlace**, las historias capturan la atención, evocan una respuesta emocional y son fáciles de recordar.
- Podemos considerar lecciones de **"Narradores Maestros"**:
  - Aristóteles (teatro): Estructura de tres actos: **planteamiento** (presentación de personajes, entorno, incidente), **conflicto** (desarrollo del problema) y **resolución** (clímax, respuesta a la pregunta dramática). El conflicto y la tensión son integrales.
  - Robert McKee (cine): La persuasión a través de la historia une una idea con una emoción, a diferencia de la retórica convencional (hechos y estadísticas) que solo persuade intelectualmente. Las historias revelan cómo y por qué cambia la vida, partiendo de un equilibrio que se rompe, lo que crea lucha, conflicto y suspenso.
  - Kurt Vonnegut (palabra escrita): Consejos clave incluyen: encontrar un tema que importe, **no divagar, mantenerlo simple, tener el valor de cortar** (eliminar lo que no ilumine el tema), sonar como uno mismo, decir lo que se quiere decir y, lo más importante, **apiadarse de los lectores** (simplificar y clarificar). La comunicación debe ser para la audiencia.
- **Construyendo la Historia**: Debe tener un *principio, nudo y desenlace*.
  - El Principio: Introduce el planteamiento (escenario, personaje principal, estado sin resolver, resultado deseado y solución). El “personaje principal” debe ser la audiencia, enmarcando la historia en términos de su problema.
  - El Nudo: Desarrolla el “lo que podría ser”, convenciendo a la audiencia de la necesidad de acción. Puede incluir antecedentes, contexto, ejemplos, datos que demuestren el problema, consecuencias de no actuar y beneficios de la solución propuesta. Debe ser relevante para la audiencia y sus motivaciones.
  - El Final: Termina con una clara llamada a la acción, reiterando la urgencia y el nuevo entendimiento.
- **La Estructura Narrativa**: Son las palabras que cuentan la historia de manera que tenga sentido y convenza a la audiencia. Un buen visual puede fallar sin una narrativa convincente.
   - Flujo Narrativo: Determinar el orden en que la audiencia experimentará la historia. Puede ser cronológico (siguiendo el proceso analítico) o empezar por el final (con la llamada a la acción).
   - El concepto “Bing, Bang, Bongo” ayuda a establecer la estructura. La idea es que primero debes decirle a tu audiencia lo que les vas a decir ("Bing", el párrafo de introducción en tu ensayo). Luego se lo dices ("Bang", el contenido real del ensayo). Luego, resume lo que les acaba de decir (“Bongo”, la conclusión).
  
<p style="width:100px;display: block; margin: 0 auto;">
   <img src="/datos/lineamientos/2.16.png">
</p>

  - Narrativa Hablada y Escrita: En una presentación en vivo, la voz en off refuerza el mensaje, pero las diapositivas deben ser concisas. En un informe escrito, la narrativa debe ser autoexplicativa y clara.
  
- **El Poder de la Repetición**: Repetir información importante ayuda a transferirla a la memoria a largo plazo. El concepto “Bing, Bang, Bongo” es clave para esto.
- **Tácticas para asegurar la Claridad de la Historia**:
	- Lógica Horizontal: Leer solo los títulos de las diapositivas (títulos de acción) debe contar la historia principal.
	- Lógica Vertical: Toda la información en una diapositiva debe ser autorreforzante; el contenido refuerza el título y viceversa.
	- Storyboarding Inverso: Revisar la comunicación final y anotar el punto principal de cada página para ver si cuenta la historia deseada.
	- Una Perspectiva Fresca: Obtener comentarios de amigas/os o colegas imparciales para ver si la comunicación logra su objetivo.
  
El **personaje principal de cada historia siempre debe ser la audiencia**, haciendo que los datos sean relevantes para ellos y transformando la simple “muestra de datos” en una “narración de historias con datos”.

<h2 id="herramientas"> 2.2 Herramientas de visualización </h2> 

Existen diversas y variadas herramientas diseñadas para crear tableros interactivos. Entre ellas podemos encontrar como las más populares, a saber: Tableu, Power BI, Looker Studio, que, como principal impedimento a la hora de implementarlas en nuestro ámbito laboral, tienen la condición de no ser Software Libre, forman parte de lo que se denomina software propietario. Esto implica que, además de requerir una licencia para acceder a sus versiones completas, los datos que trabajemos serán alojados en servidores de la empresa propietaria del software, con las consecuencias que esto conlleva.
Con los fundamentos planteados en el punto (1) y, principalmente, que rige una ordenanza con número 11063 que
>*“(…) tiene por objeto establecer los lineamientos de las políticas de incorporación y gestión de software, que garanticen la debida protección de la integridad, confidencialidad, accesibilidad, interoperabilidad y compatibilidad de la información y la auditabilidad de su procesamiento, en la Administración Municipal; el libre acceso ciudadano a la información pública ofrecida en formatos digitales; y la accesibilidad de los servicios que la administración preste al público empleando medios informáticos.”* (Ordenanza nro 11063, 2004, Artículo 1)

desde la Subdirección de Gobernanza de Datos es que se decide utilizar herramientas libres, particularmente Metabase, Grafana y Superset.
Si bien se pretende generalizar sobre ciertas prácticas, se brindarán ejemplos particulares sobre Superset.

<h1 id="intro"> 3. Introducción a Apache Superset </h1>

Ingresando a [Superset](https://superset.santafeciudad.gov.ar/), podrán encontrarse con la pantalla de inicio de sesión de Superset, el usuario de la imagen es solo un ejemplo. Es importante que cada persona que va a utilizar la herramienta tenga su propio usuario y por motivos de seguridad, sea de exclusivo uso personal.
<p style="width:800px; display: block; margin: 0 auto;">
   <img src="/datos/lineamientos/3.1.png">
</p>

La siguiente es la pantalla de inicio, en la misma contamos con una *barra de menú*, una lista desplegable de elementos **Recientes, Dashboards, Gráficos y Consultas guardadas**:

<p style="width:800px;display: block; margin: 0 auto;">
   <img src="/datos/lineamientos/3.2.png">
</p>

Este usuario no tiene aún ningún elemento a disposición, a medida que vaya creando cosas, se irán agregando a la sección correspondiente.
<p style="width:800px;display: block; margin: 0 auto;">
   <img src="/datos/lineamientos/3.3.png">
</p>

Tenemos también en la esquina superior derecha opciones de **idioma**, de **Configuración** y un acceso rápido a crear los siguientes elementos:
<p style="width:200px;display: block; margin: 0 auto;">
   <img src="/datos/lineamientos/3.4.png">
</p>

Si bien los nombres son descriptivos, hacemos una breve descripción de cada uno a modo de glosario:

**Conjunto de datos (dataset):** tabla o vista de base de datos.

**Datos:** desde este apartado podemos crear datasets desde bases de datos conectadas o desde un archivo con formato *.csv* o *.xlsx*.
<p style="width:300px;display: block; margin: 0 auto;">
   <img src="/datos/lineamientos/3.5.png">
</p>


**Gráfico (chart):** representación visual de datos (ej: gráfico de barras, línea, mapa, tabla, etc.). En este caso, se crean a partir de un dataset y permite personalizar métricas, filtros y estilos.

**SQL:** si bien SQL es el Lenguaje de Consulta Estructurado (Structured Query Language), aquí lo utilizan en el menú para dirigir a un apartado donde se pueden realizar consultas, modificar y eliminar datos en las bases de datos, así como también guardar esas consultas y acceder al historial.
<p style="width:200px;display: block; margin: 0 auto;">
   <img src="/datos/lineamientos/3.6.png">
</p>

**Tablero (Dashboard):** panel interactivo que agrupa múltiples gráficos en una sola vista. Permite analizar datos desde diferentes perspectivas y compartir el conocimiento que de allí surge.

Luego de familiarizarse con la herramienta, para comenzar a trabajar vamos a necesitar importar nuestros datos.

<h1 id="bd"> 4. Base de datos </h1>

Siendo el objetivo principal la realización de análisis exploratorios, es primordial constituir una agregación consistente de datos donde se evite la redundancia e inconsistencia, se facilite la accesibilidad y se eviten problemas de seguridad e integridad, para ello se recomienda constituir bases de datos relacionales bajo la que es hasta hoy día, la manera más efectiva de reflejo de la realidad para estos análisis: el modelado dimensional.

La Base de Datos será alojada en servidores propios sobre el motor PostgreSQL, también de licencia abierta y libre. No se tendrá vínculo directo con el motor, sino que, en este caso, utilizaremos como intermediario o “sistema de manejo” al mismo Superset.

<h2 id="bd1"> 4.1 Creación de una tabla </h2> 
Independientemente del modelado de la información, se mostrará a continuación cómo realizar la ingesta de datos para ponerlas a disposición de la herramienta.

Como recomendaciones generales, se sugiere nombrar las tablas en singular con denominaciones representativas y claras.

Se ejemplificará utilizando datos brindados por el sector Promoción de la Salud.

A fines prácticos, asumiremos cada archivo como una tabla. Como se indicó anteriormente, lo ideal es contar con la información modelada, pero se tiene en cuenta también que este es el último paso antes de la creación de tableros, por lo que puede considerarse esta presentación de datos como primitiva para un posterior refinamiento y modelado.

Como mencionamos previamente, desde el botón **+** accedemos a `Datos → Upload Excel to Dataset` desde donde se nos presentará el siguiente cuadro:

<p style="width:300px;display: block; margin: 0 auto;">
   <img src="/datos/lineamientos/4.1.png">
</p>

Desde el botón `SELECT`, elegimos el archivo, en este caso seleccionamos SISA_SALA_DENGUE.xlsx. Teniendo seleccionado `Preview uploaded file`, podemos ver una vista previa de las columnas que se van a cargar, lo que sirve para comprobar que la herramienta está leyendo correctamente el archivo.
A continuación, se puede observar lo que debería quedar seleccionado siempre para los campos `BASE DE DATOS` y `ESQUEMA`. Con un conocimiento mayor sobre el conjunto de datos, se podrá elegir un nombre más adecuado para la tabla, en este caso, a fines ejemplificadores, elegimos el que se observa en la imagen 23. Se recomienda no utilizar caracteres especiales, si es necesario utilizar más de una palabra, se deberán separar por guion bajo (_).

<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin: 0 auto;">
  <div style="text-align: center;">
    <img src="/datos/lineamientos/4.2.png" style="height: 500px;"><br>
    <span>Imagen 23</span>
  </div>
  <div style="text-align: center;">
    <img src="/datos/lineamientos/4.3.png" style="height: 500px;"><br>
    <span>Imagen 24</span>
  </div>
</div>

Para archivos *.xlsx* se puede elegir en `SHEET NAME` el nombre de la hoja de trabajo.

En el apartado `File Settings` se puede configurar cómo debe actuar el sistema ante tablas que ya existen y valores nulos. (Imagen 24)

En `Columnas` se pueden seleccionar las mismas de manera personalizada. (Imagen 25)

Finalmente, se puede determinar si se cuenta con un encabezado, la cantidad de filas a leer y si se quieren omitir. (Imagen 26)

<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin: 0 auto;">
  <div style="text-align: center;">
    <img src="/datos/lineamientos/4.4.png" style="height: 500px;"><br>
    <span>Imagen 25</span>
  </div>
  <div style="text-align: center;">
    <img src="/datos/lineamientos/4.5.png" style="height: 500px;"><br>
    <span>Imagen 26</span>
  </div>
</div>

Cuando finalmente seleccionemos `UPLOAD`, tendremos nuestra tabla para comenzar nuestros análisis.
<h2 id="bd2"> 4.2 Datasets y gráficos </h2>

Ahora en el menú `Conjuntos de datos`, ya podremos ver nuestra tabla:
<p style="width:800px;display: block; margin: 0 auto;">
   <img src="/datos/lineamientos/4.6.png">
</p>

Como acciones, puede editarse el conjunto y definir `MÉTRICAS` como funciones de agregación, por ejemplo, personalizar las columnas redefiniendo el tipo de dato o señalando si es un dato temporal o, definir columnas calculadas.
<p style="width:600px;display: block; margin: 0 auto;">
   <img src="/datos/lineamientos/4.7.png">
</p>
Si hacemos clic directamente sobre el nombre de la tabla, accedemos a la creación de un gráfico.
<p style="width:600px;display: block; margin: 0 auto;">
   <img src="/datos/lineamientos/4.8.png">
</p>
La pantalla se divide en 3 partes, la primera sección nos muestra el detalle de la tabla seleccionada, sus columnas y métricas que hayamos definido. La segunda, la configuración del gráfico que deseemos realizar.

En la parte superior de esta segunda sección, tenemos algunos de los gráficos más comunes, pero si hacemos clic en `View all charts` podremos acceder a una inmensa variedad de gráficos que Superset tiene a disposición.
<p style="width:600px;display: block; margin: 0 auto;">
   <img src="/datos/lineamientos/4.9.png">
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
   <img src="/datos/lineamientos/4.10.png">
</p>

En el apartado `Personalizar`, encontramos configuraciones propias del tipo de gráfico, en este caso: orientación de las barras y si queremos que estén apiladas, por ejemplo, títulos de los ejes, colores, etc.
<p style="width:500px;display: block; margin: 0 auto;">
   <img src="/datos/lineamientos/4.11.png">
</p>

Finalmente, guardamos el gráfico y Superset nos da la opción de agregarlo a un tablero ya creado, como aún no lo tenemos, simplemente lo guardamos.
Ya tenemos nuestro primer gráfico.

<p style="width:700px;display: block; margin: 0 auto;">
   <img src="/datos/lineamientos/4.12.png">
</p>

Para hacer otro, procedemos de la misma manera, seleccionando ahora el nuevo tipo y datos.
Supongamos que queremos representar ahora la columna `Ficha`

<p style="width:700px;display: block; margin: 0 auto;">
   <img src="/datos/lineamientos/4.13.png">
</p>

Observamos que hay un número significativo de valores nulos. La manera de actuar ante esto dependerá de los objetivos de nuestro análisis, pero aquí lo usaremos para ejemplificar algunos procedimientos.

<h3 id="bd22"> 4.2.2 Filtros </h3>

Podemos simplemente ignorar los valores nulos, para esto, en la sección `DATOS` del gráfico, vamos hasta `FILTROS` y podemos observar que por defecto selecciona un campo de fecha, esto será explicado más adelante, lo que haremos ahora, será seleccionar nuestra dimensión `FICHA` en el cuadro de diálogo, y la condición a filtrar, en este caso, queremos que ignore los valores nulos:

<p style="width:250px;display: block; margin: 0 auto;">
   <img src="/datos/lineamientos/4.14.png">
</p>


Actualizamos nuestro gráfico y solo veremos datos no nulos

<p style="width:700px;display: block; margin: 0 auto;">
   <img src="/datos/lineamientos/4.15.png">
</p>

Pueden encontrarse como opciones de filtro, 12 diferentes operadores, como pueden ser los numéricos (<,>, =, etc.), de lista (in, not in) o de comparación de cadenas de texto (like), los que la herramienta considera `SIMPLES`; así como también `SQL PERSONALIZADO`, donde podemos escribir directamente sentencias con cláusulas `WHERE` o `HAVING`, dejando en claro, que no es la única funcionalidad ignorar valores nulos.

<h3 id="bd23"> 4.2.3 Tabla virtual</h3>

La solución anterior solo tendrá efecto en cada gráfico que lo apliquemos, si en cambio, queremos mantener esta condición para todas las ocasiones donde se utilice este set de datos, tenemos dos maneras de proceder.
<h4 id="bd231"> 4.2.3.1 Nuevo conjunto de datos desde consultas</h4>

Desde el menú `SQL`, accedemos a `Laboratorio SQL`

<p style="width:700px;display: block; margin: 0 auto;">
   <img src="/datos/lineamientos/4.16.png">
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
   <img src="/datos/lineamientos/4.17.png">
</p>

Como puede observarse, esto define un nuevo tipo de conjunto de datos, una tabla de tipo virtual.
<p style="width:600px;display: block; margin: 0 auto;">
   <img src="/datos/lineamientos/4.18.png">
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
   <img src="/datos/lineamientos/4.19.png">
</p>

Nótese que estamos creando nuevos conjuntos de datos con cada modificación.
Si consideramos que el cambio que estamos haciendo debería ser definitivo para nuestro conjunto, y no debería haber más de un conjunto con diferencias menores, nuevamente seleccionando la acción *Editar*

<p style="width:700px;display: block; margin: 0 auto;">
   <img src="/datos/lineamientos/4.20.png">
</p>

accedemos a la ventana de edición, nos dirigimos a la sección `COLUMNAS CALCULADAS`, allí, el botón `AÑADIR ELEMENTO` nos permitirá definir nuestra columna nueva con la sentencia CASE que usamos en las consultas anteriores.

<p style="width:550px;display: block; margin: 0 auto;">
   <img src="/datos/lineamientos/4.21.png">
</p>

Ahora, tendremos a disposición esta columna para utilizarla donde la necesitemos.

<p style="width:400px;display: block; margin: 0 auto;">
   <img src="/datos/lineamientos/4.22.png">
</p>

<h1 id="tableros"> 5. Tableros (Dashboards)</h1>
Para crear un tablero, simplemente nos dirigimos a la sección Dashboards y pulsamos el botón con el mismo nombre.
<p style="width:600px;display: block; margin: 0 auto;">
   <img src="/datos/lineamientos/5.1.png">
</p>

Ya aquí, podemos agregar gráficos y elementos como pestañas, filas, columnas, encabezados, texto -el cual puede ser en formato Markdown o etiquetas HTML-.
<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin: 0 auto;">
  <div style="text-align: center;">
    <img src="/datos/lineamientos/5.2.png" style="height: 400px;"><br>
    
  </div>
  <div style="text-align: center;">
    <img src="/datos/lineamientos/5.3.png" style="height: 250px;"><br>
    
  </div>
</div>

Superset maneja el denominado sistema *Drag and drop*, se selecciona el elemento, se arrastra y se suelta en la ubicación donde se desee colocar.
Ya insertado el gráfico, podemos definir las propiedades con las que queremos que se visualice finalmente en el tablero.

<p style="width:550px;display: block; margin: 0 auto;">
   <img src="/datos/lineamientos/5.4.png">
</p>
<p style="width:550px;display: block; margin: 0 auto;">
   <img src="/datos/lineamientos/5.5.png">
</p>
Superset organiza la disposición de elementos por bloques que a su vez se separan en columnas. Cada bloque es independiente, se pueden agregar todos los elementos que se deseen, como por ejemplo separar en pestañas.

<p style="width:500px;display: block; margin: 0 auto;">
   <img src="/datos/lineamientos/5.6.png">
</p>

<h2 id="tableros1">5.1 Filtros </h2>

<div style="display: flex; align-items: center; justify-content: left; gap: 20px; margin: 0 auto;">
  <span>La flecha ubicada a la izquierda del tablero</span>
  <img src="/datos/lineamientos/5.7.png" style="width:20px;">
</div>

despliega la sección de filtros:
<p style="width:250px;display: block; margin: 0 auto;">
    <span></span>
    <img src="/datos/lineamientos/5.8.png">
</p>

`ADD/EDIT FILTERS` despliega la siguiente ventana

<p style="width:450px;display: block; margin: 0 auto;">
    <img src="/datos/lineamientos/5.9.png">
</p>

Supongamos que queremos definir un filtro por “Sexo Legal”, seleccionamos el tipo correspondiente, que en este caso es `Valor`, tipo que se corresponde con los campos de tipo texto o string.
Las otras opciones son:

<p style="width:200px;display: block; margin: 0 auto;">
    <img src="/datos/lineamientos/5.10.png">
</p>

**Valor:** El filtro de valor crea un menú desplegable con todos los valores únicos disponibles para esa columna.

**Rango numérico (Numerical range):** Este filtro crea un control deslizante con dos puntos de selección para definir un rango. El punto más a la izquierda del control deslizante representa el valor más bajo disponible en esa columna, mientras que el más a la derecha representa el valor más alto.
Así es como se ve el filtro en el tablero:
<p style="width:200px;display: block; margin: 0 auto;">
    <img src="/datos/lineamientos/5.11.png">
</p>

Finalmente, tenemos 3 tipos de filtros relacionados con fechas: **Período de tiempo, Columna de tiempo** y **Granularidad temporal**.

**Período de tiempo (Time Range):** aquí se despliegan diferentes opciones y formatos de fechas dentro de una amplia gama de configuraciones genéricas (como Último día, Semana pasada, Día anterior, Semana anterior, Día actual, Semana actual, etc.) disponibles para este filtro. Permitiendo también seleccionar un intervalo de tiempo personalizado. Se aplicará por igual a todos los campos tipo fecha que hayamos cargado en cada elemento o gráfico del tablero como fue explicado en la sección 3.2.2, si no indicamos ninguno, el filtro no tendrá ningún efecto.

**Granularidad temporal (Time Grain):** En éste se puede definir la granularidad, como su título lo indica, de la siguiente manera:
<p style="width:150px;display: block; margin: 0 auto;">
    <img src="/datos/lineamientos/5.12.png">
</p>

**Columna de tiempo (Time Column):** Con éste, seleccionamos una columna del dataset sobre el que estamos trabajando, por ejemplo:
<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin: 0 auto;">
  <div style="text-align: center;">
    <img src="/datos/lineamientos/5.13.png" style="height: 150px;"><br>
    
  </div>
  <div style="text-align: center;">
    <img src="/datos/lineamientos/5.14.png" style="height:150px;"><br>
    
  </div>
</div>

El cual nos trae un solo valor, ya que es la única columna de tipo fecha que tenemos.
Para este filtro, no necesitamos cargar previamente el campo en el gráfico, el uso común y recomendado es cuando se tienen múltiples columnas de fecha, se selecciona una con este filtro y luego se define la temporalidad con el **Período de tiempo**, pero solo podremos filtrar sobre esa columna.
En general, los filtros pueden configurarse con valores por defecto, dependientes de otros filtros o que si despliegan un menú, se muestre ordenado, aunque esta última opción no se recomienda ya que exige mayor esfuerzo a la herramienta.
<p style="width:300px;display: block; margin: 0 auto;">
    <img src="/datos/lineamientos/5.15.png">
</p>

Para finalizar, en la siguiente imagen puede observarse cómo los filtros pueden aplicarse solo a determinados gráficos y no a todos.
<p style="width:450px;display: block; margin: 0 auto;">
    <img src="/datos/lineamientos/5.16.png">
</p>

<h2 id="tableros2">5.2 Plantillas CSS </h2>
Otra de las grandes ventajas de esta herramienta es la de poder personalizar los estilos con código CSS.
Se establece una plantilla con el código deseado accediendo desde `Configuración → Plantilla CSS`.

<p style="width:400px;display: block; margin: 0 auto;">
    <img src="/datos/lineamientos/5.17.png">
</p>

Luego, editando el tablero, seleccionamos la opción `Editar CSS` y cargamos nuestro estilo personalizado:
<div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin: 0 auto;">
  <div style="text-align: center;">
    <img src="/datos/lineamientos/5.18.png" style="height: 200px;"><br>    
  </div>
  <div style="text-align: center;">
    <img src="/datos/lineamientos/5.19.png" style="height: 200px;"><br>    
  </div>
</div>

Donde finalmente podemos obtener nuestro tablero totalmente personalizado
<p style="width:750px;display: block; margin: 0 auto;">
    <img src="/datos/lineamientos/5.20.png">
</p>

<h1 id="reco"> 6. Recomendaciones clave </h1>

[Ver sección](/datos/analitica/lineamientos/recomendaciones)

<h3 id="principios1">1. Cuándo usar gráficos</h3>
Los gráficos son especialmente valiosos cuando buscamos mostrar relaciones, tendencias o excepciones que no son evidentes en tablas o texto. Mientras que las tablas comunican valores exactos y permiten búsquedas puntuales, los gráficos convierten la información numérica en formas visuales que el ojo humano capta de inmediato.
En contextos de toma de decisiones, la rapidez de interpretación es fundamental: los gráficos permiten obtener una visión global, detectar cambios y orientar la atención hacia lo que importa.

<h3 id="principios2">2. Principios de diseño y narrativa visual</h3>

Diseñar buenas visualizaciones no consiste en usar software, sino en comprender cómo percibe la audiencia. La clave está en la claridad, precisión y relevancia del mensaje. El diseño debe responder siempre a la pregunta: *¿esto mejora la comprensión?*

**2.1 Comprender el contexto**
Antes de graficar:
- **Quién** (audiencia): especificar a quién se comunica y qué relación existe.
- **Qué** (acción): definir lo que se quiere que la audiencia entienda o haga.
- **Cómo** (mecanismo/tono): elegir entre presentación en vivo, informe o “slideument” según el nivel de detalle y el tono (urgente, celebratorio, formal).
Herramientas como **la historia de 3 minutos**, **la gran idea** o el **storyboarding** ayudan a depurar y estructurar el mensaje.

**2.2 Elegir una visualización efectiva**
Un puñado de gráficos resuelve la mayoría de necesidades:
- Texto simple y tablas (valores exactos).
- Gráficos de barras y líneas (preferidos para categorías y series temporales).
- Gráficos de puntos o mapas de calor (para relaciones y densidades).
Visualizaciones a evitar: gráficos de torta, de dona, 3D o con ejes secundarios, ya que dificultan la interpretación.

**2.3 Eliminar el desorden**
El exceso de elementos aumenta la carga cognitiva y distrae de lo importante. Los principios Gestalt (proximidad, similitud, cerramiento, continuidad, conexión) son claves para diferenciar señales de ruido. Un diseño ordenado usa espacio en blanco, alineación y contraste estratégico.

**2.4 Enfocar la atención**
Los atributos preatentivos (color, tamaño, posición, movimiento) permiten guiar la mirada antes de que la audiencia sea consciente de ello.
- Usar color y tamaño con moderación.
- Reservar la parte superior izquierda para lo más importante.
- Diseñar pensando también en accesibilidad (ej. daltónicos).
- Preferentemente utilizar las siguiente paletas de colores
  
   <p style="width:750px;display: block; margin: 0 auto;">
    <img src="/datos/lineamientos/6.1.png">
</p>


**2.5 Pensar como un/a diseñador/a**
“La forma sigue a la función”:
- Resaltar lo importante y eliminar distracciones.
- Crear jerarquías visuales claras.
- Usar títulos de acción y anotaciones directas.
- Mantener un diseño limpio, accesible y estético.
- Validar con la audiencia y ajustar en función de su aceptación.

<h3 id="principios3">3. Evitar errores comunes</h3>

Los fallos más frecuentes son:
- Uso excesivo de gráficos circulares o en 3D.
- Escalas manipuladas (ej. barras sin base cero).
- Abuso de colores chillones, sombras o degradados sin propósito comunicativo.
La simplicidad y sobriedad fortalecen el mensaje. Cada decisión visual debe tener un propósito.

<h3 id="principios4">4. Diseño de dashboards</h3>

Los dashboards condensan información clave en una sola pantalla. Su eficacia depende de un diseño que permita:
  1. Escaneo rápido de la situación.
  2. Identificación de focos de interés.
  3. Acceso a detalles adicionales según necesidad.
El diseño debe balancear densidad informativa y legibilidad, con navegación intuitiva y uso estratégico del color.

<h3 id="principios5">5. Cultura visual y responsabilidad</h3>

Visualizar datos no es solo una tarea técnica, sino también ética y cultural. Una narrativa visual clara evita la desinformación, incluso cuando esta ocurre por desconocimiento más que por intención.
Desarrollar una cultura visual implica:
- Contar historias donde la audiencia sea el personaje principal.
- Usar los datos para generar conocimiento útil y decisiones informadas.
- Comprometerse con principios sólidos de diseño visual que promuevan precisión, claridad y responsabilidad.

<h1 id="ref"> 7. Referencias bibliográficas</h1>

- Bayo, M & otros. (Septiembre 2014) Aplicación de la Ley de Software Libre en la Provincia de Santa Fe. 43 Jornadas Argentinas de Informática. Simposio Argentino sobre Tecnología y Sociedad. Universidad de Palermo, Buenos Aires, Argentina.
- Crameri, F., Shephard, G. E., & Heron, P. J. (2020). The misuse of colour in science communication. Nature Communications, 11(5444), https://doi.org/10.1038/s41467-020-19160-7
- Knaflic, C.N. (2015). Storytelling with Data: A Data Visualization Guide for Business Professionals. Wiley.
- Ordenanza nro 11063 de 2004. Santa Fe. Argentina. Disponible en: https://www.concejosantafe.gov.ar/wp-content/uploads/Ordenanza/Ordenanza_11063.pdf