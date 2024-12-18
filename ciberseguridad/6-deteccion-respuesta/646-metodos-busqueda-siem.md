---
Creación: 2024-12-15
Notas relacionadas:
  - "[[613-siem]]"
Fuente: Coursera
---
# Métodos de búsqueda con herramientas SIEM
#ciberseguridad #curso-6 #modulo-4 

---
Hasta ahora, ha aprendido cómo puede utilizar las herramientas de **administración de información y eventos de seguridad (SIEM** ) para buscar eventos de seguridad como intentos fallidos de inicio de sesión. Recuerde que SIEM es una aplicación que recopila y analiza datos de registro para monitorear actividades críticas en una organización. En esta lectura, examinará cómo las herramientas SIEM como Splunk y Chronicle utilizan diferentes métodos de búsqueda para encontrar, filtrar y transformar los resultados de la búsqueda.

No todas las organizaciones utilizan la misma herramienta SIEM para recopilar y centralizar sus datos de seguridad. Como analista de Seguridad, tendrás que estar preparado para aprender a utilizar diferentes herramientas SIEM. Es importante comprender los diferentes tipos de búsquedas que pueden realizarse con las herramientas SIEM para poder encontrar datos de eventos relevantes que respalden sus investigaciones de seguridad.
## Búsquedas en Splunk

Como ha aprendido, Splunk tiene su propio lenguaje de consulta llamado **Lenguaje de Procesamiento de Búsqueda (SPL)** . SPL se utiliza para buscar y recuperar eventos de los índices utilizando la aplicación de Búsqueda e Informes de Splunk. Una búsqueda SPL puede contener muchos comandos y argumentos diferentes. Por ejemplo, puede utilizar comandos para transformar los resultados de la búsqueda en un formato gráfico o filtrar los resultados para obtener información específica.

He aquí un ejemplo de una búsqueda básica de SPL que está consultando un índice para un evento fallido:

`index=main fail`

- **`index=main`** : Este es el comienzo del comando de búsqueda que le dice a Splunk que recupera eventos de un índice llamado main . Un índice almacena datos de eventos que han sido recopilados y procesados ​​por Splunk.

- **`fail`** : Este es el término de búsqueda. Esto le dice a Splunk que devuelva cualquier evento que contenga el término fail .

Saber cómo utilizar SPL de forma eficaz tiene muchos beneficios. Ayuda a acortar el tiempo que se tarda en devolver los resultados de la búsqueda. También le ayuda a obtener los resultados exactos que necesita de varias fuentes de Datos. SPL admite muchos tipos diferentes de búsquedas que quedan fuera del alcance de esta lectura. Si desea obtener más información sobre SPL, explore [la referencia de búsqueda de Splunk](https://docs.splunk.com/Documentation/Splunk/9.0.2/SearchReference/UnderstandingSPLsyntax).
### Tuberías

Anteriormente, es posible que haya aprendido acerca de cómo se utiliza piping en el shell bash de Linux. A modo de repaso, las tuberías envían la salida de un comando como entrada a otro comando.

SPL también utiliza el carácter de tubería `|` para separar los comandos individuales en la búsqueda. También se utiliza para encadenar comandos de forma que la salida de un comando se combine en el siguiente comando. Esto es útil porque puede refinar los datos de varias maneras para obtener los resultados que necesita utilizando un solo comando.

He aquí un ejemplo de dos comandos que se encadenan:

`index=main fail | chart count by host`

- **`index=main fail`** : Este es el comienzo del comando de búsqueda que le dice a Splunk que recupera los eventos de un índice llamado main para los eventos que contienen el término de búsqueda fail .

- **`|`** : El carácter de tubería separa y encadena los dos comandos `index=main` y `chart count by host` . Esto significa que la salida del primer comando `index=main` se utiliza como entrada del segundo comando `chart count by host` .

- **`chart count by host`** : Este comando le dice a Splunk que transforma los resultados de la búsqueda creando un `chart` de acuerdo con el `count` o número de eventos. El argumento `by host` indica a Splunk que liste los eventos por `host`, que son los nombres de los dispositivos de los que proceden los eventos. Este comando puede ser útil para identificar hosts con un número excesivo de fallos en un entorno.
### Comodin

Un **comodín** es un carácter especial que puede ser sustituido por cualquier otro carácter. Un comodín suele simbolizarse con un asterisco `*` . Los comodines coinciden con caracteres en valores de cadena. En Splunk, el comodín que utiliza depende del comando con el que esté utilizando el comodín. Los comodines son útiles porque pueden ayudar a encontrar Eventos que contienen Datos que son similares pero no totalmente idénticos. He aquí un ejemplo de uso de un comodín para ampliar los resultados de búsqueda de un término de búsqueda:

`index=main fail*`

- **`index=main`** : Este Comando recupera Eventos de un index llamado `main` .

- **`fail*`** : El comodín después de `fail` representa cualquier carácter. Esto indica a Splunk que busque todas las terminaciones posibles que contengan el término fail . Esto amplía los resultados de la búsqueda para devolver cualquier evento que contenga el término fail como "failure" o "failed".

**Consejo profesional** : Las comillas dobles se utilizan para especificar la búsqueda de una frase o cadena exacta. Por ejemplo, si desea buscar únicamente los eventos que contengan la frase exacta de `login failure`, puede encerrar la frase entre comillas dobles "login failure" . Esta búsqueda sólo coincidirá con los eventos que contengan la frase exacta "login failure" y no con otros eventos que contengan las palabras "failure" o "login" por separado.
## Búsquedas en Chronicle

En Chronicle, puede buscar eventos utilizando el Campo de búsqueda. También puede utilizar el Filtrado de Procedimientos para aplicar filtros a una búsqueda y refinar aún más los resultados de la misma. Por ejemplo, puede utilizar el Filtrado de procedimiento para incluir o excluir resultados de búsqueda que contengan información específica relativa a un tipo de evento o a una fuente de registro. Hay dos tipos de búsquedas que se pueden realizar para encontrar eventos en Chronicle, una Búsqueda en el Modo de Datos Unificado (UDM) o una Búsqueda en el Registro sin Procesar.
### Búsqueda en el Modelo Unificado de Datos (UDM)

La Búsqueda UDM es el tipo de búsqueda por defecto utilizado en Chronicle. Puede realizar una búsqueda UDM escribiendo su búsqueda, haciendo clic en "Buscar" y seleccionando "Búsqueda UDM" A través de una Búsqueda UDM, Chronicle busca datos de seguridad que han sido ingestados, analizados y normalizados. La búsqueda en UDM ofrece resultados más rápidos que la búsqueda en registros sin procesar, ya que busca entre datos indexados y estructurados que se han normalizado en UDM.

Una búsqueda UDM recupera eventos formateados en UDM y estos eventos contienen campos UDM. Existen muchos tipos diferentes de campos UDM que pueden utilizarse para consultar información específica de un evento. Discutir todos estos campos UDM está más allá del alcance de esta lectura, pero puede aprender más sobre los campos UDM explorando [la lista de campos UDM de Crónica](https://cloud.google.com/chronicle/docs/reference/udm-field-list). Sepa que todos los eventos UDM contienen un conjunto de campos comunes que incluyen:

- **Entidades** : Las entidades también se conocen como sustantivos. Todos los eventos UDM deben contener al menos una entidad. Este campo proporciona contexto adicional sobre un dispositivo, usuario o proceso que está involucrado en un evento. Por ejemplo, un evento UDM que contiene información de entidad incluye los detalles del origen de un evento, como el nombre de host, el nombre de usuario y la dirección IP del evento.

- **Metadatos del evento**: Este Campo proporciona una descripción básica de un Evento, incluyendo qué tipo de Evento es, marcas de tiempo y más.

- **Metadatos de red**: Este campo proporciona información sobre los eventos relacionados con la red y los detalles del protocolo.

- **Resultados de seguridad** : Este campo proporciona el resultado relacionado con la seguridad de los sucesos. Un ejemplo de resultado de Seguridad puede ser que un software antivirus detecte y ponga en cuarentena un archivo malicioso informando de "virus detected and quarantined."

He aquí un ejemplo de una búsqueda UDM sencilla que utiliza el campo de metadatos de eventos para localizar eventos relacionados con inicios de sesión de usuarios:

`metadata.event_type = “USER_LOGIN”`

- **`metadata.event_type = “USER_LOGIN”`** : Este Campo UDM `metadata.event_type` contiene información sobre el tipo de Evento. Esto incluye información como la marca de tiempo, la conexión a la red, la autenticación del usuario, etc. Aquí, el tipo de evento especifica `USER_LOGIN` , que busca eventos relacionados con la autenticación.    

Utilizando sólo los campos de metadatos, puedes empezar a buscar eventos rápidamente. ASÍ COMO continúe practicando la búsqueda en Chronicle utilizando la Búsqueda UDM, encontrará más campos. Pruebe a utilizar estos campos para formar búsquedas específicas que le permitan localizar distintos eventos.
### **Búsqueda de registros sin procesar**

Si no puede encontrar la información que busca a través de los Datos normalizados, utilizando una Búsqueda de registro en bruto buscará a través de los registros en bruto, sin analizar. Puede realizar una búsqueda de registros sin procesar escribiendo su búsqueda, haciendo clic en "Buscar" y seleccionando "Búsqueda de registros sin procesar" Como se trata de una búsqueda en registros sin procesar, tarda más que una búsqueda estructurada. En el Campo de búsqueda, puede realizar una Búsqueda de registro sin procesar especificando información como nombres de usuario, nombres de archivo, hashes, etc. Chronicle recuperará los Eventos asociados a la búsqueda.

**Consejo profesional** : La búsqueda de registros sin procesar admite el uso de expresiones regulares, que pueden ayudarle a realizar una búsqueda para que coincida con patrones específicos.
## Puntos clave

Las herramientas SIEM como Splunk y Chronicle tienen sus propios métodos para buscar y recuperar Datos de Eventos. Como analista de seguridad, es importante comprender cómo aprovechar estas herramientas para encontrar rápida y eficazmente la información que necesita. Esto le permitirá explorar los datos de forma que le ayudarán a detectar amenazas, así como a Responder rápidamente a los Incidentes de Seguridad.
## Recursos para obtener más información

Aquí tiene algunos Recursos por si desea obtener más información sobre la búsqueda de eventos con Splunk y Chronicle:

- [Manual de búsqueda](https://docs.splunk.com/Documentation/Splunk/9.0.1/Search/GetstartedwithSearch)de Splunk sobre cómo utilizar el Lenguaje de Procesamiento de Búsqueda (SPL) de Splunk.

- [Guía rápida de Chronicle](https://cloud.google.com/chronicle/docs/review-security-alert)sobre los distintos tipos de búsqueda.