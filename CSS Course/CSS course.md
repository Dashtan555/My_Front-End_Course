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

1. ## **Primeros Pasos**
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

2. ## **Fundamentos**
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

        </style>
    </head>
    <body>
        <p>Texto <span>1</span></p>
        <p class="claseTexto">Texto <span>2</span></p>
        <p class="claseTexto">Texto <span>3</span></p>
        <p id="textoUnico">Texto <span>4</span></p>
    </body>
</html>
```