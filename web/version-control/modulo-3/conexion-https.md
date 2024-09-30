# Conexión a GitHub a través de HTTPS

Creado: 26 de septiembre de 2024 2:26

---

La conexión a GitHub a través de **HTTPS** sirve para interactuar de forma segura con los repositorios remotos alojados en GitHub. Al usar HTTPS, las comunicaciones entre tu máquina local y GitHub están encriptadas, lo que asegura que los datos no puedan ser interceptados o manipulados durante el intercambio.

Un Token de Acceso Personal es una contraseña especial que usted utiliza en lugar de la contraseña real de su cuenta. Cuando haya terminado de utilizar el token, puede revocarlo para que ya no pueda ser utilizado. También es posible fijar un tiempo de caducidad para el token. Esto ayuda a mantener la seguridad de su cuenta.

### Generar un Token de Acceso Personal

Ahora necesitamos configurar nuestro Token de Acceso Personal.

# Paso 1:

Inicie sesión en Github.

# Paso 2:

Haga clic en el icono de perfil en la parte superior derecha de la pantalla y seleccione Configuración.

# Paso 3:

En la pantalla de Configuración, en el lado izquierdo haga clic en Configuración de Desarrollador.

# Paso 4:

En la pantalla de Configuración del desarrollador, haga clic en Tokens **de acceso personal**. Debajo, haga clic en **Fichas (clásicas)**. A continuación, haga clic en el botón **Generar** **nuevo token** y seleccione **Generar nuevo to**ken (clásico).

# Paso 5

En la página Nuevo token de acceso personal, introduzca un nombre para el token y un tiempo de caducidad. Si desea revocar manualmente el token, establezca el tiempo de caducidad en **No Expiration**.

# Paso 6

En ámbitos, seleccione **repo**.

# Paso 7

Desplácese hasta el final de la página y haga clic en**Generate token**.

# Paso 8

El token ya está generado. Asegúrese de copiar y tomar nota del token, ya que se ocultará al salir de la página. Este token puede utilizarse ahora cuando se conecte a un repositorio a través de HTTPS.

> ***Nota:** Si pierde el token, puede borrar el antiguo y crear uno nuevo.*
> 

# Accediendo a repositorios

Cuando acceda a un repositorio y utilice la autenticación HTTPS, asegúrese de que tiene acceso/permiso para conectarse, y entonces sólo utilice la dirección HTTPS para el propio repositorio Git. 
![Accediendo a repositorios](img/github-http-conexion.png)