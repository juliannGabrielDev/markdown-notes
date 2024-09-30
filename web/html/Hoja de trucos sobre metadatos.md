# Hoja de trucos sobre metadatos

Creado: 29 de septiembre de 2024 9:46

---

## Etiquetas HTML `<meta>`

Anteriormente en el curso, usted aprendió acerca de las etiquetas meta y cómo puede aprovecharlas para transmitir información a los motores de búsqueda para categorizar mejor sus páginas. Le recomendamos que tenga a mano esta hoja de trucos cuando cree sus aplicaciones web. La estructura de una etiqueta meta es la siguiente:

**Nombre** 
El nombre de la propiedad puede ser el que desee, aunque los navegadores suelen esperar un valor que entiendan y sobre el que puedan realizar una acción. Un ejemplo sería 
```html
<meta name="author" content="name"> 
```
para indicar el autor de la página. 

**Contenido** 
El campo de contenido especifica el valor de la propiedad. Por ejemplo, puede utilizar 
```html
<meta name="language" content="english">
```
para especificar el idioma de la página web a los motores de búsqueda. 

**Conjunto de caracteres ****
El charset es un campo especial que le permite especificar la codificación de caracteres utilizada en la página para que el navegador pueda mostrarla correctamente. El más utilizado es utf-8, y usted lo añadiría a su cabecera HTML de la siguiente manera: 
```html
<meta charset="UTF-8">  
```

**HTTP-equiv** 
Este campo significa equivalente HTTP, y se utiliza para simular cabeceras de respuesta HTTP. Es raro verlo, y se recomienda utilizar las cabeceras HTTP en lugar de las metaetiquetas HTML http-equiv. Por ejemplo, la siguiente etiqueta indicaría al navegador que actualice la página cada 30 minutos: 
```html
<meta http-equiv="refresh" content="30">
```

## Meta-etiquetas básicas (meta tags Para SEO)

**`<meta name="description"/>`** proporciona una breve descripción de la página web

**`<meta name=”title”/>`** especifica el título de la página web

**`<meta name="author" content="name">`** especifica el autor de la página web

**`<meta name="language" content="english">`** especifica el idioma de la página web

**`<meta name="robots" content="index,follow" />`** indica a los motores de búsqueda cómo rastrear o indexar una página determinada

**`<meta name="google"/>`** indica a Google que no muestre el cuadro de búsqueda sitelinks de su página al mostrar los resultados de búsqueda

**`<meta name="googlebot" content=”notranslate” />`** indica a Google que no desea proporcionar una traducción automática para su página si el usuario utiliza un idioma diferente

**`<meta name="revised" content="Sunday, July 18th, 2010, 5:15 pm" />`** especifica la última fecha y hora de modificación en la que ha realizado determinados cambios

**`<meta name="rating" content="safe for kids">`** especifica la audiencia prevista para su página

**`<meta name="copyright" content="Copyright 2022">`** especifica un Copyright.

---

## etiquetas `<meta http-equiv="..."/>
`
**`<meta http-equiv="content-type" content="text/html">`** especifica el formato del documento devuelto por el servidor

**`<meta http-equiv="default-style"/>`** especifica el formato del documento de estilo

**`<meta http-equiv="refresh"/>`** especifica la duración de la página antes de que se considere obsoleta

**`<meta http-equiv=”Content-language”/>`** especifica el idioma de la página

**`<meta http-equiv="Cache-Control" content="no-cache">`** indica al navegador cómo almacenar en caché su página

---

## Meta-etiquetas de diseño adaptable/móvil

```html
<meta name="format-detection" content="telephone=yes"/>
``` 
indica que los números de teléfono deben aparecer como enlaces de hipertexto en los que se puede hacer clic para realizar una llamada telefónica

```html
<meta name="HandheldFriendly" content="true"/>
``` 
especifica que la página puede visualizarse correctamente en dispositivos móviles

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
``` 
especifica el área de la ventana en la que se puede ver el contenido de la web.