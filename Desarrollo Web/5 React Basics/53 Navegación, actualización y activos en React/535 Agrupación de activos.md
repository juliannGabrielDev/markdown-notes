---
Fecha: 2024-12-21
Categoría: Uso de activos en React
tags:
  - front-end
  - curso-5
  - modulo-3
---
Anteriormente, aprendió qué son los activos en React y las mejores prácticas para almacenarlos en las carpetas de su proyecto.

En esta lectura, aprenderá sobre las ventajas y desventajas de incrustar activos, incluyendo ejemplos de activos del lado cliente/servidor. También aprenderá acerca de las ventajas y desventajas inherentes al uso de aplicaciones con muchos activos.

Es probable que los archivos de la aplicación se agrupen cuando se trabaja con una aplicación React. ==La agrupación es un proceso que toma todos los archivos importados de una aplicación y los une en un único archivo, denominado **paquete**==. Varias herramientas pueden realizar este bundling. Dado que, en este curso, ha utilizado el `create-react-app` para construir varias aplicaciones React, se centrará en webpack. Esto se debe a que webpack es la herramienta incorporada en `create-react-app`.

Empecemos explicando qué es webpack y por qué lo necesita.

En pocas palabras, webpack es un agrupador de módulos.

En la práctica, esto significa que tomará varios tipos de archivos, como archivos SVG y de imagen, archivos CSS y SCSS, archivos JavaScript y archivos TypeScript, y los empaquetará juntos para que un navegador pueda entender ese paquete y trabajar con él.

¿Por qué es importante?

Cuando construya sitios web, probablemente podría prescindir de webpack ya que la estructura de su proyecto podría ser sencilla: podría tener una única biblioteca CSS, como Bootstrap, cargada desde una **CDN (red de distribución de contenidos)**. También podría tener un único archivo JavaScript en su documento HTML estático. Si eso es todo, no necesita utilizar webpack en tal escenario.

Sin embargo, el desarrollo web moderno puede volverse complejo.

He aquí un ejemplo de las primeras líneas de código en un único archivo de una aplicación React:

```jsx
import React from 'react';
import '@atlaskit/css-reset';
import styled from 'styled-components';
import './index.css';
import { ThemeProvider } from './contexts/theme';
import { DragDropContext } from 'react-beautiful-dnd';
import { BrowserRouter as Router, Route, Switch } from 'react-router-dom';
import Nav from './components/Nav';
import data from './data';
import Loading from './components/Loading';
```

Las importaciones aquí son de bibliotecas y recursos ficticios porque las bibliotecas específicas no son necesarias. Todas estas importaciones diferentes pueden ser de varios tipos de archivos: .js, .svg, .css, etc.

A su vez, todos los archivos importados pueden tener sus propios archivos importados, e incluso éstos pueden tener sus importaciones.

Esto significa que, dependiendo de otros archivos, todos estos archivos pueden crear un **gráfico de dependencias**. El orden en el que se cargan todos estos archivos es esencial. Ese gráfico de dependencias puede llegar a ser tan complejo que resulte casi imposible para un humano estructurar un proyecto complejo y agrupar todas esas dependencias adecuadamente.

Esta es la razón por la que se necesitan herramientas como webpack.

Así, webpack construye un gráfico de dependencias y agrupa los módulos en uno o más archivos que un navegador puede consumir.

Mientras hace eso, también hace lo siguiente:

- Convierte el código JS moderno - que sólo puede ser entendido por los navegadores modernos - en versiones antiguas de JavaScript para que los navegadores más antiguos puedan entender su código. Este proceso se conoce como _transpilar_. Por ejemplo, puede transpilar código ES7 a código ES5 utilizando webpack.

- Optimiza su código para que se cargue lo más rápidamente posible cuando un usuario visita sus páginas web.

- Puede procesar su código SCSS en el CSS normal, que los navegadores pueden entender.

- Puede construir mapas de código fuente de los bloques de construcción del paquete.

- Puede producir varios tipos de archivos basados en reglas y plantillas. Esto incluye archivos HTML, entre otros.

Otra característica significativa de webpack es que ayuda a los desarrolladores a crear aplicaciones web modernas.

Le ayuda a conseguirlo utilizando dos modos: modo de **producción** o modo de **desarrollo** .

En el modo de **desarrollo**, webpack agrupa sus archivos y optimiza sus agrupaciones para las actualizaciones, de modo que cualquier actualización de cualquiera de los archivos de su aplicación desarrollada localmente se vuelve a agrupar rápidamente. También construye mapas de fuentes para que pueda inspeccionar el archivo original incluido en el código empaquetado.

En el modo de **producción**, webpack empaqueta sus archivos para que estén optimizados para la velocidad. Esto significa que los archivos se minifican y organizan para que ocupen la menor cantidad de memoria posible. Por lo tanto, están optimizados para la velocidad porque estos paquetes se descargan rápidamente cuando un usuario visita el sitio web en línea.

Una vez que todos los archivos fuente de su aplicación se han agrupado en un único archivo bundle, ese único archivo bundle se sirve a un visitante que navegue por la versión en vivo de su aplicación en línea, y todo el contenido de la aplicación se sirve a la vez.

Esto funciona muy bien para las aplicaciones más pequeñas, pero si tiene una aplicación más extensa, es probable que este enfoque afecte a la velocidad de su sitio. Cuanto más tarde en cargarse una aplicación web, más probable será que el visitante la abandone y se dirija a otro sitio web no relacionado. Hay varias formas de abordar este problema de un paquete grande.

Una de ellas es la división del código, una práctica en la que un agrupador de módulos como webpack divide el archivo de un único paquete en varios paquetes, que luego se cargan en función de las necesidades. Con la ayuda del code-splitting, puede **cargar perezosamente** sólo las partes que el visitante de la aplicación necesita tener en un momento dado. Este enfoque reduce significativamente los tiempos de descarga y permite que las aplicaciones impulsadas por React obtengan velocidades mucho mejores.

Existen otras formas de abordar estos problemas.

Un ejemplo de alternativa viable es SSR (Server-side rendering).

Con SSR, los componentes de React se renderizan en HTML en el servidor, y el visitante descarga el código HTML terminado. Una alternativa a SSR es la renderización del lado del cliente, que descarga el archivo index.html y luego deja que React inyecte su propio código en un elemento HTML dedicado (el elemento **raíz** en create-react-app). En este curso, sólo ha trabajado con el renderizado del lado del cliente.

A veces, puede combinar el renderizado del lado del cliente y el renderizado del lado del servidor. Este enfoque da como resultado lo que se conoce como **aplicaciones isomórficas**.

En esta lectura, usted aprendió acerca de las ventajas y desventajas de incrustar activos, incluyendo ejemplos de activos del lado cliente/servidor. También aprendió sobre las compensaciones inherentes al uso de apps con muchos activos.