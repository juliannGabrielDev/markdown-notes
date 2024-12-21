# Enviar
#front-end #curso-4 #modulo-1 

---
## Acción y método
El envío de formularios es una parte esencial de la World Wide Web. Pero la forma en que se envía el formulario viene determinada por dos atributos esenciales: la acción y el método. 
### `action`
El atributo action especifica a qué dirección web debe enviarse el formulario. Esta dirección es la ubicación del código del lado del servidor que procesará la solicitud.
```html
<form action="/login">
</form>
```
Es importante tener en cuenta que la acción puede ser una dirección URL completa, como `https://meta.com`, una ruta absoluta, como `/login`, o una ruta relativa, como `login`. La ruta absoluta, que comienza con una barra oblicua, utilizará la dirección base del sitio web actual, como `https://meta.com` y la combinará con la ruta absoluta. Por ejemplo, si `/login` es la ruta absoluta, el formulario se enviará a `https://meta.com/login`. Si la dirección es `https://meta.com/company-info/` y `/login` es la ruta absoluta, la dirección de envío seguirá siendo `https://meta.com/login`. Del mismo modo, una ruta relativa combinará la dirección web actual con una ruta relativa. Por ejemplo, si el navegador web se encuentra actualmente en la página web `https://meta.com/company-info/`, y la ruta relativa se establece en `login`, el formulario se enviará a `https://meta.com/company-info/login`. 
### `method`
El atributo method especifica qué método HTTP se utiliza para enviar el formulario; `GET` o `POST`.
El formulario utilizará por defecto el método HTTP `GET` cuando no se proporcione el atributo method. ==Como ya sabrá, cuando el formulario se envía utilizando el método HTTP `GET`, los datos de los campos del formulario se codifican en la URL==. Y ==cuando el formulario se envía utilizando el método HTTP `POST`, los datos se envían como parte del cuerpo de la petición HTTP==. Cuando el servidor web recibe la solicitud, procesa los datos y devuelve una respuesta HTTP. 
La respuesta indica el resultado del envío, que puede ser satisfactorio o fallido debido a datos no válidos o incorrectos. Sin embargo, como desarrollador front-end, es esencial saber que los formularios no son la única forma de enviar datos al servidor web. A medida que aprenda más sobre JavaScript y las bibliotecas front-end, descubrirá que los desarrolladores a menudo envían solicitudes HTTP directamente a través de código y envían datos como parte del cuerpo de la solicitud HTTP en un formato de texto llamado JavaScript Object Notation, o JSON. Pero ese es un tema para otro curso.
