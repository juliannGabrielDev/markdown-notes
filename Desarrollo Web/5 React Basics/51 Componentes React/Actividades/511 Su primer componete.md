---
Fecha: 2024-12-19
Categoría: Los componetes de React y dónde viven
tags:
  - front-end
  - curso-5
  - modulo-1
---
# Tarea
---
Ha aprendido que puede agregar otro componente dentro del componente App, y luego renderizar ese nuevo componente dentro de la Sentencia de retorno del componente App.

En este ejercicio, practicará cómo hacerlo.

```jsx
​function Heading() {
	return (
		<h1>This is an h1 heading</h1>
	)
}

function App() {
	return (
		<div className="App">
			This is the starting for "Your first component" ungraded lab
			<Heading />
		</div>
	);
}

export default App;
```