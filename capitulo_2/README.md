## HTML

Es un lenguaje de marcado de hipertexto, los lenguajes de marcado brindan una serie de recursos que permiten escribir texto ordenado y bien definido. HTML funciona con base en etiquetas, la estructura base de HTML es la siguiente:

~~~html
<html>
<head>
</head>
<body>
</body>
</html>
~~~

La etiqueta **html** envuelve a todo el documento, la etiqueta **head** contiene todos los métadatos y referencias y la etiqueta **body** contiene todo el contenido que se muestra en el navegador.

Las etiquetas principales son:
* h1,h2,h3...(son etiquetas para encabezados, van desde **h1** que representa al título principal hasta **h6** que esta en la posición más baja dentro de la jerarquía de encabezados)

* div es una etiqueta que permite encapsular una porción de etiquetas, esto se hace con la finalidad de tener el texto más ordenado y para darle una mejor semántica al texto

* p la etiqueta p es utilizada para envolver párrafos

Algunas etiquetas necesitan una etiqueta de cierre como la etiqueta de párrafo ```html <p> </p>```, este tipo de etiquetas esperan recibir un contenido dentro del espacio de apertura y de cierre. Existen también etiquetas que no necesitan de una etiqueta de cierre como por ejemplo la etiqueta ```html <br>```` que representa un salto de línea dentro del texto; este tipo de etiqueta no necesitan una etiqueta de cierre porque no esperan recibir un contenido adicional.

Las etiquetas tienen una característica denominada atributos que extienden o enriquecen el comportamiento de las etiquetas, algunos de los atributos más comunes en las etiquetas html son: id, css, style, entre otros. Existen ciertos atributos que funcionan únicamente en determinadas etiquetas como src que es utilizado comunmente en la etiqueta **img** o en la etiqueta **script**.

## CSS
Hojas de estilo en cascada, nos permiten estilizar el texto escrito en HTML brindando así, un sistema que permita que nuestras páginas se vean bien estéticamente. Para enlazar un archivo .css a una página HTMl se debe de utilizar la etiqueta **link** dentro de las etiquetas **head** del documento HTML de la siguiente manera:

~~~html
<head>
	<link rel="stylesheet" href="css/main.css">
</head>

~~~

Dentro del atributo href se ingresa la dirección del archivo .css que queremos enlazar.

Se pueden definir los estilos dentro del documento con la etiqueta **style** pero no es recomendable debido a que a medida que la página vaya creciendo, es muy probable que el manejo de los estilos se vuelva tedioso y costoso.

CSS consiste en selectores que se enlaza a los elementos HTML, existen muchos tipos de selectores dentro de los que podemos destacar:

* de tipo: son selectores que hacen referencia directamente a determinadas etiquetas HTML, cuando se usa este selector se indica que todos los elementos que sean del tipo de etiqueta a la que se esta refiriendo, se le aplique determinados estilos. Ejemplo:

~~~css
	h1 {
		background-color: black;
		color: red;
	}
~~~

* de clase: son selectores que se representan por un punto **.** y serán aplicados a las etiquetas que contengan el atributo class con el nombre de la clase. Ejemplo:

~~~css
.caja {
	margin: 10px;	
	padding: 10px;
}

~~~

~~~html
<div class="caja">
	some content
</div>
~~~

* de id: son selectores que hacen referencia a etiquetas html que tengan el atributo id con el nombre del id de las hojas de estilo, este tipo de selector es de identificador único, eso quiere decir que no se puede aplicar a más de un elemento, se representa con **#**. Ejemplo:

```css
#my_caja {
	background-color: red;
}
```

```html
<div id="caja">
	some content
</div>
```

Los selectores contienen propiedades que son aquellas características que deseamos estilizar en las etiquetas HTML


## Javascript

Es un lenguaje de programación que nos permite dar interactividad a las páginas, este lenguaje manipula el DOM(Document Object Model) que consiste en un árbol jerárquico que represeta todo el contenido de la página web. Mediante la manipulación del DOM, javascript es capaz de poder darle a las páginas el dinamismo y funcionalidad que esperamos de nuestras páginas. Para poder enlazar un archivo .js a nuestra página web debemos hacerlo con la siguiente etiqueta:

~~~html
<script src="js/main.js">
</script>
~~~

Es posible también escribir código javascript dentro de las etiquetas **script**, sin embargo, no se recomienda, pues, es mejor tener el código en archivos separados para tener un mejor orden.