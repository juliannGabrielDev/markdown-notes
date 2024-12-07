# Hoja de trucos: Elementos interactivos del formulario
#front-end #curso-4 #modulo-1 

---
Al rellenar formularios HTML, esperamos que los usuarios se atengan a ciertas reglas, como utilizar números cuando se les pide o formatear correctamente una URL o un correo electrónico cuando es necesario. Sin embargo, ==los humanos son propensos a cometer errores y, en algunos casos, pueden pasar por alto algunos de los datos que introducen== . Por eso es importante asegurarse de que la forma de los datos que esperamos en cada campo es correcta. La ==validación de formularios HTML== es un conjunto de **atributos** que podemos añadir a las entradas de los formularios para realizar una validación automática en nombre del usuario. Los atributos más importantes que utilizará para la validación son los siguientes:

## Obligatorio
Denota una entrada obligatoria que el usuario no puede dejar vacía. Puede utilizarse con cualquier tipo de entrada, como contraseña, radio, texto, etc. 
```html
<input type="text" id="firstName" name="firstName" required>
```
## Longitud máxima
Especifica la longitud máxima de una entrada de texto, en otras palabras, el número máximo de caracteres que se pueden introducir para un campo específico. Si se proporciona, impedirá que el usuario introduzca más caracteres que el límite.
```html
<input type="text" id="description" name="description" maxlength="50">
```
## Longitud mínima
Especifica la longitud mínima de una entrada de texto. Si se establece, la entrada no aceptará menos caracteres que los especificados. 
```html
<input type="password" id="password" name="password" minlength="8">
```
## Atributos mín. y máx
Determinan los valores mínimo y máximo permitidos para un campo de entrada. Suelen aplicarse a entradas de texto numéricas, entradas de rango o fechas.
```html
<input type="number" id="quantity" name="quantity" min="1" max="10">
<input type="range" id="volume" name="volume" min="1" max="100">
```
<input type="number" id="quantity" name="quantity" min="1" max="10"> <br><input type="range" id="volume" name="volume" min="1" max="100">
## Múltiple
Indica que el usuario puede introducir más de un valor en un mismo campo de entrada. Este atributo sólo puede utilizarse para los tipos de entrada correo electrónico y archivo.
```html
<input type="file" id="gallery" name="gallery" multiple>
```
<input type="file" id="gallery" name="gallery" multiple>
## Patrón
Define un patrón particular que el valor de un campo de entrada debe cumplir para ser considerado válido. Este atributo espera una expresión regular para especificar el patrón. Funciona con los tipos de entrada texto, fecha, búsqueda, URL, tel, correo electrónico y contraseña. Por ejemplo, puede restringir los números de teléfono para que sólo sean del Reino Unido. 
```html
<input type="tel" id="phone" name="phone" pattern=”^(?:0|\+?44)(?:\d\s?){9,10}$”>
```