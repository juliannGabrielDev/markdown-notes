---
Fecha: 2024-12-20
Categoría: Uso y estilo de los componentes
tags:
  - front-end
  - curso-5
  - modulo-1
---
Ya ha aprendido un poco sobre el uso de expresiones como accesorios. Éstas pueden ser, entre otras cosas, operadores ternarios, llamadas a funciones o algunas operaciones aritméticas.

Sin embargo, puede pasar casi cualquier tipo de expresión como `prop`.

Por ejemplo:

```jsx
const bool = false; 

function Example(props) {
    return (
        <h2>The value of the toggleBoolean prop is: {props.toggleBoolean.toString()}</h2>
    );
};

export default function App() { 
    return ( 
        <div className="App"> 
            <Example toggleBoolean={!bool} /> 
        </div> 
    ); 
};
```

En el ejemplo anterior, está utilizando el `!bool`, es decir, el operador NOT, que evalúa a `true`, ya que `!false` es verdadero.

Además, para que la proposición `toggleBoolean` se muestre en la página, está convirtiendo su valor booleano en una cadena utilizando el método `toString` incorporado en JavaScript.

He aquí una extensión del código anterior que muestra más formas de trabajar con expresiones como props en React.

Lo que ocurre aquí es que se están pasando varios props al componente Example, y renderizando cada uno de los valores de estos props en la pantalla.

```jsx
const bool = false;
const str1 = "just";

function Example(props) {
    return (
        <div>
            <h2>
                The value of the toggleBoolean prop is:{props.toggleBoolean.toString()}
            </h2>
            <p>The value of the math prop is: <em>{props.math}</em></p>
            <p>The value of the str prop is: <em>{props.str}</em></p>
        </div>
    );
};

export default function App() {
    return (
        <div className="App">
            <Example
                toggleBoolean={!bool}
                math={(10 + 20) / 3}
                str={str1 + ' another ' + 'string'}
            />
        </div>
    );
};
```

En esta mejora del componente `Example`, se le están pasando tres props: `toggleBoolean`, `math`, y `str`. El `toggleBoolean` no se ha modificado, y se han añadido el `math` prop y el `str` prop.

La prop `math` está ahí para mostrar que se pueden añadir operadores aritméticos y números dentro de JSX, y se evaluará igual que en JavaScript plano.

La prop `str` está ahí para mostrar que puede concatenar cadenas, así como cadenas y variables - lo que se muestra añadiendo literales de cadena de `" another "` y `" string"` a la variable `str1`.

En resumen, al igual que puede utilizar expresiones dentro de componentes de función, también puede utilizarlas como valores prop dentro de elementos JSX, al renderizar esos componentes de función.