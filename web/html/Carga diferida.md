# Carga diferida

Creado: 19 de julio de 2024 22:31

La carga diferida (lazy loading) en HTML se puede implementar utilizando el atributo `loading` en las etiquetas de imagen (`<img>`). Este atributo acepta los valores `lazy`, `eager` y `auto`, siendo `lazy` el que permite la carga diferida.

```html
<img src="imagen.jpg" alt="Descripción de la imagen" loading="lazy">

```
Al utilizar `loading="lazy"`, las imágenes solo se cargarán cuando estén a punto de entrar en el viewport, mejorando así el rendimiento de la página.