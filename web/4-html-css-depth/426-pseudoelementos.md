# Pseudoelementos
#front-end #curso-4 #modulo-2 

---
A estas alturas ya sabe que ==los pseudoelementos le ayudan a aplicar estilo a una parte específica de un elemento==. En primer lugar, examinemos la sintaxis de un pseudoelemento.
```css
selector::pseudo-element {
	property: value;
}
```
## `::first-letter`
Puede utilizar `first-letter` para cambiar el color de sólo la primera letra de cada uno de los tres puntos del texto de ejemplo.
```css
li::first-letter {
	color:coral;
	font-size: 1.3em;
	font-weight: bold;
	line-height: 1;
}
```
<ul class="border">
    <li class="fe-426-li">Based in Chicago, Illinois, Little Lemon is a family-owned Mediterranean restaurant, focused on traditional recipes served with a modern twist. </li> 
    <li class="fe-426-li">The chefs draw inspiration from Italian, Greek, and Turkish culture and have a menu of 12–15 items that they rotate seasonally. The restaurant has a rustic and relaxed atmosphere with moderate prices, making it a popular place for a meal any time of the day.</li> 
	<li class="fe-426-li">Little Lemon is owned by two Italian brothers, Mario and Adrian, who moved to the United States to pursue their shared dream of owning a restaurant. To craft the menu, Mario relies on family recipes and his experience as a chef in Italy.</li> 
  </ul> 
  Aunque el código sólo ha cambiado la primera letra de cada punto, supone una gran diferencia en términos de presentación. Ahora vamos a cambiar el tipo de letra de otra manera.
  
---
## `::first-line`
First-line cambiará la primera línea completa de cada una de las viñetas a verde mar claro.
```css
li::first-line {
	color: lightseagreen;
	text-decoration: underline;
	line-height: 1;
}
```
<p class="fe-426-p-fl border">Based in Chicago, Illinois, Little Lemon is a family-owned Mediterranean restaurant, focused on traditional recipes served with a modern twist. The chefs draw inspiration from Italian, Greek, and Turkish culture and have a menu of 12–15 items that they rotate seasonally. The restaurant has a rustic and relaxed atmosphere with moderate prices, making it a popular place for a meal any time of the day.</p> 

---
## `::selection`
La selección es otro pseudoelemento útil. Por ejemplo, puede utilizarlo cuando esté tomando notas en su dispositivo porque le permite resaltar un texto específico. Su efecto se hace evidente sólo después de que el usuario seleccione el contenido. En las páginas web actuales, normalmente verá colores invertidos de blanco-negro a negro-blanco al seleccionar una porción de texto.
```css
li::selection {
	color:brown;
	background-color: antiquewhite;
	line-height: 1;
}
```
<p class="fe-426-p-s border">Based in Chicago, Illinois, Little Lemon is a family-owned Mediterranean restaurant, focused on traditional recipes served with a modern twist. The chefs draw inspiration from Italian, Greek, and Turkish culture and have a menu of 12–15 items that they rotate seasonally. The restaurant has a rustic and relaxed atmosphere with moderate prices, making it a popular place for a meal any time of the day.</p> 

---
## `::marker`
Los marcadores se suelen utilizar para añadir elementos de estilo a una lista, por ejemplo, para colorear las viñetas. Por ejemplo, puede mejorar la experiencia del usuario si utiliza un marcador de la siguiente manera.
```css
li::marker {
	color: cornflowerblue;
	content: '<> ';
	font-size: 1.1em;
}
```
<ul class="border">
    <li class="fe-426-li-mk">Based in Chicago, Illinois, Little Lemon is a family-owned Mediterranean restaurant, focused on traditional recipes served with a modern twist. </li> 
    <li class="fe-426-li-mk">The chefs draw inspiration from Italian, Greek, and Turkish culture and have a menu of 12–15 items that they rotate seasonally. The restaurant has a rustic and relaxed atmosphere with moderate prices, making it a popular place for a meal any time of the day.</li> 
	<li class="fe-426-li-mk">Little Lemon is owned by two Italian brothers, Mario and Adrian, who moved to the United States to pursue their shared dream of owning a restaurant. To craft the menu, Mario relies on family recipes and his experience as a chef in Italy.</li> 
  </ul> 

---
## `::before` y `::after`
Otro par de pseudoelementos son los pseudoelementos `::before` y `::after`. Permiten añadir contenido antes y después de un elemento en el que están permitidos. ==En otras palabras, se puede añadir nuevo contenido a una página sin añadir código HTML para ello==. También puede añadir opciones de estilo para este contenido. Hagamos un ejemplo en el que se añade texto antes y después de unas pautas de cocina para identificarlas como consejos importantes.
```html
<body>
	<p id="tips"> Don't rinse your pasta after it is drained. </p>
	<p> Slice the tomatoes. Take the extra efforts to seed them. </p>
	<p id="tips"> Peel and seed large tomatoes. </p>
</body>
```

```css
#tips::before{
	background: darkkhaki;
	color:darkslategray;
	content: "Tip:";
	padding-left: 3px;
	padding-right: 5px;
	border-radius: 10%;
}

#tips::after{
	background:darkkhaki;
	color:darkslategray;
	content: "!!";
	padding-right: 5px;
	border-radius: 20%;
}
```
<div class="border">
	<p id="fe-426-tips"> Don't rinse your pasta after it is drained. </p>
	<p> Slice the tomatoes. Take the extra efforts to seed them. </p>
	<p id="fe-426-tips"> Peel and seed large tomatoes. </p>
</div>

Los ejemplos aquí expuestos ilustran que la adición de un código sencillo para los pseudoelementos puede mejorar enormemente el aspecto de las páginas web. Existen muchos otros pseudoelementos y algunos son más populares que otros. Puede seguir su propio estilo y explorar las posibilidades creativas que ofrecen las pseudoclases y los pseudoelementos.