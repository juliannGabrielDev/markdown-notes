# BETWEEN
#sintaxis #comandos #sql 

---
Otro operador utilizado tanto para datos numéricos como para datos de fecha y hora es el operador `BETWEEN`. `BETWEEN` filtra por números o fechas dentro de un rango.
```sql
SELECT firstname, lastname, hiredate
FROM employees
WHERE hiredate BETWEEN '2002-01-01' AND '2003-01-01';
```
**Nota:** El operador `BETWEEN` es inclusivo. Esto significa que los registros con un `hiredate` del 1 de enero de 2002 o del 1 de enero de 2003 se incluyen en los resultados de la consulta anterior.