# Uso responsable de sudo
#Ciberseguridad #linux #Teoría 

---
El comando `sudo` es importante para los analistas de Seguridad porque ==permite a los usuarios tener permisos elevados sin poner en riesgo el sistema== ejecutando comandos como usuario raíz.

---
Para gestionar la autorización y autenticación, necesita ser un **usuario raíz,** o un usuario con privilegios elevados para modificar el sistema. Al usuario raíz también se le puede llamar **"superusuario"**. Usted se convierte en usuario raíz iniciando sesión como usuario root. Sin embargo, ==ejecutar comandos como usuario raíz no es recomendable en Linux porque puede crear Riesgos de Seguridad si actores maliciosos comprometen esa cuenta==. También es fácil cometer errores irreversibles, y el sistema no puede rastrear quién ejecutó un comando. Por estas razones, en lugar de registrarse como usuario raíz, se recomienda utilizar `sudo` en Linux cuando necesite privilegios elevados.

El comando `sudo` ==otorga temporalmente permisos elevados a usuarios específicos==. El nombre de este comando proviene de **"superuser do"** Los usuarios deben tener acceso en un archivo de configuración para utilizar sudo. 

Este archivo se llama "archivo sudoers" Aunque utilizar sudo es preferible a iniciar sesión como usuario raíz, es importante ser consciente de que los usuarios con permisos elevados para utilizar sudo podrían correr más riesgos en caso de ataque.

Además, incluso si necesita acceso a `sudo`, debe tener cuidado de utilizarlo sólo con los comandos que necesite y nada más. Ejecutar comandos con sudo permite a los usuarios saltarse los típicos Controles de seguridad que existen para impedir el acceso elevado a un atacante.

**Nota**: Tenga cuidado con sudo si copia comandos de una fuente en línea. Es importante que no utilice sudo accidentalmente.