# Encapsulamiento de Ethernet

Ethernet es una de las dos tecnologías LAN utilizadas hoy en día, siendo la otra LAN inalámbrica (WLAN). Ethernet utiliza comunicaciones por cable, incluyendo pares trenzados, enlaces de fibra óptica y cables coaxiales.

Ethernet funciona en la capa de enlace de datos y en la capa física. Es una familia de tecnologías de red definidas en los estándares IEEE 802.2 y 802.3. Ehternet soporta los siguientes anchos de banda.

-   10 Mbps
-   100 Mbps
-   1000 Mbps (1 Gbps)
-   10.000 Mbps (10 Gbps)
-   40,000 Mbps (40 Gbps)
-   100,000 Mbps (100 Gbps)

# Ethernet y el modelo OSI

![](https://ccnadesdecero.es/wp-content/uploads/2017/11/Encapsulamiento-Ethernet.png)

Ethernet se define mediante protocolos de capa física y de capa de enlace de datos.

# Subcapa de Enlace de datos

![](https://ccnadesdecero.es/wp-content/uploads/2017/11/Subcapas-de-Enlace-de-Datos-1.png)

# Estándares Ethernet en la subcapa MAC

![](https://ccnadesdecero.es/wp-content/uploads/2017/11/Subcapa-LLC.png)

# Campos de Trama de Ethernet

El tamaño de trama dee Ethernetes de 64 bytes, y el máximo es de 1518 bytes. Esto incluye todos los bytes del campo de dirección MAC de destino a través del campo de secuencia de verificación de trama (FCS). El campo preámbulo no se incluye al describir el tamaño de una trama.

Cualquier trama de menos de 64 bytes de longitud se considera un fragmento de colisión o una trama corta, y es descartada automáticamente por las estaciones receptoras. Las tramas de más de 1500 bytes se consideran ''Jumbos'' o tramas ''bebés gigantes''.

Si el tamaño de [[La Trama]] es inferior que el mínimo o mayor que el máximo, el dispositivo recpetor descarta la trama. Es posible que las tramas descartadas se originen en colisiones u otras señales no deseadas. Ellas se consideran inválidas. Las tramas Jumbo suelen ser compatibles con la mayoría de los switches y NIC Fast Ethernet y Gigabit Ethernet.

# Campos de la trama Ethernet

![](https://ccnadesdecero.es/wp-content/uploads/2017/11/Campos-de-trama-Ethernet.png)

## Detalles de la trama de Ethernet

-   **Campos Preámbulo y Delimitador de Inicio de Trama** - El preámbulo (7 bytes) y el Delimitador de tramas de inicio (SFD), también llamado Iniciode Trama (1 byte), los campos se utilizan para la sincronización entre el envío y recepción de dispositivos. Estos priomeros ocho bytes de trama son utilizados para llamar la atención de los nodos receptores.
-   **Campo Dirección MAC de Destino** - Este campo de 6 bytes es el identificador del destinario deseado. Esta dirección es usada por la capa 2 para ayudar a los dispositivos enm determinar si una trama está dirigido a ellos. La dirección en la trama es comparada con la dirección MAC en el dispositivo. Si hay una coincidencia, el acepta la trama. Puede ser Unicast o Multicast o Broadcast.
-   **Campo Dirección MAC de Origen** - Este campo de 6 bytes identifica la NIC o la interfaz de origen de la trama.
-   **Tipo/Longitud** - Este campo de 2 bytes identifica el protocolo de capa superior encapsulado en la trama de Ethernet. Los valores comunes son, en hexadecimal, 0x800 para IPv4, 0x86DD para IPv6 y 0x806 para ARP. **Nota**: También puede ver este campo denominado como Ethernet, type o Length.
-   **Campos de Datos** - Este campo (46 - 1500 bytes) contiene los datos encapsulados de una capa superior, que ser una PDU genérica de capa 3, o más comúnmente, un paquete IPv4. Todas las tramas deben tener, al menos, 64 bytes de longitud. Si un paquete pequeño es encapsulado, bits adicionales llamados **PAD** se utilizan para aumentar el tamaño de la trama a este tamaño mínimo.
-   **Campo Secuencia de Verificación de Trama** - El campo de verificación de trama o Frame Check Sequence (FCS) (4 bytes) se usa para detectar errores en una trama. Utiliza una Comprobación Cíclica de Redundancia o Cyclic Redundancy Check (CRC). El dispositivo de envío incluye los resultados de un CRC en el campo FCS de la trama. El dispositvo receptor recibe la trama y genera una CRC para buscar por errores. Si los cálculos coinciden, significa que no se produjo ningún error. Cálculos que no se descarta. Un cambio en los datos podría ser el resultado de una interrupción de las señales eléctrica squie respresentan los bits.