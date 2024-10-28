# La cláusula WHERE y los operadores básicos
#sql #sintaxis #comandos 

---
## WHERE
Para crear un filtro en SQL, debe utilizar la palabra clave WHERE. WHERE indica la condición para un filtro.

Si necesitara enviar correos electrónicos a empleados con un título de Personal de TI, podría utilizar una consulta como la del siguiente ejemplo. Puede ejecutar este ejemplo para examinar lo que devuelve:
```sql
SELECT firstname, lastname, title, email
FROM employees
WHERE title = 'IT Staff';
```

## Filtrado por patrones

También puede filtrar basándose en un **patrón**. Por ejemplo, puede identificar las entradas que empiezan o terminan con un carácter o caracteres determinados. Filtrar por un patrón requiere incorporar dos elementos más a su cláusula WHERE:

- un comodín
- el operador LIKE

### Comodines

Un **comodín** es un ==carácter especial que puede ser sustituido por cualquier otro carácter==. Dos de los comodines más útiles son el signo de porcentaje (`%`) y el guión bajo (`_`):

- El signo de porcentaje sustituye a cualquier otro carácter.
- El símbolo de subrayado sólo sustituye a otro carácter.

| Patrón | Resultados que podrían devolver |
| ------ | ------------------------------- |
| `a%`   | `apple123, art, a`              |
| `a_`   | `as, an, a7`                    |
| `a__`  | `ant, add, a1c`                 |
| `%a`   | `pizza, Z6ra, a`                |
| `_a`   | `ma, 1a, Ha`                    |
| `%a%`  | `Again, back, a`                |
| `_a_`  | `Car, ban, ea7`                 |
### LIKE

Para aplicar comodines al filtro, debe utilizar el operador `LIKE` en lugar del signo igual (`=`). `LIKE` se utiliza con `WHERE` para buscar un patrón en una columna. Ejemplo:
```sql
SELECT lastname, firstname, title, email
FROM employees
WHERE title LIKE 'IT%';
```