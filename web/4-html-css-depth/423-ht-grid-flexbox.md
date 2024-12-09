# Hoja de trucos: Grid y Flexbox
#front-end #curso-4 #modulo-2 

---
# Cuadrícula

La sintaxis para crear una cuadrícula:
```css
selector{
	display: grid; /* or inline-grid */
}
```
La abreviatura de rejilla consiste en las siguientes propiedades con valores por defecto:

`grid`
Una rejilla le permitirá organizar los distintos elementos de su página.

---
`grid-template-rows: none`
Esta característica le permite configurar sus elementos para que se organicen de forma similar a las filas de una tabla.

---
`grid-template-columns: none`
Esta característica le permite configurar sus elementos pero con esta configuración los elementos se organizan como columnas en una tabla.

---
`grid-template-areas: none`
Esta característica le permite configurar los nombres de una cuadrícula y cómo se sitúan unos en relación con otros.

---
`grid-auto-rows: auto`
Ajuste por defecto para todos los tamaños de fila que no se hayan configurado explícitamente.

---
`grid-auto-columns: auto`
Configuración por defecto para todos los tamaños de columna que no se hayan configurado explícitamente.

---
`grid-auto-flow: row`
Ubicación por defecto para las filas que no se hayan asignado explícitamente.

---
`column-gap: normal`
Esto establece el espacio entre las columnas

---
`row-gap: normal`
Establece el espacio entre las filas

---
## Propiedades de la rejilla para el contenedor

`grid-template-columns: measurement units | % units |repeat()`
Define los nombres de las filas y mantiene constante el tamaño de los elementos de las columnas. Puede aceptar un rango de tamaños de medidas diferentes.

---
`grid-template-rows: measurement units | % units |repeat()`
Define los nombres de las líneas, y mantiene un tamaño constante de las filas. Puede aceptar un rango de tamaños de medida diferentes.

---
`grid-auto-columns: measurement unit (fixed value for all columns)`
Determina el tamaño por defecto para las columnas que no se han configurado explícitamente.

---
`grid-auto-rows: measurement unit (fixed value for all rows)`
Determina el tamaño por defecto para las filas que no se han configurado explícitamente.

---
`grid-template: “header header” auto`
Permite definir y mantener celdas con nombre en una cuadrícula.

`“main right” 75vh`

Esto define dos celdas denominadas `main` y `right`, que tienen un tamaño del 75% de la altura de la ventana gráfica.

`“footer footer” 20rem`

Esto define dos celdas denominadas footer y footer, que tienen un tamaño de 20 raíz em (rem). Esto define el tamaño en relación con el tamaño de la fuente html.

---
### Espacio

`grid-gap: measurement units`
Determina el espacio entre filas y columnas.

`grid-column-gap: measurement units`
Determina el espacio entre columnas.

`grid-row-gap: m-unit-1 m-unit-2`
Determina el espacio entre columnas.

---
### Alineación

`justify-items: start | center | end | stretch`
Define el espacio por defecto que se asigna a cada elemento de la cuadrícula.

`align-items: start | center | end | stretch`
Define el espacio por defecto relacionado con un elemento a lo largo del eje de bloques de la cuadrícula.

`place-items: start | stretch /* shorthand for two properties above */`
Esta función le permite alinear los elementos con las direcciones de bloque y en línea.

---
### Justificación

`justify-content: start | center | end | stretch | space-between | space-evenly | space-around`
Define la asignación de espacio del navegador a los elementos de contenido en relación con el eje principal.

`align-content: start | center | end | stretch | space-between | space-evenly | space-around`
Define la asignación de espacio del navegador a los elementos de contenido en relación con el eje transversal y el eje de bloque.

`place-content: center | start`
Esta función le permite alinear los elementos con las direcciones de bloque y en línea.

---
### Posicionamiento

`grid-auto-flow: row | column | dense`
Esto se refiere a cómo se colocan automáticamente los elementos dentro de la cuadrícula.

`grid-auto-columns: measurement units`
Se refiere al tamaño de las columnas creadas sin especificaciones de tamaño concretas.

`grid-auto-rows: measurement units`
Se refiere al tamaño de las filas creadas sin especificaciones concretas.

---
## Propiedades de la rejilla para los elementos (hijo)

`grid-column: column position /* E.g. 1/2 */`
Permite especificar en qué parte de la rejilla debe comenzar la columna.

`grid-column-start: column start position.`
Esta propiedad determina la posición inicial de la columna en la que se coloca un elemento en la rejilla.

`grid-column-end: column end position`
Esta propiedad determina la posición final de la columna en la que se coloca un elemento en una cuadrícula.

`grid-row: row position /* E.g. 1/2 */`
Permite especificar en qué parte de la cuadrícula debe comenzar la fila.

`grid-row-start: row start position`
Esta propiedad determina la posición de inicio de fila en la que se coloca un elemento en una rejilla.

`grid-row-end: row end position`
Esta propiedad determina la posición de fin de fila en la que se coloca un elemento en una rejilla.

---
## Justificación y alineación

`justify-self: start | center | end | stretch`
Determina cómo se coloca un elemento dentro de su contenedor alineado en relación con el eje correspondiente.

`align-self: start | center | end | stretch`
Alinea un elemento dentro de un área de la rejilla.

`place-self: start | stretch /* shorthand for two properties above */`
Este ajuste permite alinear y justificar un elemento dentro de un bloque.

---
# Flexbox

La sintaxis para crear un flexbox:
```css
selector{
	display: flex | inline-flex
}
```
La visualización se refiere a cómo desea que se muestre el selector. Establecer `display: flex;` hace que el selector dado sea una caja flex. Establecer `display: inline-flex;` hace que el selector sea un contenedor flexbox mientras que estará en línea.
## Propiedades del contenedor flexbox

`flex-direction: row | row-reverse | column | column-reverse`
Es posible especificar la dirección que seguirán sus elementos. Tradicionalmente el texto va de izquierda a derecha que es la configuración por defecto de flex sin embargo se puede establecer de derecha a izquierda o incluso de arriba a abajo. Las cuatro direcciones de flex son

- `row`: organizado de izquierda a derecha
- `row-reverse`: organizado de derecha a izquierda
- `column`: organizada de arriba a abajo
- `column-reverse`: organizada de abajo a arriba.

---
`flex-wrap: wrap | nowrap`
La disposición estándar consiste en trazar los elementos de izquierda a derecha en línea recta. La función de ajuste le permite personalizarlo para que se ajuste al tamaño de la ventana que muestra la página.

- `wrap`: Envuelve automáticamente los elementos medida que se reduce el espacio de la ventana.
- `nowrap`: Ajuste por defecto, los elementos permanecen rígidos y no responden a los ajustes realizados en el tamaño de la ventana.

---
`align-items: flex-start | flex-end | center | stretch`

Determina cómo deben colocarse los elementos flexibles en la página. Los elementos pueden alinearse de varias maneras:

- `flex-start`: Similar a la escritura estándar, los elementos comienzan en la esquina superior izquierda y se posicionan de izquierda a derecha.
- `flex-end`: La posición comienza en la esquina inferior derecha.
- `center`: El elemento se posiciona desde el centro.
- `stretch`: el elemento se expande hasta llenar el contenedor.

---
`justify-content: flex-start | flex-end | center | space-between | space-evenly`
Determina la alineación de los elementos flex.

- `flex-start`: va de derecha a izquierda a lo largo del eje principal.
- `flex-end`: va de izquierda a derecha a lo largo del eje principal.
- `center`: Empezando en el centro, la alineación se expande a partir de ahí.
- `space-between`: el primer y el último elemento están a ras de la pared izquierda y derecha respectivamente, todos los demás elementos están espaciados uniformemente.
- `space-evenly`: cada elemento es equidistante entre sí y de la pared límite.

---
## Propiedades de los elementos flexbox (hijo)

`flex-grow: factor of flex’s main size`
Este atributo permite que el contenedor flex crezca proporcionalmente a los demás contenedores presentes.

`flex-shrink: factor of flex’s main size`
Esto permite que los elementos se encojan en relación con los elementos que los rodean.

`flex-basis: auto | factor of main’s size | measurement unit`
Establece el tamaño principal inicial de un elemento. Puede anularse si se configuran otros elementos estilizados.

`order:position in flex /* Set ascending by default */`
El posicionamiento estándar de los elementos es por orden de origen, sin embargo esta función le permitirá configurar dónde aparecen los elementos en la página.

`align-self: start | center | end | stretch`
Esto determina en qué parte de la página se posicionarán los elementos hijos. De forma similar a los atributos flex principales, el inicio está a la izquierda y el final a la derecha.