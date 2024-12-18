---
Creación: 2024-12-16
Fuente: Coursera
---
#ciberseguridad #curso-7 #modulo-2 

---
En esta lectura, revisará lo que aprendió sobre las funciones y examinará cómo las funciones pueden mejorar la eficiencia en un entorno de ciberseguridad.
## Funciones en ciberseguridad

Una **función** es una sección de código que puede reutilizarse en un programa. Las funciones son importantes en Python porque le permiten automatizar partes repetitivas de su código. En ciberseguridad, es probable que adopte algunos procesos que repetirá a menudo.

Cuando trabaje con registros de Seguridad, a menudo se encontrará con tareas que deben repetirse. Por ejemplo, si fuera responsable de encontrar actividad de inicio de sesión maliciosa basada en intentos de inicio de sesión fallidos, podría tener que repetir el proceso para múltiples registros.

Para evitarlo, podría definir una función que tomará un registro como entrada y devolverá todos los inicios de sesión potencialmente maliciosos. Sería fácil aplicar esta función a diferentes registros.
## Definición de una función

En Python, trabajará con funciones integradas y funciones definidas por el usuario. **Funciones integradas** son funciones que existen dentro de Python y pueden ser llamadas directamente. La función print() es un ejemplo de función integrada.

Las **funciones definidas por el usuario** son funciones que los programadores diseñan para sus necesidades específicas. Para definir una función, necesita incluir un encabezado de función y el cuerpo de su función.
### Encabezado de función

La cabecera de la función es lo que indica que Python está empezando a definir una función. Por ejemplo, si desea definir una función que muestre un mensaje `"investigate activity"` , puede incluir este encabezado de función:

```python
def mostrar_mensaje_de_investigacion():
```

La palabra clave `def` se coloca antes del nombre de una función para definir una función. En este caso, el nombre de esa función es `display_investigation_message` .

Los paréntesis que siguen al nombre de la función y los dos puntos ( `:` ) al final del encabezado de la función son también partes esenciales de la sintaxis.
### Cuerpo de la función

El cuerpo de la función es un bloque de código con sangría después del encabezado de la función que define lo que hace la función. La sangría es muy importante cuando se escribe una función porque separa la definición de una función del resto del código.

Para agregar un cuerpo a su definición de la función `display_investigation_message()` , agregue una línea sangrada con la función `print()` . Su definición de función se convierte en lo siguiente:

```python
def mostrar_mensaje_de_investigacion():
    print("investigar actividad")
```
## Llamada a una función

Después de definir una función, puede utilizarla tantas veces como sea necesario en su código. Utilizar una función después de definirla se denomina llamar a una función. Para llamar a una función, escriba su nombre seguido de un paréntesis. Así, para la función que definió previamente, puede utilizar el siguiente código para llamarla:

```python
mostrar_mensaje_de_investigación()
```

Aunque utilizará funciones de formas más complejas a medida que amplíe sus conocimientos, el siguiente código le ofrece una introducción sobre cómo la función `display_investigation_message()` puede formar parte de una sección de código más amplia. Puede ejecutarla y analizar su salida:

```python
def display_investigation_message():
    print("investigate activity")
    
application_status = "potential concern"
email_status = "okay"

if application_status == "potential concern":
    print("application_log:")
    display_investigation_message()

if email_status == "potential concern":
    print("email log:")
    display_investigation_message()
```

La función `display_investigation_message()` se utiliza dos veces dentro del código. Imprimirá mensajes `"investigate activity"` sobre dos registros diferentes cuando las condiciones especificadas se evalúen a `True` . En este ejemplo, sólo la primera declaración condicional se evalúa a `True` , por lo que el mensaje se imprime una vez.

Este Código llama a la función desde dentro de las condicionales, pero usted podría llamar a una función desde una variedad de lugares dentro del código.

**Nota:** Llamar a una función dentro del cuerpo de su definición de función puede crear un bucle infinito. Esto ocurre cuando no se combina con una lógica que detiene la llamada a la función cuando se cumplen determinadas condiciones. Por ejemplo, en la siguiente definición de función, después de llamar por primera vez a `func1()` , ésta seguirá llamándose a sí misma y creará un bucle infinito:

```python
def func1():
    func1()
```
## Claves

Las funciones de Python son importantes a la hora de escribir código. Para definir sus propias funciones, necesita los dos componentes esenciales: el Encabezado de la función y el Cuerpo de la función. Después de definir una función, puede llamarla cuando sea necesario.