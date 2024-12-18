# Pruebas de penetración
#ciberseguridad #curso-5 #modulo-3

---
Un plan de Seguridad eficaz se basa en pruebas periódicas para encontrar los puntos débiles de una organización. Anteriormente, aprendió que las evaluaciones de **vulnerabilidad**, el proceso de revisión interna de los sistemas de Seguridad de una organización, se utilizan para diseñar estrategias de defensa basadas en las debilidades del sistema. En esta lectura, aprenderá cómo los Equipos de Seguridad evalúan la eficacia de sus defensas mediante pruebas de penetración.

## Pruebas de penetración

Una **prueba de penetración**, o pen test, es un ataque simulado que ayuda a identificar vulnerabilidades en sistemas, redes, sitios web, aplicaciones y procesos. El ataque simulado en una prueba de penetración implica el uso de las mismas herramientas y técnicas que los actores maliciosos con el fin de imitar un ataque en la vida real. Dado que una prueba de penetración es un ataque autorizado, se considera una forma de hacking ético. A diferencia de una evaluación de vulnerabilidades que encuentra puntos débiles en la Seguridad de un sistema, una prueba de penetración explota esos puntos débiles para determinar las consecuencias potenciales si el sistema se rompe o es penetrado por un agente de amenaza.

Por ejemplo, el Equipo de ciberseguridad de una empresa financiera podría simular un ataque a su aplicación bancaria para determinar si existen puntos débiles que permitirían a un atacante robar información de sus clientes o transferir fondos ilegalmente. Si la prueba de penetración descubre errores de configuración, el Equipo puede abordarlos y mejorar la Seguridad general de la aplicación.

**Nota:** Las organizaciones reguladas por PCI DSS, HIPAA o GDPR deben realizar pruebas de penetración de forma rutinaria para mantener los Estándares de cumplimiento.

## Aprender de perspectivas variadas

Estos ataques autorizados son realizados por pen testers expertos en programación y arquitectura de redes. Dependiendo de sus objetivos, las organizaciones pueden utilizar algunos enfoques diferentes para las pruebas de penetración:

- Las pruebas del Equipo Rojo _simulan_ ataques para identificar vulnerabilidades en sistemas, redes o aplicaciones.

- Las pruebas del equipo azul se centran en la _defensa_ _y la Respuesta ante incidentes_ para validar los sistemas de Seguridad existentes en una organización.

- Las pruebas del equipo púrpura son _colaborativas_ y se centran en mejorar la postura de seguridad de la organización combinando elementos de los ejercicios de los equipos rojo y azul.
    

Las Pruebas de penetración de los equipos rojos suelen ser realizadas por "pen testers" independientes contratados para evaluar los sistemas internos. Aunque los equipos de ciberseguridad también pueden contar con sus propios expertos en pruebas de penetración. Independientemente del enfoque, los expertos en pruebas de penetración deben tomar una decisión importante antes de simular un ataque: _¿Cuánto acceso e Información necesito?_

## Estrategias de pruebas de penetración

Existen tres estrategias comunes de pruebas de penetración:

- Las **pruebas de caja abierta** son aquellas en las que el evaluador tiene el mismo acceso privilegiado que tendría un desarrollador interno a información como la arquitectura del sistema, el flujo de datos y los diagramas de red. Esta estrategia recibe varios nombres diferentes, como pruebas de penetración internas, de pleno conocimiento, de caja blanca y de caja clara.

- Las pruebas de **caja cerrada** son aquellas en las que el probador tiene poco o ningún acceso a los sistemas internos, algo similar a lo que haría un hacker malintencionado. Esta estrategia se conoce a veces como pruebas de penetración externas, de caja negra o de conocimiento cero.

- Las **pruebas de conocimientos parciales** se producen cuando la persona que realiza las pruebas tiene acceso y conocimientos limitados de un sistema interno; por ejemplo, un representante de atención al cliente. Esta estrategia también se conoce como pruebas de caja gris.

Las pruebas de caja cerrada tienden a producir las simulaciones más exactas de un ataque en el mundo real. No obstante, cada estrategia produce resultados valiosos al demostrar cómo un atacante podría infiltrarse en un sistema y a qué información podría acceder.