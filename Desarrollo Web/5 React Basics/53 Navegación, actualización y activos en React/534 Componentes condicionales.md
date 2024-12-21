---
Fecha: 2024-12-21
Categoría: Enlaces y enrutamiento
tags:
  - front-end
  - curso-5
  - modulo-3
---
¿Alguna vez ha visitado un sitio web que requiriera una cuenta de usuario? Para iniciar sesión hace clic en un botón **Iniciar** sesión y, una vez que ha iniciado sesión, el botón **Iniciar sesión** cambia a un botón **Cerrar sesión**.

Esto se hace a menudo utilizando algo llamado renderizado condicional.

En un curso anterior, ya aprendió sobre condiciones simples utilizando declaraciones `if` y `switch`.

El uso de estas sentencias le permite cambiar el comportamiento del código en función de que se cumplan determinadas condiciones.

Por ejemplo, puede asignar a una variable un valor diferente en función del resultado de la comprobación de una condición.

```jsx
let name; 

if (Math.random() > 0.5) { 
    name = "Mike" 
} else { 
    name = "Susan" 
}
```

```jsx
let name; 
let newUser = true; 

if (Math.random() > 0.5 && newUser) { 
    name = "Mike" 
} else { 
    name = "Susan" 
}
```

La representación condicional se basa en el mismo principio. Mediante el uso de condiciones, puede devolver diferentes componentes hijos. Esto se hace a menudo utilizando los props que se pasan al componente padre, pero también puede hacerse basándose en el estado del componente.

Veamos un ejemplo sencillo.

Supongamos que tiene dos componentes hijos llamados `LoginButton` y `LogoutButton`; cada uno mostrando su botón correspondiente.

En el componente padre, llamado `LogInOutButton`, puede comprobar las props pasadas al componente padre y devolver un componente hijo diferente en función del valor de las props.

En este ejemplo, la props contiene una propiedad llamada `isLoggedIn`. Cuando ésta se establece en `true`, se devuelve el componente `LogoutButton`. En caso contrario, se devuelve el componente `LoginButton`.

```jsx
function LogInOutButton(props) {
const isLoggedIn = props.isLoggedIn;
  if (isLoggedIn) {
    return <LogoutButton />;
  } else {
  return <LoginButton />;
}
```

Entonces, cuando se utiliza el componente padre `LogInOutButton`, se puede pasar la props.

```jsx
<LogInOutButton isLoggedIn={false} />
```

Este es un ejemplo sencillo que muestra cómo puede cambiar lo que se muestra basándose en una comprobación de condiciones. Utilizará esto a menudo cuando desarrolle aplicaciones React.