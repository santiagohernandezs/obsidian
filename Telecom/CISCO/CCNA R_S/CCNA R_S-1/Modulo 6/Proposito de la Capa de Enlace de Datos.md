# La capa de enlace de datos

La capa de enlace de datos del modelo OSI (Capa 2), como se muestra en la figura, prepara los datos de red para la red física.

La capa de enlace de datos es responsable de las comunicaciones de tarjerta de interfaz de red (NIC) a tarjeta de red.

La capa de vínculo de datos realiza lo siguiente :

-   Permite que las capas superiores accedan a los medios. El protocolo de capa superior no conoce completamente el tipo de medio que se utiliza para reenviar los datos.
-   Acepta datos, generalmente paquetes de capa 3 (es decir, IPv4 o IPv6) y los encapsula en tramas de capa 2.
-   Controla cómo los datos se colocan y reciben en los medios.
-   Intercambia tramas entre punto finales a través de los medios de red.
-   Recibe datos encapsulados, generalmente paquetes de capa 3, y los dirige al protocolo de capa superior adecuado.
-   Realiza la detección de errores y rechaza cualquier trama dañada.

![](https://ccnadesdecero.es/wp-content/uploads/2017/11/Capa-Enlace-de-Datos-en-OSI.png)

En redes de equipos, un nodo es un dispositivo que puede recibir, crear, almacenar o reenviar datos a lo largo de una ruta de comunicaciones. Un nodo puede ser un dispositivo final como un portátil, un teléfono móvil, o un dsipositivo intermediario como un Ethernet Switch.

Sin la capa de enlace de datos , un protocolo de capa de red, tal como IP, tendría que tomar medidas para conectarse con todos los tipos de medios que pudieran existir a lo largo de la ruta de envío. Además, cada vez que se desarrolla un nueva tecnología de red o medio IP, tendría que adpatarse.

La figura muestra un ejemplo de cómo la capa de enlace de datos agrega información de destino Ethernet de Capa 2 y NIC de origen a un paquete de Capa 3. A continuación, convertiría esta infromación a un formato compatible con la capa física (es decir Capa 1)

![](https://ccnadesdecero.es/wp-content/uploads/2017/11/Capa-1-y-Capa-2-de-OSI.png)

# Subcapas de enlace de datos IEEE 802 LAN/WAN

Los estándares IEEE 802 LAN/WAN son específicos para LAN Ethernet, LAN inalámbricas (WLAN), redes de área personal inalámbrica (WPAN) y otros tipos de redes locales y metropolitanas. La capa de enlace de datos IEEE 802 LAN/WAN consta de las dos subcapas siguientes.

-   **Logical Link Control (LLC)**: Esta subcapa IEEE 802.2 se comunica entre el software red y el hardware del dispositivo. Coloca en [[La Trama]] información que identifica qué protocolo de capa de red se utiliza para [[La Trama]]. Esta información permite que múltiples protocolos de Capa 3, como IPv4 e IPv6, utilicen la misma interfaz de red y medios.
    
-   **Media Access Control (MAC)**: Implementa esta subcapa (IEEE 802.3, 802.11 o 802.15) en hardware. Es responsable de la encapsulación de datos y el control de acceso a los medios. Proporciona direccionamiento de capa de anlce de datos y está integrado con varias tecnologías de capa física.
    

La figura muestra las dos subcapas (LLC y MAC) de la capa de enlace de datos.

![](https://ccnadesdecero.es/wp-content/uploads/2017/11/Subcapas-de-Enlace-de-Datos-1.png)

La subcapa LLC toma los datos del protocolo de red, que generalmente es un paquete IPv4 o IPv6, y agrega información de control de Capa 2 para ayudar a entregar el paquete al nodo de destino.

La subcapa MAC controla la NIC y otro hardware que es responsable de enviar y recibir datos en el medio LAN/MAN con cable o inalámbrico.

La subcapa MAC proporciona encapsulación de datos:

-   **Delimitación de tramas** - El proceso de entramado proporciona delimitadores importantes que se utilizan para identificar un grupo de bits que componen una trama. Estos bits delimitadores proporcionan sincronización entre los nodos de transmisión y de recepción.
    
-   **Direccionamiento** - proporciona direccionamiento de origen y destino para transportar la trama de capa 2 entre dispositivos en el mismo medio compartido.
    
-   **Detección de errores** - Cada trama contiene un tráiler utilizado para detectar errores de transmisión.
    

La subcapa MAC también proporciona control de acceso a medios, lo que permite que varios dispositivos se comuniquen a través de un medio compartido (semidúplex). Las comunicaciones dúplex completo no requieren control de acceso.

# Provisión de acceso a los medios

Las interfaces del router encapsulan el paquete en la trama apropiada. Se utiliza un método adecuado de control de acceso a los medios para acceder a cada enlace. en cualquier intercambio de paquetes de capas de red, puede haber muchas transiciones de medios y capa de enlace de datos. En cada salto a lo largo de la ruta, un router realiza las siguientes funciones de Capa 2:

En cada salto a lo largo de la ruta, un router realiza las siguinetes funciones de capa 2:

1.  Aceptan una trama proveniente de un medio.
2.  Desencapsulan la trama.
3.  Vuelven a encapsular el paquete en una trama nueva.
4.  Reenvían la nueva trama adecuada al medio de ese segmento de la red física.

---

# Estandares de la capa de enlace de datos.

Los ptorocolo de la capa 2 generalmente no están definidos por los Request for Comments (RFC), a diferencia de las capas superiores del protocolo TCP/IP. El Internet Engineering Task Force (IETF) Mantiene los protocolos y servicios funcionales para el conjunto de protocolos TCP/IP en las capas superiores, pero no definen las funciones y el funcionamiento de la capa de acceso a la red TCP/IP.

Las organizaciones de ingenierí que definen los estándares abiertos y protocolos que se aplican a la capa de acceso a la red (capa física y capa de enlace de datos del modelo OSI) incluyen lo siguiente:

-   Instituto de Ingenieros Eléctricos y Electrónicos (IEEE)
-   Unión Internacional de Telecomunicaciones (ITU)
-   Organización Internacional para la Estandarización (ISO)
-   Instituto Nacional Estadounidense de Estándares (ANSI)