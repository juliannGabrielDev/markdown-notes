---
Creación: 2024-12-16
Fuente: Coursera
tags:
  - ciberseguridad
  - curso-7
  - modulo-1
---
Una **sentencia iterativa** es código que ejecuta repetidamente un conjunto de instrucciones. Dependiendo de los criterios, las sentencias iterativas se ejecutarán cero o más veces. Hemos iterado código utilizando tanto los bucles `for` como los bucles `while` . En esta lectura, recapitulará la sintaxis de los bucles. Después, aprenderá a utilizar las palabras clave `break` y `continue` para controlar la ejecución de los bucles.

## Bucles `for`

Si necesita iterar a través de una secuencia especificada, debe utilizar un bucle `for` .

El siguiente bucle itera a través de una secuencia de nombres de usuario. 

```python
for i in ["elarson", "bmoreno", "tshah", "sgilmore"]:
    print(i)
```
La primera línea de este código es la cabecera del bucle. Directamente después de `for` , aparece la variable de bucle . ==La variable de bucle es una variable que se utiliza para controlar las iteraciones de un bucle==. En los bucles para , la variable de bucle forma parte de la cabecera. En este ejemplo, la variable de bucle es `i` .

El resto del encabezado del bucle indica la secuencia a iterar. El operador aparece antes de la secuencia para indicar a Python que ejecuta el bucle para cada elemento de la secuencia. En este ejemplo, la secuencia es la lista de nombres de usuario. El encabezado del bucle debe terminar con dos puntos ( `:` ).

La segunda línea de este ejemplo de bucle es el cuerpo del bucle. El cuerpo del bucle para puede constar de varias líneas de programación. En el cuerpo, se indica lo que el bucle debe hacer en cada iteración. En este caso, es `print(i)` , o lo que es lo mismo, muestra el valor actual de la variable del bucle durante esa iteración del bucle. Para que Python ejecute el código correctamente, el cuerpo del bucle debe tener una sangría mayor que la cabecera del bucle.

**Nota:** Cuando se utiliza en un bucle `for` , el operador precede a la secuencia sobre la que iterará el bucle `for` . Cuando se utiliza en una sentencia condicional, el operador en se utiliza para evaluar si un objeto forma parte de una secuencia. En el ejemplo if `"elarson" in ["tshah", "bmoreno", "elarson"]` se evalúa como `True` porque `"elarson"` forma parte de la secuencia que sigue a in .

### Bucle a través de una lista

El uso de bucles en Python le permite iterar fácilmente a través de listas, como una lista de recursos informáticos. En el siguiente bucle `for` , `active` es la variable de bucle y otra variable, `computer_assets` , es la secuencia. La variable `computer_assets` almacena una lista. Esto significa que en la primera iteración el valor de activo será el primer elemento de esa lista, y en la segunda iteración, el valor de activo será el segundo elemento de esa lista. 

```python
computer_assets = ["laptop1", "desktop20", "smartphone03"]

for asset in computer_assets:
    print(asset)
```

**Nota:** También es posible hacer un bucle a través de una cadena. Esto devolverá cada carácter uno a uno. Puede observarlo ejecutando el siguiente bloque de código que itera a través de la cadena` "security"` :

```python
string = "security"
for character in string:
    print(character)
```

### Uso de range()

Otra forma de iterar a través de un bucle para basarse en una secuencia de números, y esto puede hacerse con `range()` . La función `range()` genera una secuencia de números. Acepta entradas para el punto inicial, el punto final y el incremento entre paréntesis. Por ejemplo, el siguiente código indica que se inicia la secuencia de números en `0` , se detiene en `5` , y se incrementa cada vez en `1` :

`range(0, 5, 1)`

**Nota:** El punto de inicio es inclusivo, lo que significa que 0 se incluirá en la secuencia de números, pero el punto de parada es exclusivo, lo que significa que 5 se excluirá de la secuencia. Concluirá un número entero antes del punto de parada.

Cuando ejecute este código, podrá observar cómo `5` queda excluido de la secuencia:

```python
for i in range(0, 5, 1):
    print(i)
```

Debe tener en cuenta que siempre es necesario incluir el punto de parada, pero si el punto de inicio es el valor por defecto de `0` y el incremento es el valor por defecto de `1` , no es necesario especificarlos en el código. Si ejecuta este código, obtendrá los mismos resultados:

```python
for i in range(5):
    print(i)
```

## bucles `while`

Si desea que un bucle esté basado en una condición, debe utilizar un bucle `while` . Mientras la condición sea `True` , el bucle continúa, pero cuando se evalúa a `False` , el bucle `while` sale. El siguiente bucle `while` continúa mientras la condición que `i < 5` sea `True` :

```python
i = 1

while i < 5:
    print(i)
    i = i + 1
```

En este bucle `while` , el encabezado del bucle es la línea `while i < 5:` . A diferencia de los bucles `for` , el valor de una variable de bucle utilizada para controlar las iteraciones no se asigna dentro de la cabecera del bucle en un bucle `while` . En su lugar, se asigna fuera del bucle. En este ejemplo, a `i` se le asigna un valor inicial de `1` en una línea que precede al bucle.

La palabra clave `while` indica el inicio de un bucle `while` . A continuación, el encabezado del bucle indica la condición que determina cuándo termina el bucle. Esta condición utiliza los mismos operadores de comparación que las sentencias condicionales. Al igual que en un bucle for , la cabecera de un bucle while debe terminar con dos puntos ( `:` ).

El cuerpo de un bucle mientras indica las acciones a realizar en cada iteración. En este ejemplo, se trata de mostrar el valor de `i` e incrementar el valor de `i` en `1` . Para que el valor de `i` cambie con cada iteración, es necesario indicarlo en el cuerpo del bucle `while` . En este ejemplo, el bucle itera cuatro veces hasta alcanzar un valor de `5` .

### Enteros en la condición de bucle

A menudo, como se acaba de demostrar, la condición del bucle se basa en valores enteros. Por ejemplo, es posible que desee permitir que un usuario se registre siempre que lo haya hecho menos de cinco veces. Entonces, su variable de bucle, login_attempts , puede ser inicializada a 0 , incrementada por 1 en el bucle, y la condición de bucle puede especificar iterar sólo cuando la variable sea menor que `5` . Puede ejecutar el código siguiente y revisar la iteración de cada intento de inicio de sesión:

```python
login_attempts = 0

while login_attempts < 5:
    print("Login attempts:", login_attempts)
    login_attempts = login_attempts + 1
```

### Valores booleanos en la condición del bucle

Las condiciones de los bucles `while` también pueden depender de otros tipos de datos, incluidas las comparaciones de Datos booleanos. En las comparaciones de datos booleanos, su condición de bucle puede comprobar si una variable de bucle es igual a un valor como `True` o `False` . El bucle itera un número indeterminado de veces hasta que la condición booleana deja de ser `True` .

En el ejemplo siguiente, se utiliza un valor booleano para salir de un bucle cuando un usuario ha realizado cinco intentos de inicio de sesión. Una variable llamada `count` realiza un seguimiento de cada intento de inicio de sesión y cambia la variable `login_status` a `False` cuando `count` es igual a `4` . (El incremento de `count` de `0` a `4` representa cinco intentos de inicio de sesión.) Dado que la condición `while` sólo itera cuando `login_status` es `True` , saldrá del bucle. Puede ejecutarlo para explorar esta salida:

```python
count = 0
login_status = True

while login_status == True:
    print("Try again.")
    count = count + 1
    if count == 4:
        login_status = False
```

## Gestionar bucles

Puede utilizar las palabras clave `break` y `continue` para controlar más sus iteraciones de bucle. Ambas se incorporan a una sentencia condicional dentro del cuerpo del bucle. Pueden insertarse para ejecutarse cuando la condición en una sentencia `if` es `True` . La palabra clave `break` se utiliza para salir de un bucle. La palabra clave `continue` se utiliza para saltarse una iteración y continuar con la siguiente.

## `break`

Cuando desee salir de un bucle `for` o `while` basándose en que una condición concreta de una sentencia `if` sea `True` , puede escribir una sentencia condicional en el cuerpo del bucle y escribir la palabra clave `break` en el cuerpo de la condicional.

El siguiente ejemplo lo demuestra. La sentencia condicional con `break` ordena a Python salir del bucle porque si el valor de la variable de bucle active es igual a `"desktop20"` . En la segunda iteración, esta condición se evalúa como `True` . Puede ejecutar este código para observar esto en la salida:

```python
computer_assets = ["laptop1", "desktop20", "smartphone03"]

for asset in computer_assets:
    if asset == "desktop20":
        break
    print(asset)
```

Como era de esperar, los valores de `"desktop20"` y `"smartphone03"` no se imprimen porque el bucle se rompe en la segunda iteración.

## `continue`

Cuando desee saltarse una iteración basada en una determinada condición en una sentencia `if` siendo `True` , puede agregar la palabra clave `continue` en el cuerpo de una sentencia condicional dentro del bucle. En este ejemplo, continue se ejecutará cuando la variable de bucle de activo sea igual a `"desktop20"` . Puede ejecutar este código para observar cómo difiere esta salida del ejemplo anterior con `break` :

```python
computer_assets = ["laptop1", "desktop20", "smartphone03"]

for asset in computer_assets:
    if asset == "desktop20":
        continue
    print(asset)
```

El valor `"desktop20"` en la segunda iteración no se imprime. Sin embargo, en este caso, el bucle continúa hasta la siguiente iteración y se imprime `"smartphone03"` .

## Bucle infinito

Si crea un bucle que no sale, se denomina bucle infinito. En estos casos, debe presionar **CTRL-C** o **CTRL-Z** en su teclado para detener el bucle infinito. Puede que necesite hacer esto cuando ejecute un servicio que procese datos constantemente, como un servidor web.