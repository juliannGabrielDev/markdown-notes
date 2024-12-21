---
Fecha: 2024-12-20
Categoría: Uso y estilo de los componentes
tags:
  - front-end
  - curso-5
  - modulo-1
---
Así que ha explorado varias formas de definir componentes en React; esto incluye declaraciones de función, expresiones de función y funciones de flecha.

A medida que continúe con la construcción de su conocimiento de la sintaxis de React, aprenderá a hacer un mayor uso de JSX y expresiones JSX incrustadas.

En esta lectura, se familiarizará con la forma de utilizar expresiones ternarias para lograr un retorno aleatorio, así como la forma de invocar funciones dentro de expresiones JSX.

## **1 Una forma diferente de escribir un condicional if...else**
---
Es probable que esté familiarizado con la estructura de un condicional if...else. Aquí tiene un rápido repaso:

```js
let name = 'Bob';
if (name == 'Bob') {
    console.log('Hello, Bob');
} else {
    console.log('Hello, Friend');
};
```

El código anterior funciona como sigue:

1. Primero, declaro una variable `name` y la establezco en una cadena de `"Bob"`.

2. A continuación, utilizo la sentencia `if` para comprobar si el valor de la variable de nombre es `"Bob"`. Si lo es, quiero `console.log` la palabra `"Bob"`.

3. En caso contrario, si el valor de la variable de nombre no es `"Bob"`, el bloque else se ejecutará y mostrará las palabras `"Hello, Friend"` en la consola.

Más arriba le he dado un ejemplo de utilización de un condicional *if...else*. ¿Sabía que existe otra forma, diferente, de hacer efectivamente lo mismo? Se conoce como **operador ternario**. Un operador ternario en JavaScript utiliza dos caracteres distictos: el primero **es el signo de interrogación**, es decir, el carácter `?`. A la izquierda del carácter `?`, usted pone _una condición que le gustaría comprobar_. Al igual que hice en la declaración anterior *if...else*, la condición que estoy comprobando es `name == 'Bob'`. En otras palabras, le estoy pidiendo al motor de JavaScript que mire el valor que está almacenado dentro de la variable `name`, y que verifique si ese valor es el mismo que `'Bob'`. Si lo es, entonces el motor JavaScript devolverá el valor booleano de `true`. Si el valor de la variable name es algo diferente de `'Bob'`, el valor que devolverá el motor JavaScript será el valor booleano de `false`.

He aquí el código que refleja la explicación del párrafo anterior:

```js
name == 'Bob' ?
```

Observe que el código anterior está incompleto. Tengo la condición que estoy comprobando (la parte `name == 'Bob'` ). También tengo el carácter `?`, es decir, el primero de los dos caracteres necesarios para construir un operador ternario sintácticamente válido. Sin embargo, aún necesito el segundo carácter, que son los dos puntos, es decir, el carácter `:`. Este carácter se coloca después del carácter de signo de interrogación. Ahora puedo ampliar mi código para incluirlo también:

```js
name == Bob ? "Yes, it is Bob" : "I don't know this person";
```

Así es, en esencia, como funciona el operador ternario. Es sólo una sintaxis abreviada que puedo utilizar como sustituto de la sentencia `if`. Para demostrar que realmente es así, aquí está mi ejemplo inicial *if...else*, escrito como operador ternario:

```js
let name = 'Bob';
name == 'Bob' ? console.log('Hello, Bob') : console.log('Hello, Friend');
```

## **2 Uso de expresiones ternarias en JSX**
---
Examinemos un ejemplo de componente que utiliza una expresión ternaria para cambiar aleatoriamente el texto que se muestra.

```jsx
function Example() {
    return (
        <div className="heading">
            <h1>{Math.random() >= 0.5 ? "Over 0.5" : "Under 0.5"}</h1>
        </div>
    );
};
```

Dentro del elemento `<h1>`, las llaves indican a React que desea que analice el código que contiene como JavaScript normal.

A continuación, dentro de las llaves, puede añadir una expresión ternaria. Toda declaración ternaria conceptualmente, expresada en pseudocódigo, funciona así:

```
comparison ? true : false
```

En el ejemplo de código real que aparece al principio de esta lección, la parte de comparación, que va a la izquierda del signo de interrogación, utiliza el operador `>=` (mayor que o igual a) para devolver un valor booleano. Si el resultado de la comparación se evalúa como `true`, entonces se devuelve la cadena `"Más de 0,5"`. En otras palabras, se devolverá lo que haya entre el signo de interrogación y el carácter de punto y coma. De lo contrario, si el resultado de la comparación se evalúa como `false`, entonces se devuelve la cadena `"Menos de 0,5"`. En otras palabras, la expresión ternaria devolverá el valor situado a la derecha de los dos puntos.

Así es como puede utilizar una expresión ternaria para comprobar una condición justo dentro de un componente y devolver un valor dinámicamente.

## **3 Uso de llamadas a funciones en JSX**
---
Otra forma de trabajar con una expresión en JSX es invocar una función. La invocación a una función es una expresión porque toda expresión devuelve un valor, y la invocación a una función siempre devolverá un valor, incluso cuando ese valor de retorno sea `undefined`.

Como en el ejemplo anterior, puede utilizar la invocación de funciones dentro de JSX para devolver un número aleatorio:

```jsx
function Example2() {
    return (
        <div className="heading">
            <h1>Here's a random number from 0 to 10: 
                { Math.floor(Math.random() * 10) + 1 }
            </h1>
        </div>
    );
};
```

En el componente `Example2`, se están utilizando los métodos incorporados `Math.floor()` y `Math.random()`, así como algunos valores numéricos y operadores aritméticos, para mostrar un número aleatorio entre `0` y `10`.

También puede extraer esta funcionalidad en una función independiente:

```jsx
function Example3() {

    const getRandomNum = () => Math.floor(Math.random() * 10) + 1

    return (
        <div className="heading">
            <h1>Here's a random number from 0 to 10: { getRandomNum() }</h1>
        </div>
    );
};
```

La función `getRandomNum()` también puede escribirse como una declaración de función, o como una expresión de función. No tiene por qué ser una función de flecha.

Pero observemos ambas alternativas: la expresión de función _y_ la declaración de función.

**Expresión de función:**

```js
const getRandomNum = function() {
    return Math.floor(Math.random() * 10) + 1
} ;
```

**Declaración de función:**

```js
function getRandomNum() {
    return Math.floor(Math.random() *10) + 1
};
```

Por supuesto, existen muchos otros ejemplos. Los utilizados aquí están ahí para ayudarle a comprender lo versátil y fluida que es la sintaxis JSX. A medida que mejore sus habilidades en React, encontrará muchas formas creativas de utilizar expresiones JavaScript en JSX.

Ahora que ha completado esta lectura, usted ha aprendido acerca de algunas maneras más que usted puede utilizar expresiones en JSX.