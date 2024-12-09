# Todos los selectores y su especificidad
#front-end #curso-4 #modulo-2 

---
La especificidad es la **clasificación** o **puntuación** que ayuda a CSS a determinar la regla final que se aplicará a un elemento determinado.

Esta lectura le ayudará a comprender cómo el elemento con la especificidad "más alta" es seleccionado por CSS. Pero antes de seguir leyendo, es importante tener en cuenta que estas reglas sólo se aplican en los casos en que surgen conflictos para las propiedades.
## Jerarquía de especificidad
CSS tiene un conjunto de reglas que utiliza para 'puntuar' o asignar un cierto peso a los selectores y esto crea una jerarquía de especificidad. Basándose en los pesos, existen cuatro categorías en esta jerarquía:

- Estilos en línea
- IDs
- Clases, atributos y pseudoclases
- Elementos y pseudoelementos
## Cálculo de puntuaciones
CSS utiliza internamente el modelo jerárquico para calcular la especificidad de los selectores utilizados en una página web. Pero a menudo, a medida que aumenta el tamaño del código CSS, los desarrolladores se enfrentan inevitablemente a conflictos de reglas. En estos casos, ==los desarrolladores utilizan la jerarquía de especificidad para calcular la precedencia de las reglas CSS== y controlar el resultado de sus páginas web.

Veamos un ejemplo práctico de cómo determinar la puntuación de unos selectores.

**#hello {} será 0100**
**div {} será 0001 y**
**div p.foo {} será 0012**

En el orden indicado, a ==las cuatro categorías se les asignarán los valores 1000, 100, 10 y 1, teniendo los selectores de elementos el valor más bajo de 1==. Estas puntuaciones se calcularán respectivamente para cada elemento presente dentro del selector. A continuación, se calculará la puntuación total de estos elementos y el que tenga el valor más alto tendrá la mayor especificidad.

Aunque los pesos asignados a partir de la estructura jerárquica ayudan a un enfoque sistemático, ==hay algunas directrices y reglas más que cobran importancia especialmente en los casos en los que la puntuación de los distintos selectores es la misma==. Algunas de ellas son:

- Cada selector tendrá una puntuación y un lugar en la jerarquía
- En el caso de selectores con igual especificidad, la última o más reciente regla escrita es la que se aplicará
- En general, el selector ID debe aplicarse en los casos en los que necesite estar seguro de una regla
- Los selectores universales tienen un valor de especificidad nulo.