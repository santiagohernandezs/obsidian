La topología de una red es la configuración o realición de los dispositivos en la red y las interconexiones entre ellos.

Existen dos tipos de topología utilizadas al describir las redes LAN y WAN:

-   **Topología Física** - Identifica las conexiones físicas y cómo se interconectan los dispositivos intermedios, es decir, routers, switchs y APs). La topología física también puede incluir la ubicación específica del dispositivo, como el número de habitación y la ubicación en el reck del equipo.
-   **Topologolía Lógica** - Se refiere a la forma en que una red transfiere tramas de un nodo al siguiente. esta topología identifica las conexiones virtuales mediante interfaces de dispositivo y esquemas de direccionamiento IP de capa 3.

La capa de enlace de datos ''ve'' la topología lógica de una red al controlar el acceso de datos a los medios. Es la topología lógica la que influye en el tipo de trama de red y control de acceso a los medios que se utilizan.

# Topología Física

![](https://ccnadesdecero.es/wp-content/uploads/2017/11/Diagrama-Red-de-Topolog%C3%ADa-F%C3%ADsica.png)

# Topología Lógica

![](https://ccnadesdecero.es/wp-content/uploads/2017/11/Diagrama-Red-de-Topolog%C3%ADa-L%C3%B3gica.png)

---

# Topologías de WAN

Las figuras se ilustran cómo las WAN se interconectan comúnmente mediante tres topologías físicas comunes de WAN.

## Point to Point (PTP)

Esta es la topología WAN más simple y común. Es un enlace permanente entre dos terminales.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Topolog%C3%ADa-Punto-a-Punto.png)

## Hub and Spoke (Estrella)

Esta es una versión WAN de la topología en estrella en la que un sitio central interconecta sitios de sucursal mediante el uso de enlaces punto a punto. Los sitios de sucursales no pueden intercambiar datos con otros sitios de sucursales sin pasar por el sitio central.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Topolog%C3%ADa-Hub-y-Spoke.png)

## Malla

Esta topología proporciona alta disponibilidad, pero requiere que cada sistema final esté interconectado con cualquier otro sistema. Por lo tanto, los costos administrativos y físicos pueden ser importantes. Básicamente, cada enlace es un enlace punto a punto al otro nodo.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Topolog%C3%ADa-Malla-WAN.png)

**Nota:** Un híbrido es una variación o combinación de cualquier topología. Por ejemplo, una malla parcial es una topología híbrida en la que algunos, pero no todos, los dispositivos finales están interconectados.

---

# Topología WAN de punto a punto

Las topologías físicas punto a punto conectan dos nodos directamente, como se muestra en la figura. En esta disposición, los dos nodos no tienen que compartir los medios con otros hosts. Además, cuando se utiliza un protocolo de comunicaciones en serie, como el Protocolo punto a punto (PPP), un nodo no tiene que hacer ninguna determinación sobre si una trama entrante está destinada para él u otro nodo. Por lo tanto, los protocolos de enlace de datos lógicos pueden ser muy simples, dado que todas las tramas en los medios solo pueden transferirse entre los dos nodos. El nodo coloca las tramas en los medios en un extremo y esas tramas son tomadas de los medios por el nodo en el otro extremo del circuito punto a punto.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Topolog%C3%ADa-WAN-punto-a-punto.png)

**Nota**: Las topologías PTP están limitadas a dos nodos.

**Nota**: Una conexión PTP a través de Ehternet requiere que el dispositivo determine si [[La Trama]] está destinada a este nodo.

Un nodo de origen y un nodo de destino pueden estar conectados entre sí a travpes de cierta distancia geográfica utilizandomúltiples dispositivos intermedios. Sin embargo, el uso de dispositivos físicos en al red no afecta la topología lógica.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Ejemplo-Topolog%C3%ADa-WAN.png)

---

# Topologías de LAN

En las LAN multiacceso, los dispositivos finales (es decir, nodos) están interconectados utilizando topologías estrella o estrella extendida, como se muestra en la figura. En este tipo de topología, los dispositivos finales están conectados a un dispositivo intermediario central, en este caso, un switch Ethernet. A **extended star** extiende esta topología interconectando varios switches Ethernet. La topología en estrella es fácil de instalar, muy escalable (es fácil agregar y quitar dispositivos finales) y de fácil para la resolución de problemas. Las primeras topologías en estrella interconectaban terminales mediante Ethernet hubs.

A veces, es posible que solo haya dos dispositivos conectados en la LAN Ethernet. Un ejemplo son dos routers interconectados. Este sería un ejemplo de Ethernet utilizado en una topología punto a punto.

**Topologías LAN heredadas**

Las tecnologías antiguas Ethernet y Token Ring LAN heredadas incluían otros dos tipos de topologías:

-   **Bus** - Todos los sistemas finales se encadenan entre sí y terminan de algún modo en cada extremo. No se requieren dispositivos de infraestructura, como switches, para interconectar los dispositivos finales. Las redes Ethernet heredadas a menudo eran topologías de bus que usaban cables coaxiales porque era económico y fácil de configurar.
-   **Anillo** - Los sistemas finales se conectan a su respectivo vecino y forman un anillo. El anillo no necesita ser terminado, a diferencia de la topología del bus. La interfaz de datos distribuidos de fibra heredada (FDDI) y las redes Token Ring usaban topologías de anillo.

Las figuras ilustran cómo los dispositivos finales están interconectados en las LAN. Es común que una línea recta en un gráfico de redes represente una red LAN Ethernet que incluye una estrella simple y una estrella extendida.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Topolog%C3%ADas-f%C3%ADsicas-de-LAN.png)

---

# Comunicación Full-Duplex y Semi-Duplex

Es la dirección de la transmición de datos entre dos dispositivos. Hay dos modos comunes de dúplex.

## Comunicación Semi-Dúplex

Los dos dispositvos pueden transmitir y recibir en los medios pero no pueden hacerlo simultáneamente. Las WLAN y las topologías de bus heredadas con switches Ethernet utilizan el modo semidúplex. Semidúplex permite que solo un dispositivo envíe o reciba a la vez en el medio compartido.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Comunicaci%C3%B3n-Half-Duplex.png)

## Comunicación Full-Dúplex

Ambos dispositivos pueden transmitir y recibir simultáneamente en los medios compartidos. La capa de enlace de datos supone que los medios están disponibles para transmitir para ambos en cualquier momento.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Comunicaci%C3%B3n-Half-Duplex.png)

En resumen, las comunicaciones semidúplex restringen el intercambio de datos a una dirección a la vez. El dúplex completo permite el envío y la recepción de datos simultáneamente. Es importante que dos interfaces interconectadas, como la **NIC de un host y una interfaz en un switch Ethernet, operen con el mismo modo dúplex.** De lo contrario, habrá incompatibilidad de dúplex y se generará ineficiencia y latencia en el enlace.

---

# Métodos de Control de Acceso

Las LAN Ehternet WLAN son un ejemplo de una red de accesos múltiples. Una red multiacceso es una red que puede tener dos o más dispositivos finales que intentan acceder simultáneamente.

Algunas redes de acceso múltiple requieren reglas que rijan la forma de compartir los medios físicos. Hay dos métodos básicos de control de acceso al medio para medios compartidos:

-   Acceso por contienda.
-   Acceso controlado.

## Acceso por contienda

En las redes multiacceso basadas en contencion, todos los nodos operan en semidúplex, compitiendo por el uso del medio. Sin embargo, solo un dispositivo puede enviar a la vez. Por lo tanto, hay un proceso si más de un dispositivo transmite al mismo tiempo. Algunos ejemplos de métodos de acceso basados en contencion son los siguientes:

-   Acceso múltiple con detección de colisiones CSMA/CD (Carrier Sense Multiple Access with Collision Detection)utilizado en LAN Ethernet de topología de bus heredada
-   El operador detecta el acceso múltiple con prevención de colisiones CSMA / CA (Carrier Sense Multiple Access with Collision Avoidance )utilizado en LAN inalámbricas

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Acceso-basado-en-la-contenci%C3%B3n.png)

## Acceso controlado

En una red de acceso múltiple basada en control, cada nodo tiene su propio tiempo para usar el medio. Estos tipos deterministas de redes no son eficientes porque un dispositivo debe aguardar su turno para acceder al medio. Algunos ejemplos de redes multiacceso que utilizan acceso controlado son los siguientes:

-   Anillo de TokenLegacy
-   ARCNETheredado

**Nota**: Hoy en día, las redes Ethernet funcionan en dúplex completo y no requieren un método de acceso.

# Acceso por contención: CSMA/CD

-   **LAN inalámbrica (utiliza CSMA/CA)**
-   **LAN Ethernet de topología de bus heredada (utiliza CSMA/CD)**
-   **LAN Ethernet heredada con un hub (utiliza CSMA/CD)**

Estas redes funcionan en modo semidúplex, lo que significa que solo un dispositivo puede enviar o recibir a la vez. esto requiere un proceso poara gestionar cuándo puede enviar un dispositivo y qué sucede cuando múltiples dispositivos envían al mismo tiempo.

**Si dos dispositivos transmiten al mismo tiempo, se prodeuce una colisión**. ****Para las LAN Ethernet heredas, ambos dispositivos detectarán la colisión de la red. Esta es la parte de **Detección de Colisiones (CD)** de **CSMA/CD**. La NIC compara los datos transmitidos con los datos recibidos, o al reconocer que la amplitud de la señal es más alta de lo normal en los medios. Los datos enviados por ambos dispositivos se dañarán y deberán enviarse nuevamente.

[](https://ccnadesdecero.es/wp-content/uploads/2020/03/Proceso-de-CSMA-CD.png)

## Explicación

### PC1 envía una trama.

La PC1 tiene una trama que se sebe enviar a la PC3. La NIC de PC1 necesita determinar si algún dispostivo está transmitiendode otro dispositivoestá trasnmitiendo en el medio. Si no recibe trasmisiones de otro dispositivo, asumirá que la red está disponible para enviar.


### El hub recibe [[La Trama]]

El hub Ethernet recibe y envía la trama. Un hub de Ethernet también se conoce como repetidor multipuerto. Todos los bits que se reciben de un puerto entrante se regeneran y envían a todos los puertos.

Si otro dispositivo, como una PC2, quiere transmitir, pero está recibiendo una trama, deberá epserar hasta que el canal está libre.

### El hub envía la trama

Todos los dispositivos que están conectados al hub reciben la trama. Dado que la trama tiene un dirección destino de enlace de datos para la PC3, solo ese dispositivo acpetará y copiará toda la trama. Todas las demás NIC del dispositivo ignorarán la trama.


# Acceso por contención: CSMA/CA

Otra forma de CSMA

Otra forma de CSMA utilizada por las WLAN IEEE 820.11 es **Carrier Sense Multiple Access with Collision Avoidance (CSMA/CA)**.

CSMA/CA utiliza un método similar a CSMA/CD para detectar si el medio está libre, usa técnicas adicionales. En entornos inalámbricos, es posible que un dispositivo no detecte una colisión. CSMA/CA no detecta colisiones pero intenta evitarlas ya que guarda antes de transmitir. Cada dispositivo que transmite incluye la duración que necesita para la trasnmisión. Todos los demás dispositivos inalámbricos reciben esta infromación y saben durante cuánto tiempo no estará disponible.

En la figura, si el host A recibe una trama inalámbrica desde el punto de acceso, los hosts B y C también verán la trama y cuánto tiempo el medio no estará disponible.

Luego de que un dispositivos inalámbricos envía una trama 802.11, el receptor devuelve un acuso de recibo para que el emisor sepa que se recibió la trama.

Ya sea que es una red LAN Ethernet con concentradores o una red WLAN, los sistemas por contención no escalan bien bajo un uso intensivo de los medios.