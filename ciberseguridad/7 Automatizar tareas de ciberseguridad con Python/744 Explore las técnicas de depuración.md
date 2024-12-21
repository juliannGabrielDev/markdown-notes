---
Fecha: 2024-12-18
Fuente: Coursera
tags:
  - ciberseguridad
  - curso-7
  - modulo-4
---
## Tipos de errores

Es una parte normal del desarrollo de código en Python recibir mensajes de error o descubrir que el código que está ejecutando no funciona como pretendía. Lo importante es que sepa cómo solucionar los errores cuando se produzcan. Comprender los tres tipos principales de errores puede ayudarle. Estos tipos incluyen los errores de sintaxis, los errores lógicos y las excepciones.

### Errores de sintaxis

Un **error de sintaxis** es un error que implica un uso no válido de un lenguaje de programación. ==Los errores de sintaxis se producen cuando hay un error con la propia sintaxis de Python==. Algunos ejemplos comunes de errores de sintaxis son el olvido de un signo de puntuación, como el corchete de cierre de una lista o los dos puntos después del encabezado de una función.

Cuando ejecute código con errores de sintaxis, la salida identificará la ubicación del error con el número de línea y una parte del código afectado. También describe el error. Los errores de sintaxis suelen comenzar con la etiqueta `"SyntaxError:"`. A continuación, le sigue una descripción del error. La descripción puede ser simplemente `"invalid syntax"`. O si olvida un paréntesis de cierre en una función, la descripción podría ser `"unexpected EOF while parsing"`. `"EOF"` significa `"fin de archivo"`.

El siguiente código contiene un error de sintaxis. Ejecútelo y examine su salida:

```python
message = "You are debugging a syntax error
print(message)

"""
Error on line 1:
    message = "You are debugging a syntax error
                                              ^
SyntaxError: EOL while scanning string literal
"""
```

Sale el mensaje `"SyntaxError: EOL while scanning string literal"`. `"EOL"` significa "fin de línea". El mensaje de error también indica que el error se produce en la primera línea. El error se produjo porque faltaba una comilla al final de la cadena de la primera línea. Puede solucionarlo añadiendo esa comilla.

**Nota:** A veces encontrará la etiqueta de error `"IndentationError"` en lugar de `"SyntaxError"`. `"IndentationError"` es una subclase de `"SyntaxError"` que se produce cuando la sangría utilizada con una línea de código no es sintácticamente correcta.

### Errores lógicos 

Un **error lógico** es un error que se produce cuando la lógica utilizada en el código produce resultados no deseados. Los errores lógicos pueden no producir mensajes de error. En otras palabras, el código no hará lo que usted espera que haga, pero sigue siendo válido para el intérprete.

Por ejemplo, el uso de un operador lógico incorrecto, como un signo mayor o igual que (`>=`) en lugar del signo mayor que (`>`) puede dar lugar a un error lógico. Python no evaluará una condición como usted pretendía. Sin embargo, el código es válido, por lo que se ejecutará sin un mensaje de error.

El siguiente ejemplo muestra un mensaje relacionado con si un usuario ha alcanzado o no el número máximo de cinco intentos de inicio de sesión. La condición en la sentencia `if` debería ser `login_attempts < 5`, pero está escrita como `login_attempts >= 5`. Se ha asignado un valor de `5` a `login_attempts` para que pueda explorar lo que muestra en ese caso:

```python
login_attempts = 5
if login_attempts >= 5:
    print("User has not reached maximum number of login attempts.")
else:
    print("User has reached maximum number of login attempts.")

# User has not reached maximum number of login attempts.
```

La salida muestra el mensaje `"User has not reached maximum number of login attempts."` Sin embargo, esto no es cierto ya que el número máximo de intentos de inicio de sesión es cinco. Se trata de un error lógico.

Los errores lógicos también pueden producirse cuando se asigna un valor incorrecto en una condición o cuando un error con la indentación hace que una línea de código se ejecute de una forma que no estaba prevista.

### Excepciones

Una **excepción** es un error que implica que el código no puede ejecutarse aunque sea sintácticamente correcto. Esto ocurre por una gran variedad de razones.

Una causa común de una excepción es cuando el código incluye una variable que no ha sido asignada o una función que no ha sido definida. En este caso, su salida incluirá `"NameError"` para indicar que se trata de un error de nombre. Después de ejecutar el siguiente código, utilice el mensaje de error para determinar qué variable no se ha asignado:

```python
username = "elarson"
month = "March"
total_logins = 75
failed_logins = 18
print("Login report for", username, "in", month)
print("Total logins:", total_logins)
print("Failed logins:", failed_logins)
print("Unusual logins:", unusual_logins)

"""
Error on line 8:
    print("Unusual logins:", unusual_logins)
NameError: name 'unusual_logins' is not defined
"""
```

La salida indica que hay un `"NameError"` que afecta a la variable `unusual_logins`. Puede solucionarlo asignando un valor a esta variable.

Además de los errores de nombre, se emiten los siguientes mensajes para otros tipos de excepciones:

- `"IndexError"`: Se produce un error de índice cuando se coloca un índice en notación entre corchetes que no existe en la secuencia a la que se hace referencia. Por ejemplo, en la Lista `usernames = ["bmoreno", "tshah", "elarson"]`, los índices son `0`, `1`, y `2`. Si referenciara esta lista con la sentencia `print(usernames[3])`, se produciría un error de índice.

- `"TypeError"`: Se produce un error de tipo por utilizar un tipo de datos incorrecto. Por ejemplo, si intentara realizar un cálculo matemático sumando un valor de cadena a un número entero, obtendría un error de tipo.

- `"FileNotFound"`: Un error de archivo no encontrado se produce al intentar abrir un archivo que no existe en la ubicación especificada.

## Estrategias de depuración

Tenga en cuenta que si tiene varios errores, el intérprete de Python emitirá mensajes de error de uno en uno, empezando por el primer error que encuentre. Después de corregir ese error y volver a ejecutar el código, el intérprete emitirá otro mensaje para el siguiente error de sintaxis o excepción que encuentre.

Cuando se trata de errores de sintaxis, los mensajes de error que recibe en la salida le ayudarán generalmente a solucionar el error. Sin embargo, con los errores lógicos y las excepciones, puede que necesite estrategias adicionales.

### Depuradores

En este curso, usted ha estado ejecutando código en un entorno de cuaderno. Sin embargo, puede escribir código Python en un IDE (entorno de desarrollo integrado). Un **IDE (entorno de desarrollo integrado** ) es una aplicación de software para escribir código que proporciona asistencia para la edición y herramientas de corrección de errores. Muchos IDE ofrecen herramientas de detección de errores en forma de depurador. Un **depurador** es una herramienta de software que ayuda a localizar el origen de un error y a evaluar sus causas.

En los casos en los que no puede encontrar la línea de código que está causando el problema, los depuradores le ayudan a reducir el origen del error en su programa. Lo hacen trabajando con puntos de interrupción. Los puntos de interrupción son marcadores colocados en determinadas líneas de código ejecutable que indican qué secciones de código deben ejecutarse al depurar.

Algunos depuradores también tienen una Característica que le permite comprobar los valores almacenados en variables a medida que cambian a lo largo de su código. Esto es especialmente útil para los errores lógicos, de forma que pueda localizar dónde han cambiado involuntariamente los valores de las variables.

### Utilice sentencias `print`

Otra estrategia de depuración consiste en incorporar sentencias de impresión temporales diseñadas para identificar el origen del error. Debe incorporar estratégicamente estas sentencias de impresión para que se impriman en distintos puntos del código. Puede especificar números de línea así como texto descriptivo sobre la ubicación.

Por ejemplo, puede tener un código destinado a añadir nuevos usuarios a una Lista de aprobados y, a continuación, mostrar la Lista de aprobados. El código no debe añadir usuarios que ya estén en la lista aprobada. Si analiza la salida de este código después de ejecutarlo, se dará cuenta de que hay un error lógico:

```python
new_users = ["sgilmore", "bmoreno"]
approved_users = ["bmoreno", "tshah", "elarson"]
def add_users():
    for user in new_users:
        if user in approved_users:
            print(user,"already in list")
        approved_users.append(user)
add_users()
print(approved_users)

"""
bmoreno already in list
['bmoreno', 'tshah', 'elarson', 'sgilmore', 'bmoreno']
"""
```

Aunque obtenga el mensaje `"bmoreno already in list"`, se añade una segunda instancia de `"bmoreno"` a la lista. En el código siguiente, se han añadido sentencias de impresión al código. Cuando lo ejecute, podrá examinar lo que se imprime:

```python
new_users = ["sgilmore", "bmoreno"]
approved_users = ["bmoreno", "tshah", "elarson"]
def add_users():
    for user in new_users:
        print("line 5 - inside for loop")
        if user in approved_users:
            print("line 7 - inside if statement")
            print(user,"already in list")
        print("line 9 - before .append method")
        approved_users.append(user)
add_users()
print(approved_users)

"""
line 5 - inside for loop
line 9 - before .append method
line 5 - inside for loop
line 7 - inside if statement
bmoreno already in list
line 9 - before .append method
['bmoreno', 'tshah', 'elarson', 'sgilmore', 'bmoreno']
"""
```

La sentencia print `"line 5 - inside for loop"` sale dos veces, indicando que Python ha entrado en el bucle `for` para cada nombre de usuario en `new_users`. Esto es lo esperado. Además, la sentencia print `"line 7 - inside if statement"` sólo sale una vez, y esto también es lo esperado porque sólo uno de estos nombres de usuario ya estaba en `approved_users`.

Sin embargo, la sentencia print `"line 9 - before .append method"` sale dos veces. Esto significa que el código llama al método `.append()` para ambos nombres de usuario aunque uno ya esté en `approved_users`. Esto ayuda a aislar el error lógico a esta zona. Esto puede ayudarle a darse cuenta de que la línea de código `approved_users.append(user)` debería ser el cuerpo de una sentencia `else` para que sólo se ejecute cuando `user` no esté en `approved_users`.