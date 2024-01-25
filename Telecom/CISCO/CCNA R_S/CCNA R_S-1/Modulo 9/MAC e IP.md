## Destino en la Misma Red

Hay dos direcciones principales asignadas a un dispositivo en una LAN Ethernet:

-   **Dirección física (la dirección MAC)**: se utiliza para comunicaciones NIC a NIC en la misma red Ethernet.
-   **Dirección lógica (la dirección IP)**: se utiliza para enviar el paquete desde el dispositivo de origen al dispositivo de destino. La dirección IP de destino puede estar en la misma red IP que la fuente o puede estar en una red remota.

Las direcciones físicas de capa 2 (es decir, las direcciones MAC de Ethernet) se utilizan para entregar la trama de enlace de datos con el paquete IP encapsulado de una NIC a otra NIC que está en la misma red. Si la dirección IP de destino está en la misma red, la dirección MAC de destino será la del dispositivo de destino.

Considera el siguiente ejemplo usando representaciones simplificadas de direcciones MAC.

![Destino en la misma red](https://ccnadesdecero.es/wp-content/uploads/2020/03/Destino-en-la-misma-red.png)

En este ejemplo, la PC1 quiere enviar un paquete a la PC2. La imagen muestra las direcciones MAC de origen y destino de la capa 2 y el direccionamiento IPv4 de la capa 3 que se incluiría en el paquete enviado desde la PC1.

La trama Ethernet de capa 2 contiene lo siguiente:

-   **Dirección MAC de destino**: esta es la dirección MAC simplificada de PC2, 55-55-55.
-   **Dirección MAC de origen**: esta es la dirección MAC simplificada de la NIC Ethernet en PC1, aa-aa-aa.

El paquete IP de capa 3 contiene lo siguiente:

-   **Dirección IPv4 de origen**: esta es la dirección IPv4 de PC1, 192.168.10.10.
-   **Dirección IPv4 de destino**: esta es la dirección IPv4 de PC2, 192.168.10.11.

## 2. Destino en Red Remota

Cuando la dirección IP de destino (IPv4 o IPv6) está en una red remota, la dirección MAC de destino será la dirección de la puerta de enlace predeterminada del host (es decir, la interfaz del Router).

Considera el siguiente ejemplo usando una representación simplificada de la dirección MAC.

![Destino en red remota](https://ccnadesdecero.es/wp-content/uploads/2020/03/Destino-en-red-remota.png)

En este ejemplo, la PC1 quiere enviar un paquete a la PC2. PC2 está ubicado en una red remota. Como la dirección IPv4 de destino no está en la misma red local que la PC1, la dirección MAC de destino es la de la puerta de enlace predeterminada local en el Router.

Los routers examinan la dirección IPv4 de destino para determinar la mejor ruta para reenviar el paquete IPv4. Cuando el Router recibe la trama de Ethernet, desencapsula la información de la capa 2. Usando la dirección IPv4 de destino, determina el dispositivo del siguiente salto y luego encapsula el paquete IPv4 en un nueva trama de enlace de datos para la interfaz saliente.


[![Componentes Básicos Red Computadoras](https://ccnadesdecero.es/wp-content/uploads/2017/11/Componentes-B%C3%A1sicos-Red-Computadoras-150x150.png)](https://ccnadesdecero.es/componentes-basicos-de-una-red/)

### [Componentes Básicos de Red de Computadoras](https://ccnadesdecero.es/componentes-basicos-de-una-red/)

En nuestro ejemplo, R1 ahora encapsularía el paquete con nueva información de dirección de Capa 2 como se muestra en la imagen.

![Router encapsula paquete](https://ccnadesdecero.es/wp-content/uploads/2020/03/Router-encapsula-paquete-R.png)

La nueva dirección MAC de destino sería la de la interfaz R2 G0/0/1 y la nueva dirección MAC de origen sería la de la interfaz R1 G0/0/1.

A lo largo de cada enlace en una ruta, un paquete IP se encapsula en una trama. La trama es específica de la tecnología de enlace de datos asociada con ese enlace, como Ethernet. Si el dispositivo del siguiente salto es el destino final, la dirección MAC de destino será la del NIC de Ethernet del dispositivo, como se muestra en la imagen.

![Trama en Red Remota](https://ccnadesdecero.es/wp-content/uploads/2020/03/Trama-Red-Remota.png)

¿Cómo se asocian las direcciones IP de los paquetes IP en un flujo de datos con las direcciones MAC en cada enlace a lo largo de la ruta al destino? Para los paquetes IPv4, esto se realiza a través de un proceso llamado Protocolo de resolución de direcciones (ARP). Para los paquetes IPv6, el proceso es ICMPv6 Neighbour Discovery (ND).

## 3. Packet Tracer – Identificar direcciones MAC e IP

En este Packet Tracer, actividad, completará los siguientes objetivos:

-   Recopilar información de PDU para la comunicación de red local
-   Recopilar información de la PDU para la comunicación de red remota