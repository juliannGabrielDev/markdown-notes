---
Fecha: 2024-12-20
Categoría: Uso y estilo de los componentes
tags:
  - front-end
  - curso-5
  - modulo-1
---
Anteriormente, aprendió a pasar props a y dentro de un componente. Pero también existe una prop especial llamada `props.children`, que se pasa automáticamente a cada componente. En esta lectura, aprenderá sobre `props.children` y su propósito.

Para comprender el concepto de `props.children`, considere la siguiente situación de la vida real: tiene un par de manzanas y otro par de peras. Le gustaría transportar las manzanas a cierta distancia, así que, obviamente, utilizará una bolsa.

No es una "bolsa para manzanas", ni una "bolsa para peras" Es simplemente una bolsa. No hay nada en esta bolsa que haga necesario referirse a ella como una bolsa en la que sólo y siempre llevaría manzanas, ni como una bolsa en la que sólo y siempre llevaría peras.

En cierto modo, a la bolsa "le da igual" si se utiliza para llevar manzanas o peras. Nada en la bolsa cambia. No hay cambios en el material, el tamaño, la forma o el color de la bolsa, porque puede soportar sin problemas que se lleven manzanas o peras en su interior.

Ahora, considere el siguiente componente:

```jsx
function Apples(props) {
  return (
    <div className="promo-section">
        <div>
            <h2>These apples are: {props.color}</h2>
            </div>
            <div>
            <h3>There are {props.number} apples.</h3>
        </div>
    </div>
  )
}

export default Apples
```

También existe un componente `Pears`:

```jsx
function Pears(props) {
  return (
    <h2>I don't like pears, but my friend, {props.friend}, does</h2>
  )
}
```

Ahora, la cuestión es la siguiente: Supongamos que desea un componente `Bag` , que puede utilizarse para "transportar" `Apples` o `Pears`. ¿Cómo lo haría?

Aquí es donde entra en juego `props.children` .

Puede definir un componente `Bag` de la siguiente manera:

```jsx
function Bag(props) {
    const bag = {
        padding: "20px",
        border: "1px solid gray",
        background: "#fff",
        margin: "20px 0"
    }
    return (
        <div style={bag}>
            {props.children}
        </div>
    )
}
export default Bag
```

Así, lo que esto hace en el componente `Bag` es: añade un envoltorio `div` con un estilo específico, y luego le da `props.children` como contenido.

Pero, ¿qué es este `props.children`?

Considere un ejemplo muy sencillo:

```jsx
<Example>
    Hello there
</Example>
```

El texto `Hello there` es hijo del elemento JSX `Example`. El elemento `Example` JSX anterior es una "invocación" del archivo **Example.js**, que, en React moderno, suele ser un componente de función.

Este texto `Hello there` puede pasarse como un **named prop** al renderizar el componente `Example` .

Esto es lo que parecería:

```jsx
<Example children="Hello there" />
```

Hay dos maneras de realizar esta acción. Pero esto es sólo el principio.

¿Qué pasaría si, por ejemplo, quisiera rodear el texto `Hello there` en un elemento HTML h3 ?

Obviamente, en JSX, eso es fácilmente realizable:

```jsx
<Example children={<Hello />} />
```

Incluso podría hacer que el componente Hello fuera más dinámico, dándole su propia `prop`:

```jsx
<Example children={<Hello message="Hello there" />} />
```

Entonces, ¿cómo puede hacer que funcionen los ejemplos de **Bag**, **Apples** y **Pears** del principio de esta lectura?

He aquí cómo renderizaría el componente Bag con el componente Apples como su `props.children`:

```jsx
<Bag children={<Apples color="yellow" number="5" />} />
```

Y he aquí cómo renderizaría el componente `Bag` , envolviendo al componente `Pears` :

```jsx
<Bag children={<Pears friend="Peter" />} />
```

Aunque la sintaxis anterior pueda parecer extraña, es importante entender lo que está ocurriendo.

Efectivamente, la sintaxis anterior es la misma que la de los dos ejemplos siguientes.

```jsx
<Bag>
    <Apples color="yellow" number="5" />
</Bag>

<Bag>
    <Pears friend="Peter" />
</Bag>
```

Incluso puede tener varios niveles de elementos JSX anidados, o un único elemento JSX que tenga varios hijos, como, por ejemplo:

```jsx
<Trunk>
    <Bag>
        <Apples color="yellow" number="5" />
        <Pears friend="Peter" />
    </Bag>
</Trunk>
```

Así, en la estructura anterior, hay un elemento JSX `Trunk` , dentro del cual hay un único elemento JSX `Bag` , que contiene un elemento JSX `Apples` y un elemento JSX `Pears` .

Antes de terminar esta lectura, considere de nuevo este elemento JSX:

```jsx
<Bag>
    <Apples color="yellow" number="5" />
</Bag>
```

¿Qué es **Apples** to **Bag** en el código anterior?

En el código anterior, `Apples` es un prop del componente `Bag`. Para explicarlo mejor, el componente Bolsa puede envolver al componente `Apples`, **o a** _**cualquier**_ **otro componente**, porque he utilizado la **sintaxis** `{props.children}` en la **declaración de función del componente `Bag`**. En otras palabras, al igual que en el mundo real, cuando lleva una bolsa a una tienda de comestibles, puede "envolver" una amplia variedad de comestibles dentro de la bolsa, puede hacer lo mismo en React: envolver una amplia variedad de componentes dentro del componente `Bag` , utilizando la *prop children* para conseguirlo.

Es crucial entender esto cuando se trabaja con React.

Antes de terminar esta lectura, hay otro concepto importante que debe conocer: _encontrar la cantidad adecuada de modularización_. ¿Qué significa esto? Imagine, por ejemplo, que tiene varias bolsas pequeñas, y que cada bolsa sólo puede llevar una manzana o una pera. Tendría que envolver cada "manzana" dentro de una "bolsa". Eso no tiene mucho sentido. Puede pensar en componentes que hagan que sus diseños sean modulares de forma similar. No querrá tener toda una maqueta contenida en un solo componente, porque eso sería muy difícil de trabajar. Por otro lado, si hiciera de cada elemento HTML de su maquetación un componente independiente, sería muy difícil trabajar con él, aunque esa maquetación sería modular. Así que todo es cuestión de moderación. Necesita organizar sus maquetaciones dividiéndolas en áreas significativas de la página, y luego codificar esas áreas significativas como componentes separados. eso constituiría la cantidad adecuada de modularidad. Para reforzar este punto, quizá le ayude pensar en cómo describiría una persona una página web: un menú, un pie de página, un carrito de la compra, etc.

En conclusión, cuando vea un elemento JSX envolviendo a otro elemento JSX, podrá entender fácilmente que todo es simplemente `props.children` en segundo plano.