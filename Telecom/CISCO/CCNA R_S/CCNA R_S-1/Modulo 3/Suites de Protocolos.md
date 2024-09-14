# Conjuntos de protocolos de red

En muchos casos, los protocolos deben trabajar entre sí para que la experiencia en línea sea lo más eficaz posible. Los conjuntos de protocolos están diseñados para trabajar entre sí sin ningun problema.

Un gurpo de prtocolos interrelacionados que son necesarios para realizar una función de comunicación se denomina **Suite de protocolo.**

Como se muestra en la figura, podemos utilizar capas para describir la actividad que tiene lugar en el ejemplo de comunicación cara a cara. En la capa inferior, la capa física, hay dos personas, cada una con una voz que puede pronunciar palabras en voz alta. En el medio está la capa de reglas que estipula los requisitos de comunicación incluyendo que se debe elegir un lenguaje común. En la parte superior está la capa de contenido y aquí es donde se habla realmente el contenido de la comunicación.

![](https://ccnadesdecero.es/wp-content/uploads/2017/11/Ejemplo-Conjunto-Protocolos.png)

**NOTA** - Las suites de protocolos son conjuntos de reglas que funcionan conjuntamente para ayudar a resolver un problema.

# Evolcuión de los conjuntos de protocolos

Desde 1970 ha habido varios conjuntos de portocolos diferentes, algunos desarollados por una orgnaización de estnándares y otros desarrollados por varios proveedores.

Durante la evolución de las comunicaciones de red e Internet hubo varios conjuntos de protcolos competidores, como se muestra en la figura.

![](https://ccnadesdecero.es/wp-content/uploads/2017/11/Evoluci%C3%B3n-de-suites-de-protocolo.png)

-   **Internet Protocol Suite o TCP/IP** - Este es el conjunto de protocolos más común y relevante que se utiliza hoy en día. El Conjunto de protocolos TCP/IP es un conjunto de protocolos estándar abierto mantenido por Internet Engineering Task Force (IETF).
-   **Open Systems Interconnection (OSI)** - Esta es una familia de protoclos desarrollados conjuntamente en 1977 por la Internationa Organization for Standarization (ISO) y la International telecommunication Union (ITU). El protocolo OSI también inclu{ia un modelo de siete capas llamado _modelo de referecia OSI_. Hoy OSI es conocido principalmente por su modelo en capas. Los protocolos han sido reemplazados en gran medida por TCP/IP.
-   **AppleTalk** - Un paquete de protocolos propietario de corta duración lanzado por Apple Inc. en 1985 para dispositivos Apple. En 1995, Apple adoptó TCP/IP para reemplazar a AppleTalk.
-   **Novell NetWare** - Un conjunto de protocolos propietarios de corta duración y sistema operativo de red desarrollado por Novell Inc. en 1983 utilizando el protocolo de red IPX. En 1995, Novell adoptó TCP/IP para reemplazar a IPX.

# Ejemplo de protocolo TCP/IP

Los protocolos TCP/IP son específicos de las capas de aplicación, Transporte e Internet. No hay protocolos TCP/IP en la capa de acceso a la red. Los protocolos LAN de capa de acceso a la red más comunes son los protocolos Ethernet y WLAN. Los protocolos de capa de acceso a la red son responsables de la entrega de los paquetes IP en los médios físicos.

La figura muestra un ejemplo de los tres protocolos TCP/IP utilizados para enviar paquetes entre el navegador web de un host y el servidor web. HTTP, TCP e IP son los protocolos TCP/IP utilizados. En la capa de acceso a la red, Ethernet se utiliza en el ejemplo. Sin embargo, esto también podría ser un estándar inalámbrico como WLAN o servicio celular.

![](https://ccnadesdecero.es/wp-content/uploads/2017/11/Ejemplo-protocolos-TCP-IP.png)

# Conjunto de TCP/IP

![](https://ccnadesdecero.es/wp-content/uploads/2017/11/Suite-Protocolos-TCP-IP.png)

TCP/IP tiene dos aspectos importantes para proveedores y fabricantes:

-   **Suite de protocolo estándar abierto** - esto significa que está disponible gratuitamente para el público y puede ser utilizado por cualquier proveedor en su hardware o en su software.
-   **Suite de protocolo basado en estándares** - Esto significa que ha sido respaldado por la industria de redes y aprobado por una organización de estándares. Esto asegura que productos de distintos fabricantes puedan interoperar correctamente.

---

# Capa de aplicación

### Sistemas de nombres

-   **DNS** - Domain Name System. Traduce los nombres de dominio tales como [cisco.com](http://cisco.com) a direcciones IP.

### Configuración de host

-   **DHCPv4** - Protocolo de configuración de host para IPv4. Asigna dinámicamente información de direccionamineto a IPv4 a clientes DHCPv4 al inicio y permite que las direcciones se reutilicen cuando y ano sean necesarias.
-   **DHCPv6** - Protocolo de configuración dinámica de host para IPv6. DHCPv6 es similar a DHCPv4. Un servidor DHCPv6 asigna dinámicamente información de direccionamiento IPv6 a clientes DHCPv6 al inicio y permite que las direcciones se reutilicen cuando y ano sean necesarias.
-   **SLAAC** - Autoconfiguración sin estado. Método que permite a un dispostivo obtener su información de direccionamiento IPv6 sin utilizar un servidor DHCPv6.

### Correo Electrónico

-   **SMTP** - Simple Mail Transfer Protocol. Les permite a los clientes enviar correo electrónico a un servidor de correo y les permite a los servidores enviar correo a otros dervidores.
-   **POP3** - Post Office Protocol versión 3. Permite a los clientes recuperar el correo electrónico de un servidor de correo y descargarlo en la aplicación de correo local del cliente.
-   **IMAP** - Internet Message Access Protocol. Permite que los clientes accedan a los correos electrónicos almacenados en un servidor de correo.

### Transferencia de Archivos

-   **FTP** - File Transfer Protocol. Establece las reglas que les permite a un ususario en un host acceder y transferir archivos hacia y desde otros host a través de una red. Es un protocolo confiable de entraga de archivos, orientado a la conexión y con acuse de recibo.
-   **SFTP** - SSH File Transfer Protocol. SFTP se puede utilizar para establecer una sesión segura de transferencia de archivos, en el que el archivo transferido eatá cifrado.
-   **TFTP** - Trivial file transfer Protocol. Un protocolo de transferencia de archivos simple y sin conexión con la entrega de archivos sin reconocimiento y el mejor esfuerzo posible. Utiliza menos sobrecarga que FTP.

### Web y Servicio Web

-   **HTTP** - Hypertext Transfer Protocol. Un conjunto de reglas para intercambiar texto, imágenes, sonido, video y otros archivos multimedia en la World Wide Web.
-   **HTTPS** - Secure HTTP. Una forma segura de HTTP que cifra los datos que de intercambian a través de la World Wide Web.
-   **REST** - Representational State Transfer.

---

# Capa de transporte

### Orientado a la conexión

-   **TCP** - Transmission Control Protocol. Permite la comunicación confiable entre procesos que se ejecutan en hosts independientes y tiene transmisiones y con acuse de recibo que confirman la entrega exitosa.

Sin conexión

-   **UDP** - User Datagram Protocol. Habilita un proceso que se ejecuta en un host para enviar paquetes a un proceso que se ejecuta en otro host, sin embargo, UDP no confirma la transmición correcta de datagramas.

---

# Capa de internet

### Protocolo de internet

-   **IPv4** - Protocolo de Internet versión 4. Recibe segmentos de mansaje de la capa de transporte, empaqueta mensajes en paquetes y los dirige **end-to-end** a través de una red. IPv4 utiliza una dirección de 32 bits.
-   **IPv6** - IP versión 6. Similar a IPv4 pero usa una dirección de 128 bits.
-   **NAT** - Traducción de direcciones de red. Traduce las direcciones IPv4 de una red provada de direcciones IPv4 públicas globalmente únicas.

### Mensajería

-   **ICMPv4** - Internet Control Message Protocol. Proporciona comentarios desde un host de destino a un host de origen con respecto a los errores en la entrega de paquetes.
-   **ICMPv6** - ICMP para IPv6. Funcinalidad similar a ICMPv4 pero se utiliza para paquetes IPv6.
-   **ICMPv6 ND** - Neighbor Discovery versión 6 incluye cuatro mensajes de protocolo que se utilizan para la resolución de direcciones y la detección de direcciones duplicadas.

### Protocolos de Routing

-   **OSPF** - Open Shortest Path First. Protocolo de enrutamiento de estado de vínculo que utiliza un diseño jerárquico basado en áreas. OSPF es un protocolode routing interior de estándar abierto.
-   **EIGRP** - Enhanced Interior Gateway Routing Protocol. Es un protocolo de routing abierto desarrollado por Cisco, utiliza una métrica compuesta en función del ancho de banda, la demora, la carga y la confiabilidad.
-   **BGP** - Border Gateway Protocol. Un protcolo de enrutamiento de puerta de enlace exterior estándar abierto utilizado entre los ISPs. BGP también se utiliza entre los ISPs y sus clientes privados más grandespara intercambiar información de enrutamiento.

---

# Capa de Acceso de Red

### Resolución de dirección

-   **ARP** - Proporciona la asignación de direcciones dinámicas entra un driección IP y una dirección de hardware

**Nota**: Puede ver otro estado de documentación que ARP opera en la capa de Internet (OSI Capa 3). Sin embargo, hayq ue declarar que ARP funciona en la capa 2 ya que su objetivo principal es descubrir la dirección MAC del destino. Una dirección de capa 2 es una dirección MAC.

### Protocolos de Enlace de Datos

-   **Ethernet** - Define las reglas para conectar y señalizar estándares de la capa de acceso a la red.
-   **WLAN** - Wireless Local Area Network. Define las reglas para señalización inalámbrica a través de las frecuencias de radio de 2.4 GHz y 5GHz.

---

## Conjunto de Protocolos TCP/IP

Hoy, el conjunto de protocolos TCP/IP incluye muchos protocolos y continúa evolucionando para admitir nuevos servicios. Algunos de los más populares se muestran en la imagen.

![Suite Protocolos TCP IP](https://ccnadesdecero.es/wp-content/uploads/2017/11/Suite-Protocolos-TCP-IP.png)

### Suite Protocolos TCP IP

TCP/IP es el conjunto de protocolos utilizado por Internet y las redes de hoy. TCP / IP tiene dos aspectos importantes para vendedores y fabricantes:

-   **Conjunto de protocolos estándar abierto**: esto significa que está disponible gratuitamente para el público y puede ser utilizado por cualquier proveedor en su hardware o en su software.
-   **Conjunto de protocolos basados ​​en estándares**: esto significa que ha sido respaldado por la industria de redes y aprobado por una organización de estándares. Esto garantiza que los productos de diferentes fabricantes puedan interoperar con éxito.

Haz clic en cada botón para obtener una breve descripción de los protocolos en cada capa.

-   [Capa de Aplicación](https://ccnadesdecero.es/conjuntos-protocolos-de-red/#)
-   [Capa de Transporte](https://ccnadesdecero.es/conjuntos-protocolos-de-red/#)
-   [Capa de Internet](https://ccnadesdecero.es/conjuntos-protocolos-de-red/#)
-   [Capa de Acceso a la Red](https://ccnadesdecero.es/conjuntos-protocolos-de-red/#)

### Sistema de nombres

-   **DNS:** Sistema de nombres de dominio. Traduce nombres de dominio como ccnadesdecero.es, a direcciones IP.

Configuración de host

-   **DHCPv4**: protocolo de configuración dinámica de host para IPv4. Un servidor DHCPv4 asigna dinámicamente información de direccionamiento IPv4 a los clientes DHCPv4 al inicio y permite que las direcciones se reutilicen cuando ya no sean necesarias.
-   **DHCPv6**: protocolo de configuración dinámica de host para IPv6. DHCPv6 es similar a DHCPv4. Un servidor DHCPv6 asigna dinámicamente información de direccionamiento IPv6 a clientes DHCPv6 al inicio.
-   **SLAAC**- Configuración automática de direcciones sin estado. Un método que permite que un dispositivo obtenga su información de direccionamiento IPv6 sin usar un servidor DHCPv6.

Email

-   **SMTP**: protocolo simple de transferencia de correo. Permite a los clientes enviar correos electrónicos a un servidor de correo y permite a los servidores enviar correos electrónicos a otros servidores.
-   **POP3:** Protocolo de oficina de correos versión 3. Permite a los clientes recuperar el correo electrónico de un servidor de correo y descargar el correo electrónico a la aplicación de correo local del cliente.
-   **IMAP**: Protocolo de acceso a mensajes de Internet. Permite a los clientes acceder al correo electrónico almacenado en un servidor de correo, así como mantener el correo electrónico en el servidor.

Transferencia de archivos

-   **FTP:** Protocolo de transferencia de archivos. Establece las reglas que permiten a un usuario en un host acceder y transferir archivos hacia y desde otro host a través de una red. FTP es un protocolo de entrega de archivos confiable, orientado a la conexión y reconocido.
-   **SFTP:** Protocolo de transferencia de archivos SSH. Como una extensión del protocolo Secure Shell (SSH), SFTP se puede usar para establecer una sesión segura de transferencia de archivos en la que la transferencia de archivos está encriptada. SSH es un método de inicio de sesión remoto seguro que generalmente se usa para acceder a la línea de comando de un dispositivo.
-   **TFTP:** Protocolo de transferencia de archivos trivial. Un protocolo simple de transferencia de archivos sin conexión con el mejor esfuerzo, entrega de archivos no reconocida. Utiliza menos gastos generales que FTP.

Web y servicio web

-   **HTTP:** Protocolo de Transferencia de Hipertexto. Un conjunto de reglas para intercambiar texto, imágenes gráficas, sonido, video y otros archivos multimedia en la World Wide Web.
-   **HTTPS**: HTTP Seguro. Una forma segura de HTTP que encripta los datos que se intercambian a través de la World Wide Web.
-   **REST:** Transferencia de Estado Representacional. Un servicio web que utiliza interfaces de programación de aplicaciones (API) y solicitudes HTTP para crear aplicaciones web.

## 5. Proceso de Comunicación TCP/IP

Hoy, el conjunto de protocolos TCP/IP incluye muchos protocolos y continúa evolucionando para admitir nuevos servicios. Algunos de los más populares se muestran en la imagen.

![](https://ccnadesdecero.es/wp-content/uploads/2017/11/Suite-Protocolos-TCP-IP.png)

TCP/IP es el conjunto de protocolos utilizado por Internet y las redes de hoy. TCP / IP tiene dos aspectos importantes para vendedores y fabricantes:

-   **Conjunto de protocolos estándar abierto**: esto significa que está disponible gratuitamente para el público y puede ser utilizado por cualquier proveedor en su hardware o en su software.
-   **Conjunto de protocolos basados en estándares**: esto significa que ha sido respaldado por la industria de redes y aprobado por una organización de estándares. Esto garantiza que los productos de diferentes fabricantes puedan interoperar con éxito.

Haz clic en cada botón para obtener una breve descripción de los protocolos en cada capa.

### Capa de Aplicación 
Sistema de nombres

-   **DNS:** Sistema de nombres de dominio. Traduce nombres de dominio como ccnadesdecero.es, a direcciones IP.

Configuración de host

-   **DHCPv4**: protocolo de configuración dinámica de host para IPv4. Un servidor DHCPv4 asigna dinámicamente información de direccionamiento IPv4 a los clientes DHCPv4 al inicio y permite que las direcciones se reutilicen cuando ya no sean necesarias.
-   **DHCPv6**: protocolo de configuración dinámica de host para IPv6. DHCPv6 es similar a DHCPv4. Un servidor DHCPv6 asigna dinámicamente información de direccionamiento IPv6 a clientes DHCPv6 al inicio.
-   **SLAAC**- Configuración automática de direcciones sin estado. Un método que permite que un dispositivo obtenga su información de direccionamiento IPv6 sin usar un servidor DHCPv6.

Email

-   **SMTP**: protocolo simple de transferencia de correo. Permite a los clientes enviar correos electrónicos a un servidor de correo y permite a los servidores enviar correos electrónicos a otros servidores.
-   **POP3:** Protocolo de oficina de correos versión 3. Permite a los clientes recuperar el correo electrónico de un servidor de correo y descargar el correo electrónico a la aplicación de correo local del cliente.
-   **IMAP**: Protocolo de acceso a mensajes de Internet. Permite a los clientes acceder al correo electrónico almacenado en un servidor de correo, así como mantener el correo electrónico en el servidor.

Transferencia de archivos

-   **FTP:** Protocolo de transferencia de archivos. Establece las reglas que permiten a un usuario en un host acceder y transferir archivos hacia y desde otro host a través de una red. FTP es un protocolo de entrega de archivos confiable, orientado a la conexión y reconocido.
-   **SFTP:** Protocolo de transferencia de archivos SSH. Como una extensión del protocolo Secure Shell (SSH), SFTP se puede usar para establecer una sesión segura de transferencia de archivos en la que la transferencia de archivos está encriptada. SSH es un método de inicio de sesión remoto seguro que generalmente se usa para acceder a la línea de comando de un dispositivo.
-   **TFTP:** Protocolo de transferencia de archivos trivial. Un protocolo simple de transferencia de archivos sin conexión con el mejor esfuerzo, entrega de archivos no reconocida. Utiliza menos gastos generales que FTP.

Web y servicio web

-   **HTTP:** Protocolo de Transferencia de Hipertexto. Un conjunto de reglas para intercambiar texto, imágenes gráficas, sonido, video y otros archivos multimedia en la World Wide Web.
-   **HTTPS**: HTTP Seguro. Una forma segura de HTTP que encripta los datos que se intercambian a través de la World Wide Web.
-   **REST:** Transferencia de Estado Representacional. Un servicio web que utiliza interfaces de programación de aplicaciones (API) y solicitudes HTTP para crear aplicaciones web.

---

### Capa de Transporte
Orientado a la conexión

-   **TCP:** Protocolo de control de transmisión. Permite una comunicación confiable entre procesos que se ejecutan en hosts separados y proporciona transmisiones confiables y reconocidas que confirman la entrega exitosa.

Sin conexión

-   **UDP:**- Protocolo de datagramas de usuario. Permite que un proceso que se ejecuta en un host envíe paquetes a un proceso que se ejecuta en otro host. Sin embargo, UDP no confirma la transmisión exitosa de datagramas.

---

### Capa de Internet
Protocolo de Internet

-   **IPv4:** Protocolo de Internet versión 4. Recibe segmentos de mensajes de la capa de transporte, empaqueta mensajes en paquetes y dirige paquetes para la entrega de extremo a extremo a través de una red. IPv4 usa una dirección de 32 bits.
-   **IPv6:** IP versión 6. Similar a IPv4, pero usa una dirección de 128 bits.
-   **NAT:** Traducción de direcciones de red. Traduce las direcciones IPv4 de una red privada en direcciones IPv4 públicas globalmente únicas.

Mensajería

-   **ICMPv4**: Protocolo de mensajes de control de Internet para IPv4. Proporciona comentarios de un host de destino a un host de origen sobre errores en la entrega de paquetes.
-   **ICMPv6**: ICMP para IPv6. Funcionalidad similar a ICMPv4 pero se usa para paquetes IPv6.
-   **ICMPv6 ND**: descubrimiento de vecinos ICMPv6. Incluye cuatro mensajes de protocolo que se utilizan para la resolución de direcciones y la detección de direcciones duplicadas.

Protocolos de enrutamiento

-   **OSPF**: Abrir la Ruta de Acceso Más Corta Primero. Protocolo de enrutamiento de estado de enlace que utiliza un diseño jerárquico basado en áreas. OSPF es un protocolo de enrutamiento interior estándar abierto.
-   **EIGRP**: Protocolo de Enrutamiento de Puerta de enlace Interior Mejorado. Un protocolo de enrutamiento propietario de Cisco que utiliza una métrica compuesta basada en ancho de banda, demora, carga y confiabilidad.
-   **BGP**: Potocolo de puerta de enlace de frontera. Un protocolo de enrutamiento de puerta de enlace exterior estándar abierto utilizado entre los proveedores de servicios de Internet (ISP). BGP también se usa comúnmente entre ISP y sus grandes clientes privados para intercambiar información de enrutamiento.

---

### Capa de Acceso a la Red
Resolución de dirección

-   **ARP:** Protocolo de resolución de direcciones. Proporciona la asignación dinámica de direcciones entre una dirección IPv4 y una dirección de hardware.

Protocolos de enlace de datos

-   **Ethernet**: define las reglas para los estándares de cableado y señalización de la capa de acceso a la red.
-   **WLAN**: red de área local inalámbrica. Define las reglas para la señalización inalámbrica en las frecuencias de radio de 2,4 GHz y 5 GHz.

