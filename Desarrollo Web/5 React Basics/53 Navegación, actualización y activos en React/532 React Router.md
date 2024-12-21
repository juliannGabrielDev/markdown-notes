---
Fecha: 2024-12-20
Categoría: Enlaces y enrutamiento
tags:
  - front-end
  - curso-5
  - modulo-3
---
## **Pasos**
---
Instalar la librería `react-router-dom`

```shell
npm i react-router-dom@6
```

Importar el enrutador del navegador de `react-router-dom` en el archivo `index.js` (`main.jsx` en algunos casos)

```jsx
import { BrowserRouter } from 'react-router-dom'
```

Una vez importado, necesitamos envolver el elemento jsx de la aplicación dentro del enrutador del navegador en el archivo `index.js`

```jsx
createRoot(document.getElementById('root')).render(
	<StrictMode>
		<BrowserRouter>
			<App />
		</BrowserRouter>
	</StrictMode>
)
```

Importamos `Routes`, `Route` y `Link` en el archivo `App.jsx`

```jsx
import {Routes, Route, Link} from "react-router-dom";
```

Listo, ya podemos comenzar a usar `react-router-dom`. Aquí tienes el código completo:

```jsx
import { Routes, Route, Link } from "react-router-dom";
import Contact from "./Contact";
import Home from "./Home";

function App() {
  return (
    <div>
      <nav>
        <Link to="/">Homepage</Link>
        <Link to="/contact">Contact</Link>
      </nav>

      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/contact" element={<Contact />} />
      </Routes>
    </div>
  )
}

export default App;
```