# Tipos de entrada
#Teoría #html #sintaxis 

---
Esta hoja de trucos debería servirle de referencia para decidir qué tipo se adapta mejor a su caso de uso. La mayoría de las entradas van de la mano con la etiqueta label para las mejores prácticas de accesibilidad.

## Botón
Muestra un botón en el que se puede hacer clic y se utiliza sobre todo en formularios HTML para activar un script cuando se hace clic en él. `<input type="button" value="Click me" onclick="msg()" />`

Tenga en cuenta que también puede definir botones con la etiqueta `<button>`, con la ventaja añadida de poder colocar contenido como texto o imágenes dentro de la etiqueta.
```html
<button onclick="alert('Are you sure you want to continue?')">
	<img src="https://yourserver.com/button_img.jpg"
		alt="Submit the form" height="64" width="64">
 </button>
```
## Casilla de verificación
Define una casilla de verificación que permite seleccionar o de-seleccionar valores individuales. Se utilizan para permitir que un usuario seleccione una o más opciones de un número limitado de opciones.
```html
<input type="checkbox" id="dog" name="dog" value="Dog">
<label for="dog">I like dogs</label>
<input type="checkbox" id="cat" name="cat" value="Cat">
<label for="cat">I like cats</label>
```
## Radio
Muestra un botón de radio que permite seleccionar un único valor entre varias opciones. Normalmente se presentan en grupos de radio, que es una colección de botones de radio que describen un conjunto de opciones relacionadas que comparten el mismo atributo "nombre".
```html
<input type="radio" id="light" name="theme" value="Light">
<label for="light">Light</label>
<input type="radio" id="dark" name="theme" value="Dark">
<label for="dark">Dark</label>
```
## Enviar
Muestra un botón de envío para enviar todos los valores de un formulario HTML a un manejador de formularios, normalmente un servidor. El gestor de formularios se especifica en el atributo "action" del formulario:
```html
<form action="myserver.com" method="POST">
	…
	<input type="submit" value="Submit" />
</form>
```
## Texto
Define un campo de texto básico de una sola línea en el que un usuario puede introducir texto.
```html
<label for="fname">First name:</label>
<input type="text" id="fname" name="fname">
```
## Contraseña
Define un campo de texto de una sola línea cuyo valor queda oculto, adecuado para información sensible como contraseñas.
```html
<label for="pwd">Password:</label>
<input type="password" id="pwd" name="pwd">
```
## Fecha
Muestra un control para introducir una fecha sin hora (año, mes y día).
```html
<label for="dob">Date of birth:</label>
<input type="date" id="dob" name="date of birth">
```
## Fecha-hora-local
Define un control para introducir una fecha y una hora, incluyendo el año, el mes y el día, así como la hora en horas y minutos.
```html
<label for="birthdaytime">Birthday (date and time):</label>
<input type="datetime-local" id="birthdaytime" name="birthdaytime">
```
## Correo electrónico
Define un campo para una dirección de correo electrónico. Es similar a una entrada de texto sin formato, con el añadido de que se valida automáticamente cuando se envía al servidor.
```html
<label for="email">Enter your email:</label>
<input type="email" id="email" name="email">
```
## Archivo
Muestra un control que permite al usuario seleccionar y cargar un archivo desde su ordenador. Para definir los tipos de archivos permitidos puede utilizar el atributo "aceptar". Además, para permitir la selección de varios archivos, añada el atributo "múltiple".
```html
<label for="myfile">Select a file:</label>
<input type="file" id="myfile" name="myfile">
```
## Oculto
Define un control que no se muestra pero cuyo valor se sigue enviando al servidor.
```html
<input type="hidden" id="custId" name="custId" value="3487">
```
## Imagen
Define una imagen como botón gráfico de envío. Debe utilizar el atributo "src" para señalar la ubicación de su archivo de imagen.
```html
<input type="image"src="submit_img.png" alt="Submit" width="48" height="48">
```
## Número
Define un control para introducir un número. Puede utilizar atributos para especificar restricciones, como los valores mínimo y máximo permitidos, intervalos de números o un valor por defecto.
## Rango
Muestra un widget de rango para especificar un número entre dos valores. El valor exacto, sin embargo, no se considera importante. Normalmente se representa mediante un control deslizante o un dial. Para definir el rango de valores aceptables, utilice las propiedades "mín" y "máx".
```html
<input type="range" id="volume" name="volume" min="0" max="10">
```
## Restablecer
Muestra un botón que restablece el contenido del formulario a sus valores por defecto.
```html
<input type="reset">
```
## Buscar
Define un campo de texto para introducir una consulta de búsqueda. Funcionalmente son idénticos a las entradas de texto, pero pueden tener un estilo diferente según el navegador.
```html
<label for="gsearch">Search in Google:</label>
<input type="search" id="gsearch" name="gsearch">
```
## Hora
Muestra un control para introducir un valor horario en horas y minutos, sin zona horaria.
```html
<label for="appt">Select a time:</label>
<input type="time" id="appt" name="appt">
```
## Tel
Define un control para introducir un número de teléfono. Los navegadores que no admiten "tel" retroceden a la entrada de texto estándar. Puede utilizar opcionalmente el campo "patrón" para realizar la validación.
```html
<label for="phone">Enter your phone number:</label>
<input type="tel" id="phone" name="phone" pattern="[+]{1}[0-9]{11,14}">
```
## Url
Muestra un campo para introducir una URL de texto. Funciona de forma similar a una entrada de texto, pero realiza una validación automática antes de ser enviada al servidor.
```html
<label for="homepage">Add your homepage:</label>
<input type="url" id="homepage" name="homepage">
```
## Semana
Define un control para introducir una fecha consistente en un número de semana-año y un año, sin zona horaria. Tenga en cuenta que se trata de un tipo más reciente que no es compatible con todos los navegadores.
```html
<label for="week">Select a week:</label>
<input type="week" id="week" name="week">
```
## Mes
Muestra un control para introducir un mes y un año, sin zona horaria. Tenga en cuenta que se trata de un tipo más nuevo que no es compatible con todos los navegadores.
```html
<label for="bdaymonth">Birthday (month and year):</label>
<input type="month" id="bdaymonth" name="bdaymonth" min="1930-01" value="2000-01">
```