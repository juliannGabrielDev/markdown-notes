# Preprocesadores: sass, scss, Stylus
#front-end #curso-4 #modulo-2 

---
 Los preprocesadores CSS son ==compiladores especiales utilizados para crear un archivo CSS que pueda ser referenciado por un documento HTML==. Generalmente se utilizan para reducir la cantidad de CSS que necesita escribir y le permiten reutilizar valores a través de múltiples reglas. Esto hará que la reutilización de animaciones y efectos sea mucho más fácil. Y debido a que los preprocesadores son una extensión de CSS le ayudarán no sólo en la animación sino en cualquier código CSS. 

Los preprocesadores proporcionan funciones de auditoría sobre las características CSS ya presentes. ==Algunas de las características de los preprocesadores incluyen la opción de crear variables, bucles y sentencias if else==. . Algunos de los preprocesadores más utilizados son **Sass**, **LESS**, **Stylus** y **PostCSS**. El uso de estos preprocesadores requiere la instalación de un compilador sobre su servidor web.

## SASS y SCSS
**scss**
```scss
$font-stack: Arial;
$primary-color: lightblue;

body {
	font: 100% $font-stack;
	color: $primary-color;
}
```

**sass**
```
$font-stack: Arial
$primary-color: lightblue

body
	font: 100% $font-stack
	color: $primary-color
```
```
@mixin some-rules {
	color: lightblue;
	font-size: 25px;
	font-weight: bold;
}

div {
	@include some-rules;
}
```
**Stylus CSS**
```
body
	font 100% Arial
	color lightblue
```
```
add(a, b)
	a + b

div
	margin add(10px, 20px)
```

---
Los preprocesadores también disponen de otras funciones. Y, al igual que cualquier lenguaje de programación, el espacio de los preprocesadores CSS también es competitivo, y de ningún modo son éstas las únicas opciones disponibles.

Una vez que haya adquirido una comprensión de CSS regular, se debe explorar el uso de preprocesadores. El uso de preprocesadores hoy en día es casi ineludible dado el número de funciones avanzadas que proporcionan y que no están disponibles en el CSS convencional.