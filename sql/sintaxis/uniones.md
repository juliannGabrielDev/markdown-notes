# Comparar tipos de uniones
#sql #comandos #sintaxis 

---
## INNER JOIN
El primer tipo de unión que puede realizar es una unión interna. `INNER JOIN` devuelve las filas que coinciden en una columna especificada que existe en más de una tabla.
![INNER JOIN](img/inner-join.webp)
Sólo devuelve las filas en las que hay una coincidencia, pero al igual que otros tipos de uniones, devuelve todas las columnas especificadas de todas las tablas unidas. Por ejemplo, si la consulta une dos tablas con `SELECT` *, se devuelven todas las columnas de ambas tablas.

**Nota:** Si una columna existe en las dos tablas, se devuelve dos veces cuando se utiliza `SELECT *`.
```sql
SELECT *
FROM employees
INNER JOIN machines ON employees.device_id = machines.device_id;
```
Además de seleccionar todas las columnas, puede seleccionar sólo determinadas columnas. Por ejemplo, si sólo desea que la unión devuelva las columnas `username`, `operating_system` y `device_id`, puede escribir esta consulta:
```sql
SELECT username, operating_system, employees.device_id
FROM  employees
INNER JOIN machines ON employees.device_id = machines.device_id;
```
**Nota**: En la consulta de ejemplo, `username` y `operating_system` sólo aparecen en una de las dos tablas, por lo que se escriben sólo con el nombre de la columna. En cambio, como `device_id` aparece en las dos tablas, es necesario indicar cuál devolver especificando tanto el nombre de la tabla como el de la columna (`employees.device_id`).
## LEFT JOIN
Al unir dos tablas, `LEFT JOIN` devuelve todos los registros de la primera tabla, pero sólo devuelve las filas de la segunda tabla que coincidan en una columna especificada.
![LEFT JOIN](img/left-join.webp)
La sintaxis para utilizar `LEFT JOIN` se demuestra en la siguiente consulta:
```sql
SELECT *
FROM employees
LEFT JOIN machines ON employees.device_id = machines.device_id;
```
Como con todas las uniones, debe especificar la primera tabla o tabla izquierda como la tabla que viene después de `FROM` y la segunda tabla o tabla derecha como la tabla que viene después de `LEFT JOIN`. En la consulta del ejemplo, como `employees` es la tabla izquierda, se devuelven todos sus registros. Sólo se devuelven los registros que coinciden en la columna `device_id` de la tabla derecha, machines.
## RIGHT JOIN
Al unir dos tablas, `RIGHT JOIN` devuelve todos los registros de la segunda tabla, pero sólo devuelve las filas de la primera tabla que coinciden en una columna especificada.
![RIGHT JOIN](img/right-join.webp)
La siguiente consulta demuestra la sintaxis de RIGHT JOIN:
```sql
SELECT *
FROM employees
RIGHT JOIN machines ON employees.device_id = machines.device_id;
```
`RIGHT JOIN` tiene la misma sintaxis que `LEFT JOIN`, con la única diferencia de que la palabra clave `RIGHT JOIN` indica a SQL que produzca una salida diferente. La consulta devuelve todos los registros de `machines`, que es la segunda tabla o tabla derecha. Sólo se devuelven los registros coincidentes de `employees`, que es la primera tabla o izquierda.
## FULL OUTER JOIN
`FULL OUTER JOIN` devuelve todos los registros de ambas tablas. Puede considerarlo como una forma de unir completamente dos tablas.
![FULL OUTER JOIN](img/full-outer-join.webp)
Puede revisar la sintaxis para utilizar `FULL OUTER JOIN` en la siguiente consulta:
```sql
SELECT *
FROM employees
FULL OUTER JOIN machines ON employees.device_id = machines.device_id;
```
Los resultados de una consulta `FULL OUTER JOIN` incluyen todos los registros de ambas tablas. De forma similar a `INNER JOIN`, el orden de las tablas no cambia los resultados de la consulta.
## Claves

- Cuando se trabaja en SQL, existen múltiples formas de unir tablas. Todas las uniones devuelven los registros que coinciden en una columna especificada. 
- **`INNER JOIN`** devolverá sólo estos registros. 
- Las uniones externas también devuelven todos los demás registros de una o ambas tablas. 
- **`LEFT JOIN`** devuelve todos los registros de la primera tabla o tabla izquierda.
- **`RIGHT JOIN`** devuelve todos los registros de la segunda tabla o tabla derecha.
- **`FULL OUTER JOIN`** devuelve todos los registros de ambas tablas.