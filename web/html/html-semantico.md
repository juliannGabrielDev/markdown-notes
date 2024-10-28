# Hoja de trucos de HTML semántico
#html #teoria 

---

Existen cientos de etiquetas semánticas que le ayudarán a describir el significado de sus documentos HTML. A continuación encontrará una hoja de trucos con algunas de las más comunes que utilizará en este curso y en su carrera como desarrollador.

## Etiquetas de seccionado

Utilice las siguientes etiquetas para organizar su documento HTML en secciones estructuradas. 

**`<header>`**
La cabecera de una sección de contenido o de la página web. La cabecera de la página web suele contener la marca o el logotipo del sitio web

**`<nav>`**
Los enlaces de navegación de una sección o de la página web

**`<footer>`**
El pie de página de una sección de contenido o de la página web. En una página web, a menudo contiene enlaces secundarios, el aviso de copyright, la política de privacidad y los enlaces de la política de cookies

**`<main>`**
Especifica el contenido principal de una sección o de la página web

**`<aside>`**
Conjunto de contenidos secundarios que no son necesarios para comprender el contenido principal

**`<article>`**
Un bloque de contenido independiente y autónomo, como una entrada de blog o un producto

**`<section>`**
Una sección independiente del documento que suele utilizarse dentro de los elementos cuerpo y artículo

**`<details>`**
Una sección colapsada de contenido que puede ampliarse si el usuario desea verla

**`<summary>`**
Especifica el resumen o pie de foto de un elemento `<details>`

**`<h1><h2><h3><h4><h5><h6>`**
Encabezamientos de la página web. `<h1>` indica el encabezamiento más importante mientras que `<h6>` indica el menos importante.

---

## Etiquetas de contenido

**`<blockquote>`**
Se utilizan para describir una cita

**`<dd>`**
Se utiliza para definir una descripción para el elemento `<dt>` precedente

**`<dl`**
Se utiliza para definir una lista de descripción

**`<dt>`**
Se utiliza para describir términos dentro de los elementos `<dl>`

**`<figcaption>`**
Define un pie de foto para una imagen fotográfica

**`<figure>`**
Aplica marcas a una imagen fotográfica

**`<hr>`**
Añade una línea horizontal al elemento padre

**`<li>`**
Se utiliza para definir un elemento dentro de una lista

**`<menu>`**
Una alternativa semántica a la etiqueta 

**`<ul><ol>`**
Define una lista ordenada

**`<p>`**
Define un párrafo

**`<pre>`**
Se utiliza para representar texto pre-formateado. Normalmente se representa en el navegador web utilizando una fuente mono-espaciada

**`<ul>`**
Lista desordenada

**`<blockquote>`**
Se utilizan para describir una cita

**`<dd>`**
Se utiliza para definir una descripción para el elemento `<dt>` precedente

**`<dl>`**
Se utiliza para definir una lista de descripción

**`<dt>`**
Se utiliza para describir términos dentro de los elementos `<dl>`

**`<figcaption>`**
Define un pie de foto para una imagen fotográfica

**`<figure>`**
Aplica marcas a una imagen fotográfica

**`<hr>`**
Añade una línea horizontal al elemento padre

**`<li>`**
Se utiliza para definir un elemento dentro de una lista

**`<menu>`**
Una alternativa semántica a la etiqueta `<ul>`

**`<ol>`**
Define una lista ordenada

**`<p>`**
Define un párrafo

**`<pre>`**
Se utiliza para representar texto preformateado. Normalmente se representa en el navegador web utilizando una fuente monoespaciada

**`<ul>`**
Lista desordenada.

---

## Etiquetas en línea

**`<a>`**
Un enlace de anclaje a otro documento HTML

**`<abbr>`**
Especifica que el texto que contiene es una abreviatura o acrónimo

**`<b>`**
Pone en negrita el texto que contiene. Cuando se utilice para indicar importancia, utilice en su lugar `<strong>`

**`<br>`**
Un salto de línea. Mueve el texto subsiguiente a una nueva línea

**`<cite>`**
Define el título de una obra creativa (por ejemplo, un libro, un poema, una canción, una película, una pintura o una escultura). El texto del elemento `<cite>` suele aparecer en cursiva

**`<code>`**
Indica que el texto que contiene es un bloque de código informático

**`<data>`**
Indica datos legibles por máquina

**`<em>`**
Enfatiza el texto que contiene

**`<i>`**
El texto que contiene aparece en cursiva. Se utiliza para indicar texto idiomático o términos técnicos

**`<mark>`**
El texto que contiene debe marcarse o resaltarse

**`<q>`**
El texto que contiene es una cita corta

**`<s>`**
Muestra el texto que contiene con un tachado o una línea que lo atraviesa

**`<samp>`**
El texto que contiene representa una muestra

**`<small>`**
Se utiliza para representar texto de pequeño tamaño, como los derechos de autor y el texto legal

**`<span>`**
Un elemento genérico para agrupar contenido para el estilo CSS

**`<strong>`**
Muestra el texto que contiene en negrita. Se utiliza para indicar importancia

**`<sub>`**
El texto que contiene es texto subíndice, que se muestra con una línea de base rebajada

**`<sup>`**
El texto que contiene es texto en superíndice, mostrado con una línea de base elevada

**`<time>`**
Una etiqueta semántica utilizada para mostrar tanto fechas como horas

**`<u>`**
Muestra el texto que contiene con un subrayado sólido

**`<var>`**
El texto contenedor es una variable en una expresión matemática.

---

## Contenido incrustado y etiquetas multimedia

**`<audio>`**
Se utiliza para incrustar audio en las páginas web

**`<canvas>`**
Se utilizan para representar gráficos 2D y 3D en las páginas web

**`<embed>`**
Se utiliza como elemento contenedor de contenidos externos proporcionados por una aplicación externa, como un reproductor multimedia o una aplicación plug-in. 

**`<iframe>`**
Se utiliza para incrustar una página web anidada. 

**`<img>`**
Incrusta una imagen en una página web

**`<object>`**
Similar a `<embed>` pero el contenido lo proporciona un complemento del navegador web

**`<picture>`**
Elemento que contiene un elemento <img> y uno o más elementos <source> para ofrecer imágenes alternativas para diferentes pantallas/dispositivos

**`<video>`**
Incrusta un vídeo en una página web

**`<source>`**
Especifica recursos multimedia para los elementos `<picture>`, `<audio> y<video>`

`<svg>`
Se utiliza para definir gráficos vectoriales escalables dentro de una página web.

---

## Etiquetas de tabla

**`<table>`**
Define un elemento de tabla para mostrar datos de tabla dentro de una página web

**`<thead>`**
Representa el contenido de cabecera de una tabla. Normalmente contiene un elemento `<tr>`

**`<tbody>`**
Representa el contenido principal de una tabla. Contiene uno o más elementos `<tr>`

**`<tfoot>`**
Representa el contenido del pie de página de una tabla. Normalmente contiene un elemento `<tr>`

**`<tr>`**
Representa una fila de una tabla. Contiene uno o más elementos `<td>` cuando se utiliza dentro de `<tbody>` o `<tfoot>`. Cuando se utiliza dentro de `<thead>`, contiene uno o más elementos `<th>`

**`<td>`**
Representa una celda en una tabla. Contiene el contenido de texto de la celda

**`<th>`**
Define una celda de encabezado de una tabla. Contiene el contenido de texto de la cabecera

**`<caption>`**
Define el título de un elemento de tabla

**`<colgroup>`**
Define un grupo semántico de una o varias columnas de una tabla para su formateo

**`<col>`**
Define una columna semántica en una tabla.