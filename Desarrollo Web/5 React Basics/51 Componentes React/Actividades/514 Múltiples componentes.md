---
Fecha: 2024-12-20
Categoría: Uso y estilo de los componentes
tags:
  - front-end
  - curso-5
  - modulo-1
---
Ha aprendido que los componentes de React permiten la **modularidad** y la **reutilización** con la ==capacidad de hacer que los datos sean más dinámicos pasándolos del padre al hijo== mediante accesorios. 

En este ejercicio renderizará un componente varias veces para practicar el uso de diferentes accesorios y observar qué significa exactamente "reutilizar" componentes.

Aquí está el archivo App.js completado:

```jsx
import "./App.css";
import Card from "./Card";

function App() {
return (
    <div className="App">
        <h1>Task: Add three Card elements</h1>
        <Card h2="First card's h2" h3="First card's h3" />
        <Card h2="Second card's h2" h3="Second card's h3" />
        <Card h2="Third card's h2" h3="Third card's h3" />
    </div>
  );
};

export default App;
```

Aquí está el archivo Card.js completado:

```jsx
function Card(props) {
    return (
        <div className="card">
            <h2>{props.h2}</h2>
            <h3>{props.h3}</h3>
        </div>
    );
};

export default Card;
```