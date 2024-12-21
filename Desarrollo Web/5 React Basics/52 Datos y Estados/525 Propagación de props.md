---
Fecha: 2024-12-20
Categoría: Datos y eventos
tags:
  - front-end
  - curso-5
  - modulo-2
---
Como ha aprendido anteriormente, el paso de props es una situación en la que se están pasando datos de un componente padre a un componente hijo, luego a un componente nieto, y así sucesivamente, hasta que llega a un componente más lejano, más abajo en el árbol de componentes, donde se requieren estos datos.

He aquí una aplicación muy sencilla que se centra en el proceso de paso de accesorios a través de varios componentes.

Tenga en cuenta que el objetivo aquí no es construir una app que existiría en el mundo real. El objetivo de esta app es examinar la práctica de la perforación de puntales, para que pueda centrarse en ella y comprenderla de forma aislada.

He aquí el código de la app:

```jsx
function Main(props) { 
  return <Header msg={props.msg} />; 
};

function Header(props) { 
  return ( 
    <div style={{ border: "10px solid whitesmoke" }}> 
      <h1>Header here</h1> 
      <Wrapper msg={props.msg} /> 
    </div> 
  ); 
};

function Wrapper(props) { 
  return ( 
    <div style={{ border: "10px solid lightgray" }}> 
      <h2>Wrapper here</h2> 
      <Button msg={props.msg} /> 
    </div> 
  ); 
};

function Button(props) { 
  return ( 
    <div style={{ border: "20px solid orange" }}> 
      <h3>This is the Button component</h3> 
      <button onClick={() => alert(props.msg)}>Click me!</button> 
    </div> 
  ); 
};

function App() { 
  return ( 
    <Main  
      msg="I passed through the Header and the Wrapper and I reached the Button component"  
    /> 
  ); 
}; 

export default App;
```

Esta aplicación es lo suficientemente sencilla como para que pueda entenderla por sí mismo. Abordemos los puntos principales para destacar lo que ocurre en el código anterior.

El componente superior de esta app es el componente `App`. El componente `App` devuelve el componente `Main`. El componente `Main` acepta un único atributo, denominado `msg`, como en "mensaje".

En la parte superior de la aplicación, la función `Main` declara cómo debe comportarse el componente `Main`. El componente `Main` se encarga de renderizar el componente `Header`. Tenga en cuenta que cuando el componente `Header` se renderiza desde dentro de Main, también recibe la función msg prop.

La declaración de función del componente `Header` renderiza un `h1` que dice `"Header here"`, y luego otro componente llamado `Wrapper`. Tenga en cuenta que la nomenclatura aquí es irrelevante - los componentes `Header` y `Wrapper` se nombran para que se parezca un poco más a lo que podría aparecer en una aplicación real - pero en última instancia, la atención se centra en tener múltiples componentes, en lugar de describir adecuadamente los nombres específicos de los componentes.

Así, la declaración de función del componente `Header` tiene una sentencia `return`, que **renderiza el** **componente** `Wrapper` **con la** **prop** `msg` **que se le ha pasado**.

En la declaración de función del componente `Wrapper`, hay un `h2` que dice `"Wrapper here"`, además de la renderización del componente `Button`, que también recibe el atributo `msg`.

Por último, la declaración de función del componente `Button` está codificada para recibir el objeto `props` y, a continuación, dentro de la envoltura `div`, mostrar un `h3`. En `h3` se lee `"Este es el componente Button"` y, debajo, hay un elemento `button` con un atributo `onClick` `event-handling`. Esto se pasa a una función de flecha que debe alertar a la cadena que viene del atributo `props.msg`.

El mensaje de la alerta dice `"He pasado por el Encabezado y la Envoltura y he llegado al componente Botón"`.

Eso es realmente todo lo que hay que hacer. Perforar objetos de utilería significa simplemente pasar un objeto de utilería a través de varias capas de componentes. Cuantas más capas haya, más repetitivo e innecesario parecerá esto. Hay varias maneras de lidiar con esto, como aprenderá en los elementos de la lección que siguen.