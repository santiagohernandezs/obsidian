# Desición de reenvío de host

Con IPv4 e IPv6, los paquetes siempre se crean los host de origen. El host de orgien debe poder dirigir el paquete al host de destino. Para ello, los dispositivos finales de host crean su propia tabal de enrutamiento. En este tema se explica cómo los dispositivos finales utilizan las tablas de enrutamiento.

Otra función de la capa de red es dirigir los paquetes entre un host. Un host puede envíar uin paquete a lo siguiente:

-   **Itself** - Un host puede hacer ping a sí mismo, mandando un paquete a la dirección IPv4 127.0.0.1 o a la dirección IPv6 ::1, que se conoce como interfaz de **Loopback** o de **Bucle invertido**.
-   **Host Local** - Este es un host de destino que se encuantra en la misma red local que el host emisor. Los host de origen y destino comparten la misma dirección de red.
-   **Host Remoto** - Este es un host de destino que se encuantra en una red remota. Los host de origen y destino no comparten la misma dirección de red.

![](https://ccnadesdecero.es/wp-content/uploads/2017/11/Decisi%C3%B3n-de-reenv%C3%ADo-de-host.png)

El dispositivo final de origen determina si un paquete está destinado a un host local o un host remoto. El dispositivo final de origen determina si la dirección IP de destino está en la misma red en la que se encuentra el dispositivo de origen. El método de determinación varía según la versión de IP:

-   **En IPv4**: el dispositivo de origen utiliza su propia máscara de subred junto con su propia dirección IPv4 y la dirección IPv4 de destino para realizar esta determinación.
-   **En IPv6**: el Router local anuncia la dirección de red local (prefijo) a todos los dispositivos en la red.

En una red doméstica o comercial, puede tener varios dispositivos cableados e inalámbricos interconectados mediante un dispositivo intermediario, como un Switch LAN o un punto de acceso inalámbrico (WAP). Este dispositivo intermediario proporciona interconexiones entre hosts locales en la red local. Los hosts locales pueden comunicarse entre sí y compartir información sin la necesidad de dispositivos adicionales. Si un host está enviando un paquete a un dispositivo que está configurado con la misma red IP que el dispositivo host, el paquete simplemente se reenvía desde la interfaz del host, a través del dispositivo intermediario, y directamente al dispositivo de destino.

Por supuesto, en la mayoría de las situaciones queremos que nuestros dispositivos puedan conectarse más allá del segmento de red local, como a otros hogares, negocios e Internet. Los dispositivos que están más allá del segmento de red local se conocen como hosts remotos. Cuando un dispositivo de origen envía un paquete a un dispositivo de destino remoto, se necesita la ayuda de routers y enrutamiento. El enrutamiento es el proceso de identificar la mejor ruta hacia un destino. El Router conectado al segmento de red local se denomina puerta de enlace predeterminada.

## 2. Puerta de Enlace Predeterminada

La puerta de enlace predeterminada (Default Gateway) es el dispositivo de red (es decir, el Router o el Switch de capa 3) que puede enrutar el tráfico a otras redes. Si usa la analogía de que una red es como una habitación, la puerta de enlace predeterminada es como una puerta. Si desea llegar a otra habitación o red, necesita encontrar la puerta.

En una red, una puerta de enlace predeterminada suele ser un Router con estas características:

-   Tiene una dirección IP local en el mismo rango de direcciones que otros hosts en la red local.
-   Puede aceptar datos en la red local y reenviar datos fuera de la red local.
-   Enruta el tráfico a otras redes.

Se requiere una puerta de enlace predeterminada para enviar tráfico fuera de la red local. El tráfico no se puede reenviar fuera de la red local si no hay una puerta de enlace predeterminada, la dirección de la puerta de enlace predeterminada no está configurada o la puerta de enlace predeterminada está inactiva.

## 3. Un Host Enruta a la Puerta de Enlace Predeterminada

Una tabla de enrutamiento de host generalmente incluirá una puerta de enlace predeterminada. En IPv4, el host recibe la dirección IPv4 de la puerta de enlace predeterminada, ya sea dinámicamente desde el Protocolo de configuración dinámica de host (DHCP) o configurado manualmente. En IPv6, el Router anuncia la dirección de puerta de enlace predeterminada o el host se puede configurar manualmente.

En la imagen, PC1 y PC2 están configuradas con la dirección IPv4 de 192.168.10.1 como la puerta de enlace predeterminada.

![](https://ccnadesdecero.es/wp-content/uploads/2017/11/Puerta-de-enlace-predeterminada.png)

Tener una puerta de enlace predeterminada configurada crea una ruta predeterminada en la tabla de enrutamiento de la PC. Una ruta predeterminada es la ruta o _pathway_ que tomará su computadora cuando intente ponerse en contacto con una red remota.

Tanto la PC1 como la PC2 tendrán una ruta predeterminada para enviar todo el tráfico destinado a redes remotas a R1.

## 4. Tablas de Enrutamiento de Host

En un host de Windows, el comando `**route print**` o `**netstat -r**` se puede usar para mostrar la tabla de enrutamiento del host. Ambos comandos generan la misma salida. La salida puede parecer abrumadora al principio, pero es bastante simple de entender.

La imagen muestra una topología de muestra y la salida generada por el comando `**netstat –r**`.

![](https://ccnadesdecero.es/wp-content/uploads/2017/11/Tablas-de-enrutamiento-de-host-1.png)

Al ingresar el comando `**netstat -r**` o el comando `**route print**` equivalente, se muestran tres secciones relacionadas con las conexiones de red TCP/IP actuales:

-   **Lista de interfaces**: enumera la dirección de Control de acceso a medios (MAC) y el número de interfaz asignado de cada interfaz con capacidad de red en el host, incluidos los adaptadores Ethernet, Wi-Fi y Bluetooth.
-   **Tabla de rutas IPv4**: enumera todas las rutas IPv4 conocidas, incluidas las conexiones directas, la red local y las rutas locales predeterminadas.
-   **Tabla de rutas IPv6:** enumera todas las rutas IPv6 conocidas, incluidas las conexiones directas, la red local y las rutas locales predeterminadas.