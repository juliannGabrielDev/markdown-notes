---
Fecha: 2024-12-20
Categoría: Uso y estilo de los componentes
tags:
  - front-end
  - curso-5
  - modulo-1
---
## **1 Componentes como expresiones de función**
---
Hasta este punto, es probable que sólo haya observado declaraciones de función ES5 utilizadas para definir componentes en React. Sin embargo, esta no es la única forma de hacerlo.

En esta lectura, aprenderá sobre algunos enfoques alternativos, concretamente mediante el uso de expresiones de función y funciones de flecha.

**Expresiones de función**

Empecemos con una declaración de función utilizada como componente en React:

```jsx
function Nav(props) {
    return (
        <ul>
            <li>{props.first}</li>
        </ul>
    )
}
```

El código de este componente devuelve un elemento de lista que contiene el valor de la `prop.first`.

Ahora, cambiemos esta declaración de función por una expresión de función:

```jsx
const Nav = function(props) {
    return (
        <ul>
            <li>{props.first}</li>
        </ul>
    )
}
```

El componente es, en su mayor parte, el mismo. Lo único que ha cambiado es que ahora está utilizando una función anónima (sin nombre), y asignando esta declaración de función anónima a una variable declarada utilizando la palabra clave `const`, y el nombre `Nav`. El resto del código es idéntico.

Cambiar un componente de una declaración de función a una expresión de función no cambia su comportamiento, ni cómo se escribe el código para renderizar el componente `Nav`. Sigue siendo el mismo:

```jsx
<Nav first="Home" />
```

También puede llevar este concepto un paso más allá, utilizando funciones de flecha.

## **2 Componentes como funciones de flecha**
---
Las funciones de flecha son una característica esencial de la versión ES6 de JavaScript.

Una de las principales ventajas de utilizar funciones de flecha es su sintaxis más corta.

Considere la expresión de la función `Nav` escrita como una función de flecha:

```jsx
const Nav = (props) => {
    return (
        <ul>
            <li>{props.first}</li>
        </ul>
    )
}
```

Entonces, la forma de pensar en esto es la siguiente:

- La propia flecha puede considerarse como el sustituto de la palabra clave `function`.

- Los parámetros que acepta esta función de flecha se enumeran antes de la propia flecha.

Para reiterar, tome la **función anónima ES5** más pequeña posible:

```js
const example = function() {}
```

Y luego observe cómo se escribe como una función de flecha:

```js
const example = () => {}
```

Otra regla importante con respecto a las funciones de flecha es que el uso de los paréntesis es opcional si hay un solo parámetro que una función acepta.

En otras palabras, otra forma correcta de escribir el componente anterior de la función de flecha Nav sería eliminar los paréntesis alrededor de `props`:

```jsx
const Nav = props => {
    return (
        <ul>
            <li>{props.first}</li>
        </ul>
    )
}
```

En todos los demás casos, cuando escriba funciones de flecha, **para cualquier número de parámetros que no sea un único parámetro, el uso de paréntesis alrededor de los parámetros es obligatorio**.

Por ejemplo, si su componente Nav no aceptara ningún parámetro, lo codificaría con paréntesis vacíos:

```jsx
const Nav = () => {
    return (
        <ul>
            <li>Home</li>
        </ul>
    )
}
```

Otra cosa interesante de las funciones de flecha es el **return implícito**. Sin embargo, sólo funciona si se encuentra en la misma línea de código que la propia flecha. En otras palabras, el retorno implícito funciona si todo su componente es una única línea de código.

Para demostrar cómo funciona, reescribamos el componente `Nav` como una sola línea de código:

```jsx
const Nav = () => <ul><li>Home</li></ul>
```

Observe que con el *return implícito*, ni siquiera tiene que utilizar las llaves que son delimitadores obligatorios del cuerpo de la función en todos los demás casos.

## **3 Uso de funciones de flecha en otras situaciones**
---
En React, al igual que en JavaScript plano, las funciones de flecha se pueden utilizar en muchas situaciones diferentes. Una de estas situaciones es su uso con, por ejemplo, el método *array* incorporado en `forEach()`.

Por ejemplo:

```js
[10, 20, 30].forEach(item => item * 10)
```

La salida de la línea de código JavaScript vainilla anterior serían tres valores numéricos:

**100200300**

Como nota al margen, el término "JavaScript vainilla" se utiliza a menudo para describir la sintaxis del lenguaje JavaScript normal y corriente, sin ningún código específico del marco de trabajo o de la biblioteca. Por ejemplo, React es una biblioteca, por lo que en este contexto, decir que un fragmento de código es "JavaScript vainilla" significa que no necesita ninguna biblioteca especial para ejecutarse. Puede ejecutarse en JavaScript "plano" sin dependencias adicionales.

También podría escribir este código en sintaxis ES5:

```js
[10, 20, 30].forEach(function(item) {
        return item * 10
    }
)
```

Independientemente de cómo lo escriba, el método `forEach()` puede ejecutarse sobre una matriz. El método `forEach()` acepta un único parámetro: una **función anónima**. Si escribe esta función anónima en sintaxis ES5, entonces contendría una sentencia return:

```js
function(item) {
    return item * 10
}
```

Si en cambio la escribe como una función ES6, puede simplificarse en una sola línea:

```js
item => item * 10
```

Ambas funciones realizan exactamente la misma tarea. Sólo la sintaxis es diferente. La función ES6 es mucho más corta porque:

- La función flecha tiene un único parámetro, por lo que no necesita añadir paréntesis alrededor del parámetro elemento (a la izquierda de la flecha).

- Como la función flecha cabe en una sola línea de código, no necesita utilizar llaves alrededor del cuerpo de la función, ni la palabra clave return; está implícito.

Las funciones de flecha se utilizan ampliamente en JSX en React, y acostumbrarse a su sintaxis y ser capaz de "analizarla mentalmente" a medida que la lee es una habilidad importante que debe tener y le ayuda a mejorar en la escritura de aplicaciones React.

Ahora que ha completado esta lectura, ha aprendido sobre algunos enfoques alternativos, concretamente mediante el uso de expresiones de función y funciones de flecha.