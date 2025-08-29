---
marp: true
theme: base
author: Julián Aragón
class: 
style: |
  /* Fondo por defecto para todas las diapositivas */
    section {
      background-image: url('./img/pie.png');
      background-size: cover;
    }
    div{
      justify-content: center; 
      gap: 10px; 
      flex-wrap: wrap; 
      margin: 0 auto;
    }

    h3{
        font-size:0.7rem;
    }

    .slides-container {
        display: flex;
        height: 800px;
        flex-direction: column;
        gap: 20px;
        padding: 30px;
    }
    
    .slide {
        border: 1px solid #e0e0e0;
        border-radius: 10px;
        overflow: hidden;
        min-height: 650px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
    }
    
    .slide-content {
        display: flex;
    }

    .title-slide{
        margin-left: 30px;
    }

    .fixed-column {
        flex: 1.2 1 0px;
        position: sticky;
        top: 0;
        align-self: flex-start;
        height: 100%;
    }
        
    .fixed-column h3 {
        color: #2c3e50;
        font-size: 1.4rem;
        border-bottom: 2px solid #3498db;
    }
        
    .fixed-column li {
        border-radius: 0 5px 5px 0;
        box-shadow: 0 2px 5px rgba(0, 0, 0, 0.05);
        font-size: 1.1rem;
    }

    .variable-column {
        flex: 1;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    
    .variable-content {
        width: 100%;
    }
    
    .variable-content h4 {
        font-size: 1.5rem;
        color: #2c3e50;
        text-align: center;
    }
            
---

<style scoped>
section {
    font-size: 35px;
    padding: 250px 45px;
    justify-content: center;
    text-align: center;
    background-image: url('./img/fondo.png');
    background-size: cover;
}

div{
    display: flex;
    text-align: center;
    align-items: center;
}

img{
    width: 250px;
}
</style>

<section>
   <h1>Introducción a la visualización de datos con Apache Superset</h1>
    <div>
        <div>
            <img src="./img/logo-infor.png"/><br/>
        </div>
        <div>
            <img src="./img/superset-logo.png"/><br/>
        </div>
    </div>
</section>

---

<style scoped>
section {
  font-size: 27px;
  padding: 20px 40px;
}

.lista{
    visibility: hidden;
}
</style>

<section data-marpit-fragments="9">
    <div class="slide">
        <div class="title-slide">
            <h1>Conceptos básicos</h1>
            <div class="fixed-column">
                <ul>
                    <li data-marpit-fragment="1">Datos</li>
                    <li data-marpit-fragment="2">Software</li>
                    <ol>
                        <li class="lista"></li>
                        <ol style="font-size: 1.5rem">
                            <li data-marpit-fragment="3">Ejecución irrestricta</li>
                            <li data-marpit-fragment="4">Acceso irrestricto al código fuente</li>
                            <li data-marpit-fragment="5">Inspección exhaustiva de los mecanismos de funcionamiento</li>
                            <li data-marpit-fragment="6">Adaptación para uso y necesidades de usuarias/os</li>
                            <li data-marpit-fragment="7">Libertad de estudio de funcionamiento</li>
                            <li data-marpit-fragment="8">Confección y distribución pública de copias</li>
                            <li data-marpit-fragment="9">Modificación del programa y distribución libre</li>
                        </ol>
                    </ol>
                </ul>
            </div>
        </div>
    </div>
</section>

---

<style scoped>
section {
  font-size: 27px;
  padding: 20px 40px;
}
</style>

<section>
<div class="slide">
    <div class="title-slide">
   <h1>Conceptos básicos</h1>
    <div class="fixed-column">
    <ul>
        <li >Datos</li>
        <li >Software</li>
        <ol>
            <li data-marpit-fragment="1">Software Libre</li>   
            <ol style="font-size: 1.5rem">
                <li >Ejecución irrestricta</li>
                <li >Acceso irrestricto al código fuente</li>
                <li >Inspección exhaustiva de los mecanismos de funcionamiento</li>
                <li >Adaptación para uso y necesidades de usuarias/os</li>
                <li >Libertad de estudio de funcionamiento</li>
                <li >Confección y distribución pública de copias</li>
                <li >Modificación del programa y distribución libre</li>
            </ol>
        </ol>
    </ul>
    </div>
    </div>
    </div>
</section>

---

<style scoped>
section {
  font-size: 40px;
  padding: 20px 40px;
}

.image-1{
    top: 0;
    left: 50%;
    transform: translateX(-50%) rotate(-5deg);
    z-index: 3;
}

.image-2 {
    bottom: 0;
    left: 25%;
    transform: translateX(-50%) rotate(3deg);
    z-index: 2;
}
        
.image-3 {
    top: 50%;
    right: 20%;
    transform: translateY(-50%) rotate(7deg);
    z-index: 1;   
}

</style>
<section data-marpit-fragments="3">
    <div>
        <div class="image-1"
            data-marpit-fragment="1">
           <img src="./img/cloud1.png"/><br/>
        </div>
        <div class="image-2" data-marpit-fragment="2">
           <img src="./img/cloud2.png"/><br/>
        </div>
        <div class="image-3" data-marpit-fragment="3">
           <img src="./img/cloud3.png"/><br/>
        </div>
    </div>
</section>

---
<style scoped>
section {
    font-size: 40px;
    padding: 2px 5px;
    justify-content: center;
    text-align: center;
}

.pdf{
    align-items: center; 
    gap: 50px; 
    flex-wrap: wrap; 
    margin: 0 auto;
}

</style>

<section>
    <div class="slide-container">
        <div class="title-slide">
            <div class="slide">
                <h1>Ordenanza nro 11063</h1>
                <div class="fixed-column">
                    <embed src="./Ordenanza_11063.pdf" type="application/pdf" width="100%"  />
                </div>
            </div>
        </div>
    </div>
</section>

---
<style scoped>
section {
    font-size: 40px;
    padding: 2px 5px;
    justify-content: center;
    text-align: center;
}

</style>
<section>
    <div>
        <h1>Análisis y visualización de datos</h1>
    </div>
</section>

---
<style scoped>
section {
  font-size: 30px;
  padding: 20px 40px;
}

ul{
    font-size: 1rem
}
</style>

<section>
    <div class="slide">
        <div class="title-slide">
            <h1>Principios de diseño y narrativa visual para comunicar patrones, tendencias y anomalías.</h1>
            <h3>Knaflic (2015)</h3>
        </div>
        <div class="fixed-column">
            <ul>
                <li>Comprender el contexto.</li>
                <li>Elegir una visualización efectiva.</li>
                <li>Eliminar el desorden.</li>
                <li>Enfocar la atención de la audiencia.</li>
                <li>Pensar como un/a Diseñador/a.</li>
                <li>Contar una historia.</li>
            </ul>
        </div>
    </div>
</section>

---
<style scoped>
section {
  font-size: 30px;
  padding: 20px 40px;
}
div{
    align-items: start; 
}

</style>

<section>
    <div class="slide">
    <div class="title-slide">
        <h1>Principios de diseño y narrativa visual para comunicar patrones, tendencias y anomalías.</h1>
        <h3>Knaflic (2015)</h3>
    </div>
        <div class="slide-content">
            <div class="fixed-column">
                <div>
                    <ul>
                        <li><strong>Comprender el contexto.</strong></li>
                        <li>Elegir una visualización efectiva.</li>
                        <li>Eliminar el desorden.</li>
                        <li>Enfocar la atención de la audiencia.</li>
                        <li>Pensar como un/a Diseñador/a.</li>
                        <li>Contar una historia.</li>
                    </ul>
                </div>
            </div>
            <div class="variable-column">
                <div class="variable-content" data-marpit-fragment="1">
                        <ul>
                            <li>Quién (Su Audiencia)</li>
                            <li>Qué (Acción)</li>
                            <li>Cómo (Mecanismo y Tono)</li>
                            <ol data-marpit-fragment="2">
                                <li>La historia de 3 minutos</li>
                                <li>La Gran idea</li>
                                <li>Storyboarding</li>
                            </ol>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>

---
<style scoped>
section {
  font-size: 30px;
  padding: 20px 40px;
}
div{
    align-items: start; 
}
img{
    width: 280px;
}
</style>

<section>
<div class="slide">
    <div class="title-slide">
        <h1>Principios de diseño y narrativa visual para comunicar patrones, tendencias y anomalías.</h1>
        <h3>Knaflic (2015)</h3>
    </div>
    <div class="slide-content">
        <div class="fixed-column">
            <ul>
                <li>Comprender el contexto.</li>
                <li><strong>Elegir una visualización efectiva.</strong></li>
                <li>Eliminar el desorden.</li>
                <li>Enfocar la atención de la audiencia.</li>
                <li>Pensar como un/a Diseñador/a.</li>
                <li>Contar una historia.</li>
            </ul>
        </div>
        <div class="variable-column">
            <div class="variable-content">
                <div>
                    <img src="./img/graphs.png" />
                </div>
            </div>
        </div>
    </div>
</div>
</section>

---

<style scoped>
section {
  font-size: 30px;
  padding: 20px 40px;
}
div{
    align-items: start; 
    
}
img{
    width: 400px;
}
</style>

<section>
<div class="slide">
    <div class="title-slide">
        <h1>Principios de diseño y narrativa visual para comunicar patrones, tendencias y anomalías.</h1>
        <h3>Knaflic (2015)</h3>
    </div>
    <div class="slide-content">
        <div class="fixed-column">
            <ul>
                <li>Comprender el contexto.</li>
                <li><strong>Elegir una visualización efectiva.</strong></li>
                <li>Eliminar el desorden.</li>
                <li>Enfocar la atención de la audiencia.</li>
                <li>Pensar como un/a Diseñador/a.</li>
                <li>Contar una historia.</li>
            </ul>
        </div>
        <div class="variable-column">
            <div class="variable-content">
                <div>
                    <img src="./img/torta1.png" />
                </div>
            </div>
        </div>
    </div>
</div>
</section>

---

<style scoped>
section {
  font-size: 30px;
  padding: 20px 40px;
}
div{
    align-items: start; 
    
}
img{
    width: 400px;
}
</style>

<section>
<div class="slide">
    <div class="title-slide">
        <h1>Principios de diseño y narrativa visual para comunicar patrones, tendencias y anomalías.</h1>
        <h3>Knaflic (2015)</h3>
    </div>
    <div class="slide-content">
        <div class="fixed-column">
            <ul>
                <li>Comprender el contexto.</li>
                <li><strong>Elegir una visualización efectiva.</strong></li>
                <li>Eliminar el desorden.</li>
                <li>Enfocar la atención de la audiencia.</li>
                <li>Pensar como un/a Diseñador/a.</li>
                <li>Contar una historia.</li>
            </ul>
        </div>
        <div class="variable-column">
            <div class="variable-content">
                <div>
                    <img src="./img/torta2.png"/>
                </div>
            </div>
        </div>
    </div>
</div>
</section>

---

<style scoped>
section {
  font-size: 30px;
  padding: 20px 40px;
}
div{
    align-items: start; 
    
}
img{
    width: 300px;
}
</style>

<section>
<div class="slide">
    <div class="title-slide">
        <h1>Principios de diseño y narrativa visual para comunicar patrones, tendencias y anomalías.</h1>
        <h3>Knaflic (2015)</h3>
    </div>
    <div class="slide-content">
        <div class="fixed-column">
            <ul>
                <li>Comprender el contexto.</li>
                <li><strong>Elegir una visualización efectiva.</strong></li>
                <li>Eliminar el desorden.</li>
                <li>Enfocar la atención de la audiencia.</li>
                <li>Pensar como un/a Diseñador/a.</li>
                <li>Contar una historia.</li>
            </ul>
        </div>
        <div class="variable-column">
            <div class="variable-content">
                <div>
                    <img src="./img/anillo.png" />
                </div>
            </div>
        </div>
    </div>
</div>
</section>

---

<style scoped>
section {
  font-size: 30px;
  padding: 20px 40px;
}
div{
    align-items: start; 
    
}
img{
    width: 400px;
}
</style>

<section>
<div class="slide">
    <div class="title-slide">
        <h1>Principios de diseño y narrativa visual para comunicar patrones, tendencias y anomalías.</h1>
        <h3>Knaflic (2015)</h3>
    </div>
    <div class="slide-content">
        <div class="fixed-column">
            <ul>
                <li>Comprender el contexto.</li>
                <li><strong>Elegir una visualización efectiva.</strong></li>
                <li>Eliminar el desorden.</li>
                <li>Enfocar la atención de la audiencia.</li>
                <li>Pensar como un/a Diseñador/a.</li>
                <li>Contar una historia.</li>
            </ul>
        </div>
        <div class="variable-column">
            <div class="variable-content">
                <div>
                    <img src="./img/3d.png" />
                </div>
            </div>
        </div>
    </div>
</div>
</section>

---

<style scoped>
section {
  font-size: 30px;
  padding: 20px 40px;
}
div{
    align-items: start; 
    
}
img{
    width: 400px;
}
</style>

<section>
<div class="slide">
    <div class="title-slide">
        <h1>Principios de diseño y narrativa visual para comunicar patrones, tendencias y anomalías.</h1>
        <h3>Knaflic (2015)</h3>
    </div>
    <div class="slide-content">
        <div class="fixed-column">
            <ul>
                <li>Comprender el contexto.</li>
                <li><strong>Elegir una visualización efectiva.</strong></li>
                <li>Eliminar el desorden.</li>
                <li>Enfocar la atención de la audiencia.</li>
                <li>Pensar como un/a Diseñador/a.</li>
                <li>Contar una historia.</li>
            </ul>
        </div>
        <div class="variable-column">
            <div class="variable-content">
                <div>
                    <img src="./img/ejy.png" />
                </div>
            </div>
        </div>
    </div>
</div>
</section>

---

<style scoped>
section {
  font-size: 30px;
  padding: 20px 40px;
}
div{
    align-items: start; 
    
}
.imagenes {
    width: 500px;
    height: 400px;
    margin: 0 auto;
    position: relative;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
}

/* Estilos generales para las imágenes */
.imagenes img {
    height: 50%;
    position: absolute;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    border: 2px solid white;
}
    
 /* Imagen 1: Cuadrante superior izquierdo */
.image-1 {
    top: 0;
    left: 0;
    border-radius: 0 0 20px 0;
}

/* Imagen 2: Cuadrante superior derecho */
.image-2 {
    top: 0;
    right: 0;
    height: 200px;
    border-radius: 0 0 0 20px;
}

/* Imagen 3: Cuadrante inferior izquierdo */
.image-3 {
    bottom: 0;
    left: 0;
    border-radius: 0 20px 0 0;
}

/* Imagen 4: Cuadrante inferior derecho */
.image-4 {
    bottom: 0;
    right: 0;
    border-radius: 20px 0 0 0;
}

</style>

<section>
<div class="slide">
    <div class="title-slide">
        <h1>Principios de diseño y narrativa visual para comunicar patrones, tendencias y anomalías.</h1>
        <h3>Knaflic (2015)</h3>
    </div>
    <div class="slide-content">
        <div class="fixed-column">
            <ul>
                <li>Comprender el contexto.</li>
                <li><strong>Elegir una visualización efectiva.</strong></li>
                <li>Eliminar el desorden.</li>
                <li>Enfocar la atención de la audiencia.</li>
                <li>Pensar como un/a Diseñador/a.</li>
                <li>Contar una historia.</li>
            </ul>
        </div>
        <div class="variable-column">
            <div class="variable-content">
                <div class="imagenes">
                    <img class="image-1" src="./img/torta2.png"/>                
                    <img class="image-2" src="./img/anillo.png"/>
                    <img class="image-3" src="./img/3d.png"/>
                    <img class="image-4" src="./img/ejy.png"/>
                </div>
            </div>
        </div>
    </div>
</div>
</section>

---

<style scoped>
section {
  font-size: 30px;
  padding: 20px 40px;
}
div{
    align-items: start; 
    justify-self: center;
    
}
img{
    border-radius: 10px;
    box-shadow: 10px 10px 10px rgba(0, 0, 0, 0.2);
}
.imagenes{
    display: flex;
    flex-direction: row;

}
.image-1{
    width: 180px;
}

.image-2 {
    width: 400px;
}

</style>

<section>
<div class="slide">
    <div class="title-slide">
        <h1>Principios de diseño y narrativa visual para comunicar patrones, tendencias y anomalías.</h1>
        <h3>Knaflic (2015)</h3>
    </div>
    <div class="slide-content">
        <div class="fixed-column">
            <ul>
                <li>Comprender el contexto.</li>
                <li>Elegir una visualización efectiva.</li>
                <li><strong>Eliminar el desorden.</strong></li>
                <li>Enfocar la atención de la audiencia.</li>
                <li>Pensar como un/a Diseñador/a.</li>
                <li>Contar una historia.</li>
            </ul>
        </div>
        <div class="variable-column">
            <div class="variable-content">
                <div>
                    <div><strong>Principios Gestalt de la percepción visual</strong></div>
                </div>
                <div class="imagenes">
                    <img data-marpit-fragment="1" class="image-1" src="./img/2.2.png" />
                    <img data-marpit-fragment="1" class="image-2" src="./img/2.3.png" />
                </div>
            </div>
        </div>
    </div>
</div>
</section>

---

<style scoped>
section {
  font-size: 30px;
  padding: 20px 40px;
}
div{
    align-items: start; 
    justify-self: center;
    
}
img{
    border-radius: 10px;
    box-shadow: 10px 10px 10px rgba(0, 0, 0, 0.2);
}
.imagenes{
    display: flex;
    flex-direction: row;

}
.image-1{
    width: 350px;
}

.image-2 {
    width: 250px;
}
</style>

<section>
<div class="slide">
    <div class="title-slide">
        <h1>Principios de diseño y narrativa visual para comunicar patrones, tendencias y anomalías.</h1>
        <h3>Knaflic (2015)</h3>
    </div>
    <div class="slide-content">
        <div class="fixed-column">
            <ul>
                <li>Comprender el contexto.</li>
                <li>Elegir una visualización efectiva.</li>
                <li><strong>Eliminar el desorden.</strong></li>
                <li>Enfocar la atención de la audiencia.</li>
                <li>Pensar como un/a Diseñador/a.</li>
                <li>Contar una historia.</li>
            </ul>
        </div>
        <div class="variable-column">
            <div class="variable-content">
                <div>
                    <div><strong>Principios Gestalt de la percepción visual</strong></div>
                </div>
                <div class="imagenes">
                    <img data-marpit-fragment="1" class="image-1" src="./img/2.4.png" />
                    <img data-marpit-fragment="1" class="image-2" src="./img/2.5.png" />
                </div>
            </div>
        </div>
    </div>
</div>
</section>

---

<style scoped>
section {
  font-size: 30px;
  padding: 20px 40px;
}
div{
    align-items: start; 
    justify-self: center;
    
}
img{
    width: 500px;
    border-radius: 10px;
    box-shadow: 10px 10px 10px rgba(0, 0, 0, 0.2);
}
</style>

<section>
<div class="slide">
    <div class="title-slide">
        <h1>Principios de diseño y narrativa visual para comunicar patrones, tendencias y anomalías.</h1>
        <h3>Knaflic (2015)</h3>
    </div>
    <div class="slide-content">
        <div class="fixed-column">
            <ul>
                <li>Comprender el contexto.</li>
                <li>Elegir una visualización efectiva.</li>
                <li><strong>Eliminar el desorden.</strong></li>
                <li>Enfocar la atención de la audiencia.</li>
                <li>Pensar como un/a Diseñador/a.</li>
                <li>Contar una historia.</li>
            </ul>
        </div>
        <div class="variable-column">
            <div class="variable-content">
                <div>
                    <div><strong>Principios Gestalt de la percepción visual</strong></div>
                </div>
                <div>
                    <img src="./img/2.6.png" />
                </div>
            </div>
        </div>
    </div>
</div>
</section>

---

<style scoped>
section {
  font-size: 30px;
  padding: 20px 40px;
}
div{
    align-items: start; 
    justify-self: center;
    
}
img{
    width: 300px;
    border-radius: 10px;
    box-shadow: 10px 10px 10px rgba(0, 0, 0, 0.2);
}
</style>

<section>
<div class="slide">
    <div class="title-slide">
        <h1>Principios de diseño y narrativa visual para comunicar patrones, tendencias y anomalías.</h1>
        <h3>Knaflic (2015)</h3>
    </div>
    <div class="slide-content">
        <div class="fixed-column">
            <ul>
                <li>Comprender el contexto.</li>
                <li>Elegir una visualización efectiva.</li>
                <li><strong>Eliminar el desorden.</strong></li>
                <li>Enfocar la atención de la audiencia.</li>
                <li>Pensar como un/a Diseñador/a.</li>
                <li>Contar una historia.</li>
            </ul>
        </div>
        <div class="variable-column">
            <div class="variable-content">
                <div>
                    <div><strong>Principios Gestalt de la percepción visual</strong></div>
                </div>
                <div>
                    <img src="./img/2.7.png" />
                </div>
            </div>
        </div>
    </div>
</div>
</section>

---

<style scoped>
section {
  font-size: 30px;
  padding: 20px 40px;
}
div{
    align-items: start; 
    justify-self: center;
    
}
img{
    width: 250px;
    border-radius: 10px;
    box-shadow: 10px 10px 10px rgba(0, 0, 0, 0.2);
}
</style>

<section>
<div class="slide">
    <div class="title-slide">
        <h1>Principios de diseño y narrativa visual para comunicar patrones, tendencias y anomalías.</h1>
        <h3>Knaflic (2015)</h3>
    </div>
    <div class="slide-content">
        <div class="fixed-column">
            <ul>
                <li>Comprender el contexto.</li>
                <li>Elegir una visualización efectiva.</li>
                <li><strong>Eliminar el desorden.</strong></li>
                <li>Enfocar la atención de la audiencia.</li>
                <li>Pensar como un/a Diseñador/a.</li>
                <li>Contar una historia.</li>
            </ul>
        </div>
        <div class="variable-column">
            <div class="variable-content">
                <div>
                    <div><strong>Principios Gestalt de la percepción visual</strong></div>
                </div>
                <div>
                    <img src="./img/2.8.png" />
                </div>
            </div>
        </div>
    </div>
</div>
</section>

---

<style scoped>
section {
  font-size: 30px;
  padding: 20px 40px;
}
div{
    align-items: start; 
    justify-self: center;
    
}
img{
    width: 500px;
    border-radius: 10px;
    box-shadow: 10px 10px 10px rgba(0, 0, 0, 0.2);
}
</style>

<section>
<div class="slide">
    <div class="title-slide">
        <h1>Principios de diseño y narrativa visual para comunicar patrones, tendencias y anomalías.</h1>
        <h3>Knaflic (2015)</h3>
    </div>
    <div class="slide-content">
        <div class="fixed-column">
            <ul>
                <li>Comprender el contexto.</li>
                <li>Elegir una visualización efectiva.</li>
                <li><strong>Eliminar el desorden.</strong></li>
                <li>Enfocar la atención de la audiencia.</li>
                <li>Pensar como un/a Diseñador/a.</li>
                <li>Contar una historia.</li>
            </ul>
        </div>
        <div class="variable-column">
            <div class="variable-content">
                <div>
                    <div><strong>Principios Gestalt de la percepción visual</strong></div>
                </div>
                <div>
                    <img src="./img/2.9.png" />
                </div>
            </div>
        </div>
    </div>
</div>
</section>

---

<style scoped>
section {
  font-size: 30px;
  padding: 20px 40px;
}
div{
    align-items: start; 
    justify-self: center;
    
}
img{
    width: 500px;
    border-radius: 10px;
    box-shadow: 10px 10px 10px rgba(0, 0, 0, 0.2);
}
</style>

<section>
<div class="slide">
    <div class="title-slide">
        <h1>Principios de diseño y narrativa visual para comunicar patrones, tendencias y anomalías.</h1>
        <h3>Knaflic (2015)</h3>
    </div>
    <div class="slide-content">
        <div class="fixed-column">
            <ul>
                <li>Comprender el contexto.</li>
                <li>Elegir una visualización efectiva.</li>
                <li><strong>Eliminar el desorden.</strong></li>
                <li>Enfocar la atención de la audiencia.</li>
                <li>Pensar como un/a Diseñador/a.</li>
                <li>Contar una historia.</li>
            </ul>
        </div>
        <div class="variable-column">
            <div class="variable-content">
                <div>
                    <div><strong>Principios Gestalt de la percepción visual</strong></div>
                </div>
                <div>
                    <img src="./img/2.10.png" />
                </div>
            </div>
        </div>
    </div>
</div>
</section>

---

<style scoped>
section {
  font-size: 30px;
  padding: 20px 40px;
}
div{
    align-items: start; 
    justify-self: center;
    
}
img{
    width: 250px;
    border-radius: 10px;
    box-shadow: 10px 10px 10px rgba(0, 0, 0, 0.2);
}
</style>

<section>
<div class="slide">
    <div class="title-slide">
        <h1>Principios de diseño y narrativa visual para comunicar patrones, tendencias y anomalías.</h1>
        <h3>Knaflic (2015)</h3>
    </div>
    <div class="slide-content">
        <div class="fixed-column">
            <ul>
                <li>Comprender el contexto.</li>
                <li>Elegir una visualización efectiva.</li>
                <li><strong>Eliminar el desorden.</strong></li>
                <li>Enfocar la atención de la audiencia.</li>
                <li>Pensar como un/a Diseñador/a.</li>
                <li>Contar una historia.</li>
            </ul>
        </div>
        <div class="variable-column">
            <div class="variable-content">
                <div>
                    <div><strong>Principios Gestalt de la percepción visual</strong></div>
                </div>
                <div>
                    <img src="./img/2.11.png" />
                </div>
            </div>
        </div>
    </div>
</div>
</section>

---

<style scoped>
section {
  font-size: 30px;
  padding: 20px 40px;
}
div{
    align-items: start; 
    justify-self: center;
    
}
img{
    border-radius: 10px;
    box-shadow: 10px 10px 10px rgba(0, 0, 0, 0.2);
}
.imagenes{
    display: flex;
    flex-direction: row;

}
.image-1{
    width: 450px;
}

.image-2 {
    width: 450px;
}
</style>

<section>
<div class="slide">
    <div class="title-slide">
        <h1>Principios de diseño y narrativa visual para comunicar patrones, tendencias y anomalías.</h1>
        <h3>Knaflic (2015)</h3>
    </div>
    <div class="slide-content">
        <div class="fixed-column">
            <ul>
                <li>Comprender el contexto.</li>
                <li>Elegir una visualización efectiva.</li>
                <li><strong>Eliminar el desorden.</strong></li>
                <li>Enfocar la atención de la audiencia.</li>
                <li>Pensar como un/a Diseñador/a.</li>
                <li>Contar una historia.</li>
            </ul>
        </div>
        <div class="variable-column">
            <div class="variable-content">
                <div>
                    <div><strong>Principios Gestalt de la percepción visual</strong></div>
                </div>
                <div class="imagenes">
                    <img data-marpit-fragment="1" class="image-1" src="./img/2.12.png" />
                    <img data-marpit-fragment="1" class="image-2" src="./img/2.13.png" />
                </div>
            </div>
        </div>
    </div>
</div>
</section>

---
<style scoped>
section {
  font-size: 30px;
  padding: 20px 40px;
}
div{
    align-items: start; 
}

</style>

<section>
    <div class="slide">
    <div class="title-slide">
        <h1>Principios de diseño y narrativa visual para comunicar patrones, tendencias y anomalías.</h1>
        <h3>Knaflic (2015)</h3>
    </div>
        <div class="slide-content">
            <div class="fixed-column">
                <div>
                    <ul>
                        <li>Comprender el contexto.</li>
                        <li>Elegir una visualización efectiva.</li>
                        <li>Eliminar el desorden.</li>
                        <li><strong>Enfocar la atención de la audiencia.</strong></li>
                        <li>Pensar como un/a Diseñador/a.</li>
                        <li>Contar una historia.</li>
                    </ul>
                </div>
            </div>
            <div class="variable-column">
                <div class="variable-content" data-marpit-fragment="1">
                        <ul>
                            <li>Quién (Su Audiencia)</li>
                            <li>Qué (Acción)</li>
                            <li>Cómo (Mecanismo y Tono)</li>
                            <ol data-marpit-fragment="2">
                                <li>La historia de 3 minutos</li>
                                <li>La Gran idea</li>
                                <li>Storyboarding</li>
                            </ol>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>

---


