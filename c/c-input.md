# Ingreso de datos datos en lenguaje C
#sintaxis #c 

---
## Entendiendo la entrada de datos en C

Cuando hablamos de ingresar datos en C, nos referimos a la acción de permitir que el usuario introduzca información desde el teclado para que nuestro programa la procese. Esta interacción entre el usuario y el programa es fundamental para crear aplicaciones dinámicas y útiles.

## La función `scanf()`

La función más común para leer datos desde el teclado en C es `scanf()`. Esta función forma parte de la biblioteca estándar de entrada/salida, `stdio.h`, y su sintaxis básica es la siguiente:

```c
scanf("%tipo_de_dato", &variable);

```
- **"%tipo_de_dato"**: Especifica el tipo de dato que se espera leer (por ejemplo, %d para enteros, %f para flotantes, %c para caracteres).
- **&variable**: Es la dirección de memoria de la variable donde se almacenará el valor leído. El operador `&` se utiliza para obtener la dirección de una variable.

## Ejemplo
```c
#include <stdio.h>

int main() {
    int edad;
    float altura;
    char inicial;

    printf("Ingrese su edad: ");
    scanf("%d", &edad);

    printf("Ingrese su altura: ");
    scanf("%f", &altura);

    printf("Ingrese su inicial: ");
    scanf(" %c", &inicial); // Nota el espacio antes de %c

    printf("Usted tiene %d años, mide %.2f metros y su inicial es %c\n", edad, altura, inicial);

    return 0;
}
```