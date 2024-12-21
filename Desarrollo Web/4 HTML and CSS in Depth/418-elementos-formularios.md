# Glosario: Elementos de formularios
#front-end #curso-4 #modulo-1 

---
El elemento `<form>` de HTML es un elemento importante y útil. La siguiente ficha ofrece una visión general de los elementos que lo componen `<form>` y sus atributos comunes con ejemplos sencillos para una referencia rápida.

## `<input>`
Se utiliza para crear controles interactivos, por ejemplo, botones y diversos tipos de campos de texto, etc., para aceptar entradas o datos del usuario. El atributo clave de este elemento es `type`. Algunos valores comunes para type son: `button, checkbox, date, email, number, password, submit, text, y url`. Estos valores dictan la apariencia del elemento. Por ejemplo, este código:
```html
<form action="my_action_page">
	<label for="uname">Username:</label>
	<br>
	<input type="text" id="uname" name="username">
	<br>
	<label for="pwd">Password:</label>
	<br>
	<input type="password" id="pwd" name="pwd">
	<br><br>
	<input type="submit" value="Login">
</form>
```
<form action="my_action_page">
	<label for="uname">Username:</label>
	<br>
	<input type="text" id="uname" name="username">
	<br>
	<label for="pwd">Password:</label>
	<br>
	<input type="password" id="pwd" name="pwd">
	<br><br>
	<input type="submit" value="Login">
</form>
---
## `<label>`
Define una etiqueta para un elemento. Tiene un atributo `"for"`, cuyo valor debe ser igual al atributo id del elemento al que se asocia. Observe cómo en el ejemplo anterior, el `<label>` se asocia con el `<input>` utilizando su valor id.

---
## `<select>`
Define una lista desplegable de opciones que se presentan al usuario. Tiene un par de atributos:

- `form`, el id del formulario en el que aparece el desplegable
- `name`, especifica el nombre del control
- `multiple` atributo booleano, cuando se especifica, indica si el usuario puede seleccionar varias opciones de la lista
- `required` indica si el usuario está obligado a seleccionar una opción antes de enviar el formulario
- `size` menciona el número de opciones visibles en una lista desplegable.    

Las opciones de una lista desplegable se definen utilizando el elemento `<option>` dentro de `<select>`. Observe el ejemplo en la descripción de `<option>` a continuación.

---
## `<textarea>`
Define un campo de entrada de varias líneas, normalmente para permitir al usuario introducir datos textuales más largos. Los atributos comunes de este elemento incluyen:

- `cols` define la anchura del área de texto, el valor por defecto es 20
- `form` el elemento de formulario al que se asocia el área de texto
- `maxlength` cuando se especifica, limita el número máximo de caracteres que pueden introducirse en el área de texto
- `minlength` el número mínimo de caracteres que el usuario debe introducir
- `readonly` una vez fijado, el usuario no puede modificar el contenido
- `rows` define el número de líneas de texto visibles para el área de texto

La siguiente línea de código define un área de texto de 10 líneas visibles y cerca de 30 caracteres de ancho donde el usuario puede introducir un máximo de 200 caracteres:
```html
<textarea name="response" rows="10" cols="30" maxlength=”200”>
</textarea>
```
<textarea name="response" rows="10" cols="30" maxlength=”200”>
</textarea>

---
## `<button>`
Define un botón en el que se puede hacer clic. El atributo onclick define el comportamiento cuando el botón es pulsado por el usuario. Por ejemplo, en el código siguiente, se muestra un mensaje de alerta al usuario.
```html
<button type="button" onclick="alert('You just clicked!')">Click Me!
</button>
```
<button type="button" onclick="alert('You just clicked!')">Click Me!
</button>

---
## `<fieldset>`
Se utiliza para agrupar elementos de entrada relacionados en un formulario. Por ejemplo, los elementos relacionados con la información personal del usuario y la cualificación educativa pueden agruparse por separado en dos conjuntos de campos.
### `<leyend>
Define una leyenda para el elemento `<fieldset>`. Por ejemplo:
```html
<fieldset>
	<legend>Personal Info</legend>
	<label for="fname">First name:</label><br>
	<input type="text" id="fname" name="fname" value="John"><br>
	<label for="lname">Last name:</label><br>
	<input type="text" id="lname" name="lname" value="Doe"><br>
</fieldset>

<fieldset>
	<legend>Qualificaiton</legend>
	<label for="pdegree">Primary degree:</label><br>
	<input type="text" id="pdegree" name="degree" value="Masters"><br>
	<label for="fos">Last name:</label><br>
	<input type="text" id="fos" name="field" value="Psychology"><br>
</fieldset>
```
<form>
<fieldset>
	<legend>Personal Info</legend>
	<label for="fname">First name:</label><br>
	<input type="text" id="fname" name="fname" value="John"><br>
	<label for="lname">Last name:</label><br>
	<input type="text" id="lname" name="lname" value="Doe"><br>
</fieldset>

<fieldset>
	<legend>Qualificaiton</legend>
	<label for="pdegree">Primary degree:</label><br>
	<input type="text" id="pdegree" name="degree" value="Masters"><br>
	<label for="fos">Last name:</label><br>
	<input type="text" id="fos" name="field" value="Psychology"><br>
</fieldset>
</form>

---
## `<datalist>`
Especifica una lista de opciones predefinidas para un elemento de entrada. Se diferencia de `<select>` en que el usuario aún puede proporcionar una entrada textual o numérica distinta de las opciones enumeradas.
```html
<form action="/my_action_page">
	<label for="flowers">Favourite flower:</label><br>
	<input list="flowers" name="flowers">
	<datalist id="flowers">
		<option value="Rose">
		<option value="Lily">
		<option value="Tulip">
		<option value="Daffodil">
		<option value="Orchid">
	</datalist>
</form>
```
<form action="/my_action_page">
	<label for="flowers">Favourite flower:</label><br>
	<input list="flowers" name="flowers">
	<datalist id="flowers">
		<option value="Rose">
		<option value="Lily">
		<option value="Tulip">
		<option value="Daffodil">
		<option value="Orchid">
	</datalist>
</form>

---
## `output`
Representa el resultado de un cálculo (normalmente la salida de un script) o el resultado de la acción del usuario.

---
## `<option>`
Define una opción para la lista desplegable. El siguiente ejemplo de código demuestra cómo se puede definir una lista simple, con la vista renderizada debajo del bloque de código.
```html
<label for="course">Choose a course:</label><br>
<select id="course" name="courselist">
	<option value="html">HTML Introduction</option>
	<option value="css">Styling with CSS</option>
	<option value="js">JavaScript</option>
	<option value="react">React Basics</option>
</select>
```
<label for="course">Choose a course:</label><br>
<select id="course" name="courselist">
	<option value="html">HTML Introduction</option>
	<option value="css">Styling with CSS</option>
	<option value="js">JavaScript</option>
	<option value="react">React Basics</option>
</select>

Por defecto, se selecciona el primer elemento de la lista desplegable. Para definir una opción preseleccionada, añada el atributo `selected` a la opción.

---
## `<optgroup>`
Define un grupo de opciones relacionadas en una lista desplegable. Su atributo `label` nombra al grupo.