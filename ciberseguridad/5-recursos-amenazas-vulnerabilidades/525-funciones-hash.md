# La evolución de las funciones hash
#ciberseguridad #curso-5 #modulo-2 

---
Las funciones hash son controles importantes que forman parte de la estrategia de Seguridad de toda empresa. El hash se utiliza ampliamente para la autenticación y el **no repudio**, el concepto de que no se puede negar la autenticidad de la información.

Anteriormente, aprendió que las **funciones hash** son algoritmos que producen un código que no puede ser desencriptado. Las funciones hash convierten la información en un valor único que puede utilizarse para determinar su integridad.
![Funciones Hash](img/funciones-hash.webp)
Una de las primeras funciones hash es Message Digest 5, más conocida como MD5. El profesor Ronald Rivest, del Instituto Tecnológico de Massachusetts (MIT), desarrolló MD5 a principios de la década de 1990 como una forma de verificar que un archivo enviado a través de una red coincidía con su archivo de origen.

Tanto si se utiliza para convertir un simple correo electrónico como el código fuente de una aplicación, MD5 funciona convirtiendo los datos en un valor de 128 bits. Quizá recuerde que un **bit** es la unidad más pequeña de medida de datos en una computadora. Los bits pueden ser un 0 o un 1. En una computadora, los bits representan la entrada del usuario de una forma que las computadoras pueden interpretar. En una tabla hash, esto aparece como una cadena de 32 caracteres. Alterar cualquier cosa en el archivo fuente genera un valor hash completamente nuevo.

Generalmente, cuanto más largo es el valor hash, más seguro es. No pasó mucho tiempo después de la creación de MD5 cuando los profesionales de la Seguridad descubrieron que los compendios de 128 bits daban lugar a una vulnerabilidad importante.
## Colisiones de hash

Uno de los defectos de MD5 resulta ser una característica de todas las funciones hash. ==Los algoritmos hash mapean cualquier entrada, independientemente de su longitud, en un valor de tamaño fijo de letras y números. ¿Cuál es el problema? Aunque hay una cantidad infinita de entradas posibles, ¡sólo hay un conjunto finito de salidas disponibles!==

Los Valores MD5 están limitados a 32 caracteres de longitud. Debido al tamaño limitado de la salida, se considera que el algoritmo es vulnerable a la **colisión** de hash, una instancia en la que diferentes entradas producen el mismo valor hash. Dado que los hash se utilizan para la autenticación, una colisión de hash es similar a copiar la identidad de alguien. Los atacantes pueden llevar a cabo ataques de colisión para suplantar fraudulentamente datos auténticos.
## La nueva generación de hash

Para evitar el riesgo de colisiones de hash, se necesitaban funciones que generaran valores más largos. Las deficiencias de MD5 dieron paso a un nuevo grupo de funciones conocidas como algoritmos hash seguros, o SHA.

El Instituto Nacional de Estándares y Tecnología (NIST) aprueba cada uno de estos algoritmos. Los números que aparecen junto a cada función SHA indican el tamaño de su valor hash en bits. Excepto SHA-1, que produce un compendio de 160 bits, se considera que estos algoritmos son resistentes a las colisiones. Sin embargo, eso no los hace invulnerables a otros exploits.

**Cinco funciones componen la familia de algoritmos SHA:**

- SHA-1
- SHA-224
- SHA-256
- SHA-384
- SHA-512
## Almacenamiento seguro de contraseñas

Las contraseñas suelen almacenarse en una base de datos donde se asignan a un nombre de usuario. El servidor recibe una solicitud de autenticación que contiene las credenciales proporcionadas por el usuario. A continuación, busca el nombre de usuario en la base de datos y lo compara con la contraseña proporcionada y verifica que coincide antes de concederle el acceso.

Se trata de un sistema seguro a menos que un atacante consiga acceder a la base de datos de usuarios. ==Si las contraseñas se almacenan en texto plano, un atacante puede robar esa información y utilizarla para acceder a los Recursos de la empresa==. El hash añade una capa adicional de Seguridad. ==Dado que los valores hash no pueden invertirse, un atacante no podría robar las credenciales de inicio de sesión de alguien si consiguiera acceder a la base de datos==.
### **Tablas rainbow**

Una **tabla rainbow** es un archivo de valores hash pregenerados y su texto plano asociado. Son como diccionarios de contraseñas débiles. Los atacantes capaces de obtener la base de datos de contraseñas de una organización pueden utilizar una tabla rainbow para compararlas con todos los valores posibles.
## Añadir algo de "sal"

Las Funciones con compendios más grandes son menos vulnerables a los ataques de colisión y de tabla rainbow. Pero como está aprendiendo, ningún control de Seguridad es perfecto.

**El salting** es una salvaguarda adicional que se utiliza para reforzar las funciones hash. Una _sal_ es una ==cadena aleatoria de caracteres que se añade a los Datos antes de hacer el hash==. Los caracteres adicionales producen un valor hash más único, lo que hace que los datos salados sean resistentes a los ataques de tabla rainbow.

Por ejemplo, una Base de datos que contenga contraseñas podría tener varias entradas con hash para la contraseña "password" Si todas esas contraseñas estuvieran saladas, cada entrada sería completamente diferente. Eso significa que un atacante que utilizara una tabla rainbow sería incapaz de encontrar valores coincidentes para "contraseña" en la base de datos.
![Salting](img/salting.webp)
Por esta razón, el salting se ha vuelto cada vez más común cuando se almacenan contraseñas y otros tipos de datos sensibles. La longitud y el carácter único de una sal son importantes. Al igual que ocurre con los valores hash, cuanto más larga y compleja sea una sal, más difícil será descifrarla.