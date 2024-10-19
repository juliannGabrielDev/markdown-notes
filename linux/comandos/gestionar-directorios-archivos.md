# Gestionar direcciones y archivos
#comandos #linux 

---
## Creación y modificación de directorios

| **Comandos** | **Significado**  | **Descripción**                                                                                                                                                                                                                      |
| ------------ | ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **`mkdir`**  | make directory   | El comando `mkdir` ==crea un nuevo directorio==. Puede proporcionar el nuevo directorio como una ruta de archivo absoluta, que comienza desde la raíz, o como una ruta de archivo relativa, que comienza desde su directorio actual. |
| **`rmdir`**  | remove directory | El comando `rmdir` elimina un directorio. **Nota**: El comando rmdir ==no puede eliminar directorios con archivos== o subdirectorios en su interior.                                                                                 |
## Creación y modificación de archivos

| **Comando** | **Significado** | **Descripción**                                                                                                                                     |
| ----------- | --------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| **`touch`** | touch           | El comando `touch` crea un nuevo archivo. Este archivo no tendrá ningún contenido en su interior.                                                   |
| **`rm`**    | remove          | El comando `rm` elimina, o borra, un archivo. Este comando debe utilizarse con cuidado porque no es fácil recuperar los archivos borrados con `rm`. |

| **Comando** | **Significado** | **Descripción**                                                                                                                                 |
| ----------- | --------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| **`mv`**    | move            | El comando `mv` mueve un archivo o directorio a una nueva ubicación.                                                                            |
| **`cp`**    | copy            | El comando `cp` copia un archivo o directorio en una nueva ubicación. **Nota**: El comando mv también puede utilizarse para renombrar archivos. |

## Editor de texto nano

**nano** es un ==editor de archivos de línea de comandos que está disponible por defecto en muchas distribuciones de Linux==. Muchos principiantes lo encuentran fácil de usar, y es muy utilizado en la profesión de Seguridad. Puede realizar múltiples tareas básicas en nano, como crear nuevos archivos y modificar su contenido.

También **puede crear un nuevo archivo en nano** introduciendo nano seguido de un nuevo nombre de archivo.

==Dado que no existe una función de autoguardado en nano, es importante que guarde su trabajo antes de salir==. Para guardar un archivo en nano, utilice el acceso directo del teclado **Ctrl + O**. Se le pedirá que confirme el nombre del archivo antes de guardarlo. Para salir de nano, utilice el acceso directo del teclado **Ctrl + X**.

## Redirección de la salida estándar

Hay una forma adicional de escribir en archivos. Además de la tubería (`|`), también puede utilizar los operadores corchete de ángulo recto (`>`) y doble corchete de ángulo recto (`>>`) para redirigir la salida estándar.

Cuando se utilizan con `echo`, los operadores `>` y `>>` pueden emplearse para enviar la salida de echo a un archivo especificado en lugar de a la pantalla. 

La diferencia entre ambos es que `>` sobrescribe el archivo existente, y `>>` añade su contenido al final del archivo existente en lugar de sobrescribirlo. 

El operador > debe utilizarse con cuidado, porque no es fácil recuperar los archivos sobrescritos.