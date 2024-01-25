# Encabezado de paquetes IPv4

IPv4 es uno de los principales protocolos de comunicación de la capa de red (capa 3). El encabezado del paquete IPv4 se uitiliza para garantizar que este paquete se entrega en su siguiente parada en el camino al su dispositivo final de destino.

El encabezado IPv4 consta de campos que contienen información importante sobre le paquete. Estos campos tienen números binarios que examinan el proceso de capa 3

---

# Campos de encabezado de paquete IPv4

Los valores binarios de cada campo identifican diversos parámetros de configuración del paquete IP. Los diagramas de encabezado del protocolo, que se leen de izquierda a derecha y de arriba hacia abajo, proporcionan una representación visual de consulta al analizar los campos de protocolo. El diagram de encabezado del protocolo IP en la ilustración identifica los campos de un paquete IPv4.

![](https://ccnadesdecero.es/wp-content/uploads/2017/11/Campos-Encabezado-Paquete-IPv4.png)

Los campos significativos en el encabezado IPv4 incluyen lo siguiente:

-   **Versión -** Contiene un valor binario de **4** bits establecido en **0100** que identifica esto como un paquete **IPv4**.
-   **Servicios diferenciados o DiffServ (DS)** Este campo, formalmente conocido como **Tipo de servicio (ToS)**, es un campo de 8 bits que se utiliza para determinar la prioridad de cada paquete. Los seis bits más significativos del campo **DiffServ** son los bits de **punto de código de servicios diferenciados (DSCP)** y los dos últimos bits son los bits de **notificación de congestión explícita (ECN)**.
-   **Suma de comprobación de encabezado -** Se utiliza para detectar daños en el encabezado IPv4.
-   **Tiempo de duración (Time to Live,TTL) - TTL** contiene un valor binario de 8 bits que se utiliza para limitar la vida útil de un paquete**.** El dispositivo de origen del paquete IPv4 establece el valor TTL inicial. Se reduce en uno cada vez que el paquete es procesado por un router. Si el campo TTL llega a cero, el router descarta el paquete y envía a la dirección IP de origen un mensaje de tiempo superado del protocolo de mensajes de control de Internet (ICMP). Debido a que el router disminuye el TTL de cada paquete, el router también debe volver a calcular la suma de comprobación del encabezado.
-   **Protocolo -** Este campo se utiliza para identificar el protocolo del siguiente nivel. Este valor binario de 8 bits indica el tipo de carga de datos que lleva el paquete, lo que permite que la capa de red transmita los datos al protocolo de la capa superior apropiado. ICMP (1), TCP (6) y UDP (17) son algunos valores comunes.
-   **Dirección IPv4 de origen -** Contiene un valor binario de 32 bits que representa la dirección IPv4 de origen del paquete. La dirección IPv4 de origen es siempre una dirección unicast.
-   **Dirección IPv4 de destino -** Contiene un valor binario de 32 bits que representa la dirección IPv4 de destino del paquete. La dirección IPv4 de destino es una dirección unicast, multicast o de difusión.

Los dos campos a los que se hace más referencia son los de dirección IP de origen y de destino En estos campos, se identifica de dónde viene el paquete y a dónde va