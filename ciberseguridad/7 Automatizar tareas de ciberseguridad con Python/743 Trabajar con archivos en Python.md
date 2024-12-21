---
Fecha: 2024-12-18
Fuente: Coursera
Notas relacionadas:
  - "[[742 Importar archivos en Python]]"
  - "[[741 Componentes esenciales de Python para la automatización]]"
tags:
  - ciberseguridad
  - curso-7
  - modulo-4
---
En esta lectura, revisará el método `.split()`, y también aprenderá un método adicional que puede ayudarle a trabajar con el contenido de los archivos.

## Análisis sintáctico 

Parte del trabajo con archivos implica estructurar su contenido para satisfacer sus necesidades. ==**Análisis sintáctico** es el proceso de convertir los Datos a un formato más legible==. Los Datos pueden necesitar ser más legibles de un par de maneras diferentes. En primer lugar, ciertas partes de su código Python pueden requerir la modificación a un formato específico. Al convertir los Datos a este formato, permite a Python procesarlos de una forma específica. En segundo lugar, los programadores necesitan leer e interpretar los resultados de su código, y el análisis sintáctico también puede hacer que los datos sean más legibles para ellos.

Entre los métodos que pueden ayudarle a analizar sus datos se incluyen `.split()` y `.join()`.

## `.split()`

### Conceptos básicos de .split()

El método `.split()` convierte una cadena en una lista. Separa la cadena en función de un carácter especificado que se pasa a `.split()` como argumento.

En el siguiente ejemplo, los nombres de usuario de la cadena `approved_users` están separados por una coma. Por esta razón, una cadena que contiene la coma (`","`) se pasa a `.split()` para analizarla en forma de lista. Ejecute este código y analice los diferentes contenidos de `approved_users` antes y después de que se le aplique el método `.split()`:

```python
approved_users = "elarson,bmoreno,tshah,sgilmore,eraab"
print("before .split():", approved_users)
approved_users = approved_users.split(",")
print("after .split():", approved_users)

"""
Salida: 

before .split(): elarson,bmoreno,tshah,sgilmore,eraab
after .split(): ['elarson', 'bmoreno', 'tshah', 'sgilmore', 'eraab']
"""
```

Antes de aplicar el método `.split()` a `approved_users`, éste contiene una cadena, pero después de aplicarlo, esta cadena se convierte en una lista.

Si no pasa un argumento a `.split()`, éste separará la cadena cada vez que encuentre un espacio en blanco.

**Nota:** Python considera espacios en blanco una gran variedad de caracteres. Estos caracteres incluyen espacios entre caracteres, retornos para nuevas líneas y otros.

El siguiente ejemplo muestra cómo una cadena de nombres de usuario separados por espacios puede dividirse en una lista mediante el método `.split()`:

```python
removed_users = "wjaffrey jsoto abernard jhill awilliam"
print("before .split():", removed_users)
removed_users = removed_users.split()
print("after .split():", removed_users)

"""
Salida:

before .split(): wjaffrey jsoto abernard jhill awilliam
after .split(): ['wjaffrey', 'jsoto', 'abernard', 'jhill', 'awilliam']
"""
```

Como no se pasa un argumento a `.split()`, Python divide la cadena `removed_users` en cada espacio al separarla en una lista.

### Aplicación de .split() a archivos

El método `.split()` le permite trabajar con el contenido de un archivo como una lista después de haberlo convertido en una cadena mediante el método `.read()`. Esto resulta útil de diversas maneras. Por ejemplo, si desea iterar a través del contenido del archivo en un bucle for, esto puede hacerse fácilmente cuando se convierte en una lista.

El siguiente código abre el archivo `"update_log.txt"`. A continuación, lee todo el contenido del archivo en la variable `updates` como una cadena y divide la cadena en la variable `updates` en una lista mediante la creación de un nuevo elemento en cada espacio en blanco:

```python
with open("update_log.txt", "r") as file:
	updates = file.read()
updates = updates.split()
```

Después de esto, a través de la variable `updates`, puede trabajar con el contenido del archivo `"update_log.txt"` en partes de su código que requieran que esté estructurado como una lista.

**Nota:** Debido a que la línea que contiene `.split()` no tiene sangría como parte de la sentencia `with`, el archivo se cierra primero. ==Cerrar un archivo tan pronto como ya no sea necesario ayuda a mantener la legibilidad del código==. Una vez que un archivo se lee en la variable updates, ya no se necesita y puede cerrarse.

## `.join()`

### Conceptos básicos de .join()

Si necesita convertir una lista en una cadena, también existe un método para ello. El método `.join()` concatena los elementos de un iterable en una cadena. La sintaxis utilizada con `.join()` es distinta de la utilizada con `.split()` y otros métodos con los que ha trabajado, como `.index()`.

En métodos como `.split()` o `.index()`, usted añade el método a la cadena o lista con la que está trabajando y luego pasa otros argumentos. Por ejemplo, el código `usernames.index(2)`, anexa el método `.index()` a la variable usernames, que contiene una lista. Pasa 2 como argumento para indicar qué elemento debe devolver.

Sin embargo, con `.join()`, debe pasar como argumento la lista que desea concatenar en una cadena. Añade `.join()` al carácter con el que desea separar cada elemento una vez unidos en una cadena.

Por ejemplo, en el código siguiente, la variable `approved_users` contiene una lista. Si desea unir esa lista en una cadena y separar cada elemento con una coma, puede utilizar `",".join(approved_users)`. Ejecute el código y examine lo que devuelve:

```python
approved_users = ["elarson", "bmoreno", "tshah", "sgilmore", "eraab"]
print("before .join():", approved_users)
approved_users = ",".join(approved_users)
print("after .join():", approved_users)

"""
Salida:

before .join(): ['elarson', 'bmoreno', 'tshah', 'sgilmore', 'eraab']
after .join(): elarson,bmoreno,tshah,sgilmore,eraab
"""
```

Antes de que se aplique `.join()`, `approved_users` es una lista de cinco elementos. Después de aplicarlo, es una cadena con cada nombre de usuario separado por una coma.

**Nota**: Otra forma de separar elementos cuando se utiliza el método `.join()` es utilizar `"\n"`, que es el carácter de nueva línea. El carácter `"\n"` indica que hay que separar los elementos colocándolos en nuevas líneas.

### Aplicación de .join() a archivos

Al trabajar con archivos, también puede ser necesario volver a convertir su contenido en una cadena. Por ejemplo, puede utilizar el método `.write()`. El método `.write()` escribe datos de cadena en un archivo. Esto significa que si ha convertido el contenido de un archivo en una lista mientras trabajaba con él, tendrá que volver a convertirlo en una cadena antes de utilizar `.write()`. Para ello puede utilizar el método `.join()`.

Ya ha examinado cómo podría aplicarse `.split()` al contenido del archivo `"update_log.txt"` una vez convertido en cadena mediante `.read()` y almacenado como `updates`:

```python
with open("update_log.txt", "r") as file:
	updates = file.read()
updates = updates.split()
```

Una vez que haya terminado de realizar operaciones utilizando la lista de la variable updates, es posible que desee sustituir `"update_log.txt"` por el nuevo contenido. Para ello, primero tiene que volver a convertir las actualizaciones en una cadena mediante `.join()`. A continuación, puede abrir el archivo mediante una sentencia `with` y utilizar el método `.write()` para escribir la cadena updates en el archivo:

```python
updates = " ".join(updates)

with open("update_log.txt", "w") as file:
	File.write(updates)
```

El Código `" ".join(updates)` indica que separe cada uno de los elementos de la lista en `updates` con un espacio una vez unidos de nuevo en una cadena. Y como `"w"` se especifica como segundo argumento de `open()`, Python sobrescribirá el contenido de `"update_log.txt"` con la cadena que se encuentra actualmente en la variable `updates`.