# Firewalls
#ciberseguridad #redes #teoria 

---
Anteriormente, aprendió que los cortafuegos ==son dispositivos virtuales de red (NVA) o dispositivos de hardware que inspeccionan y pueden filtrar el Tráfico de red antes de que se le permita entrar en la red privada==. Los cortafuegos tradicionales se configuran con reglas que le indican qué tipos de paquetes de datos están permitidos en función del número de puerto y la dirección IP del paquete de datos.

Existen dos categorías principales de firewalls.

- **Sin estado:** Una clase de firewall que funciona basándose en reglas predefinidas y no realiza un seguimiento de la información de los paquetes de datos.

- **Con estado:** Una clase de firewall que ==hace un seguimiento de la información que pasa a través de él y filtra proactivamente las amenazas==. A diferencia de los cortafuegos sin estado, que requieren la configuración de reglas en dos direcciones, un cortafuegos con estado sólo requiere una regla en una dirección. Esto se debe a que ==utiliza una "tabla de estado" para rastrear las conexiones, de modo que puede hacer coincidir el tráfico de retorno con una sesión existente==.

Los cortafuegos de nueva generación (NGFW) son los cortafuegos de protección tecnológicamente más avanzados. ==Superan la seguridad ofrecida por los cortafuegos con estado porque incluyen inspección profunda de paquetes (un tipo de sniffing de paquetes que examina los paquetes de datos y toma medidas si existen amenazas) y características de prevención de intrusiones que detectan las amenazas a la seguridad y notifican a los administradores del cortafuegos==. Los NGFW pueden inspeccionar el Tráfico en la capa de aplicación del Modelo TCP/IP y suelen ser conscientes de las aplicaciones. A diferencia de los firewalls tradicionales que bloquean el tráfico en función de la dirección IP y los puertos, las reglas de los NGFW pueden configurarse para bloquear o permitir el tráfico en función de la aplicación. Algunos NGFW disponen de características adicionales como Sandboxing de software malicioso, antivirus de red y filtrado de URL y DNS.