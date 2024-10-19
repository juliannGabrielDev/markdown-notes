# Protocolos de Red Adicionales
#redes #Ciberseguridad #Teoría 

---
Esta lectura le presentará algunos conceptos y protocolos adicionales que surgirán con regularidad en su trabajo como analista de Seguridad. La Autoridad de Números Asignados en Internet (IANA) asigna números de puerto a algunos protocolos. Estos números de puerto se incluyen en la descripción de cada protocolo, si se han asignado.
## Traducción de direcciones de red

Los dispositivos de su red local doméstica o de oficina tienen cada uno una dirección IP privada que utilizan para comunicarse directamente entre sí. Sin embargo, ==para que los dispositivos con direcciones IP privadas puedan comunicarse con la Internet pública, necesitan tener una única dirección IP pública== que represente a todos los dispositivos de la LAN ante el público. 

Para los mensajes salientes, el router puede sustituir una dirección IP de origen privada por su dirección IP pública y realizar la operación inversa para las respuestas. Este proceso se conoce como traducción de direcciones de red (NAT) y generalmente requiere que un router o firewall esté configurado específicamente para realizar NAT. NAT forma parte de la ==capa 2 (capa de Internet) y de la capa 3 (capa de transporte) del Modelo TCP/IP==.

| **Direcciones IP privadas**          | **Direcciones IP públicas**                         |
| ------------------------------------ | --------------------------------------------------- |
| Asignadas por el router              | Asignada por ISP e IANA                             |
| Únicas sólo dentro de la red privada | Dirección Única en Internet global                  |
| Sin coste de uso                     | Costos de arrendamiento de una dirección IP pública |
| Rangos de direcciones:               | Rangos de direcciones asignables:                   |
| - 10.0.0.0-10.255.255.255            | - 1.0.0.0-9.255.255.255                             |
| - 172.16.0.0-172.31.255.255          | - 11.0.0.0-126.255.255.255                          |
| - 192.168.0.0-192.168.255.255        | - 128.0.0.0-172.15.255.255                          |
|                                      | - 172.32.0.0-192.167.255.255                        |
|                                      | - 192.169.0.0-233.255.255.255                       |
## Protocolo de configuración dinámica de host (DHCP)

El Protocolo de configuración dinámica de host (DHCP) pertenece a la familia de protocolos de red de gestión. ==DHCP es un protocolo de capa de aplicación que se utiliza en una red para configurar dispositivos. Funciona con el router para asignar una dirección IP Única a cada dispositivo y proporcionar las direcciones del servidor DNS y de la puerta de enlace predeterminada adecuados para cada dispositivo==. Los servidores DHCP operan en el puerto UDP 67 mientras que los clientes DHCP lo hacen en el puerto UDP 68.
## Protocolo de resolución de direcciones (ARP)

La dirección IP de un dispositivo puede cambiar con el tiempo, pero su dirección MAC es permanente porque es Única para la tarjeta de interfaz de red de un dispositivo. La dirección MAC se utiliza para comunicarse con dispositivos dentro de la misma red, pero a veces, la dirección MAC es desconocida. Por eso es necesario el protocolo de resolución de direcciones (ARP). ARP ==es principalmente un protocolo de la capa de acceso a la red en el Modelo TCP/IP que se utiliza para traducir las direcciones IP que se encuentran en los paquetes de datos a la dirección MAC del dispositivo de hardware==.

Cada dispositivo de la red ejecuta ARP y mantiene un registro de las direcciones IP y MAC coincidentes en un caché ARP. ARP no tiene un número de puerto específico ya que es un protocolo de capa 2 y los números de puerto están asociados a la capa de aplicación 7.
## Telnet

Telnet es un protocolo de capa de aplicación que ==se utiliza para conectar con un sistema remoto==. Telnet envía toda la Información en texto claro. Utiliza la línea de comandos para controlar otro dispositivo de forma similar a secure shell (SSH), pero Telnet no es tan seguro como SSH. Telnet puede utilizarse para conectarse a dispositivos locales o remotos y utiliza el ==puerto TCP 23==.
## Secure Shell (SSH)

El protocolo Secure Shell (SSH) ==se utiliza para crear una conexión segura con un sistema remoto==. Este protocolo de capa de aplicación proporciona una alternativa para la autenticación segura y la encriptación de la comunicación. SSH funciona a través del ==puerto TCP 22== y es un sustituto de protocolos menos seguros, como Telnet.
## Protocolo de oficina de correos (POP)

El protocolo de oficina de correos (POP) es un protocolo de capa de aplicación (capa 4 del Modelo TCP/IP) utilizado para gestionar y recuperar correo electrónico de un servidor de correo. POP3 es la versión más utilizada de POP. Muchas organizaciones tienen un servidor de correo dedicado en la red que gestiona el correo entrante y saliente para los usuarios de la red. Los dispositivos de los usuarios enviarán solicitudes al servidor de correo remoto y descargarán los mensajes de correo electrónico localmente. Si alguna vez ha actualizado su aplicación de correo electrónico y ha visto aparecer nuevos mensajes en su bandeja de entrada, está experimentando el POP y el protocolo de acceso a mensajes de Internet (IMAP) en acción. La autenticación en texto plano sin cifrar utiliza el puerto TCP/UDP 110 y los correos electrónicos cifrados utilizan la Capa de sockets seguros/Seguridad de la capa de transporte (SSL/TLS) a través del puerto TCP/UDP 995. Cuando se utiliza POP, el correo tiene que terminar de descargarse en un dispositivo local antes de poder ser leído. Después de descargarse, el correo puede o no borrarse del servidor de correo, por lo que no garantiza que un usuario pueda sincronizar el mismo correo electrónico en varios dispositivos.
## Protocolo de acceso a mensajes de Internet (IMAP)

IMAP se utiliza para el correo electrónico entrante. ==Descarga las cabeceras de los correos electrónicos y el contenido del mensaje. El contenido también permanece en el servidor de correo electrónico, lo que permite a los usuarios acceder a su correo electrónico desde múltiples dispositivos==. IMAP utiliza el ==puerto TCP 143== para el correo electrónico no cifrado y el puerto TCP 993 a través del protocolo TLS. El uso de IMAP permite a los usuarios leer parcialmente el correo electrónico antes de que termine de descargarse. Dado que el correo se guarda en el servidor de correo, permite al usuario sincronizar los correos electrónicos de varios dispositivos.
## Protocolo simple de transmisión de correo (SMTP)

El Protocolo simple de transmisión de correo (SMTP) ==se utiliza para transmitir y encaminar el correo electrónico del remitente a la dirección del destinatario==. SMTP funciona con el software del Agente de Transferencia de Mensajes (MTA), que busca en los servidores DNS para resolver las direcciones de correo electrónico en direcciones IP, con el fin de garantizar que los correos electrónicos lleguen a su destino previsto. SMTP utiliza el ==puerto TCP/UDP 25== para los correos electrónicos no cifrados y el ==puerto TCP/UDP 587== que utiliza TLS para los correos electrónicos cifrados. El puerto TCP 25 suele ser utilizado por el spam de gran volumen. SMTP ayuda a filtrar el spam regulando cuántos correos electrónicos puede enviar una fuente a la vez.
## Protocolos y números de puerto

Recuerde que los números de puerto son utilizados por los dispositivos de red para determinar qué debe hacerse con la información contenida en cada paquete de datos una vez que llegan a su destino. Los firewalls pueden filtrar el Tráfico no deseado basándose en los números de puerto. Por ejemplo, una organización puede configurar un firewall para que sólo permita la accesibilidad al puerto TCP 995 (POP3) a las direcciones IP pertenecientes a la organización.

Como analista de Seguridad, necesitará conocer muchos de los protocolos y números de puerto mencionados en este curso. Pueden ser utilizados para determinar sus conocimientos técnicos en las entrevistas, por lo que es una buena idea memorizarlos. También aprenderá sobre nuevos protocolos en el trabajo en un puesto de Seguridad.

| Protocolo | Puerto                                                                      |
| --------- | --------------------------------------------------------------------------- |
| DHCP      | Puerto UDP 67 (servidores)<br>Puerto UDP 68 (clientes)                      |
| ARP       | Ninguno                                                                     |
| Telnet    | Puerto TCP 23                                                               |
| SSH       | TCP puerto 22                                                               |
| POP3      | TCP/UDP puerto 110 (sin cifrar)<br>TCP/UDP puerto 995 (encriptado, SSL/TLS) |
| IMAP      | TCP puerto 143 (sin cifrar)<br>Puerto TCP 993 (encriptado, SSL/TLS)         |
| SMTP      | TCP/UDP puerto 25 (sin cifrar)                                              |
| SMTPS     | TCP/UDP puerto 587 (encriptado, TLS)                                                                            |
