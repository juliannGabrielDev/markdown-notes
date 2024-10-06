# Información sobre los principios de seguridad OWASP
#Teoría #Ciberseguridad 

---
En el lugar de trabajo, los principios de seguridad están integrados en las tareas diarias. Ya sea analizando registros, supervisando un panel de administración de información y eventos de seguridad (SIEM) o utilizando un [escáner de vulnerabilidades](https://csrc.nist.gov/glossary/term/vulnerability_scanner), utilizará estos principios de alguna manera.

Anteriormente, se le presentaron varios principios de seguridad OWASP. Estos incluyen:

- **Minimizar la superficie de ataque**: La superficie de ataque se refiere a todas las vulnerabilidades potenciales que un Agente de amenaza podría explotar.
    
- **Principio de privilegio mínimo**: Los usuarios tienen la menor cantidad de acceso necesario para realizar sus tareas cotidianas.
    
- **Defensa en profundidad**: Las organizaciones deben disponer de diversos controles de seguridad que mitiguen los riesgos y amenazas.
    
- **Separación de funciones**: Las acciones críticas deben depender de varias personas, cada una de las cuales debe seguir el principio de privilegio mínimo.
    
- **Seguridad sencilla**: Evite las soluciones innecesariamente complicadas. La complejidad dificulta la seguridad.
    
- Solucione**correctamente** los problemas de seguridad: Cuando se produzcan incidentes de seguridad, identifique la causa raíz, contenga el impacto, identifique las vulnerabilidades y lleve a cabo pruebas para garantizar que la corrección se realiza correctamente.

## Principios de seguridad OWASP adicionales

A continuación, usted aprenderá acerca de cuatro principios de seguridad OWASP adicionales que los analistas de ciberseguridad y sus equipos utilizan para mantener las operaciones de la organización y las personas a salvo.

### Establecer valores predeterminados seguros

Este principio significa que el estado de seguridad óptimo de una aplicación es también su estado por defecto para los usuarios; debería costar un trabajo extra hacer que la aplicación sea insegura.

### Fallar con seguridad

Fallar de forma segura significa que cuando un control falla o se detiene, debe hacerlo pasando por defecto a su opción más segura. Por ejemplo, cuando un cortafuegos falla, debería simplemente cerrar todas las conexiones y bloquear todas las nuevas, en lugar de empezar a aceptarlo todo.

### No confíes en los servicios

Muchas organizaciones trabajan con socios externos. Estos socios externos suelen tener políticas de seguridad diferentes a las de la organización. Y la organización no debe confiar explícitamente en que los sistemas de sus socios sean seguros. Por ejemplo, si un proveedor externo realiza el seguimiento de los puntos de recompensa de los clientes de una aerolínea, ésta debería asegurarse de que el saldo es exacto antes de compartir esa información con sus clientes.

### Evitar la seguridad por oscuridad

La seguridad de los sistemas clave no debe basarse en mantener ocultos los detalles. Considere el siguiente ejemplo FROM OWASP (2016): [OWASP Mobile Top 10](https://owasp.org/www-project-mobile-top-10/2016-risks/)

La seguridad de una aplicación no debería basarse en mantener en secreto el código fuente. Su seguridad debe basarse en muchos otros factores, incluidas políticas de contraseñas razonables, defensa en profundidad, límites de transacciones comerciales, arquitectura de red sólida y controles de fraude y auditoría.