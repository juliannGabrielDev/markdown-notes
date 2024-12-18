---
Fecha: 2024-12-17
Fuente: Coursera
tags:
  - ciberseguridad
  - curso-7
  - modulo-2
---
Los comentarios de varias líneas se utilizan cuando se necesitan más de 79 caracteres en un solo comentario. Por ejemplo, esto puede ocurrir al definir una función si el comentario describe sus entradas y sus tipos de datos, así como su salida. 

Existen dos formas de escribir comentarios de varias líneas en Python que se utilizan habitualmente. La primera es mediante el uso del símbolo de hashtag ( `#` ) en varias líneas:

```python
# La función remainder_login_attempts() toma dos parámetros enteros,

# el máximo de intentos de inicio de sesión permitidos y el total de intentos realizados,

# y devuelve un entero que representa los intentos de inicio de sesión restantes

def remaining_login_attempts(maximum_attempts, total_attempts):
    return maximum_attempts - total_attempts
```

Otra forma de escribir comentarios de varias líneas es mediante cadenas de documentación. Las cadenas de documentación, también llamadas ***docstrings***, son cadenas que se escriben en varias líneas y se utilizan para documentar el código. Para crear una cadena de documentación, utilice comillas triples ( `""" """` ). 

También puedes agregar el comentario a la función en el ejemplo anterior de esta manera:

```python
"""
La función remainder_login_attempts() toma dos parámetros enteros,

los intentos máximos de inicio de sesión permitidos y el total de intentos realizados,

y devuelve un entero que representa los intentos de inicio de sesión restantes
"""
```