# División en Subredes y CIDR
#ciberseguridad #teoria 

---
La **división en subredes** es la subdivisión de una red en grupos lógicos denominados subredes. Funciona como una red dentro de otra red. La división en subredes divide un rango de direcciones de red en subredes más pequeñas dentro de la red. Estas subredes más pequeñas se forman en función de las direcciones IP y la máscara de red de los dispositivos de la red. La división en subredes crea una red de dispositivos para que funcionen como su propia red. Esto hace que la red sea más eficiente y también puede utilizarse para crear zonas de seguridad. Si los dispositivos de una misma subred se comunican entre sí, el Switch cambia las transmisiones para que permanezcan en la misma subred, lo que mejora la velocidad y la eficacia de las comunicaciones.
## Notación de enrutamiento entre dominios sin clase para la división en subredes

El direccionamiento entre dominios sin clase (CIDR) es un método de asignación de máscaras de subred a direcciones IP para crear una subred. El direccionamiento sin clase sustituye al direccionamiento con clase. El direccionamiento classful se utilizó en la década de 1980 como sistema de agrupación de direcciones IP en clases (de la Clase A a la Clase E). Cada clase incluía un número limitado de direcciones IP, que se fueron agotando a medida que el número de dispositivos que se conectaban a Internet superaba el rango classful en la década de 1990. El direccionamiento CIDR sin clases amplió el número de direcciones IPv4 disponibles.

CIDR permite a los profesionales de la ciberseguridad segmentar las redes classful en trozos más pequeños. Las direcciones IP CIDR tienen el mismo formato que las direcciones IPv4, pero incluyen una barra oblicua ("/'") seguida de un número al final de la dirección. Este número adicional se denomina prefijo de red IP. Por ejemplo, una dirección IPv4 normal utiliza el formato 198.51.100.0, mientras que una dirección IP CIDR incluiría el prefijo de red IP al final de la dirección, 198.51.100.0/24. Esta dirección CIDR engloba todas las direcciones IP entre 198.51.100.0 y 198.51.100.255. El sistema de direccionamiento CIDR reduce el número de entradas en las tablas de enrutamiento y proporciona más direcciones IP disponibles dentro de las redes. Puede intentar convertir direcciones CIDR a IPv4 y viceversa mediante una herramienta de conversión en línea, como [IPAddressGuide](https://www.ipaddressguide.com/cidr), para practicar y comprender mejor este concepto.

**Nota:** Puede que aprenda más sobre CIDR durante su carrera, pero no se tratará con mayor profundidad en este programa de certificación. Por ahora, sólo necesita una comprensión básica de este concepto.

## Beneficios de seguridad de la división en subredes

La división en subredes permite a los profesionales y analistas de redes crear una red dentro de su propia red sin solicitar otra dirección IP de red a su proveedor de servicios de Internet. Este proceso utiliza el ancho de banda de la red de forma más eficiente y mejora el rendimiento de la red. La división en subredes es uno de los componentes de la creación de subredes aisladas mediante el aislamiento físico, la configuración del enrutamiento y los firewalls.

## Puntos clave

La división en subredes es una estrategia de Seguridad común utilizada por las organizaciones. La división en subredes permite a las organizaciones crear redes más pequeñas dentro de su red privada. Esto mejora la eficacia de la red y puede utilizarse para crear zonas de seguridad.