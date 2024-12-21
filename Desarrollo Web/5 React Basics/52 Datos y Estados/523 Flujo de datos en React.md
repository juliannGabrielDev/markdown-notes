---
Fecha: 2024-12-20
Categoría: Datos y eventos
tags:
  - front-end
  - curso-5
  - modulo-2
---
Acaba de aprender cómo puede establecerse la relación padre-hijo para que los datos fluyan de padre a hijo.

En esta lectura, aprenderá a detallar el flujo de datos de padre a hijo. A continuación, aprenderá por qué las muestras de código deben ser claras y concisas. Por último, explorará el flujo de datos con más detalle mediante más ejemplos. Esto le servirá para refrescar los conocimientos adquiridos en cursos anteriores.

## **1 Flujo de datos padre-hijo**
---
En React, el flujo de datos es unidireccional. A veces se dice que el flujo de datos es unidireccional. Dicho de otro modo, los datos en React fluyen de un componente padre a un componente hijo. El flujo de datos comienza en la raíz y puede fluir a múltiples niveles de anidamiento, desde el componente raíz (componente padre) al componente hijo, luego al componente nieto, y más abajo en la jerarquía.

Una aplicación React consta de muchos componentes, organizados como un árbol de componentes. Los datos fluyen desde el componente raíz a todos los componentes de la estructura de árbol que requieren estos datos, utilizando props.

Los props son inmutables (no se pueden cambiar).

Los dos principales beneficios de este flujo de datos unidireccional son que permite a los desarrolladores

1. comprender la lógica de las aplicaciones React más rápidamente y

2. simplificar el flujo de datos.

He aquí un ejemplo práctico de esto:

Imagine que el componente padre pasa una prop (nombre) al componente hijo. El componente hijo utiliza entonces esta prop para renderizar el nombre en la UI.

## **2 Componente padre:**
---
```jsx
function Dog() {
    return (
        <Puppy name="Max" bowlShape="square" bowlStatus="full" />
    );
};
```

## **3 Componente hijo:**
---
```jsx
function Puppy(props) {
    return (
        <div>
            {props.name} has <Bowl bowlShape="square" bowlStatus="full" />
        </div>
    );
};
```

## **4 Componente nieto:**
```jsx
function Bowl(props) {
    return (
        <span>
            {props.bowlShape}-shaped bowl, and it's currently {props.bowlStatus}
        </span>
    );
};
```

Hacer que los datos se muevan a través de las props en una sola dirección hace que sea más sencillo entender la lógica de cómo interactúan los componentes. Si los datos se movieran por todas partes, todo el tiempo, entonces sería mucho más difícil comprender su flujo lógico. Cualquier optimización que intentara implementar probablemente no sería todo lo eficiente que podría ser, especialmente en el React moderno.