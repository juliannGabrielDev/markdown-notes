# La evolución de los protocolos de Seguridad inalámbrica
#redes #ciberseguridad #teoria 

---
En los primeros tiempos de Internet, todas las comunicaciones se realizaban a través de cables físicos. No fue hasta mediados de la década de 1980 cuando las autoridades de Estados Unidos designaron un espectro de frecuencias de ondas de radio que podían utilizarse sin licencia, por lo que Internet tuvo más oportunidades de expandirse.

A finales de los 90 y principios de los 2000, se desarrollaron tecnologías para enviar y recibir datos por radio. Hoy en día, los usuarios acceden a Internet sin cables a través de ordenadores portátiles, teléfonos inteligentes, tabletas y escritorios. Los dispositivos inteligentes, como termostatos, cerraduras de puertas y cámaras de Seguridad, también utilizan Internet inalámbrico para comunicarse entre sí y con los servicios de Internet.
![Protocolos de Seguridad Inalámbrica](wpa.webp)
## Introducción a los protocolos de Comunicación inalámbrica

En la actualidad, muchas personas se refieren a Internet inalámbrico como Wi-Fi. ==**Wi-Fi** hace referencia a un conjunto de Estándares que definen la comunicación para las LAN inalámbricas==. Wi-Fi es un término de marketing encargado por la Alianza para la Compatibilidad de Ethernet Inalámbrica (WECA). Desde entonces, la WECA ha cambiado el nombre de su organización por el de Wi-Fi Alliance.

Los Estándares y protocolos Wi-Fi se basan en la familia 802.11 de estándares de comunicación de Internet determinados por el Instituto de Ingenieros Eléctricos y Electrónicos (IEEE). Por lo tanto, como analista de Seguridad, es posible que también vea referirse a Wi-Fi como IEEE 802.11.
### Privacidad equivalente por cable (WEP)

La privacidad equivalente por cable (WEP) es un protocolo de seguridad inalámbrica diseñado para proporcionar a los usuarios el mismo nivel de privacidad en las conexiones de red inalámbricas que el que tienen en las conexiones de red por cable. WEP se desarrolló en 1999 y es el más antiguo de los Estándares de Seguridad inalámbrica.

==En la actualidad, WEP está en gran medida fuera de uso, pero los analistas de Seguridad deben seguir entendiendo WEP en caso de que se encuentren con él==. Por ejemplo, un router de red puede haber utilizado WEP como protocolo de seguridad por defecto y el administrador de la red nunca lo cambió. O puede que los dispositivos de una red sean demasiado antiguos para soportar los protocolos de seguridad Wi-Fi más recientes. No obstante, un actor malintencionado podría romper potencialmente la encriptación WEP, por lo que ahora se considera un protocolo de Seguridad de alto riesgo.
### **Acceso Wi-Fi protegido (WPA)**

El Acceso Wi-Fi protegido (WPA) se desarrolló en 2003 para mejorar el WEP, solucionar los problemas de Seguridad que presentaba y sustituirlo. WPA siempre pretendió ser una medida transitoria para poder establecer la retrocompatibilidad con el hardware más antiguo.

Los fallos de WEP estaban en el propio protocolo y en cómo se utilizaba la encriptación. WPA abordó esta debilidad utilizando un protocolo llamado protocolo de integridad de clave temporal (TKIP). El algoritmo de encriptación WPA utiliza claves secretas más grandes que las WEP, lo que hace más difícil adivinar la clave por ensayo y error.

WPA también incluye una comprobación de integridad del mensaje que incluye una etiqueta de autenticación del mensaje con cada transmisión. Si un actor malintencionado intenta alterar la transmisión de algún modo o reenviarla en otro momento, la comprobación de integridad del mensaje de WPA identificará el ataque y rechazará la transmisión.

A pesar de las mejoras de Seguridad de WPA, sigue teniendo vulnerabilidades. Los actores maliciosos pueden utilizar un ataque de reinstalación de claves (o ataque KRACK) para desencriptar las transmisiones que utilicen WPA. Los atacantes pueden introducirse en el proceso de protocolo de enlace de autenticación WPA e insertar una nueva clave de encriptación en lugar de la dinámica asignada por WPA. Si establecen la nueva clave en todos ceros, es como si la transmisión no estuviera encriptada en absoluto.

Debido a esta importante vulnerabilidad, WPA fue sustituido por una versión actualizada del protocolo denominada WPA2.
### **WPA2 Y WPA3**

#### **WPA2**

La segunda versión de Wi-Fi Acceso Wi-Fi protegido -conocida como WPA2- se lanzó en 2004. WPA2 mejora a WPA utilizando el Estándar de encriptación avanzada (AES). WPA2 también mejora el uso de TKIP de WPA. WPA2 utiliza el protocolo de código de autenticación de mensajes mediante cadena de bloques de cifrado en modo contador (CCMP), que proporciona encapsulación y garantiza la autenticación e integridad de los mensajes. Debido a la solidez de WPA2, hoy en día se considera el estándar de seguridad para todas las transmisiones Wi-Fi. WPA2, al igual que su predecesor, es vulnerable a los ataques KRACK. Esto llevó al desarrollo de WPA3 en 2018.
#### **Personal**

El modo personal de WPA2 es el más adecuado para las redes domésticas por varias razones. Es fácil de Implementar, la configuración inicial lleva menos tiempo para personal que para la versión empresarial. La frase de contraseña global para la versión personal de WPA2 debe aplicarse a cada una de las computadoras y puntos de acceso de una red. Esto la hace ideal para redes domésticas, pero inmanejable para organizaciones.
#### **Empresa**

El modo WPA2 Enterprise funciona mejor para aplicaciones empresariales. Proporciona la Seguridad necesaria para las redes inalámbricas en entornos empresariales. La configuración inicial es más complicada que la del modo personal WPA2, pero el modo empresa ofrece un control individualizado y centralizado de la accesibilidad Wi-Fi a una red empresarial. Esto significa que los administradores de red pueden conceder o retirar el acceso de los usuarios a una red en cualquier momento. Los usuarios nunca tienen acceso a las claves de encriptación, lo que impide a los posibles atacantes recuperar las claves de red de las computadoras individuales.
#### **WPA3**

WPA3 es un protocolo Wi-Fi seguro y su uso está creciendo a medida que salen al mercado más dispositivos compatibles con WPA3. Estas son las diferencias clave entre WPA2 y WPA3:

- WPA3 aborda la vulnerabilidad del protocolo de enlace de autenticación a los ataques KRACK, presente en WPA2.

- WPA3 utiliza la Autenticación Simultánea de Iguales (SAE), un acuerdo de autenticación de contraseñas y uso compartido de claves de cifrado. Esto impide que los atacantes descarguen datos de las conexiones de redes inalámbricas a sus sistemas para intentar descodificarlos.

- WPA3 ha aumentado la encriptación para que las contraseñas sean más seguras utilizando una encriptación de 128 bits, y el modo WPA3-Enterprise ofrece una encriptación opcional de 192 bits.
## Claves

Como analista de seguridad, conocer la historia de cómo se desarrollaron los protocolos de seguridad Wi-Fi le ayudará a comprender mejor qué debe tener en cuenta a la hora de proteger las redes inalámbricas. Es importante que comprenda las vulnerabilidades de cada protocolo y lo importante que es que los dispositivos de su red utilicen las tecnologías de seguridad más actualizadas.