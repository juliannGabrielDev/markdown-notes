---
Fecha: 2024-12-20
Categoría: Los componetes de React y dónde viven
tags:
  - front-end
  - curso-5
  - modulo-1
---
Crear el componete `Heading` e importarlo en el componete `App`.

Aquí está el contenido del archivo **Heading.js**:

```jsx
function Heading() {
    return (
        <h1>This is an h1 heading</h1>
    )
}

export default Heading;
```

Aquí está el contenido del archivo **App.js**:

```jsx
import Heading from "./Heading";

function App() {
  return (
    <div className="App">
      <Heading />
    </div>
  );
}

export default App;
```