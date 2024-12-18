# Principio de privilegio mínimo
#ciberseguridad #curso-5 #modulo-2

---
El mínimo privilegio es un ==control de seguridad fundamental que respalda la tríada de confidencialidad, integridad y disponibilidad (CID) de la Información==. En esta lectura, aprenderá cómo el principio de privilegio mínimo reduce el riesgo, cómo se implementa habitualmente y por qué debe auditarse de forma rutinaria.
## Limitar el acceso reduce el riesgo
Implementar el principio de privilegio mínimo puede reducir en gran medida el riesgo de incidentes costosos como la filtración de datos:

- Limitando el acceso a la Información sensible
- Reduciendo las posibilidades de modificación, manipulación o pérdida accidental de Datos
- Apoyando la supervisión y administración de sistemas

El mínimo privilegio reduce en gran medida la probabilidad de que un ataque tenga éxito al conectar Recursos específicos a usuarios concretos y poner límites a lo que pueden hacer. Es un control de Seguridad importante que debe aplicarse a cualquier recurso. Definir claramente quién o quiénes son sus usuarios suele ser el primer paso para implementar el mínimo privilegio de forma eficaz.

**Nota:** El privilegio mínimo está estrechamente relacionado con otro principio de seguridad fundamental, la separación de _funciones, un ==concepto de seguridad que divide las tareas y responsabilidades entre distintos usuarios para evitar que un solo usuario tenga el control absoluto de las funciones críticas de la empresa==. 

## Determinar el acceso y la autorización
Estos son los tipos más comunes de cuentas de usuario:

- Las **cuentas de invitado** se proporcionan a usuarios externos que necesitan acceder a una red interna, como clientes, contratistas o socios comerciales.
- Las **cuentas de usuario** se asignan al personal en función de sus funciones laborales.
- Las **cuentas de servicio** se conceden a aplicaciones o software que necesitan interactuar con otro software de la red.
- Las **cuentas con privilegios** tienen permisos elevados o acceso administrativo.
## Auditoría de los privilegios de las cuentas
Establecer las cuentas de usuario adecuadas y asignarles los privilegios apropiados es un primer paso útil. Auditar periódicamente esas cuentas es una parte clave para mantener seguros los sistemas de su empresa.

Existen tres enfoques comunes para auditar las cuentas de usuario:

- Auditorías de uso
- Auditorías de privilegios
- Auditorías de cambio de cuentas.
### Auditorías de uso
Al realizar una auditoría de uso, el equipo de seguridad revisará a qué recursos accede cada cuenta y qué hace el usuario con el recurso. Las auditorías de uso pueden ayudar a determinar si los usuarios están actuando de acuerdo con las políticas de Seguridad de una organización. También pueden ayudar a identificar si un usuario tiene permisos que pueden ser revocados porque ya no se utilizan.
### Auditorías de privilegios
Los usuarios tienden a acumular con el tiempo más privilegios de acceso de los que necesitan, un problema conocido como **_acumulación de privilegios_**. Esto puede ocurrir si un empleado recibe un ascenso o cambia de equipo y sus obligaciones laborales cambian. Las auditorías de privilegios evalúan si la función de un usuario está en consonancia con los Recursos a los que tiene acceso.
### Auditorías de cambio de cuentas
Los servicios de directorio de cuentas mantienen registros y bitácoras asociados a cada usuario. Los cambios en una cuenta suelen guardarse y pueden utilizarse para auditar el Directorio en busca de actividades sospechosas, como múltiples intentos de cambiar la contraseña de una cuenta. Realizar auditorías de cambios en las cuentas ayuda a garantizar que todos los cambios en las cuentas son realizados por usuarios autorizados.