## 1. La Capa de Red

La capa de red, o Capa OSI 3, proporciona servicios para permitir que los dispositivos finales intercambien datos a través de redes. Como se muestra en la figura, IP versión 4 (IPv4) e IP versión 6 (IPv6) son los principales protocolos de comunicación de la capa de red. Otros protocolos de capa de red incluyen protocolos de enrutamiento como Open Shortest Path First ([[OSPF]]) y protocolos de mensajería como Internet Control Message Protocol (ICMP).

**Protocolos de capa de red**


![Protocolos de capa de red](https://ccnadesdecero.es/wp-content/uploads/2017/11/Protocolos-de-capa-de-red.png)


Para lograr comunicaciones end-to-end a través de los límites de la red, los protocolos de capa de red realizan cuatro operaciones básicas:

  

1.  **Direccionamiento de terminales**: Los terminales se deben configurar con una dirección IP única para identificarlos en la red.
2.  **Encapsulamiento**: La capa de red encapsula la unidad de datos del protocolo (PDU) de la capa de transporte a un paquete. El proceso de encapsulación agrega información de encabezado IP, como la dirección IP de los hosts de origen (envío) y destino (recepción). El proceso de encapsulación lo realiza el origen del paquete IP.
3.  **Enrutamiento o Routing**: La capa de red proporciona servicios para dirigir los paquetes a un host de destino en otra red. Para viajar a otras redes, el paquete debe ser procesado por un Router. La función del Router es seleccionar la mejor ruta y los paquetes directos hacia el host de destino en un proceso conocido como enrutamiento. Un paquete puede cruzar muchos Routers antes de llegar al host de destino. Cada Router que un paquete cruza para llegar al host de destino se llama salto.
4.  **Desencapsulamiento**: Cuando el paquete llega a la capa de red del host de destino, el host verifica el encabezado IP del paquete. Si la dirección IP de destino dentro del encabezado coincide con su propia dirección IP, el encabezado IP se elimina del paquete. Después de que el paquete es desencapsulado por la capa de red, la PDU de Capa 4 resultante se pasa al servicio apropiado en la capa de transporte. El proceso de desencapsulación lo realiza el host de destino del paquete IP.

**Nota**: Se denomina «salto» a cada router que cruza un paquete antes de alcanzar el host de destino.

Existen varios protocolos de capa de red. Sin embargo, solo hay dos protocolos de capa de red que suelen implementarse:

1.  Protocolo de Internet versión 4 (IPv4)
2.  Protocolo de Internet versión 6 (IPv6)

Protocolos de capa de red antiguos

-   Intercambio Novell de paquetes de internetwork (IPX)
-   AppleTalk
-   Servicio de red sin conexión (CLNS/DECNet)

A diferencia de la capa de transporte (OSI Layer 4), que gestiona el transporte de datos entre los procesos que se ejecutan en cada host, los protocolos de comunicación de la capa de red (es decir, IPv4 e IPv6) especifican la estructura de paquetes y el procesamiento utilizado para transportar los datos de un host a otro anfitrión. El funcionamiento sin tener en cuenta los datos transportados en cada paquete permite que la capa de red transporte paquetes para múltiples tipos de comunicaciones entre múltiples hosts.


![Capa Red Capa Transporte](https://ccnadesdecero.es/wp-content/uploads/2017/11/Capa-Red-Capa-Transporte.png)

Capa Red Capa Transporte

## 2. Encapsulación IP

IP encapsula el segmento de la capa de transporte (la capa justo por encima de la capa de red) u otros datos agregando un encabezado IP. El encabezado IP se usa para entregar el paquete al host de destino.

La imagen ilustra cómo la PDU de la capa de transporte es encapsulada por la PDU de la capa de red para crear un paquete IP.


![PDU de capa de transporte](https://ccnadesdecero.es/wp-content/uploads/2017/11/PDU-de-capa-de-transporte.png)

PDU de capa de transporte

El proceso de encapsular datos capa por capa permite que los servicios en las diferentes capas se desarrollen y escalen sin afectar las otras capas. Esto significa que los segmentos de la capa de transporte pueden empaquetarse fácilmente por IPv4 o IPv6 o por cualquier protocolo nuevo que pueda desarrollarse en el futuro.

El encabezado IP es examinado por dispositivos de Capa 3 (es decir, routers y switches de Capa 3) a medida que viaja a través de una red hasta su destino. Es importante tener en cuenta que la información de direccionamiento IP permanece igual desde el momento en que el paquete sale del host de origen hasta que llega al host de destino, excepto cuando el dispositivo realiza la traducción de direcciones de red (NAT) para IPv4.

Los routers implementan protocolos de enrutamiento para enrutar paquetes entre redes. El enrutamiento realizado por estos dispositivos intermediarios examina el direccionamiento de la capa de red en el encabezado del paquete. En todos los casos, la porción de datos del paquete, es decir, la PDU de la capa de transporte encapsulada u otros datos, permanece sin cambios durante los procesos de la capa de red.

## 3. Características de IP

IP fue diseñado como un protocolo con **baja sobrecarga**. Proporciona solo las funciones que son necesarias para entregar un paquete desde una fuente a un destino a través de un sistema interconectado de redes. El protocolo no fue diseñado para rastrear y administrar el flujo de paquetes. Estas funciones, si es necesario, son realizadas por otros protocolos en otras capas, principalmente TCP en la capa 4.

Estas son las características básicas de IP:

-   **Sin conexión**: no hay conexión con el destino establecido antes de enviar paquetes de datos.
-   **Mejor esfuerzo**: la IP es inherentemente poco confiable porque la entrega de paquetes no está garantizada.
-   **Independiente de los medios**: la operación es independiente del medio (es decir, cobre, fibra óptica o inalámbrico) que transporta los datos.

## 4. IP Sin conexión

IP no tiene conexión, lo que significa que IP no crea una conexión de extremo a extremo dedicada antes de enviar los datos. La comunicación sin conexión es conceptualmente similar a enviar una carta a alguien sin notificar al destinatario por adelantado.

**Sin conexión – Analogía – Red**


![IP Sin conexión](https://ccnadesdecero.es/wp-content/uploads/2017/11/IP-Sin-conexi%C3%B3n.png)


Las comunicaciones de datos sin conexión funcionan según el mismo principio. Como se muestra en la imagen, IP no requiere un intercambio inicial de información de control para establecer una conexión de extremo a extremo antes de que se reenvíen los paquetes.

## 5. IP: Mejor esfuerzo

IP tampoco requiere campos adicionales en el encabezado para mantener una conexión establecida. Este proceso reduce en gran medida la sobrecarga de IP. Sin embargo, sin una conexión de extremo a extremo preestablecida, los remitentes desconocen si los dispositivos de destino están presentes y son funcionales al enviar paquetes, ni saben si el destino recibe el paquete o si el dispositivo de destino puede acceder y leer el paquete.

El protocolo IP no garantiza que todos los paquetes que se entregan sean recibidos. La imagen ilustra la característica de entrega poco confiable, Entrega de servicio mínimo o de mejor esfuerzo del protocolo IP.

![IP con Mejor esfuerzo](https://ccnadesdecero.es/wp-content/uploads/2017/11/IP-con-Mejor-esfuerzo.png)

)IP con Mejor esfuerzo. Como un protocolo de capa de red poco confiable, IP no garantiza que se recibirán todos los paquetes enviados. Otros protocolos administran el proceso de seguimiento de paquetes y aseguran su entrega.

## 6. IP: Independiente del Medio

Que sea poco confiable significa que IP no tiene la funcionalidad para administrar o recuperar paquetes no recibidos o dañados. Esto se debe a que, si bien los paquetes IP se envían con información sobre la ubicación de la entrega, no contienen información que se pueda procesar para informar al remitente si la entrega fue exitosa. Los paquetes pueden llegar al destino dañados, fuera de secuencia o en absoluto. IP no proporciona capacidad para retransmitir paquetes si se producen errores.

Si se entregan paquetes fuera de servicio, o faltan paquetes, entonces las aplicaciones que usan los datos, o servicios de capa superior, deben resolver estos problemas. Esto permite que IP funcione de manera muy eficiente. En el conjunto de protocolos TCP/IP, la confiabilidad es la función del protocolo TCP en la capa de transporte.

IP opera independientemente de los medios que transportan los datos en las capas inferiores de la pila de protocolos. Como se muestra en la imagen, los paquetes IP se pueden comunicar como señales electrónicas a través de un cable de cobre, como señales ópticas a través de fibra o de forma inalámbrica como señales de radio.

![IP Independiente de medios](https://ccnadesdecero.es/wp-content/uploads/2017/11/IP-Independiente-de-medios.png)

IP Independiente de medios

La capa de enlace de datos OSI es responsable de tomar un paquete IP y prepararlo para la transmisión a través del medio de comunicación. Esto significa que la entrega de paquetes IP no se limita a ningún medio en particular.

Sin embargo, hay una característica principal de los medios que la capa de red considera: el tamaño máximo de la PDU que cada medio puede transportar. Esta característica se conoce como la unidad de transmisión máxima (**MTU**). Parte de la comunicación de control entre la capa de enlace de datos y la capa de red es el establecimiento de un tamaño máximo para el paquete. La capa de enlace de datos pasa el valor de MTU a la capa de red. La capa de red determina qué tan grandes pueden ser los paquetes.

En algunos casos, un dispositivo intermedio, generalmente un Router, debe dividir un paquete IPv4 cuando lo reenvía de un medio a otro con una MTU más pequeña. Este proceso se llama **fragmentar el paquete o fragmentación**. La fragmentación causa latencia. Los paquetes IPv6 no pueden ser fragmentados por el Router.

