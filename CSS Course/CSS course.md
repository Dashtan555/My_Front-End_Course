# CSS

**Índice**
1. [Primeros pasos](#id1)
    * [Partes de CSS](#id1.1)
    * [Usos](#id1.2)
    * [Resets](#id1.3)
2. [Fundamentos](#id2)
    * [Sintaxis](#id2.1)
    * [Selectores](#id2.2)
    * [Cascada](#id2.3)
    * [Especificidad](#id2.4)
    * [Unidades](#id2.5)
3. [Texto](#id3)
    * [Fuentes](#id3.1)
4. [Modelo de Caja](#id4)
    * [Caja](#id4.1)
    * [Margen y Relleno](#id4.2)
    * [Borde](#id4.3)
    * [Contorno](#id4.4)
5. [Estilos](#id5)
    * [Fondo](#id5.1)
    * [Color](#id5.2)
6. [Layouts](#id6)
    * [Layouts](#id6.1)
    * [Prefijos](#id6.2)
    * [Posiciones](#id6.3)
    * [Floats](#id6.4)
    * [Flexbox](#id6.4)
    * [Grid](#id6.4)
7. [Dise;o Receptivo](#id7)
    * [Media Query](#id7.1)
    * [Móvil primero](#id7.2)
8. [Complementos](#id8)
    * [Transiciones](#id8.1)
    * [Transformaciones](#id8.2)
    * [Animaciones](#id8.3)
    * [Centrar](#id8.4)

___
<div id='id1'>

## **1. Primeros Pasos**
CSS sirve para dar estilo a nuestras páginas web.

<div id='id1.1'>

* ### **Partes de CSS**
Comienza con la etiqueta `<style> </style>`
* **p:** Esto es el selector.
* **color: red;**: Esto se llama declaración.
* **color:** Esto se denomina propiedad.
* **red**: Esto es el valor 
```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            p {
                color: red;
            }
        </style>
        <body>
            <p>Hola Mundo</p>
        </body>
    </head>
</html>
```
<div id='id1.2'>

* ### **Usos**
Normalmente los archivos de estilo de css se llaman **styles.css** puede hacer de tres maneras:
* Por archivo externo.
* A traves de la etiqueta `<style> </style>`
* Colocarlo en línea con la etiqueta que se quiera estilizar.
```html
<!DOCTYPE html>
<html>
    <head>
        <!-- Estilo mediante archivo -->
        <link rel="stylesheet" href="./Usos/styles.css"/>
        <!-- Estilo interno el de abajo -->
        <style>  
            p{
                font-weight: 900;
            }
        </style>
        <body>
            <!-- Estilo en línea -->
            <p style="font-size: 25px;">Hola Mundo</p>
        </body>
    </head>
</html>
```

```html
<!-- Ejemplo de cambiar de color ante una accion a un link -->
<!DOCTYPE html>
<html>
    <link rel="stylesheet" href="./styles.css"/>
    <a href="www.google.com">Ir a google</a>

    <p Style="color: royalblue;"> Me encantó </p>
</html>
```

<div id='id1.3'>

* ### **Resets**
Nos permite resetear el fomato inicial de las páginas web, ya que en cada explorador se muestra de una manera diferente, ya que cada explorador tiene un formato diferente para mostrar las páginas web.

Se puede usar como ejemplo esto para estandarizar nuestros diseños en nuestros proyectos cdnjs: https://cdnjs.cloudflare.com/ajax/libs/meyer-reset/2.0/reset.min.css

```html
<!DOCTYPE html>
<html>
    <head>
        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/meyer-reset/2.0/reset.min.css">
    </head>
    <body>
        <fieldset>
            <legend>Radio Buttons</legend>
            <input id="uno" type="radio" value="Uno"/>
            <label for="uno">Uno</label>
            <input id="dos" type="radio" value="Dos"/>
            <label for="dos">Dos</label>
            <input id="tres" type="radio" value="Tres"/>
            <label for="tres">Tres</label>
        </fieldset>
    </body>
</html>
```
**Reto:** Crea un reset de CSS que establezca el margen y el relleno de todos los elementos en cero, y elimine la lista de viñetas predeterminada en los elementos de lista.
El `*` es un selector universal que permite seleccionar todos lo elementos de una página web.

```CSS
/* Solución */
*{
  margin: 0;
  padding: 0;
}
ul{
  list-style: none;
}
```
<div id='id2'>

## **2. Fundamentos**
A continuación se nuestra como se debe presentar la información en archivos **CSS**.  
<img src="./CSS_REFERENCE.jpg" height="300">

<div id='id2.1'>

* ### **Sintaxis**
Aquí se denota como se puede usar el estilo en **CSS**, los comentarios estan formados por: `/*Comentarios*/`, en css es recomendable escribir para abajo dejando ver todos las declaraciones, y como se muestra en el ejemplo se puede añadir una clase para que sea un direccionador.

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8" />
        <style>
            /* comentarios */
            p.primero{
                color: red;
                font-size: 25px;
            }
            h1{
                color: blue;
            }
        </style>
    </head>
    <body>
        <h1>Título</h1>
        <p class="primero">Párrafo</p>
    </body>
</html>
```
<div id='id2.2'>

* ### **Selectores**
Selectores, son como `p` que indica a que etiqueta se va a aplicar el estilo o como el ejemplo de: `p.primero{}`, mostrado en el ejemplo anterior.
Se puede aplicar varios selectores como:
* **`p`**: selecciona la etiqueta de `p` = párrafo, existen más como: `h1`, `h2`, `q` entre ottros.
* **`.claseTexto`** Selecciona todas las etiquetas indicadoras del la `class="claseTexto"` seleccionada.
* **`#textoUnico`** Selecciona a una sola etiqueta identificada con el `id=textoUnico`, id se puede usar solo una vez que indica a un solo elemento.
* **`.claseTexto span`** Selecciona la etiqueta `span` dentro de las etiquetas que tengas la `class=claseTexto`
* **`p, span`** Selecciona todo los párrafos y span que se encuentren, llamado selector de grupo.
* **`div > h2`**: Selecciona la etiqueta `h2` que es la hija de una etiqueta `div`.
* **`button:hover`**: Selecciona el botón cuando el cursor está sobre el botón.
* **`div::after`**: Selecciona una etiqueta 'ficticia' que se crea después de elemento `div`
* **`p[title]`**: Selecciona a todas las etiquetas `p` que tienen el atributo title.

Hay que tener en cuenta que los cambios se van leyendo de arriba a abajo siendo el ultimo cambio el que se muestra.


```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            p{
                color: blue;
                font-size: 25px;
            }
            .claseTexto{
                color: red;
                font-size: 25px;
            }
            #textoUnico{
                color: green;
                font-size: 25px;
            }
            .claseTexto span{
                color: purple;
                font-size: 25px;
            }
            p, span{
                text-decoration: underline;                
            }
            div > h2{
                color:red;
                font-size: 50px;
            }
            div > p{
                color: blue;
                text-decoration: none;
            }
            div > button{
                color: green;
            }

        </style>
    </head>
    <body>
        <p>Texto <span>1</span></p>
        <p class="claseTexto">Texto <span>2</span></p>
        <p class="claseTexto">Texto <span>3</span></p>
        <p id="textoUnico">Texto <span>4</span></p>
        <div>
            <h2>Selectores</h2>
            <p>Esta es una prueba de selectores.</p>
            <button>
                Prueba realizada.
            </button>
        </div>
    </body>
</html>
```

<div id='id2.3'>

* ### **Cascada** ### 
En los archivos de las páginas web, se aplica los estilos en cascada, en el navegador primero se abre el archivo html, luego se aplican los estilos del archivo CSS en cascada, por lo cual se aplica al final el ultimo estilo definido, a continuación se presenta un ejemplo:

```html
<!DOCTYPE html>
<html>
    <head>
        <link rel="stylesheet" href="./styles.css">
        <style>
            p{
                color: red;
            }
        </style>

    </head>
    <body>
        <p style="color: green">Estos son ejemplos de la aplicación del diseño en cascada.</p>
    </body>
</html>
```
Los estilos aplicados a las etiquetas padres, se pasan directamente a las clases hijo.  

**Resultado:**

<img src="./Pruebas de Codigo/Fundamentos/Cascada/cascada.png"/>

<div id='id2.4'>

* ### **Especificidad**
Esta sirve en una forma distinta de cascada, ya que da importancia en un sentido contrario al de cascada, dando mayor importancia a la especificidad con la que se apunte a los diferentes elementos.
Señalando de la siguientes manera:
* **`.`**: Para las `class`
* **`#`**: Para los `id`
* **`p.textos#textos1`**: Para un `id` en una `class` de una etiqueta `p`

```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            p.textos#texto1{
                color: blue !important;
            }
            p.textos#texto1{
                color: green;
            }
            #texto1 {
                color: yellow;
            }
            .textos{
                color: orange;
            }
            p{
                color: red;
            }
            body{
                color: purple;
                font-size: 25px;
            }
        </style>
    </head>
    <body>
        <p id="texto1" class="textos">Texto de prueba</p>
    </body>
</html>
```

<img src="./Pruebas de Codigo/Fundamentos/Especificidad/especificidad.png" height="120">

<div id='id2.5'>

* ### **Unidades**
Las unidades ayudan a dar formato en las páginas web, el fin es hacer las páginas mas resposivas y adaptivas, teniendo en cuenta la cantidad enorme que existen en el mercado.

|Unidades       | Tipo            |Pantalla  |
|---------------|---------------- |   -------|
|pixeles        | Unidad absoluta |Se asegura que deve ocupar los pixeles destinados para esa pantalla.        |
|porcentaje     | Valor relativo|Este es un valor relativo al padre, en el caso del ejemplo al `<body>`, si el padre cambia, de igual manera el hijo.  |
|3em            | Unidad relativa       | Es una unidad relativa al font-size del padre, y es utilizado para 'Fuentes'   |
|3rem           | Unidad relativa        | Esta es una unidad relativa a la raíz, lo que determina el navegador. Raíz = `<html>`   |

```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            html{
                font-size: 10px;
            }
            body{
                margin: 0;
                font-size: 50%;
                width: 100%;
            }
            h1{
                background: greenyellow;
                /* px Absioluta */
                width: 300px;
                /* relativa al tamaño del padre */
                width: 6%;
                /* em Relativa a font-size del padre */
                font-size: 3em;
                /* rem Relativa a font-size de la raíz */
                font-size: 3rem;
            }
        </style>
    </head>
    <body>
        <h1>Unidades</h1>
    </body>
</html>
```

**Resultado:**  
<img src='./Pruebas de Codigo/Fundamentos/Unidades/Unidades.png'>

<div id='id3'>

## **3. Texto**
Las fuentes para el texto se usan mucho para dar un estilo, identidad a una página web. existen varios recurso pero uno que se puede usar es:

[**Google fonts**](https://fonts.google.com/ "Fuentes de Google")


<div id='id3.1'>

 * ### **Fuentes**
  En todo documento existe texto, este texto va a tener un tipo de letra o diseño a este tipo de letra o diseño se le llama fuente o font, cual sirve para dar diferentes sensaciones en tú página web.

 **`font-family`** Aquí se presenta la familia de fuentes, en la cual la primera opción es un tipo de letra única o muy especifica, sino encuentra el navegador, da paso a la siguiente y al final busca una familia de fuentes.

* serif. Con detalles en las letras
* sans-serif. simples
* monospace: un mismo espacio entre letras
* cursive: cursiva
* fantasy: algo epico y fantasioso.

**`font-weight`** Esta se refiere al ancho de las letras, se puede usar desde `100` o `900`siendo 900 el ancho maximo o se puede usar palabras claves como: `bold`, `lighter`, `normal`, y otros.  

Para ver cambios uno se debe asegurar que la familia de fuentes tiene los diferentes grosores, sino no se va a aplicar ningun cambio.  

**`font-style`** En esta existen diferentes propiedades como: `normal`, `oblique`, `italic`.

Se debe tener en cuenta que las fuentes son archivos que incluyen todas las imagnes de cada uno de los caracteres, si no existe alguna propiedad no se aplica cambios.

**`font-size`** Esta propiedad permite el cambio del tamaño de la fuente.

```html
<!DOCTYPE html>
<html>
    <head>
        <!-- <link rel="preconnect" href="https://fonts.googleapis.com">
        <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
        <link href="https://fonts.googleapis.com/css2?family=Ubuntu+Mono&display=swap" rel="stylesheet"> -->
        <style>
            @import url('https://fonts.googleapis.com/css2?family=Ubuntu+Mono&display=swap');
            p{
                font-family: 'Ubuntu Mono', monospace;
                font-weight: lighter;
                font-style: oblique;
                font-size: 25px;

            }

        </style>
    </head>
    <body>
        <p>
            Este es un texto de prueba: Mientras los actores siguen en huelga, uno de los problemas es la posibilidad de que los estudios acaben con sus trabajos de actuación gracias a la inteligencia artificial. CNN conversó con la empresa MARZ, especializada en efectos visuales a través de inteligencia
        </p>
    </body>
</html>
```

**Resultado:**
<img src='./Pruebas de Codigo/Fuentes/Fuentes.png'>

<div id='id4'>

 ## **4. Modelo de Caja (Box Model)**

 
Cada elemento de html puede ser en forma de bloque o de linea, son como pequeñas cajas que guardan información dentro.

* `<div>`: elemnto de bloque.
* `<span>`: elemento de línea.

<div id='id4.1'>

* ### **Caja**
A continuación se muestra una imagen que simboliza a las cajas que representan cada elemento de **HTML**.

<img src='./Pruebas de Codigo/Box Model/Caja/imagen referencia caja.jpg'>

Para dar formato a cada uno de estos elementos existen diferentes propiedades como:

* `background-color`: Para dar color a la caja.
* `padding`: Que da un espacio que se da entre el contenido y la caja.
* `border`: Borde la caja se puede añadir más propiedades como, que puede ser `solid` o `dasehd` y hasta color del borde.
* `margin`: Espacio al rededor de la caja.
* `width`: Puede tener un ancho usado con esta propiedad
* `height`: Puede cambiarse el alto
* `box-sizing`: `content-box`, signifíca que la caja va a tener el tamaño del contenido, o `border-box` esta propiedad considera al borde y al padding.

Los elementos de línea o de bloque actuan diferente, sin embargo podemos hacer que actue como un elemento de bloque o de línea.
* `display`: Aquí podemos cambiar el comportamiento de los elementos como: `block`; bloque, `line`; línea, `inline-block`; es una propiedad intermedia.
Todo esto se debe tener encuenta al usar altura y ancho dependiendo de los diferentes objetivos del proyecto.


```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            body{
                margin: 0;
            }
            div{
                background-color: red;
                padding: 10px;
                border: 10px solid blue;
                margin: 20px;
                width: 100px;
                height: 100px;
                box-sizing: content-box;
            }

        </style>
    </head>
    <body>
        <div>Box Model</div>
    </body>
</html>
```
**Resultado:**  
<img src='./Pruebas de Codigo/Box Model/Caja/Box.png' height='200'>
