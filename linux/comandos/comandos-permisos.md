# Comandos de permisos
#linux #comandos 

---
## Permisos de lectura

En Linux, los permisos se representan con una cadena de 10 caracteres(**drwxrwxrwx**) . Los permisos incluyen:

- **leer (r)**: para archivos, esta es la capacidad de leer el contenido del archivo; para directorios, esta es la capacidad de leer todo el contenido en el directorio incluyendo tanto archivos como subdirectorios

- **escribir (w)**: para archivos, esta es la capacidad de hacer modificaciones en el contenido del archivo; para directorios, esta es la capacidad de crear nuevos archivos en el directorio

- **ejecutar (x)**: para los archivos, es la capacidad de ejecutar el archivo si se trata de un programa; para los directorios, es la capacidad de entrar en el directorio y acceder a sus archivos.

Estos permisos se otorgan a estos tipos de propietarios:

- **usuario**: el propietario del archivo
- **grupo**: un grupo mayor del que forma parte el propietario
- **otro**: todos los demás usuarios del sistema.

## Exploración de los permisos existentes

Puede utilizar el comando `ls` para investigar quién tiene permisos sobre archivos y directorios. 

Existen opciones adicionales que puede añadir al comando `ls` para que su comando sea más específico. Algunas de estas opciones proporcionan detalles sobre los permisos. He aquí algunas opciones de ls importantes para los analistas de Seguridad:

- `ls -a`: Muestra los archivos ocultos. Los archivos ocultos comienzan con un punto (.) al principio.

- `ls -l`: Muestra los permisos de archivos y directorios. También muestra otra información adicional, como el nombre del propietario, el grupo, el tamaño del archivo y la hora de la última modificación.

- `ls -la`: Muestra los permisos de archivos y directorios, incluidos los archivos ocultos. Es una combinación de las otras dos opciones.
## Cambio de permisos

El **principio de privilegio mínimo** es el concepto de conceder sólo el acceso y la autorización mínimos necesarios para completar una tarea o función. En otras palabras, los usuarios no deben tener privilegios que vayan más allá de lo necesario. No seguir el principio de privilegio mínimo puede crear riesgos de Seguridad.

El comando chmod puede ayudarle a gestionar esta autorización. El comando chmod cambia los permisos de archivos y directorios.
### **Uso de chmod**

El comando `chmod` requiere dos argumentos. El primer argumento indica cómo cambiar los permisos, y el segundo argumento indica el archivo o directorio para el que desea cambiar los permisos. Por ejemplo, el siguiente comando añadiría todos los permisos a `login_sessions.txt`:

`chmod u+rwx,g+rwx,o+rwx login_sessions.txt`

Si quisiera quitar todos los permisos, podría utilizar

`chmod u-rwx,g-rwx,o-rwx login_sessions.txt`

Otra forma de asignar estos permisos es utilizar el signo igual `(=)` en este primer argumento. El uso de `=` con `chmod` establece, o asigna, los permisos exactamente como se especifican. Por ejemplo, el siguiente comando establecería permisos de lectura para login_sessions.txt para usuario, grupo y otros:

`chmod u=r,g=r,o=r login_sessions.txt`

Este Comando sobrescribe los permisos existentes. Por ejemplo, si el usuario tenía previamente permisos de escritura, estos permisos de escritura se eliminan después de que usted especifique sólo permisos de lectura con `=`.

La siguiente tabla repasa cómo se utiliza cada carácter dentro del primer argumento de `chmod`:

| **Carácter** | **Descripción**                                             |
| ------------ | ----------------------------------------------------------- |
| **`u`**      | Indica que se realizarán cambios en los permisos de usuario |
| **`g`**      | Indica que se realizarán cambios en los permisos de grupo   |
| **`o`**      | Indica que se realizarán cambios en otros permisos          |
| **`+`**      | Añade permisos al usuario, grupo u otro                     |
| **`-`**      | Elimina permisos del usuario, grupo u otro                  |
| **`=`**      | Asigna permisos al usuario, grupo u otro.                   |

**Nota:** Cuando hay cambios de permisos a más de un tipo de propietario, se necesitan comas para separar los cambios para cada tipo de propietario. No debe añadir espacios después de esas comas.