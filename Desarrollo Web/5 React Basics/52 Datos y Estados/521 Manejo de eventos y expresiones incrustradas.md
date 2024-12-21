---
Fecha: 2024-12-20
Categoría: Eventos dinámicos y cómo manejarlos
---
En esta lectura, aprenderá las diferentes formas de incrustar expresiones en manejadores de eventos en React:

- Con una función ES5 anónima inline

- Con una función ES6 anónima en línea (una función de flecha)

- Utilizando una declaración de función independiente

- Usando una expresión de función separada

Puede que esta lectura le resulte útil como hoja de referencia.

Para mayor claridad y simplicidad: una función simplemente registrará por consola algunas palabras. Esto le permitirá comparar la diferencia en la sintaxis entre estos cuatro enfoques, mientras que el resultado de la manipulación de eventos siempre será el mismo: sólo algunas palabras de salida a la consola.

## **1 Manejo de eventos utilizando funciones ES5 anónimas en línea**
---
Este enfoque le permite pasar directamente una declaración de función ES5 como valor del atributo `event-handling` de onClick:

```jsx
<button onClick={function() {console.log('first example')}}>
    An inline anonymous ES5 function event handler
</button>
```

Aunque es posible escribir sus manejadores de clics utilizando esta sintaxis, no es un enfoque común y no encontrará este tipo de código muy a menudo en las aplicaciones React.

## **2 Manejar eventos usando funciones ES6 anónimas en línea (funciones flecha)**
---
Con este enfoque, puede pasar directamente una declaración de función ES6 como valor del atributo de gestión de eventos `onClick`:

```jsx
<button onClick={() => console.log('second example')}>
    An inline anonymous ES6 function event handler
</button>
```

Este enfoque es mucho más común que el anterior. Si desea mantener toda su lógica dentro de la expresión JSX asignada al atributo onClick, utilice esta sintaxis.

## **3 Manejar eventos usando declaraciones de función separadas**
---
Con este enfoque, usted declara una declaración de función ES5 separada, y luego hace referencia a su nombre en el atributo `onClick` de manejo de eventos, como se indica a continuación:

```jsx
function App() {
    function thirdExample() {
        console.log('third example');
    };
    return (
        <div className="thirdExample">
            <button onClick={thirdExample}>
                using a separate function declaration
            </button>
        </div>
    );
};
export default App;
```

Esta sintaxis tiene sentido utilizarla cuando su lógica `onClick` es demasiado compleja para caber fácilmente en una función anónima. Aunque este ejemplo no muestra realmente este escenario, imagine una función que tiene, por ejemplo, 20 líneas de código, y que necesita ejecutarse cuando se dispara el evento click. Este es un caso de uso perfecto para una declaración de función separada.

## **4 Manejo de eventos mediante expresiones de función separadas**
---
**Sugerencia**_:_ Una forma de determinar si una función está definida como una expresión o una declaración es: si no comienza la línea con la palabra clave function, entonces es una expresión.

En el siguiente ejemplo, está asignando una función de flecha ES6 anónima a una variable `const -` por lo tanto, se trata de una expresión de función.

A continuación, está utilizando el nombre de esta variable `const` para manejar el evento `onClick`, por lo que este es un ejemplo de manejo de eventos utilizando una expresión de función independiente.

```jsx
function App() {
    const fourthExample = () => console.log('fourth example');

    return (
        <div className="fourthExample">
            <button onClick={fourthExample}>
                using a separate function expression
            </button>
        </div>
  );
};
export default App;
```

La sintaxis en este ejemplo es muy común en React. Utiliza funciones de flecha, pero también nos permite manejar situaciones en las que nuestra expresión de función separada abarca varias líneas de código.

En este punto de la lección de lectura, ha aprendido los diversos tipos de funciones que puede utilizar para manejar eventos en React. Algunas de ellas son más comunes que otras, pero ahora que conoce todas las diferentes formas de hacerlo, puede entender el código de otras personas más fácilmente, así como elegir la sintaxis que mejor se adapte a su caso de uso dado, como una guía de estilo de codificación específica de la empresa.