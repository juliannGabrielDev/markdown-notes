# Filtros con AND, OR y NOT
#sql #comandos #sintaxis 

---
## AND
En primer lugar, `AND` se utiliza para filtrar a partir de dos condiciones. `AND` especifica que ambas condiciones deben cumplirse simultáneamente.
```sql
SELECT firstname, lastname, email, country, supportrepid
FROM customers
WHERE supportrepid = 5 AND country = 'USA';
```

## OR
El operador `OR` también conecta dos condiciones, pero `OR` especifica que puede cumplirse cualquiera de ellas. Devuelve resultados en los que se cumple la primera condición, la segunda o ambas.
```sql
SELECT firstname, lastname, email, country
FROM customers
WHERE country = 'Canada' OR country = 'USA';
```

## NOT
A diferencia de los dos operadores anteriores, el operador `NOT` sólo funciona con una única condición, y no con varias. El operador `NOT` niega una condición. Esto significa que SQL devuelve todos los registros que no coinciden con la condición especificada en la consulta.
```sql
SELECT firstname, lastname, email, country
FROM customers
WHERE NOT country = 'USA';
```
SQL devuelve todas las entradas en las que los clientes no son de EE.UU..

**Consejo profesional:** Otra forma de encontrar valores que no sean iguales a un determinado valor es utilizando el operador `<>` o el operador `!=`. Por ejemplo, `WHERE country <> 'USA'` y `WHERE country != 'USA'` son los mismos filtros que `WHERE NOT country = 'USA'`.