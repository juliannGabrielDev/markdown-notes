# Filtrado SQL frente a filtrado Linux
#sql #teoria #ciberseguridad

---
En esta lectura, explorará las diferencias entre ambas herramientas en lo que respecta al filtrado. También aprenderá que una forma de acceder a SQL es a través de la línea de comandos de Linux.

## Acceso a SQL

Existen muchas interfaces para acceder a SQL y muchas versiones diferentes de SQL. Una forma de acceder a SQL es a través de la línea de comandos de Linux.

Para acceder a SQL desde Linux, debe escribir un comando para la versión de SQL que desee utilizar. Por ejemplo, si desea acceder a SQLite, puede introducir el comando `sqlite3` en la línea de comandos.

Después de esto, cualquier comando que escriba en la línea de comandos se dirigirá a SQL en lugar de a los comandos de Linux.
## Diferencias entre el filtrado de Linux y SQL

Aunque tanto Linux como SQL le permiten filtrar datos, existen algunas diferencias que afectan a cuál debe elegir.

### Propósito

==Linux filtra datos en el contexto de archivos y directorios de un sistema de computadoras==. Se utiliza para tareas como la búsqueda de archivos específicos, la manipulación de permisos de archivo o la gestión de procesos.

==SQL se utiliza para filtrar datos dentro de un sistema de gestión de bases de datos==. Se utiliza para consultar y manipular datos almacenados en tablas y recuperar información específica basada en criterios definidos.

### Sintaxis

Linux utiliza varios comandos y opciones de línea de comandos específicos para cada herramienta de filtrado. La sintaxis varía en función de la herramienta y el propósito. Algunos ejemplos de comandos de Linux son find, sed, cut, e grep

SQL utiliza el **Lenguaje de Consulta Estructurada (SQL)**, un lenguaje estandarizado con palabras clave y cláusulas específicas para filtrar datos en diferentes bases de datos SQL. Algunos ejemplos de palabras clave y cláusulas SQL son WHERE, SELECT, JOIN

### Estructura

SQL ofrece mucha más estructura que Linux, que es más libre y no tan ordenado.

Por ejemplo, si quisiera acceder a un registro de los intentos de inicio de sesión de los empleados, SQL tendría cada registro separado en columnas. Linux imprimiría los Datos como una línea de texto sin esta organización. Como resultado, Seleccionar una columna específica para analizar sería más fácil y eficiente en SQL.

En términos de estructura, SQL proporciona resultados que son más fácilmente legibles y que pueden ajustarse más rápidamente que cuando se utiliza Linux.

### Unir tablas

Algunas decisiones relacionadas con la seguridad requieren información de diferentes tablas. ==SQL permite al analista unir varias tablas al devolver los datos==. Linux no tiene esa misma funcionalidad; no permite que los datos se conecten a otra Información en su computadora. Esto es más restrictivo para un analista que revisa registros de Seguridad.

### Mejores usos

COMO analista de Seguridad, es importante entender cuándo puede utilizar cada herramienta. Aunque SQL tiene una estructura más organizada y le permite unir tablas, esto no significa que no haya situaciones que requieran que filtre datos en Linux.

Muchos de los datos utilizados en ciberseguridad se almacenarán en un formato de base de datos que funcione con SQL. Sin embargo, otros registros pueden estar en un formato que no sea compatible con SQL. Por ejemplo, si los datos están almacenados en un archivo de texto, no podrá buscar en ellos con SQL. En esos casos, es útil saber cómo filtrar en Linux.