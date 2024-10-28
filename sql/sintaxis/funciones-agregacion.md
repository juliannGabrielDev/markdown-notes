# Funciones de Agregación
#sintaxis #sql #comandos 

---
En SQL, las funciones de **agregación** ==son funciones que realizan un cálculo sobre varios puntos de datos y devuelven el resultado del cálculo==. Los datos reales no se devuelven.

Existen varias funciones de agregación que realizan diferentes cálculos:
- **`COUNT`** devuelve un único número que representa el número de filas devueltas por la consulta.
- **`AVG`** devuelve un único número que representa la media de los datos numéricos de una columna.
- **`SUM`** devuelve un único número que representa la suma de los datos numéricos de una columna.
### Sintaxis de la función de agregación
Para utilizar una función de agregación, coloque la palabra clave correspondiente después de la palabra clave `SELECT` y, a continuación, entre paréntesis, indique la columna sobre la que desea realizar el cálculo.
```sql
SELECT COUNT(firstname)
FROM customers;
```