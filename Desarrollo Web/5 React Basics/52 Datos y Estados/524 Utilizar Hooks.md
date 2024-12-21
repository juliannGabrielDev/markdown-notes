---
Fecha: 2024-12-20
Categoría: Datos y eventos
tags:
  - front-end
  - curso-5
  - modulo-2
---
Ahora que entiende qué son los hooks en React y tiene unos conocimientos básicos sobre el hook `useState`, vamos a profundizar un poco más. En esta lectura, aprenderá a utilizar hooks en componentes React y comprenderá los casos de uso del hook `useState`.

Supongamos que tiene un componente con un campo de texto de entrada. El usuario puede escribir en este campo de texto. El componente necesita hacer un seguimiento de lo que el usuario teclea dentro de este campo de texto. Puede añadir estado y utilizar el gancho `useState`, para mantener la cadena.

A medida que el usuario sigue tecleando, el estado local que mantiene la cadena necesita actualizarse con el último texto que se ha tecleado.

Analicemos el siguiente ejemplo.

```jsx
import { useState } from 'react';

export default function InputComponent() { 
  const [inputText, setText] = useState('hello'); 

  function handleChange(e) { 
    setText(e.target.value); 
  } 

  return ( 
    <> 
      <input value={inputText} onChange={handleChange} /> 
      <p>You typed: {inputText}</p> 
      <button onClick={() => setText('hello')}> 
        Reset 
      </button> 
    </> 
  ); 
} 
```

Para ello, definamos un componente React y llamémoslo InputComponent_._ Este componente renderiza tres cosas:

- Un campo de texto de entrada

- El texto que se ha introducido en el campo

- Un botón de reinicio para devolver el campo a su estado por defecto

A medida que el usuario empieza a escribir en el campo de texto, también se muestra el texto que se ha escrito.

La variable de estado `inputText` y el método `setText` se utilizan para establecer el texto actual que se teclea. El hook `useState` se inicializa al principio del componente.

```jsx
const[inputText, setText] = useState('hello');
```

Por defecto, el inputText se fijará en `"hello"`.

A medida que el usuario teclea, la función `handleChange`, lee el último valor de entrada del elemento DOM de entrada del navegador, y llama a la función `setText`, para actualizar el estado local de `inputText`.

```jsx
function handleChange(e) {
    setText(e.target.value);
};
```

Finalmente, al pulsar el botón de reinicio, `inputText` se actualizará de nuevo a `"hello"`.

¿No es genial?

Tenga en cuenta que el `inputText` aquí es estado local y es local al `InputComponent`. Esto significa que fuera de este componente, `inputText` no está disponible y es desconocido. En React, el estado siempre se refiere al estado local de un componente.

Los hooks también vienen con un conjunto de reglas, que usted necesita seguir mientras los usa. Esto se aplica a todos los hooks React, incluyendo el hook `useState` que acaba de aprender.

- Sólo puede llamar a hooks en el nivel superior de su componente o a sus propios hooks.

- No puede llamar hooks dentro de bucles o condiciones.

- Sólo puede llamar a hooks desde funciones React, y no desde funciones JavaScript normales.

Para demostrarlo, ampliemos el ejemplo anterior, para incluir tres campos de texto de entrada dentro de un único componente. Esto podría ser un formulario de registro con campos para el nombre, apellido y correo electrónico.

```jsx
import { useState } from 'react'; 

export default function RegisterForm() { 
  const [form, setForm] = useState({ 
    firstName: 'Luke', 
    lastName: 'Jones', 
    email: 'lukeJones@sculpture.com', 
  }); 

  return ( 
    <> 
      <label> 
        First name: 
        <input 
          value={form.firstName} 
          onChange={e => { 
            setForm({ 
              ...form, 
              firstName: e.target.value 
            }); 
          }} 
        /> 
      </label> 
      <label> 
        Last name: 
        <input 
          value={form.lastName} 
          onChange={e => { 
            setForm({ 
              ...form, 
              lastName: e.target.value 
            }); 
          }} 
        /> 
      </label> 
      <label> 
        Email: 
        <input 
          value={form.email} 
          onChange={e => { 
            setForm({ 
              ...form, 
              email: e.target.value 
            }); 
          }} 
        /> 
      </label> 
      <p> 
        {form.firstName}{' '} 
        {form.lastName}{' '} 
        ({form.email})
      </p> 
    </> 
  ); 
} 
```

Observe que está utilizando un objeto `form` para almacenar el estado de los tres valores de los campos de entrada de texto:

```jsx
const[form, setForm] =useState({
firstName:'Luke',
lastName:'Jones',
    email:'lukeJones@sculpture.com',
});
```

No necesita tener tres variables de estado separadas en este caso, y en su lugar puede consolidarlas todas juntas en un objeto `form` para una mejor legibilidad.

Además del gancho `useState`, hay otros hooks que resultan útiles, como `useContext`, `useMemo`, `useRef`, _etc_ . Cuando necesite compartir la lógica y reutilizar la misma lógica en varios componentes, puede extraer la lógica en un hook personalizado. Los hooks personalizados ofrecen flexibilidad y pueden utilizarse para una amplia gama de casos de uso, como el manejo de formularios, animaciones, temporizadores y muchos más.

A continuación, le explicaré cómo funciona el gancho `useRef`.

## **El gancho useRef**
---
Utilizamos el hook `useRef` para acceder directamente a un elemento hijo.

Cuando invoque el hook `useRef`, éste devolverá un objeto `ref`. El objeto `ref` tiene una propiedad llamada `current`.

```jsx
import { useRef } from 'react';

function TextInputWithFocusButton() {
  // Creamos una referencia para el elemento de entrada de texto
  const inputEl = useRef(null);

  // Función que se ejecuta al hacer clic en el botón
  const onButtonClick = () => {
    // `current` apunta al elemento de entrada de texto montado
    inputEl.current.focus(); // Colocamos el foco en el input
  };

  return (
    <>
      {/* Campo de texto */}
      <input 
        // Asignamos la referencia al input para poder acceder a él más tarde
        ref={inputEl} 
        type="text" 
      />

      {/* Botón para enfocar el input */}
      <button onClick={onButtonClick}>Focus the input</button>
    </>
  );
}
```

Utilizando el atributo ref en el elemento de entrada, puedo entonces acceder al valor actual e invocar el método `focus()` sobre él, enfocando así el campo de entrada.

Hay situaciones en las que es necesario acceder directamente al DOM, y aquí es donde entra en juego el hook `useRef`.

## Conclusión

En esta lectura, ha explorado los hooks en detalle y comprende cómo utilizar el hook `useState` para mantener el estado dentro de un componente. Usted también entiende los beneficios del uso de ganchos dentro de un componente React.