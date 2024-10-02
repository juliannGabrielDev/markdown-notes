# Repaso de conceptos fundamentales 2
#Examen #Teoría 

---
### Indique los niveles del modelo de Internet (OSI)
7. Aplicación
6. Presentación
5. Sesión
4. Transporte
3. Red
2. Enlace de datos
1. Física

### ¿Qué niveles del modelo de Internet son los niveles de soporte de red?

1. Física
2. Enlace de datos
3. Red

### ¿Qué niveles del modelo de Internet es el nivel de soporte de usuario?

- Aplicación
- Transporte

### ¿Cuál es la diferencia entre la entrega de paquetes en el nivel de red y la entrega en el nivel de transporte?

- El nivel de transporte es responsable de la entrega de origen a destino (extremo a extremo) de todo el mensaje.
- El nivel de red supervisa la entrega de extremo a extremo de paquetes individuales, no reconoce ninguna relación entre estos paquetes.

### ¿Qué es un proceso paritario?

Es cuando el nivel X de un dispositivo se comunica con el nivel X del otro, par ello en el paso de nivel a nivel en el emisor, se añade información que se decodifica en el nivel correspondiente del receptor. Ademas existe una interfaz entre niveles que permite una modularidad del modelo.

### ¿Cómo se pasa la información de un nivel al siguiente en el modelo de Internet?

Cada capa del protocolo le pasa datos a la siguiente capa y esta le añade datos propios de control y luego pasa el conjunto a la siguiente capa.

### ¿Qué son las cabeceras y las colas y cómo se añaden y se eliminan?

- Son los datos de control añadidos al principio y al final del paquete de datos.
- Las cabeceras se añaden al mensaje en los niveles 6, 5, 4, 3, 2 y el nivel dos añade una cola.

### ¿De que se ocupa el nivel físico en el modelo de Internet?

El nivel físico coordina las funciones necesarias para transmitir un flujo de bits sobre un nivel físico.

### ¿Cuáles son las responsabilidades del nivel de enlace de datos?

El nivel de enlace de datos es el responsable de la entrega de unidades de datos de una estación a la siguiente sin errores.

### ¿Cuáles son las responsabilidades del nivel de transporte en el modelo de Internet?

El nivel de transporte es el responsable de la entrega de origen a destino de todo el mensaje.

### ¿Cuál es la diferencia entre el puerto, 1 dirección lógica y una dirección física?

- Un puerto: la cabecera del nivel de transporte debe además incluir un tipo de dirección denominado dirección de punto de servicio (un puerto).
- Dirección lógica: el nivel de red añade una cabecera al paquete que viene del nivel superior que entre otras cosas incluye las direcciones lógicas del emisor y receptor.
- Dirección física: el nivel de enlace de datos añade una cabecera a la trama para definir la dirección física del emisor.

### ¿Indica algunos servicios ofrecidos por el nivel de aplicación en el modelo de Internet?

- Terminal virtual de red: una versión de un termino fijo y permite al usuario acceder a una maquina remota. Para hacerlo la aplicación crea una emulación de software.
- Servicios de correo: esta aplicación proporciona las bases para el envío y el almacenamiento del correo electrónico. 