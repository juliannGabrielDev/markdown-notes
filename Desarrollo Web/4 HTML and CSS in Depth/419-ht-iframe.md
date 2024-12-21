# Hoja de trucos: iframe
#front-end #curso-4 #modulo-1 

---
El `<iframe>` es el elemento marco en línea que incrusta una página HTML en otra página. Aparte de los atributos globales, que pueden formar parte de iframe, a continuación se enumeran los principales atributos específicos del elemento.
## `allow`
Especifica qué funciones o permisos están disponibles para el marco, por ejemplo, el acceso al micrófono, la cámara, otras API, etc. Por ejemplo:

- `allow="fullscreen”` se puede activar el modo de pantalla completa
- `allow=“geolocation”` permite acceder a la ubicación del usuario

Para especificar más de una característica, debe utilizarse un separador de punto y coma entre características. Por ejemplo, lo siguiente permitiría utilizar la cámara y el micrófono:
```html
<iframe src="https://example.com/…" allow="camera; microphone"> </iframe>
```
<iframe src="https://example.com/…" allow="camera; microphone"> </iframe>

---
## `name`
El nombre para el `<iframe>`. Por ejemplo 
```html
<iframe name = "My Frame" width="400" height="300"></iframe>
```

---
## `height`
Especifica la altura del marco. El valor por defecto es 150, en términos de píxeles CSS. 

---
## `weight`
Especifica la anchura del marco, en términos de píxeles CSS. El valor por defecto es de 300 píxeles.

---
## `referrerpolicy`

Un referrer es la cabecera HTTP que permite a la página saber quién la está cargando. Este atributo indica qué información de referenciador enviar al cargar el recurso marco. Los valores habituales son:

- `no-referrer` No se enviará la cabecera referrer
- `origin` El referrer se limitará al origen de la página de referencia
- `strict-origin` El origen del documento se enviará como referrer sólo cuando se utilice el mismo nivel de seguridad de protocolo (HTTPS a HTTPS).

---
## `sandbox`

Para reforzar la seguridad, una caja de arena aplica restricciones adicionales al contenido en `<iframe>`. Para levantar restricciones particulares, se utiliza un valor de atributo (token de permiso). A continuación se enumeran los tokens de permiso más comunes:

- `allow-downloads` Permite al usuario descargar un elemento
- `allow-forms` Permite al usuario enviar formularios
- `allow-modals` El recurso puede abrir ventanas modales
- `allow-orientation-lock` Permite que el recurso bloquee la orientación de la pantalla
- `allow-popups` Permite que se abran ventanas emergentes
- `allow-presentation` Permite iniciar una sesión de presentación
- `allow-scripts` Permite que el recurso ejecute scripts sin crear ventanas emergentes.

Tenga en cuenta que cuando el valor de este atributo está vacío, se aplican todas las restricciones. Para aplicar más de un permiso, utilice una lista separada por espacios. Por ejemplo, lo siguiente permitiría el envío de formularios y la ejecución de secuencias de comandos manteniendo activas las demás restricciones:
```html
<iframe src="my_iframe_sandbox.html" sandbox="allow-forms allow-scripts">
</iframe>
```

---
## `src`
La URL de la página a incrustar en `<iframe>`. Si se utiliza el valor about:blank se incrustaría una página vacía.

---
## `srcdoc`

Le permite especificar el HTML en línea a incrustar en el `<iframe>`. Una vez definido, este atributo anularía el atributo `src`.

Por ejemplo, el siguiente código mostrará "Mi html en línea" en el marco, en lugar de cargar my_iframe_src.html
```html
<iframe src="my_iframe_src.html" srcdoc="<p>My inline html</p>" >
</iframe>
```

---
## `loading`

Este atributo le permite especificar si el iframe debe cargarse inmediatamente cuando se carga la página web (`eager`) o cargarse cuando el iframe se muestra en el navegador (`lazy`). Esto le permite aplazar la carga del contenido del iframe si se encuentra más abajo en su página web y fuera del área de visualización cuando la página se carga inicialmente.
```html
<iframe src="my_iframe_src.html" loading="lazy" >
</iframe>
```

---
## `title`
Este atributo le permite añadir una descripción al iframe con fines de accesibilidad. El valor de este atributo debe describir con precisión el contenido del iframe.
```html
<iframe src="history.html" title="An embedded document about the history of my family" >
</iframe>
```