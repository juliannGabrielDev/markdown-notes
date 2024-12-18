---
Fuente: Coursera
Creación: 2024-12-17
tags:
  - ciberseguridad
  - curso-7
  - modulo-2
---
## Trabajar con variables en funciones.

Trabajar con variables en funciones requiere comprender tanto los **parámetros** como los **argumentos**. Los términos parámetros y argumentos tienen usos distintos cuando se refieren a variables en una función. Además, si desea que la función devuelva un resultado, debe estar familiarizado con las sentencias return.
### Parámetros

Un **parámetro** es un objeto que se incluye en la definición de una función para utilizarlo en ella. Cuando define una función, crea variables en la cabecera de la función. A continuación, pueden utilizarse en el cuerpo de la función. En este contexto, estas variables se denominan parámetros. Por ejemplo, considere la siguiente función:

```python
def remaining_login_attempts(maximum_attempts, total_attempts):
    print(maximum_attempts - total_attempts)
```

Esta función toma dos variables, `maximum_attempts` y `total_attempts` y las utiliza para realizar un cálculo. En este ejemplo, `maximum_attempts` y `total_attempts` son parámetros.
### Argumentos

En Python, un **argumento** son los datos que se introducen en una función cuando se llama a ella. Al llamar a `remaining_login_attempts` en el siguiente ejemplo, los enteros `3` y `2` se consideran argumentos:

```python
remaining_login_attempts(3, 2)
```

Estos enteros pasan a la función a través de los parámetros que se identifican al definir la función. En este caso, esos parámetros serían `max_attempts` y `total_attempts` . 3 está en la primera posición, por lo que pasa a `max_attempts` . Del mismo modo, 2 está en la segunda posición y pasa a `total_attempts` .
### Sentencias de retorno

Cuando se definen funciones en Python, se utilizan sentencias de retorno si se desea que la función devuelva una salida. La palabra clave `return` se utiliza para devolver información de una función.

La palabra clave `return` aparece delante de la información que desea devolver. En el siguiente ejemplo, está antes del cálculo de cuántos intentos de inicio de sesión quedan:

```python
def remaining_login_attempts(maximum_attempts, total_attempts):
    return maximum_attempts - total_attempts
```

Las sentencias de retorno son útiles cuando desea almacenar lo que devuelve una función dentro de una variable para utilizarlo en otra parte del código. Por ejemplo, puede utilizar esta variable para cálculos o dentro de sentencias condicionales. En el siguiente ejemplo, la información devuelta por la llamada a `remaining_login_attempts` se almacena en una variable llamada `remaining_attempts` . A continuación, esta variable se utiliza en una condicional que imprime un mensaje `"Your account is locked"` cuando `remaining_attempts` es menor o igual que `0` . Puede ejecutar este código para explorar su resultado:

```python
def remaining_login_attempts(maximum_attempts, total_attempts):
    return maximum_attempts - total_attempts

remaining_attempts = remaining_login_attempts(3, 3)

if remaining_attempts <= 0:
    print("Your account is locked")
```