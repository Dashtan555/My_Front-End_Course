<!-- Mis apuntes de Programación -->
# **HTML**

**Índice**
1. [Primeros pasos](#id1)
2. [Texto](#id2)
3. [Navegación](#id3)
4. [Imágenes](#id4)
5. [Multimedia](#id5)
    * [iFrame](#id5.1)
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

el primer documento de una pagina html debe ser **index.html**

### Hola mundo
```html
<p>Hello Word..!</p>
```

### Partes de Html

1. Simbolos que se abren y se cierran, estas se denominan etiquetas: 
* p = párrafo  
* a = vínculo
2. Atributos, le da a las etiquetas caracteristicas especiales (title)
3. Texto entre las etiquetas (Párrafo)
4. Cometarios <!-- -->

```html
<!-- Este es un comentario -->
<p title="Nota">Párrafo</p>
```
5. Entidades de caracteres:  
* &copy;  
* &cap;  
* &coprod;

Una pagina web tiene una estructura de una arbol.

<div id='id2'>

## **Texto**

<div id='id3'>

## **Neavegación**

<div id='id4'> 

## **Imágenes**

<div id='id5'>

## **Multimetimedia**

<div id='id5.1'>

* ### **iFrame**
Permite poner contenido de otros sitios web en mi página
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
1. < div>  se utilza par agrupar etiquetas
2. < span> se utilza para un grupo mas pequeño de una o más palabras junto con atributos
3. < p>    se uza como un contenedor de un grupo de texto

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
    * *id* Identificación unica / para identificar una etiqueta, identificar parrafo, mas usado con CSS, solo para una etiqueta sola
    * *class* Parecido al anterior pero sirve para identificar algun grupo, se puede rusar.
    * *contenteditable* Puedes editar este contenido
    * *lang* Indica el lenguaje del contenigo es-Españo, en-English, es-MX español de Mexico, ayuda a Google a encontrar la página
    * *dir* Indica la dirección "rtl" right to left de izaquierda a derecha, para escritos en arabe por ejemplo.

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