# La trama

La capa de enlace de datos prepara los datos encapsulados (generalmente un paquete IPv4 o IPv6) para el transporte a través de los medios locales encapsulándolos con un **encabezado** y un **trailer** para crear una trama.

El protoclo de enlace de datos es responsable de las comunicaiones de NIC a NIC dentro de una misma red. Si bien existen muchos protocolos de capa de enlace de datos diferentes que describen las tramas de la capa de enlace de datos, cada tipo de trama tiene sus tres partes básicas:

-   Encabezado
-   Datos
-   Tráiler

A diferencia de protocolos de encapsulación, la capa de enlace de datos agrega información en forma de tráiler al final de la trama. Sin embargo, la estructura de la trama y los campos contenidos en el encabezado y tráiler varían de acuerdo con el protocolo.

No hay una estructura de trama que cumpla con las necesidades de todos los transportes a través de todos los tipos de medios. Según el entorno la cantida de información de control que necesita la trama varía para cumplir con los requisitos de control de acceso al medio de la topología lógica y de los medios. Por ejemplo, una trama WLAN debe incluir procedimientos para evitar colisiones y, por lo tanto, requiere información de control adicional en comparación con otra trama Ethernet.

---

# Campos de trama.

El tramado rompe la transmición en agruipaciones descifrables, con la información de control insertada en el ancabezado y tráiler como valores en campos diferentes

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Campos-de-trama-en-Red.png)

-   **Indicadores de arranque y detención de trama** - Se utilizan para identificar los límites de comienzo y finalización de la trama.
-   **Direccionamiento** - Inidca los nodos de origen y de destino en los medios.
-   **Tipo** - Identifica el protocolo de capa 3 en el campo de datos
-   **Control** - Identifica los servicios especiales de control de flujo, como la calidad del servicio (QoS). QoS otroga prioridad de reenvío a ciertos tipos de mensajes.
-   **Datos** - Incluye el contenido de la trama, es decir, el encabezado del paquete, el encabezado del segmento y los datos.
-   **Detección de errores** - Se incluye después de los datos para fromar el trailer.

Los protocolo de enlace de datos agregan un trailer al final de cada trama. En un proceso llamado detección de errores, el avance determina si la trama llegó con errores o no. Coloca un resumen lógico o matemático de los bits que componen la trama en el avance. La capa de enlace de datos agrega detección de errores porque las señales en los medios podrían estar sujetas a interferencia, distorsión o pérdida que cambiará sustrancialmente los valores de los bits.

Un nodo de transmisión crea un resumen lógico del contenido de la trama, conocido como el valor de C**omprobación de Redundancia Cíclica** **(CRC)**. Este valor se coloca en el C**ampo Secuencia de Verificación de la Trama (FCS)** para representar el contenido de la trama. En el tráiler Ethernet, el FCS proporciona un método para que el nodo receptor determine si la trama experimentó errores de transmisión.

---

# Direcciones de capa 2

La capa de enlace de datos proporciona el direccionamiento utilizado en el transporte de una trama a través de un medio local compartido. Las direcciones de dispositivo en esta capa se llaman direcciones físicas. El direccionamiento de la capa de enlace de datos está contenido en el encabezado de la trama y especifica el nodo de destino de la trama en la red local. Normalmente se encuentra al principio de la trama, por lo que la NIC puede determinar rápidamente si coincide con su propia dirección de Capa 2 antes de aceptar el resto de la trama. El encabezado de la trama también puede contener la dirección de origen de la trama.

A diferencia de las direcciones lógicas de la Capa 3, que son jerárquicas, las direcciones físicas no indican en qué red está ubicado el dispositivo. En cambio, la dirección física es única para un dispositivo en particular. Un dispositivo seguirá funcionando con la misma dirección física de capa 2, incluso si el dispositivo se mueve a otra red o subred. Por lo tanto, las direcciones de capa 2 sólo se utilizan para conectar dispositivos dentro del mismo medio compartido, en la misma red IP.

Las figuras ilustran la función de las direcciones de Capa 2 y Capa 3. A medida que el paquete IP se mueve de host a router, de router a router y, finalmente, de router a host, es encapsulado en una nueva trama de enlace de datos, en cada punto del recorrido. Cada trama de enlace de datos contiene la dirección de origen de enlace de datos de la tarjeta NIC que envía la trama y la dirección de destino de enlace de datos de la tarjeta NIC que recibe la trama.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Funciones-direcciones-Capa-2-y-Capa-3.png)

El host de origen encapsula el paquete IP de capa 3 en una trama de capa 2. En el encabezado de trama, el host agrega su dirección de Capa 2 como origen y la dirección de Capa 2 para R1 como destino.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Funciones-direcciones-Capa-2-y-Capa-3-2.png)

R1 encapsula el paquete IP de Capa 3 en una nuevo trama de Capa 2. En el encabezado de trama, R1 agrega su dirección de Capa 2 como origen y la dirección de Capa 2 para R2 como destino.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Funciones-direcciones-Capa-2-y-Capa-3-3.png)

R2 encapsula el paquete IP de capa 3 en una nuevo trama de capa 2. En el encabezado de trama, R2 agrega su dirección de Capa 2 como origen y la dirección de Capa 2 para el servidor como destino.

---

# Tramas LAN y WLAN

Los protocolos Ehtenet son utilizados por LAN cableadas. Las comunicaciones inalámbricas caen bajo protocolos WLAN (IEEE 802.11) Estos protocolos fuieron diseñaods para redes multiacceso.

Tradicionalmente, los WLAN utilizaban otros tipos de protocolos para vairos tipos de topologías punto a punto, hub-spoke y de malla completa. Alguno de los protocolos WAN comunes a lo largo de los años han incluido:

-   Protocolo punto a punto (PPP)
-   Control de enlace de datos de alto nivel (HDLC, High-Level Data Link Control)
-   Frame Relay
-   Modo de transferencia asincrónica (ATM)
-   X.25

Estos protocolos de capa 2 ahora están siendo reemplazados en la WAN por Ethernet.

En una red TCP/IP, todos los protocolos de capa 2 del modelo OSI funcionan con la dirección IP en la capa 3. Sin embargo, el protocolo de capa 2 específico que se utilice depende de la topología lógica y de los medios físicos.

Cada protocolo realiza el control de acceso a los medios para las topologías lógicas de Capa 2 que se especifican. Esto significa que una cantidad de diferentes dispositivos de red puede actuar como nodos que operan en la capa de enlace de datos al implementar estos protocolos. Estos dispositivos incluyen las tarjetas de interfaz de red en PC, así como las interfaces en routers y en switches de la Capa 2.

El protocolo de la Capa 2 que se utiliza para una topología de red particular está determinado por la tecnología utilizada para implementar esa topología. La tecnología está, a su vez, determinada por el tamaño de la red, en términos de cantidad de hosts y alcance geográfico y los servicios que se proveerán a través de la red.

Una LAN generalmente usa una tecnología de alto ancho de banda capaz de soportar grandes cantidades de hosts. El área geográfica relativamente pequeña de una LAN (un solo edificio o un campus de varios edificios) y su alta densidad de usuarios hacen que esta tecnología sea rentable.

Sin embargo, utilizar una tecnología de ancho de banda alto no es generalmente rentable para redes de área extensa que cubren grandes áreas geográficas (varias ciudades, por ejemplo). El costo de los enlaces físicos de larga distancia y la tecnología utilizada para transportar las señales a través de esas distancias, generalmente, ocasiona una menor capacidad de ancho de banda.

La diferencia de ancho de banda normalmente produce el uso de diferentes protocolos para las LAN y las WAN.

Los protocolos de la capa de enlace de datos incluyen:

-   Ethernet
-   802.11 inalámbrico
-   Protocolo punto a punto (PPP)
-   Control de enlace de datos de alto nivel (HDLC, High-Level Data Link Control)
-   Frame Relay