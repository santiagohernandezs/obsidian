# Descripción general de ARP

Cada dispositivo de red Ethernet tineen una dirección MAC Ethernet única. Cuando un dispositivo envía una trama de capa 2 de ethernet, contiene estas dos direcciones.

-   **Dirección MAC de Destino** - La dirección MAC Ethernet del dispositivo de destino en el mismo segmento de red local. Si el host de destino está en otra red, entonces la dirección de destino de la trama sería la del gateway predeterminado (es decir, router).
-   **Dirección MAC de Origen** - La dirección MAC de la NIC de Ethernet en el host de origen.

La figura ilustra el problema al enviar una trama a otro host en el mismo segmento de red IPv4.

![](https://ccnadesdecero.es/wp-content/uploads/2017/11/Descripci%C3%B3n-general-de-ARP.png)

Para enviar un paquete a otro host en la misma red IPv4 local, un host debe reconocer la dirección IPv4 y la dirección MAC de dispositivo de destino. Las direcciones IPv4 de destino del dispositivo se conocen o se reseulven por el nombre del dispositivo. Sin embargo las direcciones MAC deben ser descubiertas.

Un dispositivo utiliza el protocolo de resolución de direcciones (ARP) para determinar la dirección MAC de destino de un dispositivo local cunado conoce su dirección IPv4.

ARP proporciona dos funciones básicas:

-   Resolución de direcciones IPv4 a direcciones MAC
-   Mantener una tabla de asignaciones de direcciones IPv4 a MAC

---

# Funciones del ARP

Cuando se envía un paquete a la cpaa de enlace de datos para encapsularlo en una trama de Ethernet, el dispositivo consulta una tabla en su memoria para encontrar la dirección MAC que está asignada a la dirección IPv4. Esta tabal se almacena temporalmente en la memoria RAM y se denomina tabla ARP o caché ARP.

El dispositov emisor busca en su tabla ARP la dirección IPv4 y la dirección MAC correspondiente.

-   Si la dirección IPv4 de destino del paquete está en la misma red que la dirección IPv4 de origen, el dispositov busca la dirección IPv4 de destino en la tabla ARP.
-   Si la dirección IPv4 de destino está en una red diferente que la dirección IPv4 de origen, el dispositivo busca la dirección IPv4 del gateway predeterminado.

En ambos casos, se realiza una búsqueda de la dirección IPv4 y la dirección MAC correspondiente para el dispositivo.

En cada entrada o fila de la tabal ARP, se enlaza una dirección IPv4 con una dirección IPv4 con una dirección MAC. Llamamos a la relación entre los dos valores un mapa. Esto solamente significa que es posible busca r una dirección IPv4 en la tabal y encontrar la direción MAC correspondiente. La tabla ARP almaecna temporalmente (en caché) la asignación para los dispositivos de la LAN.

Si ele dispositivo localiza la dirección IPv4, se utiliza la dirección MAC correspondiente como la dirección MAC de destino de la trama, Si no se encuentra ninguna entrada, el dispositivo envía una solicitud de ARP.

---

# Eliminación de entradas de una tabla ARP

Para cada dispositivo, un temporizador de memoria caché ARP elimina las entradas de ARP que no se hayan utilizado durante un período especificado. Los tiempos varían según el sistema operativo del dispositivo. Por ejemplo, los sistemas operativos Windows más recientes alamcenn entradas de tabla ARP entre 15 y 45 segundos, como de ilustra en la figura.

![](https://ccnadesdecero.es/wp-content/uploads/2017/11/Eliminar-entradas-de-tabla-ARP.png)

Los comandos también se pueden usar para eliminar manualmente algunas o todas las entradas de la tabal ARP. Después de eliminar una entrada, el proceso de envío de una solicitud de ARP y de recepción de una respuesta de ARP de ocurrir nuevamente para que se introduzca la asignación en la tabla ARP.

---

# Tablas ARP en dispositivos de red

En un router Cisco, el comando **show ip arp** se utiliza para mostrar la tabla ARP, como se muestra en la figura.

![](https://ccnadesdecero.es/wp-content/uploads/2017/11/Broadcasts-ARP.png)

En una PC con windows 10, el comando **arp-a** se usa para mostrar la tabal ARP, como se muestra en la figura.

![](https://ccnadesdecero.es/wp-content/uploads/2017/11/Suplantaci%C3%B3n-ARP.png)

---

# Problemas de ARP - Difusión ARO y suplantación ARP

Todos los dispositivos de la red local reciben y procesan una solicitud de ARP debido a que es una trama de disfusión. En una red comercial típicam estas difusiones tendrían, probablemente, u efecto mínimo en el rendimiento d ela red. Sin embargo, si se encendiera una gran cantidad de dispositivos que comeczaran a acceder a los servicios de red al mismo tiempo, el rendimiento podría disminuir durante un breve período, como se muestra en la figura.Después que los dispositivos envían las solicitudes de difusión ARP iniciales y obtienen las direcciones MAC necesarias, se minimiza cualquier efecto en la red.

En algunos casos, el uso de ARP puede conducir a un riego potencial de seguridad. Un atacnate puede usar la suplantación ARP para realizar un ataque de envenenamiento ARP. Esta técnica utilizada por un atacante para responder a una solicitud de ARP de una direcciónIPv4 que pertence a otro dispositivo, como la puerta de enlace predetermianda, tal como muestra en la ilustración. El receptor de la respuesta de ARP agrega la dirección MAC incorrecta a la tabla ARP y envía estos paquetes al atacante. Los switches de nivel empresarial incluyen técnicas de mitigación conocidas como “inspección dinámica de ARP (DAI)”. DAI está más allá del alcance de este curso.