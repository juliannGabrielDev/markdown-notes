# Blame

Creado: 28 de septiembre de 2024 15:21

---

El comando `git blame` es una herramienta de Git que te permite ver el historial de cambios de cada línea de un archivo, identificando qué usuario hizo cada modificación y cuándo la hizo. Es muy útil cuando quieres rastrear la autoría o el origen de una línea específica de código o texto en un archivo.

### Sintaxis básica:

```bash
git blame <archivo>
```

### ¿Qué información muestra `git blame`?

Cuando ejecutas `git blame <archivo>`, obtienes una lista donde cada línea del archivo está acompañada de:

1. **SHA-1 del commit**: El identificador único del commit donde esa línea fue modificada por última vez.
2. **Autor**: La persona que realizó ese cambio.
3. **Fecha y hora**: Cuándo se hizo el cambio.
4. **Número de línea en el archivo**: La línea actual en el archivo junto con la línea del archivo original donde ocurrió el cambio.

### Ejemplo de salida:

```bash
e735ab1a (Julián Gabriel 2023-08-24 15:32:18 +0200  1) #include <stdio.h>
e735ab1a (Julián Gabriel 2023-08-24 15:32:18 +0200  2) int main() {
c9f1b5f2 (María Pérez   2023-09-01 12:42:11 +0200  3)     printf("Hola Mundo\n");
e735ab1a (Julián Gabriel 2023-08-24 15:32:18 +0200  4)     return 0;
e735ab1a (Julián Gabriel 2023-08-24 15:32:18 +0200  5) }
```

### Casos de uso de `git blame`:

1. **Rastrear bugs**: Si encuentras un error en el código, puedes usar `git blame` para ver quién lo introdujo y cuándo. Esto ayuda a identificar la historia detrás de una línea y puede ayudar a entender el contexto de por qué se escribió de cierta manera.
2. **Auditoría del código**: Al ver qué persona cambió qué línea y cuándo, es más fácil hacer una auditoría del código y ver el historial detallado de cambios.
3. **Colaboración**: Si tienes preguntas sobre una parte del código, puedes saber quién es la persona responsable de un cambio y consultarle directamente.

### Opciones útiles de `git blame`:

- **`L <inicio>,<fin>`**: Para ver quién cambió líneas específicas, por ejemplo, de la línea 10 a la 20:
    
    ```bash
    git blame -L 10,20 <archivo>
    ```
    
- **`C`**: Sirve para seguir líneas movidas o copiadas de otros archivos.
- **`e`**: Muestra los correos electrónicos de los autores en lugar de los nombres.
- **`-since` y `-until`**: Puedes limitar la búsqueda a un rango de tiempo específico:

```bash
git blame --since=2.weeks.ago <archivo>
```

En resumen, `git blame` es una poderosa herramienta para investigar el historial de cada línea en un archivo, lo que te ayuda a entender la evolución del código o texto en tu proyecto.
![Sintaxis de salida blame](blame.webp)