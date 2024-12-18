---
Fecha: 2024-12-17
Fuente: Coursera
tags:
  - ciberseguridad
  - curso-7
  - modulo-2
---
Un **Módulo** es un archivo Python que contiene funciones adicionales, variables, clases y cualquier tipo de código ejecutable. También aprendió que una **biblioteca** es una colección de módulos que proporcionan código al que los usuarios pueden acceder en sus programas. Se le presentan algunos módulos de la Biblioteca estándar de Python y un par de bibliotecas externas. En esta lectura, aprenderá a importar un módulo que existe en la Biblioteca estándar de Python y a utilizar sus funciones. También ampliará sus conocimientos sobre las bibliotecas externas.
## La biblioteca estándar de Python

La **Biblioteca estándar de Python** es una extensa colección de códigos Python que a menudo viene empaquetada con Python. Incluye una variedad de módulos, cada uno con código preconstruido centrado en un tipo particular de tarea.

Por ejemplo, anteriormente se le presentaron los siguientes módulos de la Biblioteca estándar de Python:

- El módulo `re` , que proporciona funciones utilizadas para la búsqueda de patrones en archivos de registro.

- El módulo `csv` , que proporciona funciones utilizadas al trabajar con archivos .csv

- Los módulos `glob` y `os` , que proporcionan funciones utilizadas al interactuar con la línea de comandos

- Los módulos `time` y `datetime` , que proporcionan funciones utilizadas al trabajar con marcas de tiempo.

Otro módulo de la Biblioteca estándar de Python es `statistics` . El módulo `statistics` incluye funciones utilizadas al calcular estadísticas relacionadas con datos numéricos. Por ejemplo, `mean()` es una función del módulo `statistics` que toma datos numéricos como entrada y calcula su media (o promedio). Además, median() es una función del módulo estadístico que toma datos numéricos como entrada y calcula su mediana (o valor medio).
## Cómo importar módulos desde la Biblioteca estándar de Python

Para acceder a los módulos de la Biblioteca estándar de Python, debe importarlos. Puede elegir entre importar un módulo completo o sólo importar funciones específicas de un módulo.
### Importar un módulo completo

Para importar un módulo completo de la biblioteca estándar de Python, se utiliza la palabra clave `import` . La palabra clave `import` busca un módulo o una biblioteca en un sistema y lo agrega al entorno local de Python. Después de `import` , especifique el nombre del módulo que desea importar. Por ejemplo, puede especificar `import statistics` para importar el módulo `statistics` . Esto importará todas las funciones dentro del módulo `statistics` para usarlas más adelante en su código.

Como ejemplo, es posible que desee utilizar la función `mean()` del módulo de estadísticas para calcular la cantidad promedio de intentos de inicio de sesión fallidos por mes para un usuario en particular. En el siguiente bloque de código, la cantidad total de intentos de inicio de sesión fallidos para cada uno de los doce meses se almacena en una lista llamada `monthly_failed_attempts` . Ejecute este código y analice cómo se puede utilizar `mean()` para calcular el promedio de estos totales mensuales de inicios de sesión fallidos y almacenarlo en `mean_failed_attempts` :

```python
import statistics

monthly_failed_attempts = [20, 17, 178, 33, 15, 21, 19, 29, 32, 15, 25, 19]

mean_failed_attempts = statistics.mean(monthly_failed_attempts)

print("mean:", mean_failed_attempts)
```

El resultado devuelve una media de `35,25` . Es posible que notes el valor atípico de `178` y quieras encontrar también el valor medio. Para hacerlo a través de la función `median()` , puedes utilizar el siguiente código:

```python
import statistics

monthly_failed_attempts = [20, 17, 178, 33, 15, 21, 19, 29, 32, 15, 25, 19]

median_failed_attempts = statistics.median(monthly_failed_attempts)

print("median:", median_failed_attempts)
```

Esto le da el valor `20,5` , que también podría ser útil para analizar las estadísticas de intentos de inicio de sesión fallidos del usuario.

**Nota:** Al importar un módulo completo de la biblioteca estándar de Python, debe identificar el nombre del módulo con la función cuando lo llama. Puede hacerlo colocando el nombre del módulo seguido de un punto ( `.` ) antes del nombre de la función. Por ejemplo, los bloques de código anteriores usan `statistics.mean()` y `statistics.median()` para llamar a esas funciones.
### Importar funciones específicas desde un módulo

Para importar una función específica de la biblioteca estándar de Python, puedes usar la palabra clave `from` . Por ejemplo, si quieres importar solo la función `median()` del módulo `statistics`  , puedes escribir `from statistics import median` .

Para importar varias funciones de un módulo, puede separar las funciones que desea importar con una coma. Por ejemplo, `from statistics import mean, median` importa las funciones `mean()` y `median()` del módulo `statistics` .

Un detalle importante a tener en cuenta es que si importa funciones específicas de un módulo, ya no tendrá que especificar el nombre del módulo antes de esas funciones. Puede examinar esto en el siguiente código, que importa específicamente solo las funciones `median()` y `mean()` del módulo de estadísticas y realiza los mismos cálculos que los ejemplos anteriores:

```python
from statistics import mean, median

monthly_failed_attempts = [20, 17, 178, 33, 15, 21, 19, 29, 32, 15, 25, 19]

mean_failed_attempts = mean(monthly_failed_attempts)
print("mean:", mean_failed_attempts)

median_failed_attempts = median(monthly_failed_attempts)
print("median:", median_failed_attempts)
```

Ya no es necesario especificar `statistics.mean()` o `statistics.median()` y en su lugar el código incorpora estas funciones como `mean()` y `median()` .
## Bibliotecas externas

Además de la biblioteca estándar de Python, también puedes descargar bibliotecas externas e incorporarlas a tu código Python. Por ejemplo, anteriormente conociste Beautiful Soup ( `bs4` ) para analizar archivos HTML y NumPy ( `numpy` ) para matrices y cálculos matemáticos. Antes de usarlas en un Jupyter Notebook o en un entorno de Google Colab, primero debes instalarlas.

Para instalar una biblioteca, como `numpy` , en cualquier entorno, puede ejecutar la siguiente línea antes de importar la biblioteca:

```python
pip install numpy
```

Después de instalar una biblioteca, puedes importarla directamente a Python usando la palabra clave `import` de manera similar a cómo la usaste para importar módulos desde la biblioteca estándar de Python. Por ejemplo, después de la instalación de numpy , puedes usar este código para importarla:

```python
import numpy
```
