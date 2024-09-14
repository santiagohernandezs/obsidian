# Mensajes de descubrimiento de vecinos IPv6

El protocolo IPv6 Descubrimiento de vecinos se conoce a veces como ND o NDP. ND proporciona servicios de resolución de direcciones, detección de routers y redirección para IPv6 mediante ICMPv6. ICMPv6 ND utilza cinco mensajes ICMPv6 para realizar estos vecinos

-   NS: Mensajes de solicituda de vecinos.
-   NA: Mensajes de anuncio de vecino.
-   RS: Mensaje de solicitud del router.
-   RA: Mensajes de anuncio del router.
-   Mensaje de redirección.

Los mensajes de solicitud de veciono y anuncio de utilizan para la mensajería de desipositivo a dispositivo, como la resolución de direcciones (similar a ARP para IPv4). Los dispositvos incluyen ambos, hosts y routers.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Mensajes-de-dispositivo-a-dispositivo.png)

Los mensajes de solicitud de router y anuncio de roouter son para mensajes entre dispositivos y router. Normalmente la detección de routers se utiliza para al asignación dinámica de direcciones y la configuración automática de direcciones sin estado (SLAAC.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Mensajes-entre-dispositivos-y-routers.png)

**Nota**: El quinto mensaje ICMPv6 ND es un mensaje de redirección que se utiliza para una mejor selección de siguiente salto. Esto está fuera del alcance de este curso.

IPv6 ND se define en IETF RFC 4861

# Descubrimiento de vecino IPv6: resolución de direcciones

Al igual que ARP par aIPv4, los dispositivos IPv6 ND para determinar la dirección MAC de un dispositivo que tiene un dirección IPv6 conocida.

Los mensajes ICMPv6 Solicitud de vecino y Anuncio de vecino se utilizan para la resolución de la dirección MAC. Esto es similar a las solicitudes ARP y las respuestas ARP utilizadas por ARP para IPv4. Por ejemplo, supongamos que PC1 desea hacer ping a PC2 en la dirección IPv6 2001:db8:acad: :11. Para determinar

En el proceso de resolución de direcciones MAC Ethernet ICMPv6 utiliza Solicitud de Router y Anuncio de Vecino