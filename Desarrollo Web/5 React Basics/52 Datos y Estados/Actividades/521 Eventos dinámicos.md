---
Fecha: 2024-12-20
Categoría: Eventos dinámicos y cómo manejarlos
tags:
  - front-end
  - curso-5
  - modulo-1
---
## **Tarea**
---
Cuando un usuario interactúa con tu aplicación React está desencadenará eventos. Ya has aprendido a manejar eventos generados por el usuario así que ahora puedes reforzar lo que has aprendido practicando el manejo de eventos. Para hacerlo más divertido en este ejercicio construirás un sencillo juego de adivinar números.

Aquí está el archivo **App.js** completado:

```jsx
function App() {

  function handleClick() {
    let randomNum = Math.floor(Math.random() * 3) + 1;
    console.log(randomNum);
    let userInput = prompt('type a number');
    alert(`Computer number: ${randomNum}, Your guess: ${userInput}`);
  }

  return (
    <div>
      <h1>Task: Add a button and handle a click event</h1>
      <button onClick={handleClick}>Guess the number between 1 and 3</button>
    </div>
  );
}

export default App;
```