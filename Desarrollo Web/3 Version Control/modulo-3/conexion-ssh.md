# Conexión a GitHub a través de SSH

Creado: 26 de septiembre de 2024 2:26

---

Si planea utilizar Github desde su dispositivo local, la forma recomendada de autenticarse es utilizando Secure Shell, o SSH para abreviar. Esto requiere la creación de claves: una pública y otra privada. La ventaja de utilizar SSH es que no necesita introducir sus credenciales cuando interactúa con el repositorio remoto. Las claves se generan y almacenan en su máquina local y luego la clave pública se copia en el servidor de Github. Cuando termine la configuración, todas las operaciones se autenticarán utilizando las claves.

### Generar claves SSH

El proceso es el mismo tanto para Windows como para Mac. En Windows, puede utilizar el terminal Git Bash y en Mac, funcionará el terminal estándar.

1. Abra el terminal
2. Introduzca lo siguiente:
	```bash 
	ssh-keygen -t ed25519 -C "your@email.com"
	```
3. Sustituya el correo electrónico por el suyo propio y pulse Intro.
4. Le pedirá que introduzca una contraseña. Pulse intro para omitir la configuración de una contraseña y haga lo mismo para volver a introducir la misma frase de contraseña.

```
Generating public/private ed25519 key pair.
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in ./ssh/private_key.
Your public key has been saved in ./ssh/public_key.pub.
The key fingerprint is:
SHA256:UDQI5N1FL3QSq7Gj1o12mkr9Me7qGMZAeE1s9BWIln4 your@email.com
The key's randomart image is:
+--[ED25519 256]--+
|   .o+o=+oOo.    |
|   o +B+.= =     |
|  . +++ + o .    |
|   o  ..E+ .     |
|    .  .S        |
|     o + +       |
|      B = =      |
|     + + * o     |
|      oo=o+      |
+----[SHA256]-----+
```

1. Una vez que haya confirmado se generará lo anterior para confirmar que las claves han sido creadas.
2. Ambas claves se almacenarán en la carpeta .ssh.
3. Para añadir nuestra clave a Github, necesitamos obtener una copia de la clave pública que siempre se identifica como .pub en su directorio local.

Encuentre el nombre del archivo de claves utilizando el comando de abajo.
```bash
ls ~/.ssh/
```
A continuación, utilice el comando de abajo para copiar el archivo, sustituyendo SU CLAVE por el nombre del archivo de claves de su dispositivo. Este paso difiere entre Windows y Mac.

Para mac:
```
pbcopy < ~/.ssh/<YOUR KEY>.pub
```
Para Windows y Linux:
```bash
cat ~/.ssh/<YOUR KEY>.pub | clip
```

## Añadir sus claves a Github

Ahora necesitamos añadir nuestra clave pública a Github para conceder acceso a los repositorios que creemos.

**Paso 1:** Inicie sesión en Github

**Paso 2:** Haga clic en el icono de perfil en la parte superior derecha de la pantalla y seleccione Configuración.

**Paso 3:** En la pantalla de Configuración, en el lado izquierdo bajo la sección de Acceso, haga clic en SSH y Claves GPG.

**Paso 4:** Haga clic en el botón Nueva clave SSH en verde en la parte derecha de la pantalla.

**Paso 5:** Introduzca un título y pegue la clave pública que copió anteriormente.

**Paso 6:** Haga clic en el botón **Add SSH key**.

Ahora está listo para acceder a Github a través de SSH.

## Accediendo a Repositorios

Cuando acceda a un repositorio y utilice la autenticación SSH, asegúrese de utilizar siempre la dirección SSH del repositorio.
![Accediendo a Repositorios](github-ssh-conexion.webp)