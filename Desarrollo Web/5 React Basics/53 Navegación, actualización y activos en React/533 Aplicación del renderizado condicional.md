---
Fecha: 2024-12-21
Categoría: Enlaces y enrutamiento
tags:
  - front-end
  - curso-5
  - modulo-3
---
El estado son todos los datos con los que trabaja actualmente su aplicación. Con esto en mente, puede decidir renderizar condicionalmente componentes específicos en su app, basándose en si determinados datos de estado tienen valores específicos. Para hacer esto posible, React trabaja con la sintaxis y los conceptos de JavaScript fácilmente disponibles.

Consideremos una aplicación de productividad minimalista.

La app toma la fecha y hora actuales del ordenador cliente y, basándose en los datos, muestra uno de dos mensajes en la pantalla:

1. Para los días laborables, el mensaje es "Hágalo"

1. Para los fines de semana, el mensaje es: "Descansa un poco"

Hay algunas maneras de lograr esto en React.

Un enfoque incluiría establecer un componente para cada uno de los posibles mensajes, lo que significa que tendría dos componentes. Llamémoslos `Workdays` y `Weekends`.

Entonces, tendría un componente `CurrentMessage`, que renderizaría el componente apropiado basándose en el valor devuelto por la llamada a la función `getDay()`.

Aquí tiene un componente `CurrentMessage` simplificado:

```jsx
function CurrentMessage() {
    const day = new Date().getDay();

    if (day >= 1 && day <= 5) {
        return <Workdays />
    }
    return <Weekends />
}
```

En lugar de calcularlo directamente, podría utilizar en su lugar algunos datos históricos, y quizás obtener esos datos de un usuario a través de una entrada, de un componente padre.

En ese caso, el componente `CurrentMessage` podría tener este aspecto:

```jsx
function CurrentMessage(props) {
    if (props.day >= 1 && props.day <= 5) {
        return <Workdays />
    }
    return <Weekends />
}
```

## **Renderización condicional con ayuda de variables de elementos**
---
Para mejorar aún más su componente `CurrentMessage`, es posible que desee utilizar variables de elemento. Esto es útil en algunos casos, en los que desea agilizar su código de renderizado - es decir, cuando desea separar la lógica condicional del código para renderizar su IU.

He aquí un ejemplo de cómo hacerlo con el componente `CurrentMessage`:

```jsx
function CurrentMessage({day}) {
    const weekday = (day >= 1 && day <= 5);
    const weekend = (day >= 6 && day <= 7);
    let message;

    if (weekday) {
        message = <Workdays />
    } else if (weekend) {
        message = <Weekends />
    } else {
        message = <ErrorComponent />
    }

  

    return (
        <div>
            {message}
        </div>
    )
}
```

La salida del componente `CurrentMessage` dependerá de cuál sea el valor recibido de la variable de día. Con la condición de que la variable de día tenga el valor de cualquier número entre 1 y 5 (ambos inclusive), la salida será el contenido del componente `Workdays`. En caso contrario, si la variable del día tiene el valor `6` ó `7`, la salida será el contenido del componente `Weekends`.

## **2 Renderizado condicional utilizando el operador lógico AND**
---
Otro enfoque interesante en la renderización condicional es el uso del operador lógico AND `&&` .

En el siguiente componente, se muestra cómo se utiliza el operador `&&` para conseguir un renderizado condicional:

```jsx
function LogicalAndExample() {
    const val = prompt('Anything but a 0')

    return (
        <div>
            <h1>Please don't type in a zero</h1>
            {val &&
                <h2>Yay, no 0 was typed in!</h2>
            }
        </div>
    )
}
```

Hay algunas cosas que desentrañar aquí, así que he aquí la explicación del componente `LogicalAndExample`, de arriba abajo:

1. En primer lugar, se pide al usuario que escriba en el `prompt`, especificando que se requiere cualquier cosa que no sea un carácter cero; y se guarda la entrada en el valor val.

2. En la declaración de retorno, un encabezado `h1` se envuelve dentro de un elemento `div`, y luego se utilizan llaves para incluir una expresión JSX. Dentro de esta expresión JSX hay un único operador `&&,` que está rodeado por algo de código tanto en su lado izquierdo como en su lado derecho; en el lado izquierdo, se proporciona el valor val, y en el derecho, se proporciona un fragmento de JSX.

Para entender lo que se mostrará en pantalla, considere el siguiente ejemplo en JavaScript estándar:

```jsx
true && console.log('This will show')
```

Si ejecuta este comando en la consola del navegador, saldrá el texto `'Esto se mostrará'`.

Por otro lado, considere el siguiente ejemplo:

```jsx
false && console.log('This will never show')
```

Si ejecuta _este_ comando, la salida será simplemente el valor booleano de `false`.

En otras palabras, si una proposición se evalúa como true, utilizando el operador `&&,` puede renderizar los elementos JSX que desee a la derecha del operador `&&`.