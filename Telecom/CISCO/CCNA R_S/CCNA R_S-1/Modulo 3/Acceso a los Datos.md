# Direcciones

La capa 2 y 3 son responsables de llevar el mensaje desde el origen hacia el destino, ya que ambos protocolos contienen las direcciones de origen y destino, pero tienen objetivos distintos.

-   **Direcciones de origen y de destino en la capa de red**: Son responsables de enviar el paquete IP desde el dispositivo de origen hasta el dispositivo final, ya esa en la misma red o a una red remota.
-   **Direcciones de origen y de destino de la capa de enlace de datos**: Son responsables de enviar [[La Trama]] de enlace de datos desde una tarjeta de interfaz de red (NIC) a otra en la misma red.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Direcci%C3%B3n-de-origen-y-direcci%C3%B3n-de-destino.png)

# Dirección lógica de capa 3

Una dirección de capa de red, o capa 3, se utiliza para enviar el paquete IP desde el orgien hacia el destino.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Direcci%C3%B3n-l%C3%B3gica-de-capa-3.png)

Los paquetes IP contienen dos direcciones IP:

-   **Dirección IP de origen:** La direccion IP del dispositivo emisor, la fuente de origen del paquete.
-   **Dirección IP de destino:** La direcciones

Las direcciones IP indican la dirección IP de origen original y la dirección IP de destino final. Esto es cierto tanto si el origen como el destino están en la misma red IP o en diferentes redes IP.

Una dirección IP contiene dos partes:

-   **Parte de red (IPv4) o Prefijo (IPv6)** : la parte más a la izquierda de la dirección que indica la red en la que es miembro la dirección IP. Todos los dispositivos en la misma red tendrán la misma porción de red de la dirección.
-   **Parte del host (IPv4) o ID de interfaz (IPv6)**: la parte restante de la dirección que identifica un dispositivo específico en la red. Esta porción es única para cada dispositivo o interfaz en la red.

## 3. Dispositivos en la misma red

En este ejemplo, tenemos una computadora cliente, PC1, que se comunica con un servidor FTP en la misma red IP.

-   **Dirección IPv4 de origen**: la dirección IPv4 del dispositivo emisor, la computadora cliente PC1: 192.168.1.110.
-   **Dirección IPv4 de destino**: la dirección  IPv4 del dispositivo receptor, servidor FTP: 192.168.1.9.

En la figura, observe que la porción de red de las direcciones IP de origen y de destino se encuentran en la misma red.

![Dispositivos en la misma red](https://ccnadesdecero.es/wp-content/uploads/2020/03/Dispositivos-en-la-misma-red.png)

Dispositivos en la misma red

Observa en la imagen que la porción de red de la dirección IPv4 de origen y la porción de red de la dirección IPv4 de destino son las mismas y, por lo tanto; el origen y el destino están en la misma red.

## 4. Rol de las Direcciones de Capa de Enlace de Datos: Misma Red IP

Cuando el emisor y el receptor del paquete IP están en la misma red, [[La Trama]] del enlace de datos se envía directamente al dispositivo receptor. En una red Ethernet, las direcciones de enlace de datos se conocen como direcciones de **Control de acceso a medios de Ethernet (MAC)**, como se resalta en la imagen.

![Control de acceso a medios de Ethernet o MAC](https://ccnadesdecero.es/wp-content/uploads/2020/03/Control-de-acceso-a-medios-de-Ethernet-o-MAC.png)

Control de acceso a medios de Ethernet o MAC

Las direcciones MAC están físicamente integradas en la NIC de Ethernet.

-   **Dirección MAC de orige**n: esta es la dirección del enlace de datos, o la dirección MAC de Ethernet, del dispositivo que envía [[La Trama]] del enlace de datos con el paquete IP encapsulado. La dirección MAC de la NIC Ethernet de PC1 es **AA-AA-AA-AA-AA-AA**, escrita en notación hexadecimal.
-   **Dirección MAC de destino**: cuando el dispositivo receptor está en la misma red que el dispositivo emisor, esta es la dirección de enlace de datos del dispositivo receptor. En este ejemplo, la dirección MAC de destino es la dirección MAC del servidor FTP: **CC-CC-CC-CC-CC-CC**, escrita en notación hexadecimal.

[[La Trama]] con el paquete IP encapsulado ahora se puede transmitir desde la PC1 directamente al servidor FTP.

## 5. Dispositivos en una Red Remota

Pero, ¿cuáles son los roles de la dirección de la capa de red y la dirección de la capa de enlace de datos cuando un dispositivo se comunica con un dispositivo en una red remota? En este ejemplo, tenemos una computadora cliente, PC1, que se comunica con un servidor, llamado Web Server, en una red IP diferente.

## 6. Rol de las Direcciones de Capa de Red

Cuando el remitente del paquete está en una red diferente del receptor, las direcciones IP de origen y destino representarán a los hosts en diferentes redes. Esto se indicará mediante la porción de red de la dirección IP del host de destino.

-   **Dirección IPv4 de origen**: la dirección IPv4 del dispositivo emisor, la computadora cliente PC1: 192.168.1.110.
-   **Dirección IPv4 de destino**: la dirección  IPv4 del dispositivo receptor, el servidor, el servidor web: 172.16.1.99.


![Dispositivos en una red remota](https://ccnadesdecero.es/wp-content/uploads/2020/03/Dispositivos-en-una-red-remota.png)

Dispositivos en una red remota

Observa en la imagen que la porción de red de la dirección IPv4 de origen y la dirección IPv4 de destino se encuentran en redes diferentes.

## 7. Rol de las Direcciones de Capa de Enlace de Datos: Diferentes Redes IP

Cuando el remitente y el receptor del paquete IP están en redes diferentes, la trama de enlace de datos Ethernet no se puede enviar directamente al host de destino porque el host no es directamente accesible en la red del remitente. La trama de Ethernet debe enviarse a otro dispositivo conocido como Router o puerta de enlace predeterminada (default gateway). En nuestro ejemplo, la puerta de enlace predeterminada es R1. R1 tiene una dirección de enlace de datos Ethernet que está en la misma red que PC1. Esto permite que la PC1 llegue al enrutador directamente.

![Capa 2 en diferentes redes IP](https://ccnadesdecero.es/wp-content/uploads/2020/03/Capa-2-en-diferentes-redes-IP.png)

Capa 2 en diferentes redes IP

-   **Dirección MAC de origen**: la dirección MAC de Ethernet del dispositivo emisor, PC1. La dirección MAC de la interfaz Ethernet de PC1 es AA-AA-AA-AA-AA-AA.
-   **Dirección MAC de destino**: cuando el dispositivo receptor, la dirección IP de destino, se encuentra en una red diferente del dispositivo emisor, el dispositivo emisor utiliza la [[Dirección MAC Ethernet]] de la puerta de enlace o enrutador predeterminado. En este ejemplo, la dirección MAC de destino es la dirección MAC de la interfaz Ethernet R1, 11-11-11-11-11-11. Esta es la interfaz que está conectada a la misma red que PC1, como se muestra en la imagen.

La trama de Ethernet con el paquete IP encapsulado ahora se puede transmitir a R1. R1 reenvía el paquete al destino, Servidor web. Esto puede significar que R1 reenvía el paquete a otro Router o directamente al servidor web si el destino está en una red conectada a R1.

**Es importante que la dirección IP de la puerta de enlace predeterminada se configure en cada host de la red local**. Todos los paquetes a un destino en redes remotas se envían a la puerta de enlace predeterminada. Las direcciones MAC de Ethernet y la puerta de enlace predeterminada se analizan con más detalle en otros módulos.

## 8. Direcciones de Enlace de Datos

La dirección física de la capa 2 del enlace de datos tiene una función diferente. El propósito de la dirección del enlace de datos es entregar la trama del enlace de datos desde una interfaz de red a otra interfaz de red en la misma red.

Antes de que un paquete IP pueda enviarse a través de una red cableada o inalámbrica, debe encapsularse en una trama de enlace de datos, para que pueda transmitirse a través del medio físico.