# Autenticación y autorización con `sudo`
#comandos #linux #ciberseguridad 

---
Puede utilizar sudo con muchas tareas de gestión de autenticación y autorización. Como recordatorio, **la autenticación** es el proceso de verificar quién es alguien, y **la autorización** es el concepto de conceder acceso a recursos específicos en un sistema. Algunos de los comandos clave utilizados para estas tareas son los siguientes:

### **useradd**

El comando `useradd` añade un usuario al sistema. 

Para añadir un usuario con el nombre de usuario de `fgarcia` con `sudo`, introduzca `sudo useradd fgarcia`. Existen opciones adicionales que puede utilizar con `useradd`:

- -**g**: Establece el grupo por defecto del usuario, también llamado su grupo primario
- **-G**: Añade al usuario a grupos adicionales, también llamados grupos suplementarios o secundarios.

Para utilizar la opción `-g`, el grupo primario debe especificarse después de `-g`. Por ejemplo, al introducir `sudo useradd -g security fgarcia` se añade `fgarcia` como nuevo usuario y se asigna que su grupo primario sea `security`.

Para utilizar la opción `-G`, el grupo suplementario debe pasarse al comando después de `-G`. Puede añadir más de un grupo suplementario a la vez con la opción `-G`. Al introducir `sudo useradd -G finance,admin fgarcia` se añade fgarcia como nuevo usuario y se añade a los grupos existentes finance y admin.

### **usermod**

El comando `usermod` modifica las cuentas de usuario existentes. Las mismas opciones `-g` y `-G` del comando `useradd` pueden utilizarse con `usermod` si ya existe un usuario.

Para cambiar el grupo primario de un usuario existente, necesita la opción `-g`. Por ejemplo, si introduce `sudo usermod -g executive fgarcia` cambiará el grupo primario de `fgarcia` por el grupo `executive`.

Para añadir un grupo suplementario para un usuario existente, necesita la opción `-G`. También necesita la opción `-a`, que añade el usuario a un grupo existente y sólo se utiliza con la opción `-G`. Por ejemplo, introduciendo `sudo usermod -a -G marketing fgarcia` añadiría el usuario existente `fgarcia` al grupo suplementario `marketing`.

**Nota:** Al cambiar el grupo suplementario de un usuario existente, si no incluye la opción `-a, -G` sustituirá cualquier grupo suplementario existente por los grupos especificados después de `usermod`. El uso de `-a` con `-G` garantiza que se añadan los nuevos grupos pero que no se sustituyan los grupos existentes.

Existen otras opciones que puede utilizar con `usermod` para especificar cómo desea modificar el usuario, entre las que se incluyen:

- **`-d`**: Cambia el Directorio personal del usuario.

- **`-l`**: Cambia el nombre de usuario.

- **`-L`**: Bloquea la cuenta para que el usuario no pueda registrarse.


La opción siempre va después del comando usermod. Por ejemplo, para cambiar el directorio principal de `fgarciaa` `/home/garcia_f`, introduzca `sudo usermod -d /home/garcia_f fgarcia`. La opción `-d` sigue directamente al comando usermod antes de los otros dos argumentos necesarios.

### **userdel**

El comando `userdel` borra un usuario del sistema. Por ejemplo, si introduce `sudo userdel fgarcia` borrará `fgarcia` como usuario. Tenga cuidado antes de borrar un usuario utilizando este Comando.

El comando `userdel` no borra los archivos del directorio personal del usuario a menos que utilice la opción `-r`. Introducir `sudo userdel -r fgarcia` eliminaría `fgarcia` como usuario y borraría todos los archivos de su directorio personal. Antes de borrar cualquier archivo de usuario, debe asegurarse de que tiene copias de seguridad por si las necesita más adelante.

**Nota**: En lugar de borrar al usuario, podría considerar desactivar su cuenta con `usermod -L`. Esto evita que el usuario se registre mientras le sigue dando acceso a su cuenta y a los permisos asociados. Por ejemplo, si un usuario abandonara una organización, esta opción le permitiría identificar sobre qué archivos tiene la propiedad, de modo que podría mover esta propiedad a otros usuarios.

### **chown**

El comando `chown` cambia la propiedad de un archivo o directorio. Puede utilizar `chown` para cambiar la propiedad del usuario o del grupo. Para cambiar el usuario propietario del archivo `access.txt` a `fgarcia`, introduzca `sudo chown fgarcia access.txt`. Para cambiar el propietario de grupo de `access.txt` a `security`, introduzca `sudo chown :security access.txt`. Debe introducir dos puntos (`:`) antes de `security` para designarlo como nombre de grupo.

De forma similar a `useradd`, `usermod`, y `userdel`, existen opciones adicionales que pueden utilizarse con `chown`.