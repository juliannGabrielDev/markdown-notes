---
Creación: 2024-12-16
Fuente: Coursera
---
#ciberseguridad #curso-7 #modulo-1 

---
Anteriormente, usted exploró los tipos de datos en Python. Un **tipo de dato** es una categoría para un tipo particular de elemento de datos. Usted se centra en Cadena, Lista, Flotante, Entero y Datos booleanos. Estos son los tipos de datos con los que trabajará en este curso. Esta lectura ampliará estos tipos de datos. También introducirá tres tipos adicionales.
## String

En Python, los Datos de cadena son datos formados por una secuencia ordenada de caracteres. Los caracteres de una Cadena pueden incluir letras, números, símbolos y espacios. Estos caracteres deben ir entre comillas. Todas estas son cadenas válidas:

- `"Se necesitan actualizaciones"`
- `"20%"`
- `"5.0"`
- `"35"`
- `"**/**/**" `
- `""`

**Nota:** El último elemento ( `""` ), que no contiene nada entre comillas, se denomina cadena vacía.

Puede utilizar la función `print()` para mostrar una cadena. Puede explorar esto ejecutando este código:
```python
print("updates needed")
```
Puede colocar cadenas entre combinaciones dobles ( `""` ) o simples ( `''` ). El siguiente código demuestra que se imprime el mismo mensaje cuando la cadena está entre comillas simples:
```python
print('updates needed')
```
## Lista

En Python, los datos de una **lista** son una estructura de datos que consiste en una colección de datos en forma secuencial. Los elementos de una lista pueden ser de cualquier tipo de datos, como cadenas, enteros, booleanos o incluso otras listas. Los elementos de una Lista se colocan entre corchetes, y cada elemento se separa por una coma. Las siguientes listas contienen elementos de varios tipos de datos:
- `[12, 36, 54, 1, 7]`
    
- `["eraab", "arusso", "drosas"]`
- `[True, False, True, True]`
- `[15, "approved", True, 45.5, False]`
- `[]`
## Entero

En Python, los datos **enteros** son datos formados por un número que no incluye punto decimal. Todos estos son ejemplos de datos enteros:

- `-100`
- `-12`
- `-1`
- `0`
- `1`
- `20`
- `500`

Los enteros no se entrecomillan.
## Flotante

**Datos flotantes** son aquellos que consisten en un número con un punto decimal. Todos los siguientes son ejemplos de datos flotantes:

- `-2.2`
- -`1.34`
- `0.0`
- `0,34`

Al igual que los datos enteros, los datos flotantes no se entrecomillan.

**Nota:** La división de dos valores enteros o dos valores flotantes da como resultado una salida flotante cuando se utiliza el símbolo `/` :
```python
print(1/4)
print(1.0/4.0)
```
La salida de ambos cálculos es el valor flotante de `.25` .

Si desea devolver un número entero de un cálculo, debe utilizar el símbolo `//` en su lugar:
```python
print(1//4)
print(1.0//4.0)
```
## Booleana

Datos booleanos son datos que sólo pueden tener uno de dos valores: o `True` o `False`.

No debe entrecomillar los valores booleanos.
## Tipos de datos adicionales

En este curso, trabajará con los tipos de datos Cadena, Lista, Enteros, Flotantes y Booleanos, pero existen otros tipos de datos. Estos tipos de datos adicionales incluyen los datos de tupla, los datos de diccionario y los Datos de conjunto.
### Tupla

Los **Datos de tupla** son una estructura de datos que consiste en una colección de datos que no pueden modificarse. Al igual que las listas, las tuplas pueden contener elementos de distintos tipos de datos.

Una diferencia entre los Datos de tupla y los Datos de lista es que es posible cambiar los elementos de una lista, pero no es posible cambiar los elementos de una tupla. Esto podría ser útil en un contexto de ciberseguridad. Por ejemplo, si los identificadores de software se almacenan en una tupla para garantizar que no se alterarán, esto puede proporcionar la seguridad de que una lista de control de acceso sólo bloqueará el software previsto.

La sintaxis de una tupla también es diferente de la de una lista. Una tupla se coloca entre paréntesis en lugar de entre corchetes. Todos estos son ejemplos del tipo de datos de tupla:

- `("wjaffrey", "arutley", "dkot")`
- `(46, 2, 13, 2, 8, 0, 0)`
- `(True, False, True, True)`
- `("wjaffrey", 13, True)`

**Consejo profesional:** Las tuplas son más eficientes en memoria que las listas, por lo que resultan útiles cuando se trabaja con una gran cantidad de datos.
### Diccionario

Los **Datos del diccionario** son datos que constantes de uno o más pares clave-valor. Cada clave se asigna a un valor. Entre la clave y el valor se colocando dos puntos ( : ). Las comas separan los pares clave-valor de otros pares clave-valor, y el diccionario se coloca entre corchetes ( {} ).

Los diccionarios son útiles cuando se desea almacenar y recuperar datos de forma predecible. Por ejemplo, el siguiente diccionario asigna el nombre de un edificio a un número. El nombre del edificio es el valor y el número es la clave. Después de la clave se colocan dos puntos.

```python
{ 1: "Este",
  2: "Oeste",
  3: "Norte",
  4: "Sur" }
```
### Conjunto

En Python, los **Datos de conjunto** son datos que consisten en una colección desordenada de valores únicos. Esto significa que no puede haber dos valores iguales en un conjunto.

Los elementos de un conjunto se colocan siempre entre llaves y se separan por una coma. Estos elementos pueden ser de cualquier tipo de datos. Este ejemplo de conjunto contiene cadenas de nombres de usuario:

```python
{"jlanksy", "drosas", "nmason"}
```