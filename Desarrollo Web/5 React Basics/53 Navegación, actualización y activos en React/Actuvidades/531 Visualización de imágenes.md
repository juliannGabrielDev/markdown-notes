---
Fecha: 2024-12-21
Categoría: Uso de activos en React
tags:
  - front-end
  - curso-5
  - modulo-3
---
# **Tarea**

En este laboratorio no calificado, su objetivo es agregar una imagen de la carpeta **assets** que ya ha sido agregada a la carpeta **src**. La imagen debe agregarse en el componente `App`, bajo el encabezado `h1`, dentro de la declaración `return`.

```jsx
import logo from "./assets/logo.img"

function App() {

  return (
    <div className="App">
      <h1>Task: Add an image below</h1>
      <img src={logo} alt="Logo" />
    </div>
  );
}

export default App;
```