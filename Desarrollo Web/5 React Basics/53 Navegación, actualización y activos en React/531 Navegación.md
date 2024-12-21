---
Fecha: 2024-12-20
Categoría: Enlaces y enrutamiento
tags:
  - front-end
  - curso-5
  - modulo-3
---
En esta lectura, conocerá las diferencias entre las páginas web tradicionales y las páginas web impulsadas por React (SPAs - single page applications).

Una vez que comprenda la diferencia entre estas dos formas de construir páginas web, podrá entender la diferencia necesaria entre cómo funciona la navegación en las aplicaciones web tradicionales frente a cómo funciona en las modernas páginas web SPA.

## **1 Antes de las Single-Page Apps**
---
Antes de la llegada de los modernos marcos JavaScript, la mayoría de los sitios web se implementaban como aplicaciones multipágina. Es decir, cuando un usuario hace clic en un enlace, el navegador navega a una nueva página web, envía una petición al servidor web; éste responde entonces con la página web completa y la nueva página se muestra en el navegador.

Esto puede hacer que su aplicación consuma muchos recursos del servidor web. El tiempo de CPU se gasta renderizando páginas dinámicas y el ancho de banda de la red se utiliza enviando páginas web enteras de vuelta por cada petición. Si su sitio web es complejo, puede parecer lento a sus usuarios, incluso más si tienen una conexión a Internet lenta o limitada.

Para resolver este problema, muchos desarrolladores web desarrollan sus aplicaciones web como *Single Page Applications*.

## **2 Aplicaciones de una sola página**
---
Usted utiliza muchas *Single Page Applications* cada día. Piense en su red social favorita, o en su proveedor de correo electrónico en línea, o en la aplicación de mapas que utiliza para encontrar negocios locales. Sus excelentes experiencias de usuario están impulsadas por las Aplicaciones de Página Única.

Una Aplicación de Página Única permite al usuario interactuar con el sitio web sin descargar nuevas páginas web enteras. En su lugar, reescribe la página web actual a medida que el usuario interactúa con ella. El resultado es que la aplicación resultará más rápida y receptiva para el usuario.

## **3 ¿Cómo funciona una aplicación de una sola página?**
---
Cuando el usuario navega hasta la aplicación web en el navegador, el servidor web le devuelve los recursos necesarios para ejecutar la aplicación. Existen dos enfoques para servir el código y los recursos en las aplicaciones de una sola página.

1. Cuando el navegador solicita la aplicación, devuelve y carga todo el HTML, CSS y JavaScript necesarios inmediatamente. Esto se conoce como _bundling_.

2. Cuando el navegador solicite la aplicación, devuelva sólo el mínimo HTML, CSS y JavaScript necesarios para cargar la aplicación. Los recursos adicionales se descargan según lo requiera la aplicación, por ejemplo, cuando un usuario navega a una sección específica de la aplicación. Esto se conoce como _carga perezosa_ o _división del código_.

Ambos enfoques son válidos y se utilizan en función del tamaño, la complejidad y los requisitos de ancho de banda de la aplicación. Si su aplicación es compleja y tiene muchos recursos, sus paquetes crecerán bastante y tardarán mucho tiempo en descargarse, ¡posiblemente acabe siendo más lenta que una aplicación web tradicional!

Una vez cargada la aplicación, toda la lógica y los cambios se aplican a la página web actual.

Veamos un ejemplo.

## **4 Un ejemplo de aplicación de una sola página**
---
Imagine que hay una página web que tiene una Etiqueta y un Botón. Mostrará un nombre de película aleatorio cuando se pulse el botón.

En una página web tradicional, cuando se pulsa el botón, el navegador enviará una solicitud POST al servidor web. El servidor web devolverá una nueva página web que contiene el botón y el nombre de la película, y el navegador web renderiza la nueva página.

En una aplicación de una sola página, cuando se pulse el botón, el navegador enviará una solicitud POST al servidor web. El servidor web devolverá un objeto JSON. La aplicación lee el objeto y actualiza la etiqueta con el nombre de la película.

Ya ve, ¡más eficiente!

Pero, ¿y si necesitamos tener varias páginas con diferentes diseños en nuestra aplicación?

Veamos otro ejemplo.

## **5 Diferencias prácticas entre aplicaciones de una sola página y aplicaciones multipágina**
---
Usted tiene una aplicación web que tiene una barra de navegación en la parte superior y dos páginas. Una página muestra las últimas noticias y la otra muestra la página de perfil del usuario actual. La barra de navegación contiene un enlace para cada página.

En un sitio web tradicional, cuando el usuario pulsa el enlace Perfil, el navegador web envía la solicitud al servidor web. El servidor web genera la página HTML y la devuelve al navegador web. A continuación, el navegador web renderiza la nueva página web.

En una aplicación de página única, las diferentes páginas se dividen en plantillas (o vistas). Cada vista tendrá un código HTML que contiene variables que pueden ser actualizadas por la aplicación.

El navegador web envía la solicitud al servidor web, y éste devuelve un objeto JSON. A continuación, el navegador web actualiza la página web insertando la plantilla con las variables sustituidas por los valores del objeto JSON.

## **6 Elementos de etiqueta de anclaje en elementos de una sola página**
---
Una aplicación de una sola página no puede tener elementos de etiqueta de anclaje normales como una aplicación web tradicional.

La razón es que el comportamiento por defecto de una etiqueta de anclaje es cargar otro archivo HTML desde un servidor y refrescar la página. Este refresco de página no es posible en una SPA que está impulsada por una biblioteca como React porque un refresco total de la página no es la forma en que funciona una SPA, como se explicó anteriormente en este artículo de lección.

En su lugar, una SPA viene con su propia implementación especial de etiquetas de anclaje y enlaces, que sólo dan la ilusión de cargar diferentes páginas al usuario final cuando, en realidad, simplemente cargan diferentes componentes en un único elemento del DOM real en el que se monta y actualiza el árbol DOM virtual.

Por eso la navegación en una aplicación de una sola página es fundamentalmente diferente de su homóloga en una aplicación multipágina. La comprensión de los conceptos esbozados en este artículo de la lección le hará un desarrollador React más completo.