# Protocolos de Red Comunes
#Ciberseguridad #redes #Teoría 

---

Esta lectura tratará los protocolos de red en mayor profundidad y repasará algunos protocolos básicos que ha aprendido anteriormente. También aprenderá nuevos protocolos y analizará algunas de las formas en que los protocolos intervienen en la Seguridad de las redes.
## Visión general de los protocolos de red

Un **protocolo de red** es un ==conjunto de reglas utilizadas por dos o más dispositivos de una red para describir el orden de entrega y la estructura de los datos==. Los protocolos de red sirven como instrucciones que acompañan a la información del paquete de datos. Estas instrucciones indican al dispositivo receptor qué debe hacer con los Datos. Los protocolos son como un lenguaje común que permite a los dispositivos de todo el mundo comunicarse y entenderse entre sí.

Algunos protocolos tienen vulnerabilidades que los actores maliciosos explotan. Por ejemplo, un actor nefasto podría utilizar el protocolo del sistema de nombres de dominio (DNS), que resuelve las direcciones web en direcciones IP, para desviar el tráfico de un sitio web legítimo a un sitio web malicioso que contenga software malicioso.
## Tres categorías de protocolos de red

Los protocolos de red pueden dividirse en tres categorías principales: **protocolos de comunicación, protocolos de gestión y protocolos de seguridad**. 
### **Protocolos de comunicación**

Los protocolos de comunicación ==rigen el intercambio de información en la transmisión por red==. Dictan cómo se transmiten los Datos entre dispositivos y el momento de la comunicación. También incluyen métodos para recuperar Datos perdidos en tránsito. He aquí algunos de ellos.

- **Protocolo de control de transmisión (TCP** ) es un protocolo de comunicación de Internet que ==permite que dos dispositivos formen una conexión y transmitan datos==. TCP utiliza un proceso de protocolo de enlace de tres vías. En primer lugar, el dispositivo envía una solicitud de sincronización (SYN) a un servidor. A continuación, el servidor responde con un paquete SYN/ACK para acusar recibo de la solicitud del dispositivo. Una vez que el servidor recibe el último paquete ACK del dispositivo, se establece una conexión TCP. En el Modelo TCP/IP, TCP se produce en la ==capa de transporte==.

- **Protocolo de Datagramas de Usuario (UDP)** es un ==protocolo no orientado a la conexión que no establece una conexión entre dispositivos antes de una transmisión==. Esto hace que sea menos fiable que TCP. Pero también significa que funciona bien para transmisiones que necesitan llegar a su destino rápidamente. Por ejemplo, un uso de UDP es para enviar solicitudes DNS a servidores DNS locales. En el Modelo TCP/IP, UDP se produce en la capa de transporte.

- **Protocolo de transferencia de hipertexto (HTTP)** es un protocolo de capa de aplicación que ==proporciona un método de comunicación entre clientes y servidores de sitios web==. HTTP utiliza el puerto 80. HTTP se considera inseguro, por lo que está siendo sustituido en la mayoría de los sitios web por una versión segura, denominada HTTPS que utiliza la encriptación de SSL/TLS para la comunicación. Sin embargo, todavía hay muchos sitios web que utilizan el protocolo inseguro HTTP. En el Modelo TCP/IP, HTTP se produce en la ==capa de aplicación==.

- **Sistema de nombres de dominio (DNS)** es un protocolo que ==traduce los nombres de dominio de Internet en direcciones IP==. Cuando una computadora de cliente desea acceder al dominio de un sitio web utilizando su navegador de Internet, se envía una consulta a un servidor DNS dedicado. El servidor DNS busca entonces la dirección IP que corresponde al dominio del sitio web. DNS utiliza normalmente UDP en el puerto 53. Sin embargo, si la respuesta del DNS a una solicitud es grande, pasará a utilizar el protocolo TCP. En el Modelo TCP/IP, el DNS se produce en la ==capa de aplicación==.
### **Protocolos de Gestión**

La siguiente categoría de protocolos de red son los protocolos de gestión. Los protocolos de gestión se utilizan para supervisar y gestionar la actividad en una red. Incluyen protocolos para la notificación de errores y la optimización del rendimiento en la red.

- **Protocolo simple de administración de red (SNMP)** es un protocolo de red ==utilizado para supervisar y gestionar los dispositivos de una red==. SNMP puede restablecer una contraseña en un dispositivo de red o cambiar su configuración base. También puede enviar solicitudes a los dispositivos de red para obtener un informe sobre la cantidad de ancho de banda de la red que se está utilizando. En el Modelo TCP/IP, SNMP se produce en la ==capa de aplicación==.

- **Protocolo de mensajes de control de Internet (ICMP)** es un protocolo de Internet ==utilizado por los dispositivos para informarse mutuamente de los errores de transmisión de datos a través de la red==. El ICMP es utilizado por un dispositivo receptor para enviar un informe al dispositivo emisor sobre la transmisión de datos. El ICMP se utiliza habitualmente como una forma rápida de solucionar problemas de conectividad y latencia de la red mediante la emisión del comando "ping" en un sistema operativo Linux. En el Modelo TCP/IP, el ICMP se produce en la ==capa de Internet==.
### **Protocolos de Seguridad**

Los protocolos de Seguridad son protocolos de red que garantizan que los datos se envían y reciben de forma segura a través de una red. Los protocolos de Seguridad utilizan algoritmos de encriptación para proteger los datos en tránsito. A continuación se indican algunos protocolos de Seguridad comunes.

- **Protocolo seguro de transferencia de hipertexto (HTTPS** ) es un protocolo de red que ==proporciona un método seguro de comunicación entre clientes y servidores de sitios web==. HTTPS es una versión segura de HTTP que utiliza la encriptación secure sockets layer/transport layer security (SSL/TLS) en todas las transmisiones para que los actores maliciosos no puedan leer la información contenida. HTTPS utiliza el ==**puerto 443**==. En el Modelo TCP/IP, HTTPS se produce en la **==capa de aplicación==**.

- **Protocolo seguro de transferencia de archivos (SFTP** ) es un protocolo seguro ==utilizado para transferir archivos de un dispositivo a otro a través de una red==. SFTP utiliza Secure Shell (SSH), normalmente a través del ==**puerto TCP 22**==. SSH utiliza el Estándar de encriptación avanzada (AES) y otros tipos de encriptación para garantizar que los destinatarios no deseados no puedan interceptar las transmisiones. En el Modelo TCP/IP, SFTP se produce en la ==**capa de aplicación**==. SFTP se utiliza a menudo con el almacenamiento en la nube. Cada vez que un usuario sube o baja un archivo del almacenamiento en la nube, el archivo se transfiere utilizando el protocolo SFTP.

**Nota:** Los protocolos de encriptación mencionados no ocultan la dirección IP de origen o destino del tráfico de red. Esto significa que un actor malicioso aún puede conocer cierta información básica sobre el tráfico de red si lo intercepta.
## Puntos clave

Los protocolos sobre los que ha aprendido en esta lectura son protocolos de redes básicos que los analistas de ciberseguridad de nivel básico deberían conocer. Comprender cómo funcionan los protocolos en una red es esencial. Los analistas de ciberseguridad pueden aprovechar su conocimiento de los protocolos para mitigar con éxito las vulnerabilidades de una red y prevenir potencialmente futuros ataques.