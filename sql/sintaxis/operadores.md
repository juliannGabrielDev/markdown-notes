# Operadores para filtrar fechas y números
#comandos #sql #sintaxis 

---
En SQL, el filtrado de datos numéricos y de fecha y hora suele implicar operadores. Puede utilizar los siguientes operadores en sus filtros para asegurarse de que devuelve sólo las filas que necesita:

| Operador | Descripción       |
| -------- | ----------------- |
| `<`      | menor que         |
| `>`      | mayor que         |
| `=`      | igual a           |
| `<=`     | menor o igual que |
| `>=`     | mayor o igual que |
| `<>`     | no igual a        |
```sql
SELECT firstname, lastname, birthdate
FROM employees
WHERE birthdate > '1970-01-01';
```
