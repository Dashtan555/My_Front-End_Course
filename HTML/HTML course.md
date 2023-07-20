<!-- Mis apuntes de Programación -->
# **HTML**

**Índice**
1. [Primeros pasos](#id1)
2. [Texto](#id2)
    * [Encabezado](#id2.1)
    * [Listas](#id2.2)
    * [Formatos](#id2.3)
    * [Citas](#id2.4)
    * [Tiempo](#id2.5)
3. [Navegación](#id3)
    * [Vínculos](#id3.1)
    * [Rutas](#id3.2)
    * [Navegación](#id3.3)
    * [Barras](#id3.4)
4. [Imágenes](#id4)
    * [Imagen](#id4.1)
    * [Resolución](#id4.2)
    * [Figura](#id4.3)
    * [Foto](#id4.4)
5. [Multimedia](#id5)
    * [Audio](#id5.1)
    * [Video](#id5.2)
    * [iFrame](#id5.3)
6. [Contenido](#id6)
    * [Etiqueta de Bloque (div)](#id6.1)
    * [Etiqueta de Bloque (Span)](#id6.2)
    * [Atributos globales](#id6.3)
    * [Accesibilidad](#id6.4)
7. [Estructura](#id7)
    * [DOCTYPE](#id7.1)
    * [head](#id7.2)
    * [body](#id7.3)
    * [table](#id7.4)
8. [Formularios](#id8)
    * [Input](#id8.1)
    * [Textarea](#id8.2)
    * [Fieldset](#id8.3)
    * [Form](#id8.4)
___

<div id='id1'>

## **Primeros pasos**

El primer documento de una pagina html debe ser **index.html**

### Hola mundo
Este es un código sencillo, que representa partes de lenguaje **HTML**, es un **Hola mundo**, para quién no este familiarizado con este termino, es una iniciación en el desarrollo del software.

```html
<p>Hello Word..!</p>
```

### Partes de Html

1. Simbolos `< >` que se abren y se cierran, estos se denominan etiquetas: 
`<p>`: APertura de una etiqueta, `</p>` cierre de una etiqueta, no todas las etiquetas se cierran como por ejemplo: `<br/>` esta es para dar un salto de línea y así ya esta completa.
* **`<p> </p>`** = párrafo  
* **`<a> </a>`** = vínculo
2. Atributos, le da a las etiquetas caracteristicas especiales como (title) `<p title="Nota"> </p>`
3. Texto entre las etiquetas `<p>Aquí va el texto de la etiqueta.</p>`
4. `<!-- -->` Cometarios 

```html
<!-- Este es un comentario -->
<p title="Nota">Párrafo</p>
```
5. Entidades de caracteres:  
* **`&copy;`** : &copy;  
* **`&cap;`** : &cap;  
* **`&coprod;`** : &coprod;

Una pagina web tiene una estructura de una árbol.

<div id='id2'>

## **Texto**

Simple texto, cada vez que uso la etiqueta p, salta a otra línea, el objetivo de HTML no es dar apariencia, sino mas bien dar **estructura, relevancia o significado** a los diferentes elementos y textos de una pagina web.

* **`<em>`**: enfasis.
* **`<i>`**: cursiva.
* **`<b>`**: bold, para llamar la atención.
* **`<strong>`**: importancia del contenido.
* **`<small>`**: representa un texto mas pequeño.

```html
<p>Simple Párrafo</p>
<p>Esto <em>no</em> es un error</p>
<p>Miré a las nubes y pensé, <i>esto no puede ser real!</i></p>
<p><b>HTML</b>me llama la ateción</p>
<p>No te olvides de la importacia de <strong>HTML</strong></p>
<p><small>&copy;2021. Todos los derechos reservados.</small></p>
<!-- Diferencia entre línea y bloque -->
<p>Simple <span>Párrafo</span></p> <!-- Misma línea, etiqueta de línea -->
<p>Simple <p>Párrafo</p></p> <!-- Salta a otra linea, etiqueta de bloque -->
<b>No cerrada <!-- Tener cuidado al cerrar, puede arrastrar el estilo -->
<p>Estas&nbsp;palabras&nbsp;no&nbsp;saltan&nbsp;líneas&nbsp;en&nbsp;ventanas&nbsp;pequeñas</p>

```
En **HTML** no es sensible a las mayusculas o minusculas en su programación

<div id='id2.1'>

* ### **Encabezado**
Etiquetas muy importantes que indican los títulos `<h1> Título </h1>` y subtítulos de la pagina web, da diferente significado a cada texto, sirve para ubicar al buscador como google, bing.

```html
<h1>Título</h1>
<h2>Subtítulo</h2>
<h3>Subtítulo</h3>
<h4>Subtítulo</h4>
<h5>Subtítulo</h5>
<h6>Subtítulo</h6>
```

<div id='id2.2'>

* ### **Listas**
Para generación de listas
* **`<ul>`**: lista desordenada
* **`<ol>`**: listas ordenadas
* **`<li>`**: item de lista
* **`<dt>`**: lista de definición
* **`<dd>`**: definición de la lista

```html
<!-- Listas desordenadas -->
<ul>
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
</ul>

<!-- Listas ordenadas -->

<ol>
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
</ol>

<!-- Listas de definiciones -->

<dl>
    <dt>HTML</dt>
    <dd>CSS</dd>
    <dd>JavaScript</dd>
</dl>

```

<div id='id2.3'>

* ### **Formatos**
Etiquetas que da formato
* `<code> </code>`: indica que es un codigo.
* `&lt; text &gt;`: para indicar ejemplos de código
* `<br />`: rotura de línea
* `<sub> </sub>`: subíndice
* `<sup> </sup>`: superíndice

```html
<p>Utiliza este código en CSS
    <code>{ background: blue; }</code>
</p>

<p>Utiliza este código en HTML:
    <code>&lt;body&gt;</code>
</p>

<!-- Esto muestra en una sola línea, pero al colocar <br> hace el salto -->

<p>Quiero
    ver
    esto <br/>
    en <br/>
    muchas <br/>
    líneas
</p>

<!-- Subíndice y super índice -->
<p>CO<sub>2</sub></p>
<p>n<sup>2</sup></p>
<p>Referencia a un libro.<sup>1</sup></p>
```

<div id='id2.4'>

* ### **Citas**
Estas etiquetas se utiliza para citar a otros autores
* `<blockquote> </blockquote>`: cita en bloque
* `<q> </q>`: cita en línea, debe estar dentro de un `<p>`


```html
<!-- Cita en bloque-->
<blockquote>
    <p>La mediocirdad para algunos es normal, la locura es poder ver más allá</p>
    <cite>Charly García</cite>

<!-- Cita en línea-->
    <p> Jóse Mujica dijo:
        <q>Ser libre es gastar la mayor cantidad de tiempo de nuestra bida en aquello que nos gusta hacer. </q>
    </p>
</blockquote>
```

<div id='id2.5'>

* ### **Tiempo**
Etiquetas relacionadas con el tiempo y las fechas.
Atributo:
* `<time datetime="">`: Atributo en el cual se puede incluir una fecha.
* `<datetime="10:00:00-0800">`: (0800) zona horaria 

```html
<p>
    <time datetime="2024-04-20">Sábado</time>
    a las
    <time datetime="16:20:00.5-08:00">4:20</time>
</p>

<p>Nos veos a las 
    <time datetime="2024-04-20 10:00:00-0800">10</time>
</p>
```

<div id='id3'>

## **Navegación**
Para la navegación dentro de la pagina web existen diferentes maneras:

<div id='id3.1'>

* ### **Vínculos**
Sirve para redireccionar a otros lugares, u otras páginas
* **`<a>`**: vínculos, atributo `href=""`, donde se puede icluir la dirección de otra pagina u otro elemento
```html
<a href="blog.html">Ir a la página del blog</a>
```

<div id='id3.2'>

* ### **Rutas**
  * **Vínculo relativo**: Es cuando se usa la barra oblicua / dos punto (..) significa ir a la carpeta padre, poner un solo punto (.) significa la carpeta presente.
  * **Vínculo absoluto**: Es aquel incluye la dirección completa.


```html
<!-- Vínculo relativo -->
<a href="./blog.html">Ir a la página del blog</a>

<!-- Vínculo absoluto -->
<a href="https://www.google.com/">Ir a Google</a>
```

<div id='id3.3'>

* ### **Navegación**
Consiste en el metodo de referenciar a las diferentes páginas creadas para estar apuntando en varias direcciones y asi lograr que el usuario pueda bavegar facilmente en nuestro sitio web, a tráves de los vinculos relativos u absolutos.

<div id='id3.4'>

* ### **Barras**
Barras de navegación, con diferentes viculos.  
* **`<nav> </nav>`**: Delimita una área de navegación. 
* **`<footer> </footer>`**: Es otro tipo de barra de navegación pero esta representa un pie de página.   
Contiene algunos atributos:  
    * **`<nav role="navigation">`**: Se puedes usar de varios roles.
    * **`<nav aria-label="Menú principal"">`**: Da nombre a esta etiqueta.

```html
<nav role="navigation" aria-label="Menú Principal">
    <a href="midominio.com">Hoga</a>
    <a href="midomini.com/blog.html">Blog</a>
    <a href="midominio.com/sections/about.html">Acerca De</a>
</nav>

<!-- Para no incluir tanto código -->
<nav role="navigation" aria-label="Menú Principal">
    <a href="/">Hoga</a>
    <a href="/blog.html">Blog</a>
    <a href="/sections/about.html">Acerca De</a>
</nav>

<!--  Otro tipo de barra de navegación/especifico para un pie de página -->
<footer>
    <a href="/">Hoga</a>
    <a href="/blog.html">Blog</a>
    <a href="/sections/about.html">Acerca De</a>
</footer>

```

<div id='id4'> 

## **Imágenes**

Como agregar un archivo de imagen, las imagnes  archivos no deben ser muy pesados para que la renderización de la página web sea rapida y efectiva, admite achivos como:  
* jpeg
* jpg
* png
* svg
* gif

<div id='id4.1'>

* ### **Img**
La etqueta **`<img/>`** que representa una imagen, y se debe colocar el atributo:
* **`<img src=""/>`**: Fuente de la imagen
* **`<img alt=""/>`**: Texto alternativo de la imagen
* **`<img width=""/>`**: Parametro de ancho de la imagen 
* **`<img height=""/>`**: Parametro de alto de la imagen

```html
<body>
    <img src="./arches.jpeg" alt="Arches" width="300" height="200"/>
</body>
```

<div id='id4.2'>

* ### **Resolución**
Este atributo **`<img srcset=""/>`**permite elegir el tamaño de imagen que necesitemos se muestre dependiendo de la resolución de la pantalla en la página web.

```html
<body>
    <img src="./arches.jpeg" alt="Arches" width="300" height="200" srcset="./arches-600.jpg 2x, ./arches-1200.jpg 3x"/>
</body>
```

<div id='id4.3'>

* ### **Figure**
**`<figuere> </figure>`** en esta etiqueta se puede colocar la etiqueta **`<figcaption> </figcaption>`** se puede incluir una imagen y un caption, un subtítulo, ayuda a la semantica a los buscadores.

```html
<figure>
    <img src="./arches.jpeg" alt="Arches" width="300" height="200" srcset="./arches-600.jpg 2x, ./arches-1200.jpg 3x"/>
    <figcaption>Estes es el subtítulo de la imagen</figcaption>
</figure>
```

<div id='id4.4'>

* ### **Picture**
**`<picture> </picture>`** en esta etioqueta tiene mas etiquetas que nos permite indicar las diferentes fuentes de donde proviene nuestra imagen, y tambien se puede colocar un atributo **`<source media="">`** en el cual nos permite indicar en que tamaño del navegador vamos a mostrar diferentes tipos de imagenes.

```html
<picture>
    <source media="(min-width:1200px)" srcset="./arches-1200.jpg">
    <source media="(min-width:600px)" srcset="./arches-600.jpg">
    <img src="./arches.jpeg" alt="Arches" width="300" srcset="./arches-600.jpg 2x, ./arches-1200.jpg 3x"/>
</picture>
```

<div id='id5'>

## **Multimetimedia**
En las páginas web tambien podemos incluir audio, videos; objetos multimedia.

<div id='id5.1'>

* ### **Audio**
**`<audio> </audio>`** nos permite colocar audio en nuestras páginas web, y este tambien tiene una serie de atributos muy utiles.
* **controls**: no se debe colocar qeu valor es, y representa los controles
* **src**: se coloca la dirección del audio
* **loop**: permite hacer un lazo del audio
* **autoplay**: esto permite reproducir, ni bien se entra en una página.

```html
<audio controls src="audiomp3" loop autoplay>
    <source src="audio.mp3" type="audio/mpeg">
    <source src="audio.ogg" type="audio/ogg; codec=opus">
    Los sentimos. Tú navegador no soporta este formato.
</audio>
```

<div id='id5.2'>

* ### **Video**
La etiqueta **`<video> </video>`** funciona de manera muy similar a la de audio, y esta representa un video. 

```html
<video controls src="audiomp3" loop autoplay>
    <source src="video.mp4" type="video/mp4">
    Los sentimos. Tú navegador no soporta este formato.
</video>
```

<div id='id5.3'>

* ### **iFrame**
Permite poner contenido de otros sitios web en tú página, se puede incluir algunos atributos como:
* **width**: Ancho
* **height**: Anltura
* **src**: Fuente
* **frameborder**: El tamaño del borde

```html
<!-- De Google Maps, Youtube, Facebook -->
<iframe width ="560" heigth ="315" src="https://www.youtube.com/embed/8BZp6Of6KK0" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen>       
</iframe>

<!-- Ejemplo 2 , lo encuentras en Youtube en compartir "Insertar"-->
<iframe width="560" height="315" src="https://www.youtube.com/embed/krEecQY3RUg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
```
<div id='id6'>

## **Contenedores**
1. **`<div> </div>`** se utilza par agrupar etiquetas, y formar bloques en diferentes líneas
2. **`<span> </span>`** se utilza para un grupo mas pequeño de una o más palabras junto con atributos
3. **`<p> </p>`**    se uza como un contenedor de un grupo de texto

<div id='id6.1'>

* ### **Div**
Etiqueta de bloque, cualquier información dentro de esta etiqueta se crea un bloque, muy utilizada para envolver otros elementos, existen otros
```html
<!-- Ejemplo de Div en Bloque-->
<div>Soy un Div</div>
<div>Soy un Div</div>
<div>Soy un Div</div>
```

<div id='id6.2'>

* ### **Span**
Etiqueta de bloque pero separa en lineas y no en bloque, cualquier información dentro de esta etiqueta se crea un bloque, muy utilizada para envolver otros elementos, existen otros
```html
<!-- Ejemplo de Span en línea-->
<div>Soy un Span</div>
<div>Soy un Span</div>
<div>Soy un Span</div>
```
```html
<!-- Ejemplo semántico-->
<div>Me gusta la canción <span lang="en">Elevation</span></div>
```
<div id='id6.3'>

* ### **Atributos globales**
Se puede usar en cualquier tipo de etiqueta:  

   * **id** Identificación unica / para identificar una etiqueta, identificar parrafo, mas usado con CSS, solo para una etiqueta sola
   * **class** Parecido al anterior pero sirve para identificar algun grupo, se puede rusar.
   * **contenteditable** Puedes editar este contenido
   * **lang** Indica el lenguaje del contenigo es-Españo, en-English, es-MX español de Mexico, ayuda a Google a encontrar la página
   * **dir** Indica la dirección "rtl" right to left de izaquierda a derecha, para escritos en arabe por ejemplo.

```html
<!-- Ejemplo de Atributos globales-->
<p id="parrafo1" class="muchos">No hay nadie como yo</p>
<p class="muchos">Unidos somos más</p>
<p contenteditable="true">Puedes ediatr este contenido</p>
<p lang="es">Esto esta escrito en español</p>
<p dir="rtl">Esto está escrito en العربية (árabe)</p>
```
<div id='id6.4'>

* ### **Accesibilidad**
Otro atributo global (Roles ARIA), la accesibilidad se trata de asegurarnos que personas que tienen discapacidades no tengan problemas revisando nuestra pagina Web, al manipular algun contexto para hacerlo mas visible. (como para escuchar la pagina web, para una persona con discapacidad visual)

```html
<!-- Roles Aria para Accesibilidad - Accesibilidad Tree Inspector -->
<div aria-label="H2O">
    <div aria-hidden="true">
        <span>H</span>
        <span>2</span>
        <span>O</span>
    </div>
</div>
<!-- En el ejemplo se intenta dar un formato por separado a cada letra, con el atributo globarl aria-label y aria-hidden, para personas discapacitadas se les hace facil escuchar, si es que no es util el diseño creado -->
```
* ### **Lang**
El atributo **lang** es un atributo global y especifica el idioma para el contenido de elemento.  
La etiqueta **html** encierra a toda mi pagina web
```html
<html lang="en-US"></html>
<html lang="en-GB"></html>
<p lang="es-MX">Horale guey</p>
```
<div id='id7'>

## **Estructura**
Estructura de una pagina web de principio a fin
* **Index.html:** es el archivo principal de la pagina web de mi proyecto

<div id='id7.1'>

* ### **DOCTYPE**
**<!doctype html>** Indica que tipo de documento es  
**<html.></html.>** Raiz de mi documento   
 
**lang** Idioma  
**dir** Dirección del documento rtl = (right yo left) (De izquierda a derecha) ó ltr = (left to right) (De izquierda a derecha)  
**charset** Formato de codificación de caracteres UTF-8 letras, caracteres y hasta emojis (130 000 caracteres)
```html
<!doctype html>
<html lang="es" dir="ltr" charset="UTF-8">

<!-- Información no visible que el navegador necesita -->
<head></head>

<!-- Todo el contenido visible para los usuarios -->
<body></body>

</html>
```

<div id='id7.2'>

* ### **head**
Información que debe ir en el **head**, esta información no es visible al usuario pero si necesaria para que el navegador sea mas fácil encontrarla o clasificarla.  
**meta** Te permite incluir información para la pagina (codificación de caracteres)
**title** Titulo de la pagina Web  
**link** incluye diferenetes recursos (rel) indica una hoja de estilos (href) referencia al archivo css  
**meta** (viewport) ayuda que la pagina web se adapte a la pantalla adecuadamente

```html
<head>
    <meta charset="UTF-8" />
    <title>Darwin página web</title>
    <link rel="stylesheet" href="css/style.css">
    <script src="js/script.js"></script>
    <meta name="viewport" content="width=device-width, initial-scale-1" />

    <meta name="description" content="Página de emeplo sobre aprendizaje en HTML"/>
    <meta name="application-name" content="Aplication de HTML"/>
    <meta name="msapplication-TileImagen" content="/img/mstile-144x144.png"/>
    <meta name="theme-color" content="#000000"/>

    <link rel="manifest" href="/manifest.json" />
    <link rel="icon" href="/favicon.ico" />
    <link rel="preload" href="/font.woff2" as="font" type="font/woff2" crossorigin="anonymous" />
</head>
```

<div id='id7.3'>

* ### **body**
Aqui se puede incluir todo lo que muestra al usuario, se debe incluir siempre

```html
<body>
    <nav></nav>
    <!-- Encabezado -->
    <header>
        <h1></h1>
    </header>
    <!-- COntenido principal -->
    <main>
        <!-- Articulo: Unidad de información -->
        <article></article>
        <!-- Secciones de contenido -->
        <section></section>
        <!-- Contenido de lado -->
        <aside></aside>
    </main>
    <!-- Pie de página -->
    <footer></footer>
</body>
```

<div id='id7.4'>

* ### **table**
Para crear tablas en Html  
**th** header en la tabla  
**td** datos de la tabla  
**tr** filas de la tabla (row)
```html
<table>
    <tr>
        <th>Tecnología Web</th>
        <th>Función</th>
        <th>Logo</th>
    </tr>
    <tr>
        <td>HTML</td>
        <td>Estructura</td>
        <td><img src="http://www.xaviro.com/assets/img/skills/html.svg" alt="HTML5" /></td>
    </tr>
    <tr>
        <td>CSS</td>
        <td>Estilo</td>
        <td><img src="http://www.xaviro.com/assets/img/skills/css.svg" alt="CSS" /></td>
    </tr>
    <tr>
        <td>JavaScript</td>
        <td>Interactividad</td>
        <td><img src="http://www.xaviro.com/assets/img/skills/js.svg" alt="JavaScript" /></td>
    </tr>
</table>
```

<div id='id8'>

## **Formularios**
Para ingresar información por el usuario

<div id='id8.1'>

* ### **input**
El elemento **input** representa un campo para ingresar datos y editarlos (entrada)
```html
<input type="password" />
<input type="search" />
<input type="phone" placeholder="543-766-2344"/>
<input type="date" />
<input type="color" />
<input type="file" accept="image/*" multiple/>
<input type="checkbox" value="El checkbox está marcado" />
```
<div id='id8.2'>

* ### **textarea**
Su significado es area de Texto, ,uy similar a input pero con ingreso mucho mas grande de información
```html
<textarea cols="20" rows="10" placeholder="Escribe tu texto aqui"></textarea>
```

<div id='id8.3'>

* ### **fieldset**
El elemento(etiqueta) **fieldset** representa un conjunto de controladores de formulario agrupados, opcionalmente con un título **legend** (para colocar el nombre del grupo de **fieldset**)  
Es un tipo de elemento para formularios y hay muchos otros que puedes ver en el estándar y los vas a utilizar en proyectos como **select**, **option** y **progress**.  
El atributo **name** es esencial para agrupar los elementos de radio en una única selección mutuamente exclusiva,  lo que significa que solo se puede seleccionar uno de los elementos de radio en el grupo.

```html
<fieldset>
    <legend>Checkboxes</legend>
    <input id="uno" type="checkbox" value="Uno" name="lista"/>
    <label for="uno">Uno</label>
    <br>
    <input id="dos" type="checkbox" value="Dos" name="lista"/>
    <label for="dos">Dos</label>
    <br>
    <input id="tres" type="checkbox" value="tres" name="lista"/>
    <label for="tres">Tres</label>
    <br>
    <br>

    <input id="uno1" type="radio" value="Uno" name="lista"/>
    <label for="uno1">Uno1</label>
    <br>
    <input id="dos2" type="radio" value="Dos" name="lista"/>
    <label for="dos2">Dos2</label>
    <br>
    <input id="tres3" type="radio" value="tres" name="lista"/>
    <label for="tres3">Tres3</label>
</fieldset>
```

<div id='id8.4'>

* ### **form**
La eriqueta **form** represemta una colección de elementos asociados al formulario, algunos de los cuales pueden representar valores editables que se pueden enviar a un servidor para su procesamiento.  

**form** permite enviar informacion al *backend*, este incluye el atributo **action**, y el (metodo) **method** *post*

```html
<form action="/action.php" method="post">
    <label>
        Email
        <input name="email" type="email" required placeholder="email@mail.com"/>
    </label>
    <button>Iniciar sesión</button>
</form>
<br/>
<br>
<!-- Otro ejemplo de botones de envio y reseteo -->

<form>
    <label for='name'>Nombre:</label>
    <input type='text' id='name' name='name'><br>
    <label for='email'>Correo electrónico:</label>
    <input type='email' id='email' name='email'><br>
    <label for='password'>Contraseña:</label>
    <input type='password' id='password' name='password'><br>
    <input type='submit' value='Enviar'>
    <input type='reset' value='Reiniciar'>
  </form>
```