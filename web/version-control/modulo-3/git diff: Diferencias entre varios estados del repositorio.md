# git diff: Diferencias entre varios estados del repositorio

Creado: 28 de septiembre de 2024 9:27

---

El comando `git diff` se utiliza para mostrar las diferencias entre varios estados del repositorio en Git. Es una herramienta poderosa para revisar cambios antes de confirmarlos (*commit*), comparar ramas o ver las diferencias entre commits específicos.

### Usos comunes de `git diff`:

1. **Ver los cambios no confirmados**:
Si has modificado archivos pero aún no los has agregado al área de *staging*, `git diff` te mostrará las diferencias entre la versión actual y la última versión confirmada (commit más reciente).
    
    ```bash
    git diff
    ```
    
2. **Ver los cambios preparados para commit**:
Si has agregado archivos al área de *staging* usando `git add`, pero aún no los has confirmado, puedes ver las diferencias de lo que está en *staging* con respecto al commit más reciente:
    
    ```bash
    git diff --staged
    ```
    
3. **Comparar dos ramas**:
Para comparar los cambios entre dos ramas, por ejemplo, `main` y `develop`:
    
    ```bash
    git diff main develop
    ```
    
4. **Comparar un archivo con un commit anterior**:
Para ver cómo ha cambiado un archivo específico entre el commit actual y uno anterior, puedes usar el hash del commit:
    
    ```bash
    git diff <hash_del_commit> <nombre_del_archivo>
    ```
    
5. **Ver los cambios entre dos commits específicos**:
Si quieres ver qué cambios se introdujeron entre dos commits, puedes usar los hashes de los commits:
    
    ```bash
    git diff <hash1> <hash2>
    ```
    
6. **Ver el resumen de las diferencias**:
Si solo quieres un resumen (sin los detalles línea por línea), puedes usar la opción `-stat`:
    
    ```bash
    git diff --stat
    ```
    

### Ejemplo:

Supongamos que modificas un archivo `archivo.txt`, pero aún no lo has confirmado. Ejecutar `git diff` te mostrará algo como esto:

```bash
diff --git a/archivo.txt b/archivo.txt
index e69de29..d95f3ad 100644
--- a/archivo.txt
+++ b/archivo.txt
@@ -1 +1 @@
-Hola mundo
+Hola Git
```

Esto muestra las diferencias línea por línea: en este caso, has cambiado la línea "Hola mundo" por "Hola Git".

`git diff` es muy útil para revisar los cambios que se han hecho antes de proceder a un commit, un merge, o simplemente para analizar el historial de modificaciones.