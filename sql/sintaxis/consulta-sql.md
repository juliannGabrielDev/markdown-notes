# Consulta de una base de datos
#comandos #linux #sql #ciberseguridad 

---
## Consulta SQL básica

Hay dos palabras clave esenciales en cualquier consulta SQL: **SELECT** y **FROM**. Utilizará estas palabras clave cada vez que desee consultar una base de datos SQL. Utilizarlas juntas ayuda a SQL a identificar qué datos necesita de una base de datos y la tabla de la que los devuelve.

En el vídeo se muestra esta consulta SQL:

```sql
SELECT employee_id, device_id
FROM employees;
```

En las lecturas y los cuestionarios, este curso utiliza una base de datos de muestra denominada **base de datos Chinook** para ejecutar consultas. La base de datos Chinook incluye datos que podrían crearse en una empresa de medios digitales. Un analista de seguridad empleado por esta empresa podría necesitar consultar estos datos. Por ejemplo, la base de datos contiene once tablas, entre ellas una tabla employees, una tabla customers y una tabla invoices. Estas tablas incluyen datos como nombres y direcciones.
### SELECT

La palabra clave **SELECT** indica qué columnas debe devolver. Por ejemplo, puede devolver la columna customerid de la base de datos Chinook con:
`SELECT customerid`

También puede seleccionar varias columnas separándolas con una coma. Por ejemplo, si desea devolver las columnas `customerid` y `city`, deberá escribir `SELECT customerid, city`.

Si desea devolver todas las columnas de una tabla, puede seguir la palabra clave SELECT con un asterisco (`*`). La primera línea de la consulta será `SELECT *`.

> [!CAUTION]
> Aunque las tablas que consultará en este curso son relativamente pequeñas, el uso de `SELECT *` puede no ser aconsejable cuando trabaje con bases de datos y tablas de gran tamaño; en esos casos, la salida final puede ser difícil de entender y su ejecución puede resultar lenta.
### FROM

La palabra clave **SELECT** siempre va acompañada de la palabra clave **FROM**. **FROM** indica qué tabla debe consultarse. Para utilizar la palabra clave FROM, debe escribirla después de la palabra clave **SELECT**, a menudo en una nueva línea, y seguirla con el nombre de la tabla que está consultando. Si desea devolver todas las columnas de la tabla customers, puede escribir:

```sql
SELECT *
FROM customers;
```

Si desea terminar la consulta aquí, ponga un punto y coma (`;`) al final para indicar a SQL que se trata de la consulta completa.

>[!TIP]
>Los saltos de línea no son necesarios en las consultas SQL, pero a menudo se utilizan para facilitar la comprensión de la consulta. Si lo prefiere, también puede escribir la consulta anterior en una sola línea como:
>`SELECT * FROM customers;`
