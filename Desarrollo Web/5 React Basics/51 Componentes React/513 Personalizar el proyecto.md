---
Fecha: 2024-12-20
Categoría: Los componetes de React y dónde viven
tags:
  - front-end
  - curso-5
  - modulo-1
---
Hasta ahora, ha aprendido sobre los componentes de React, pero ahora se centrará en aprender a personalizar el proyecto. Conocerá el enfoque de desarrollo del software, detallando la creación de archivos asociados independientes, la recopilación de requisitos y la posterior estructura de carpetas que se creará.

## **1 Creación de un diseño**
---
Imagine que se le ha encomendado la tarea de construir un diseño de sitio web algo más complejo utilizando React.

En este punto, aún no sabe demasiado sobre cómo funciona React, pero incluso con sus limitados conocimientos, puede construir algunos diseños relativamente interesantes.

En este momento, necesita construir un diseño sencillo centrado en la tipografía para un blog de codificación.

Esto significa que no tendrá que utilizar imágenes, lo que simplifica significativamente su tarea.

El diseño que debe construir constará de las siguientes secciones:

- Navegación principal
- Promo (anuncio principal)
- Una lista de avances de las entradas más recientes (intros)
- El pie de página

## **2 Cómo organizar su código**
---
Teniendo en cuenta la estructura anterior, ¿cómo organizaría su código?

Aquí es donde los documentos de React pueden ayudar. Sugieren dos enfoques:

1. Agrupación por características
2. Agrupación por tipo de archivo

También aconsejan no anidar las carpetas demasiado profundo, y mantener las cosas simples y no pensar demasiado en ello.

Incluso dicen que si está empezando, no debería pasar más de cinco minutos configurando un proyecto.

Teniendo en cuenta este consejo, se podría decir que para un proyecto pequeño como este, podría mantenerlo tan simple como simplemente añadir una carpeta de **componentes** y mover todos sus componentes a ella. Esto es exactamente lo que hará a continuación.

## **3 Construyendo la aplicación**
---
Dado que esta aplicación se centra en la personalización, vamos a llamarla **customizing-example**.

Lo que sigue es el comando que debe ejecutar **en una carpeta adecuada de su propio ordenador**. Por "una carpeta adecuada" me refiero a "una carpeta en la que se sienta cómodo instalando una aplicación React boilerplate". Esto también incluye que la carpeta que elija deberá ser accesible para su usuario en su SO (Sistema Operativo).

```shell
npm init react-app customizing-example
```

Esto producirá una nueva aplicación de inicio con una estructura familiar.

Inspeccionando la carpeta **src** de la aplicación de inicio, tiene este aspecto:

```
src/
    App.js
    App.test.js
    index.css
    index.js
    logo.svg
    reportWebVitals.js
    setupTests.js
```

A continuación, sólo tiene que añadirle una carpeta components, así:

```
src/
    components/
    App.js
    App.test.js
    index.css
    index.js
    logo.svg
    reportWebVitals.js
    setupTests.js
```

Dado que la carpeta components está actualmente vacía, puede añadir un componente para cada una de las secciones del blog centrado en la tipografía. Esta es la actualización estructural:

```
src/
    components/
        Nav.js
        Promo.js
        Intro1.js
        Intro2.js
        Intro3.js
        Footer.js
    App.js
    App.test.js
    index.css
    index.js
    logo.svg
    reportWebVitals.js
    setupTests.js
```

En este punto, no hay necesidad de complicar las cosas. Tiene el componente **Nav**, el componente **Promo**, el componente **Intro1**, **Intro2** y el componente **Intro3**. Por último, también hay un componente **Footer.js**.

Esto significa que ha planificado completamente la aplicación, basándose en algunas de las mejores prácticas sugeridas por el sitio web oficial de React docs, y basándose en el nivel de complejidad del propio proyecto. Dado que este proyecto es relativamente sencillo, esta estructura le parece correcta.

En esta lectura, simplemente construirá todos los componentes dentro de la carpeta components, y luego, en los próximos elementos de la lección, los importará en el archivo **App.js**.

## **4 Construir componentes**
---
Por ahora, vamos a construir los componentes. Después de haber añadido la carpeta de **componentes**, también ha añadido todos los archivos de componentes funcionales. Dado que todos ellos están actualmente vacíos, puede empezar a añadirlos, uno por uno.

Aquí tiene el contenido del archivo **Nav.js**:

```jsx
function Nav() {
    return (
        <nav className="main-nav">
            <ul>
                <li>Home</li>
                <li>Articles</li>
                <li>About</li>
                <li>Contact</li>
            </ul>
        </nav>
    );
};
export default Nav;
```

A continuación, puede centrarse en el archivo **Promo.js**:

```jsx
function Promo() {
	return (
        <div className="promo-section">
            <div>
                <h1>Don't miss this deal!</h1>
                </div>
                <div>
                <h2>Subscribe to my newsletter and get all the shop items at 50% off!</h2>
            </div>
        </div>
    );
};
export default Promo;
```

Una vez que haya terminado la sección promocional, puede centrarse en los componentes Intro.

Aquí está **Intro1.js**:

```jsx
function Intro1() {
    return (
        <div className="blog-post-intro">
            <h2>I've become a React developer!</h2>
            <div>
                <p>I've completed the React Basics course and I'm happy to announce that I'm now a Junior React Developer!</p>
                <p className="link">Read more...</p>
            </div>
        </div>
    );
};

export default Intro1;
```

Aquí está el código del componente **Intro2.js**:

```jsx
function Intro2() {
    return (
        <div className="blog-post-intro">
            <h2>Why I love front-end web development</h2>
            <div>
                <p>In this blog post, I'll list 10 reasons why I love to work as a front-end developer.</p>
                <p className="link">Read more...</p>
            </div>
        </div>
    );
};

export default Intro2;
```

Puede terminar las vistas previas de las entradas de mi blog con el código del componente **Intro3.js**:

```jsx
function Intro3() {
    return (
        <div className="blog-post-intro">
            <h2>What's the best way to style your React apps?</h2>
            <div>
                <p>There are so many options to choose from. Here's a high-level overview of the popular ones.</p>
                <p className="link">Read more...</p>
            </div>
        </div>
    );
};

export default Intro3;
```

Sólo queda una cosa más por codificar, el componente **Pie de página**, así que aquí está:

```jsx
function Footer() {
    return (
        <div className="copyright">
            <p>Made with love by Myself</p>
        </div>
    );
};

export default Footer;
```

Ahora que ha completado todos los componentes para la aplicación, aquí hay algunas cosas más interesantes sobre la sintaxis.

Estas son:

- El uso del atributo `className` en JSX
- El uso de componentes separados para el código repetitivo
- ¿Dónde están todos los props?
- ¿Por qué no utilizaba el elemento `<a>` para los enlaces vacíos?

## **5 Discutiendo la sintaxis**
---
Ahora vamos a discutir brevemente los cuatro puntos anteriores.

¿Por qué utilizar el atributo `className` en la sintaxis JSX?

Bueno, con JSX, se parece tanto a HTML que es fácil olvidar que en realidad es código JavaScript, no HTML.

Mientras que el HTML normal tiene efectivamente un atributo `class`, que se utiliza para enumerar una o más clases CSS que se utilizarán en un elemento HTML dado, esto no puede funcionar realmente en JSX. La razón es que JSX es un tipo especial de sintaxis JavaScript, y la palabra `class` es una palabra clave reservada en JSX. Por eso el equipo de React tuvo que llegar a un compromiso y así `className` se utiliza en JSX para listar una o más clases CSS a utilizar en un elemento o componente dado.

Pero, ¿por qué utilizar **Intro1.js, Intro2.js** e **Intro3.js**? ¿No es uno de los principios de la codificación el enfoque DRY, es decir, el enfoque "No te repitas"?

Efectivamente, lo es. Sin embargo, aún quedan algunos conceptos por discutir antes de aprender a reutilizar un mismo componente con variaciones en su contenido. Esto tiene que ver con los datos en los componentes, pero no se preocupe, llegaremos a eso más adelante.

La tercera pregunta es sobre el objeto **props**. Se ha mencionado antes, pero hasta ahora no se ha utilizado. Tampoco se ha utilizado en este ejemplo.

La respuesta a esta pregunta tiene que ver con la siguiente lección, titulada _**Uso y estilo de los componentes**_. En esta lección, verá en la práctica cómo puede hacer que los componentes funcionen mejor, con la ayuda de **accesorios**.

La última pregunta se refiere a no utilizar el elemento `<a>` para los enlaces vacíos de mi aplicación.

La respuesta aquí depende de si esos enlaces son "internos" -dentro de una app, o "externos", es decir, que llevan a algún enlace externo, como [_https://www.coursera.org._](https://www.coursera.org/) Si los enlaces son internos a la app - como se prevé aquí - usar la etiqueta `<a>` simplemente no es la forma React de hacer las cosas. Aprenderá por qué es así cuando hablemos del uso de React Router.

## Conclusión

Habiendo terminado esta lectura, ahora ha aprendido sobre el enfoque de desarrollo de software, detallando la creación de archivos asociados separados, la recopilación de requisitos, y la posterior estructura de carpetas a crear.