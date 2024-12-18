---
Fecha: 2024-12-17
Fuente: Coursera
Notas relacionadas:
  - "[[721 Funciones de Python en ciberseguridad]]"
tags:
  - ciberseguridad
  - curso-7
  - modulo-2
---
**Funciones integradas** son funciones que existen dentro de Python y pueden ser llamadas directamente. En esta lectura, las explorará más a fondo y también aprenderá sobre la función `min()` . Además, revisará cómo pasar la salida de una función a otra función.
## `type()`

La función `type()` devuelve el tipo de datos de su argumento. La función `type()` le ayuda a realizar un seguimiento de los tipos de datos de las variables para evitar errores a lo largo de su código.

Para utilizarla, se pasa el objeto como argumento, y devuelve su tipo de datos. Sólo acepta un argumento. Por ejemplo, puede especificar `type("security")` o `type(7)` .
### Pasar una función a otra

Cuando trabaja con funciones, a menudo necesitará pasarlas a través de `print()` si desea que el tipo de datos aparezca en la pantalla. Este es el caso cuando se utiliza una función como `type()` . Considere el siguiente código:

```python
print(type("This is a string"))
```
## `max()` y `min()`

La función `max()` devuelve la entrada numérica más grande que se le haya pasado. La función `min()` devuelve la entrada numérica más pequeña que se le haya pasado.

Las funciones `max()` y `min()` aceptan argumentos de múltiples valores numéricos o de un iterable como una lista, y devuelven el mayor o el menor valor respectivamente.

En un contexto de ciberseguridad, podría utilizar estas funciones para identificar la sesión más larga o más corta en la que se registró un usuario. Si un usuario concreto se conectó siete veces durante una semana, y usted almacenó sus tiempos de acceso en minutos en una lista, puede utilizar las funciones `max()` y `min()` para encontrar e imprimir sus sesiones más largas y más cortas:

```python
time_list = [12, 2, 32, 19, 57, 22, 14]

print(min(time_list))
print(max(time_list))
```
## `sorted()`

La función `sorted()` ordena los componentes de una lista. La función `sorted()` también funciona sobre cualquier iterable, como una cadena, y devuelve los elementos ordenados en una lista. Por defecto, los ordena en orden ascendente. Cuando se le da un iterable que contiene números, los ordena de menor a mayor; Esto incluye iterables que contienen datos numéricos, así como iterables que contienen datos de cadena que comienzan con números. Un iterable que contiene cadenas que comenzarán por caracteres alfabéticos se ordenará alfabéticamente.

La función `sorted()` toma como entrada un iterable, como una lista o una cadena. Así, por ejemplo, puede utilizar el siguiente código para ordenar la lista de sesiones de inicio de sesión de la más corta a la más larga:

```python
time_list = [12, 2, 32, 19, 57, 22, 14]

print(sorted(time_list))
print(time_list)
```