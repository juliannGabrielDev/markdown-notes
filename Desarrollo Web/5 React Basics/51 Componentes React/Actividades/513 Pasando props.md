---
Fecha: 2024-12-20
Categoría: Uso y estilo de los componentes
tags:
  - front-end
  - curso-5
  - modulo-1
---
En este laboratorio, va a crear un componente con un simple texto "Hola, ----". Si sabe de antemano que siempre va a estar saludando a "Bob", entonces podría simplemente codificar el nombre "Bob" en su componente.pero, ¿y si el nombre de la persona a la que está diciendo "hola" puede cambiar? ¿O si quiere decir "hola" a varias personas diferentes en distintos lugares de su aplicación? En estos casos, codificar un nombre no funcionaría muy bien. En su lugar, necesitará crear un componente que utilice props para pasar estos datos de nombre.

Aquí está el archivo **App.js** completado:

```jsx
import Heading from "./Heading";

function App() {
  return (
    <div className="App">
      <Heading firstName="Bob" />
      <Heading firstName="Juliann" />
      <Heading firstName="Alejandro" />
    </div>
  );
}

export default App;
```

Y aquí está el archivo **Heading.js** completado:

```jsx
function Heading(props) {
    return (
        <h1>Hello, {props.firstName}</h1>
    )
}

export default Heading;
```