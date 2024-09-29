# Puesta en escena frente a producción

Creado: 26 de septiembre de 2024 1:30

---

## Entornos de desarrollo

Todo equipo de desarrollo, antes de lanzar sus nuevas características o cambios, necesita verificar que el código que lanza no va a causar ningún problema o fallo. Para conseguirlo, normalmente configuran varios entornos para probar y verificar de distintas formas.  Una práctica común es que los equipos tengan un entorno de desarrollador, un entorno UAT o QA y un entorno de puesta en escena. El objetivo principal de este flujo es encontrar cualquier problema potencial que pueda surgir debido a los cambios o a las nuevas funciones que se añaden al código base. Cuantas más formas haya de probar los cambios, menos probabilidades habrá de que se introduzcan errores.

## Puesta en escena

El entorno de puesta en escena **debe imitar su entorno de producción**. La razón de ello es que desea probar el código en un entorno que coincida con el que tiene en producción. Esto permite a los equipos detectar o encontrar cualquier problema potencial antes de que llegue a producción. Cuanto más cercano sea el entorno de puesta en escena a su producción, más precisas serán sus pruebas. Los entornos de puesta en escena también pueden utilizarse para probar y verificar nuevas funciones y permitir que otros equipos, incluidos los de control de calidad o las partes interesadas, vean y utilicen esas funciones como prueba previa. La puesta en escena también debe abarcar todas las áreas de la arquitectura de la aplicación, incluida la base de datos y cualquier otro servicio que pueda ser necesario. Entre las áreas que se benefician de los entornos de puesta en escena se incluyen

### Nuevas características

Los desarrolladores que envíen nuevas características junto con los indicadores de características para activarlas y desactivarlas deberían hacer siempre una ronda de pruebas en un entorno de puesta en escena. Permiten a los equipos verificar que la característica funciona, que puede activarse y desactivarse mediante banderas de configuración y también que no rompe ni interfiere con la funcionalidad existente.

### Pruebas

Como el entorno de ensayo imita su entorno de producción, también es un lugar ideal para realizar pruebas. Los equipos de control de calidad lo utilizarán normalmente para verificar nuevas funciones, cambios de configuración o actualizaciones/parcheado de software. Los tipos de pruebas cubiertos serán las pruebas unitarias, las pruebas de integración y las pruebas de rendimiento. Todas, excepto las pruebas de rendimiento, pueden realizarse también en producción. Las de rendimiento también pueden realizarse en producción, pero sólo en momentos concretos, normalmente fuera de horario, ya que tendrán un efecto drástico en la experiencia del usuario.

A veces no siempre es factible tener una réplica exacta, ya sea por costes o por tiempo. Se pueden recortar ciertas áreas - por ejemplo, si su servicio está equilibrado en carga en 10 máquinas virtuales en producción, aún podría tener 4 máquinas virtuales en staging. La arquitectura subyacente es la misma, pero el rendimiento global puede ser diferente.

### Migraciones

La puesta en escena es un lugar perfecto para probar y verificar las migraciones de datos. Se pueden tomar instantáneas de la producción y utilizarlas para probar sus scripts de migración y confirmar que sus cambios no romperán nada. Si en el caso de que cause un problema, usted simplemente rollback y vuelva a intentarlo. Hacer algo como una migración en producción es extremadamente arriesgado y propenso a errores.

### Cambios de configuración

La configuración también puede causar dolores de cabeza a los equipos, especialmente en una gran arquitectura basada en la nube. Disponer de un entorno de ensayo le permitirá detectar cualquier posible problema o cuello de botella.

## Producción

La producción es en vivo. Está ahí fuera para que la gente la vea y/o interactúe con ella. Cualquier cuestión o problema que haya podido tener debería haberse detectado y solucionado en el entorno de puesta en escena. El entorno de puesta en escena proporciona al equipo una red de seguridad para atrapar estos posibles problemas. Cualquier código que se despliegue en producción debería haber sido probado y verificado antes del propio despliegue.

### Tiempo de inactividad

El tiempo de inactividad de cualquier servicio, especialmente el orientado al cliente, tendrá muy probablemente un impacto en los ingresos. Si los clientes no pueden acceder o utilizar su sitio web o aplicación en toda su capacidad, lo más probable es que ello tenga un coste. Tomemos por ejemplo una empresa de comercio electrónico que permite a los usuarios comprar bienes y servicios en línea. Si lanzan una nueva función para su carrito de la compra que rompe el proceso de pago, esto tendrá un impacto en que los clientes no puedan comprar bienes en línea.

### Vulnerabilidades

La ciberseguridad también debería desempeñar un papel importante en lo que se lanza a la producción. Cualquier actualización de software, como la aplicación de parches o el paso a la última versión, debe ser comprobada y verificada. Esta es también la misma regla para no actualizar el software cuando se publican actualizaciones críticas.

### Reputación

Los tiempos de inactividad o los problemas en la producción son perjudiciales para una empresa, ya que no infunden confianza en los usuarios finales. Si algo se cae o se rompe puede hacer que la empresa pierda clientes potenciales.