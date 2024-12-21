---
Fecha: 2024-12-19
Categoría: Introducción al curso
tags:
  - front-end
  - curso-5
  - modulo-1
---
Los módulos pueden ayudarle a guardar y acceder a su código de una manera más estructurada, y en esta lectura, usted aprenderá acerca de algunos conceptos fundamentales de trabajar con módulos de JavaScript.

Este conocimiento es crucial para entender la sintaxis y la lógica detrás de cómo se arman las aplicaciones React de ejemplo en este curso.

Esta lectura cubrirá los tres conceptos principales:

1. Módulos JavaScript
2. Exportación de módulos
3. Importación de módulos

## **1 Módulos JavaScript**
---
En JavaScript, un módulo **es simplemente un archivo**.

El propósito de un módulo es tener un código más modular, en el que pueda trabajar con archivos más pequeños, e importarlos y exportarlos para que las aplicaciones que construya sean más personalizables y tengan más partes componibles.

Un módulo puede ser tan simple como una sola función en un archivo separado.

Considere la siguiente declaración de función:

```js
function addTwo(a, b) {
	console.log(a + b);
}
```

Digamos que tiene un archivo llamado **addTwo.js** que sólo contiene el código anterior.

¿Cómo convertiría este archivo en un módulo JavaScript?

Todo lo que tendría que hacer para convertirlo en un módulo JavaScript es utilizar la sintaxis de exportación.

## 2 Exportación de módulos
---
Hay más de una forma de exportar un módulo en JavaScript.

Aunque no se enumeran todas las diferencias sintácticas, a continuación se presentan algunos ejemplos que cubrirán todas las formas en que se realizará la importación y exportación de módulos JavaScript en este curso.

En general, existen dos formas de exportar módulos en JavaScript:

1. Utilizando exportaciones por defecto
2. Utilizando exportaciones con nombre

### **2.1 Exportaciones por defecto**

Puede tener una **exportación por defecto** por cada módulo JavaScript.

Utilizando el archivo **addTwo.js** anterior como ejemplo, aquí hay dos maneras de realizar una exportación por defecto:

```js
export default function addTwo(a, b) {
	Console.log(a + b);
}
```

Así, en el ejemplo anterior, está añadiendo las palabras clave `export default` delante de la declaración de la función `addTwo`.

He aquí una sintaxis alternativa:

```js
function addTwo(a, b) {
	console.log(a + b);
}

export default addTwo;
```

### **2.2 Exportaciones nombradas**

Las exportaciones con nombre son una forma de exportar sólo ciertas partes de un archivo JavaScript determinado.

A diferencia de las exportaciones por defecto, puede exportar tantos elementos de cualquier archivo JavaScript como desee.

En otras palabras, sólo puede haber una exportación por defecto, pero tantas exportaciones con nombre como desee.

Por ejemplo:

```js
function addTwo(a, b) {
	console.log(a + b);
}

function addThree(a, b, c) {
	console.log(a + b + c);
}
```

Si desea exportar las funciones `addTwo` y `addThree` como exportaciones con nombre, una forma de hacerlo sería la siguiente:

```js
function addTwo(a, b) {
	console.log(a + b);
}

function addThree(a, b, c) {
	console.log(a + b + c);
}

export { addTwo, addThree };
```

## **3 Importar módulos**
---
Al igual que al exportar módulos en JavaScript, existen varias formas de importarlos.

La sintaxis exacta depende de cómo se exportó el módulo.

Digamos que tiene dos módulos en una carpeta.

El primer módulo es **addTwo.js** y el segundo módulo es **mathOperations.js**.

Usted desea importar el módulo **addTwo.js** al módulo **mathOperations.js**.

### **3.1 Importar un módulo que se exportó por defecto**

Considere el ejemplo anterior de exportar la función addTwo como módulo por defecto:

```js
function addTwo(a, b) {
	console.log(a + b);
}

export default addTwo;
```

Para importarla al módulo **mathOperations .js**, podría utilizar la siguiente sintaxis:

```js
import addTwo from "./addTwo";
```

Así, podría comenzar esta importación con la palabra clave `import` y, a continuación, el nombre con el que utilizará este código importado dentro del archivo **mathOperations.js**. A continuación, escribiría la palabra clave `from`, y por último la ubicación del archivo, _sin la extensión .js_.

Contraste la importación anterior de la función por defecto `addTwo export` con la diferente sintaxis de importación si la función `addTwo` fuera en cambio una exportación con nombre:

```js
import { addTwo } from "./addTwo";
```

## **Conclusión**
---
En esta lectura, ha aprendido lo más básico sobre qué son los módulos en JavaScript, por qué se utilizan y cómo se exportan e importan.

Los ejemplos que ha visto aquí son el núcleo de cómo tratará las importaciones y exportaciones de varios módulos en las aplicaciones React de ejemplo de este curso.

Sin embargo, tenga en cuenta que hay muchas más advertencias, reglas e implementaciones del trabajo con módulos en JavaScript. Los ejemplos dados en esta lectura están ahí sólo para facilitar la comprensión de lo que está sucediendo en las aplicaciones React que construirá en este curso. La intención de esta lectura era sólo para que se familiarice con la sintaxis más común utilizada - no como una visión completa de los módulos en JavaScript.