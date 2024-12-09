# Hoja de trucos: CSS pseudo
#front-end #curso-4 #modulo-2 

---
## Selectores de atributos

| **Selector**       | **Sintaxis**        | **Ejemplo**                                                                                    |
| ------------------ | ------------------- | ---------------------------------------------------------------------------------------------- |
| [atributo]         | [href] {}           | Selecciona todos los elementos con un atributo href                                            |
| [atributo=valor]   | [lang="fr"] {}      | Selecciona todos los elementos con un atributo lang que tenga el valor "fr"                    |
| [atributo~=valor]  | [input~=hello] {}   | Elementos con atributo input que contengan la subcadena "hola" separada por espacios en blanco |
| [atributo\|=valor] | [lang\|=en] {}      | Elementos con un valor del atributo lang igual a "en" o "en-"(guión en)                        |
| [atributo^=valor]  | a[href^="https"] {} | Todo elemento `<a>` con valor de atributo href comienza por "https"                                  |
| [attribute$=valor] | a[href$=".docx"] {} | Cada elemento `<a>` con valor de atributo href termina con ".docx"                                   |
| [atributo*=valor]  | a[href*="meta"] {}  | Cada elemento `<a>` con valor de atributo href tiene la subcadena "meta"                             |

## Selectores de pseudoclases

| **Pseudoclase**        | **Ejemplo**               | **Descripción de la selección**                                                                                 |
| ---------------------- | ------------------------- | --------------------------------------------------------------------------------------------------------------- |
| :active                | a:active { }              | Todos los enlaces activos                                                                                       |
| :checked               | input:checked { }         | Todos los elementos `<input>` marcados                                                                          |
| :default               | input:default { }         | Todos los elementos `<input>` por defecto                                                                       |
| :disabled              | input:disabled { }        | Todos los elementos `<input>` desactivados                                                                      |
| :empty                 | div:empty { }             | Todos los elementos `<div>` sin hijos                                                                           |
| :enabled               | input:enabled { }         | Todos los elementos `<input>` habilitados                                                                       |
| :first-child           | p:first-child { }         | Todos los elementos `<p>` que son el primer hijo de un elemento padre                                           |
| :first-of-type         | p:first-of-type { }       | Todos los elementos `<p>` que son el primer elemento `<p>` de un elemento padre                                 |
| :focus                 | input:focus { }           | Elemento de entrada bajo foco                                                                                   |
| :fullscreen            | :fullscreen { }           | El elemento en modo de pantalla completa                                                                        |
| :hover                 | p:hover { }               | Efecto de la acción al pasar el ratón por encima                                                                |
| :invalid               | input:invalid { }         | Elementos de entrada con un valor no válido                                                                     |
| :last-child            | p:last-child { }          | Todos los elementos `<p>` que son el último hijo de un elemento padre                                           |
| :last-of-type          | p:last-of-type { }        | Todos los elementos `<p>` que son el último elemento `<p>` de un elemento padre                                 |
| :link                  | a:link { }                | Todos los enlaces no visitados                                                                                  |
| :not_(selector_)       | :not(div) { }             | Todos los elementos que no son un elemento `<div>`                                                              |
| :nth-child_(n_)        | div:nth-child(3) { }      | Todos los elementos `<p>` que son el tercer hijo de un elemento padre                                           |
| :nth-last-child(_n)    | div:nth-last-child(3) { } | Todos los elementos `<div>` que son el tercer hijo de un elemento padre, contando desde el último elemento hijo |
| :nth-last-of-type(_n_) | p:nth-last-of-type(2) { } | El segundo hermano a partir del último hijo de un elemento padre.                                               |
| :nth-of-typ(_n_)       | p:nth-of-type(2) { }      | El segundo hermano de un elemento padre.                                                                        |
| :only-of-type          | p:only-of-type { }        | Todos los elementos `<p>` que son sólo elementos `<p>` dentro de su padre                                       |
| :only-child            | p:only-child { }          | Todos los elementos `<p>` que son sólo hijos de un elemento padre                                               |
| :optional              | input:optional { }        | Los elementos de entrada sin atributo "requerido"                                                               |
| :required              | input:required { }        | Selecciona los elementos de entrada con el atributo "requerido" especificado                                    |
| :root                  | :root { }                 | El elemento raíz del documento                                                                                  |
| :selection             | ::selection { }           | La parte de un elemento que es seleccionada por un usuario                                                      |
| :valid                 | input:valid { }           | Todos los elementos de entrada con un valor válido                                                              |
| :visited               | a:visited { }             | Selecciona todos los enlaces visitados                                                                          |

## Selectores de pseudoelementos

| **Sintaxis**   | **Ejemplo**            | **Descripción**                                                                |
| -------------- | ---------------------- | ------------------------------------------------------------------------------ |
| ::after        | p::after { }           | Inserta el contenido después del contenido del elemento <p>                    |
| ::before       | p::before { }          | Inserta el contenido antes del contenido del elemento <p>                      |
| ::first-letter | p::first-letter { }    | Selecciona la primera letra de cada elemento <p>                               |
| ::first-line   | p::first-line { }      | Selecciona la primera línea de cada elemento <p>                               |
| ::placeholder  | input::placeholder { } | Selecciona los elementos de entrada con el atributo "placeholder" especificado |
| ::marker       | ::marker { }           | Selecciona marcadores en una lista                                             |