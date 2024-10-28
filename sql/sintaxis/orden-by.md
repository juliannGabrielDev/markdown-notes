# ORDEN BY
#sql #comandos #sintaxis 

---
Las tablas de las bases de datos suelen ser muy complicadas, y aquí es donde resultan útiles otras palabras clave de SQL. **ORDER BY** es una palabra clave importante para organizar los datos que extrae de una tabla.

==**ORDER BY** secuencia los registros devueltos por una consulta en función de una columna o columnas especificadas==. Puede ser en orden ascendente o descendente.
### Ordenación ascendente

Para utilizar la palabra clave **ORDER BY**, escríbala al final de la consulta y especifique una columna en la que basar la ordenación. En este ejemplo, SQL devolverá las columnas `customerid`, `city` y `country` de la tabla `customers`, y los registros se ordenarán por la columna `city`:

```sql
SELECT customerid, city, country
FROM customers
ORDER BY city;
```
### Ordenación descendente

También puede utilizar **ORDER BY** con la palabra clave **DESC** para ordenar en orden descendente. La palabra clave **DESC** ==indica a SQL que ordene los números de mayor a menor, o alfabéticamente de la Z a la A==. 

```sql
SELECT customerid, city, country
FROM customers
ORDER BY city DESC;
```
### Ordenación basada en varias columnas

También puede elegir varias columnas por las que ordenar. Por ejemplo, puede elegir primero la columna `country` y después la columna `city`. A continuación, SQL ordena la salida por `country`, y para las filas con el mismo `country`, las ordena basándose en `city`. Puede ejecutar esto para explorar cómo SQL muestra esto:

```sql
SELECT customerid, city, country
FROM customers
ORDER BY country, city;
```