---
Fecha: 2024-12-19
Categoría: Los componetes de React y dónde viven
tags:
  - front-end
  - curso-5
  - modulo-1
---
## **1 Introducción**
---
Los componentes son una buena manera de construir sitios web en React porque le permiten construir aplicaciones más modulares. Sin embargo, ¿cómo se construyen componentes utilizando React, JSX y JavaScript? Aprenderá cómo funciona en esta lección.

## **2 Un navegador no puede entender la sintaxis JSX**
---
Esto significa que hacer que un navegador entienda el código React requiere un montón de tecnologías de apoyo.

Un ejemplo de tal tecnología es un **transpilador**.

Un **transpilador** toma un trozo de código y lo transforma en algún otro código.

Para entender por qué se hace esto, he aquí un ejemplo de una declaración de variable ES6:

```js
const PI = 3.14
```

Se trata de una sintaxis ES6 perfectamente válida.

Sin embargo, si utiliza un ordenador muy antiguo, ese ordenador tendrá un navegador antiguo. Tal vez ese navegador fue construido antes de que ES6 saliera en 2015.

Esto significa que el motor JavaScript que está incorporado en el navegador de su ordenador antiguo es probable que sea un motor JavaScript ES5.

En ES5, la única forma de declarar una variable es la siguiente:

```js
var pi = 3.14
```

Lo que esto significa es que para que este viejo navegador entienda el código ES6, la única forma de hacerlo es **transpilándolo** .

Si le apetece, puede intentar transpilar el código ES6 a ES5 usted mismo, utilizando [el sitio web es6console](https://es6console.com/).

Ahora, pasemos a otro ejemplo de transpilación.

Supongamos que desea utilizar una nueva sintaxis de ECMAScript, la más moderna, en una aplicación. El único problema es que esta nueva sintaxis no está soportada actualmente por ningún navegador; ni siquiera por un navegador actualizado.

Sin embargo, al transpilar la nueva sintaxis más moderna de JavaScript en algo que los navegadores modernos puedan entender, es capaz de convertir un código que el navegador no puede comprender, en código que sí puede comprender, ejecutar y producir un resultado a partir de él.

Probablemente el sitio más popular que muestra cómo funciona esto es [Babel](https://babeljs.io/). Como reza el encabezamiento del sitio web, "Babel es un compilador de JavaScript".

Esto le lleva finalmente al punto de esta discusión sobre transpilar código JavaScript.

Lo que Babel hace es lo siguiente: le permite transpilar código JSX (que no puede ser entendido por un navegador) en código JavaScript plano (que puede ser entendido por un navegador).

Aquí es donde React y JSX entran en juego.

Para que el código React sea entendido por un navegador, necesita tener un **paso de transpilación** en el que el código JSX se convierta en código JavaScript plano con el que un navegador moderno pueda trabajar.

Para demostrar cómo funciona esto, vamos a utilizar el componente Heading de la lección anterior.

Añada el código JSX en [la réplica en línea de Babel](https://babeljs.io/repl#?browsers=defaults%2C%20not%20ie%2011%2C%20not%20ie_mob%2011&build=&builtIns=false&corejs=3.21&spec=false&loose=false&code_lz=GYVwdgxgLglg9mABACQKYEMAmMwHMAUADgE5yEDOAlIgN4BQijixqUIxSAPABYCMAfDRJlyAOlhQANqgC-nAPR9-dGUA&debug=false&forceAllTransforms=false&modules=false&shippedProposals=false&circleciRepo=&evaluate=false&fileSize=false&timeTravel=false&sourceType=module&lineWrap=true&presets=env%2Creact%2Cstage-2&prettier=false&targets=&version=7.22.20&externalPlugins=&assumptions=%7B%7D "Link updated to use the latest version of Babel"). Repl significa "bucle de lectura-evaluación-impresión" y acepta el código que usted escriba, lo evalúa y produce algún resultado. En el caso concreto de [el Babel repl en línea](https://babeljs.io/repl#?browsers=defaults%2C%20not%20ie%2011%2C%20not%20ie_mob%2011&build=&builtIns=false&corejs=3.21&spec=false&loose=false&code_lz=GYVwdgxgLglg9mABACQKYEMAmMwHMAUADgE5yEDOAlIgN4BQijixqUIxSAPABYCMAfDRJlyAOlhQANqgC-nAPR9-dGUA&debug=false&forceAllTransforms=false&modules=false&shippedProposals=false&circleciRepo=&evaluate=false&fileSize=false&timeTravel=false&sourceType=module&lineWrap=true&presets=env%2Creact%2Cstage-2&prettier=false&targets=&version=7.22.20&externalPlugins=&assumptions=%7B%7D "Link updated to use the latest version of Babel")ese resultado es algún código transpilado. Aquí tiene una explicación más detallada.

Si ha visitado la URL enlazada anteriormente, encontrará una página web que tiene dos paneles. A la izquierda, está el código fuente JSX:

```jsx
function Heading(props) {
	return <h1>{props.title}</h1>
}
```

... y a la derecha, está el código JavaScript transpilado y sin formato. Sin embargo, asegúrese de seleccionar el tiempo de ejecución **clásico** para React en la barra lateral izquierda.

```js
function Heading(props) {
	return /*#__PURE__*/React.createElement("h1", null, props.title);
}
```

Así pues, aquí tiene un objeto React, y este objeto tiene un método createElement() en él. El método se invoca con tres argumentos:

1. `"h1"`
2. `null`
3. `props.title`

El primer argumento es el elemento DOM a renderizar - en este caso, un elemento `h1`. La segunda propiedad es cualquier atributo HTML que deba añadirse, y aquí hay un `null` - lo que significa que debería haber un objeto con algún dato, pero no hay ningún dato, así que en lugar del objeto está el valor null. La tercera propiedad es el contenido del HTML interno del elemento DOM especificado como primer argumento - en este caso, el contenido del HTML interno del elemento `h1`.

Ahora volvamos a utilizar Babel, y esta vez transpilemos la sintaxis de render para el componente Heading:

```jsx
<Heading title="This is the heading text!"></Heading>
```

De nuevo utilizando [la réplica de Babel](https://babeljs.io/repl#?browsers=defaults%2C%20not%20ie%2011%2C%20not%20ie_mob%2011&build=&builtIns=false&corejs=3.21&spec=false&loose=false&code_lz=DwCQpghgJglgdgcwAQBcYoDZgLwCIAqAFjAM5KmqFhJXTzIpgAeKAhLgHzAD04diHIA&debug=false&forceAllTransforms=false&modules=false&shippedProposals=false&circleciRepo=&evaluate=false&fileSize=false&timeTravel=false&sourceType=module&lineWrap=true&presets=env%2Creact%2Cstage-2&prettier=false&targets=&version=7.22.20&externalPlugins=&assumptions=%7B%7D "Link updated to use the latest Babel")y como puede comprobarse en [el enlace](https://babeljs.io/repl#?browsers=defaults%2C%20not%20ie%2011%2C%20not%20ie_mob%2011&build=&builtIns=false&corejs=3.21&spec=false&loose=false&code_lz=DwCQpghgJglgdgcwAQBcYoDZgLwCIAqAFjAM5KmqFhJXTzIpgAeKAhLgHzAD04diHIA&debug=false&forceAllTransforms=false&shippedProposals=false&circleciRepo=&evaluate=false&fileSize=false&timeTravel=false&sourceType=module&lineWrap=true&presets=env%2Creact%2Cstage-2&prettier=false&targets=&version=7.18.5&externalPlugins=&assumptions=%7B%7D), la salida de la transpilación es el siguiente código. Asegúrese de seleccionar el tiempo de ejecución **clásico** para React en la barra lateral izquierda.

```js
/*#__PURE__*/
React.createElement(Heading, {
	title: "This is the heading text!"
});
```

De nuevo, tiene la llamada al método `React.createElement()`, y esta vez, el primer elemento a renderizar es `Heading`, y entonces tiene un objeto como segundo argumento (en lugar de un `null` que tenía en el ejemplo de transpilación anterior).

Esto me lleva a una pregunta interesante: ¿Cuál es el código mínimo que debe tener un componente para poder mostrar algo en la pantalla cuando se renderiza?

```jsx
function Example() {
    return <div>An element</div>
}

export default Example
```