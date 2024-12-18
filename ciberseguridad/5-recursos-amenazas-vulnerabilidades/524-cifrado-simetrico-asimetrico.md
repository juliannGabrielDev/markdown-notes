# Cifrado simétrico y asimétrico
#ciberseguridad #curso-5 #modulo-2 

---
- **Cifrado**: proceso de conversión de datos de un formato legible a un formato codificado.
- **Infraestructura de clave pública** (PKI): framework de encriptación que asegura el intercambio de información en línea.
- **Cifrado**: un algoritmo que cifra la información.
## Tipos de encriptación

Existen dos tipos principales de encriptación:

- El **cifrado simétrico** consiste en utilizar una única clave secreta para intercambiar información. Dado que utiliza una sola clave para la encriptación y la desencriptación, el emisor y el receptor deben conocer la clave secreta para bloquear o desbloquear el cifrado.
- La **criptografía asimétrica** es la utilización de una vinculación de claves públicas y privadas para la encriptación y desencriptación de datos. Utiliza dos claves distintas: una clave pública y una clave privada. La clave pública se utiliza para la encriptación de los Datos y la privada para su desencriptación. La clave privada sólo se entrega a los usuarios con acceso autorizado.
## La oscuridad no es seguridad

En el mundo de la criptografía, hay que demostrar que un cifrado es indescifrable antes de afirmar que es seguro. Según el [principio de Kerchoff](https://en.wikipedia.org/wiki/Kerckhoffs%27s_principle), la criptografía debe diseñarse de forma que todos los detalles de un algoritmo -excepto la clave privada- sean conocibles sin sacrificar su Seguridad. Por ejemplo, puede acceder en línea a todos los detalles sobre el funcionamiento de la encriptación AES y, sin embargo, sigue siendo indescifrable.

En ocasiones, las organizaciones implementan sus propios algoritmos de encriptación personalizados. Se han dado casos en los que esos sistemas criptográficos secretos han sido rápidamente descifrados tras hacerse públicos.

**Consejo profesional:** Un sistema criptográfico _no debe_ considerarse seguro si requiere secreto sobre su funcionamiento.