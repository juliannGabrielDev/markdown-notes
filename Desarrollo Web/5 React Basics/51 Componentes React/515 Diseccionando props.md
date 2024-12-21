---
Fecha: 2024-12-20
Categoría: Uso y estilo de los componentes
tags:
  - front-end
  - curso-5
  - modulo-1
---
Recordemos que, al igual que los parámetros en una función JavaScript que permiten pasar valores como argumentos, React utiliza propiedades, o **props**, para pasar datos entre componentes. Pero, ¿cómo funcionan exactamente?

En esta lectura, utilizará un transpilador para descomponer el código JSX a JavaScript plano, haciendo su propósito más comprensible.

Recuerde primero que el código JSX en React es sólo azúcar sintáctico - es decir, una forma más agradable de escribir código difícil de leer.

Para que el navegador entienda este azúcar sintáctico, necesita transpilar JSX a código JavaScript plano. Tiene un recurso en línea, en la URL de [babeljs.io](https://babeljs.io/ "Babel.io"), que le permite inspeccionar los resultados de esta transpilación. Una vez que visite el sitio web, asegúrese de navegar hasta el enlace _Pruébelo_ en la navegación principal.

Por ejemplo, supongamos que tiene un componente que devuelve un fragmento de JSX:

```jsx
function App() {
  return <h1>Hello there</h1>
}
```

... si utilizara el transpilador Babel para transpilar este código JSX de azúcar sintáctico a código JavaScript plano, obtendría de vuelta un código inusual:

```js
"use strict";
function App() {
    return /*#__PURE__*/React.createElement("h1", null, "Hello there");
}
```

Sólo quiere centrarse en la parte `React.createElement("h1", null, "Hello there");`. Puede ignorar el resto.

Esto significa que la función `createElement` recibe tres argumentos:

1. El elemento envolvente a renderizar.

2. Un valor nulo (que está ahí para mostrar la ausencia de un valor de objeto JavaScript esperado).

3. El contenido interno que irá dentro del elemento envolvente.

Curiosamente, el contenido interno que irá dentro del elemento envolvente también puede ser una llamada a la función `createElement` .

Por ejemplo, supongamos que tiene una estructura de elementos JSX un poco más compleja:

```jsx
function App() { 
  return (
    <div>
	    <h1>Hello there</h1> 
    </div>
  )
}
```

... la sentencia de retorno transpilada en JavaScript plano devuelve de nuevo dos funciones `createElement`:

```js
"use strict";
function App() {
  return /*#__PURE__*/React.createElement("div", null, /*#__PURE__*/React.createElement("h1", null, "Hello there"));
}
```

Si formatea esta salida, elimina la línea `"use strict"` y los comentarios `__PURE__`, obtendrá una salida más legible:

```js
function App() {
  return React.createElement(
    "div",
    null,
    React.createElement("h1", null, "Hello there")
  );
}
```

Así que ahora el tercer argumento de la llamada a `React.createElement` más externa es otra llamada a `React.createElement`.

Así es como puede anidar tantos elementos como desee.

Esto significa que una estructura JSX anidada no es más que un montón de llamadas `React.createElement` anidadas, pasadas a otras llamadas `React.createElement` como su tercer argumento.

## **El segundo - null - argumento**
---
El segundo argumento de `null` puede - en este caso - ser sustituido por un objeto vacío.

En ese caso, su código contendría un par de llaves en lugar de la palabra null:

```js
"use strict";

function App() {
  return React.createElement(
    "div",
    {},
    React.createElement("h1", {}, "Hello there")
  );
}
```

Este objeto se denomina objeto _props_. Es el principal mecanismo de envío de datos de un componente padre a un componente hijo en React.

La forma en que esto funciona se describe en React docs utilizando el siguiente código:

```
React.createElement(
  type,
  [props],
  [...children]
)
```


## **El tercer argumento (...children)**
---
Es el contenido interno que irá dentro del elemento envolvente. Es lo que hace posible anidar elementos dentro de otros elementos, imitando la forma en que funciona HTML.

En esta lectura ha aprendido a utilizar un transpilador para descomponer el código JSX en JavaScript plano, haciendo más comprensible su propósito.