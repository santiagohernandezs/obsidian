## 1. Estándares de la Capa Física

Los protocolos y las operaciones de las capas superiores de OSI se realizan utilizando software diseñado por ingenieros de software y científicos informáticos. Los servicios y protocolos en el conjunto TCP/IP están definidos por el **Grupo de trabajo de ingeniería de Internet (IETF)**.

La capa física consta de circuitos electrónicos, medios y conectores desarrollados por ingenieros. Por lo tanto, es necesario que las principales organizaciones especializadas en ingeniería eléctrica y en comunicaciones definan los estándares que rigen este hardware.

Existen muchas organizaciones internacionales y nacionales, organizaciones de regulación gubernamentales y empresas privadas que intervienen en el establecimiento y el mantenimiento de los estándares de la capa física. Por ejemplo, los estándares de hardware, medios, codificación y señalización de la capa física están definidos y regidos por estas organizaciones de estándares:

-   Organización Internacional para la Estandarización (ISO)
-   Asociación de las Industrias de las Telecomunicaciones (TIA) y Asociación de Industrias Electrónicas (EIA)
-   Unión Internacional de Telecomunicaciones (ITU)
-   Instituto Nacional Estadounidense de Estándares (ANSI)
-   Instituto de Ingenieros Eléctricos y Electrónicos (IEEE)
-   Autoridades nacionales reguladoras de las telecomunicaciones, incluida la Federal Communication
-   Commission (FCC) de los Estados Unidos y el Instituto Europeo de Estándares de Telecomunicaciones (ETSI)

|Organismo de estandarización|Estándares de red Conocidos|
|:---:|:---:|
|ISO|ISO 8877: adoptó oficialmente los conectores RJ (p. ej., RJ-11, RJ-45) | ISO 11801: Estándar de cableado de red similar a EIA/TIA 568.|
|EIA/TIA|TIA-568-C: estándares de cableado de telecomunicaciones, utilizados en casi todas las redes de datos, voz y video. | TIA-569-B: estándares de construcción comercial para rutas y espacios de telecomunicaciones. | TIA-598-C: código de colores para fibra óptica. | TIA-942: estándar de infraestructura de telecomunicaciones para centros de datos.|
|ANSI|568-C: Diagrama de pines RJ-45.Desarrollado en conjunto con EIA/TIA.|
|ITU-T|G.992: ADSL.|
|IEEE|802.3: Ethernet | 802.11: LAN inalámbrica (WLAN) y malla (certificación Wi-Fi) | 802.15: Bluetooth.|

Además de estos, a menudo hay grupos de normas de cableado regionales como CSA (Asociación de Normas Canadienses), CENELEC (Comité Europeo de Normalización Electrotécnica) y JSA / JIS (Asociación de Normas Japonesas), que desarrollan especificaciones locales.

![Estándares de capa física](https://ccnadesdecero.es/wp-content/uploads/2017/11/Est%C3%A1ndares-de-capa-f%C3%ADsica.png)

Estándares de capa física

Los estándares de la capa física abarcan tres áreas funcionales:

-   Componentes físicos
-   Codificación
-   Señalización

## 2. Componentes Físicos

Los componentes físicos son los dispositivos de hardware electrónico, medios y otros conectores que transmiten las señales que representan los bits. Los componentes de hardware como NIC, interfaces y conectores, materiales de cable y diseños de cable están especificados en estándares asociados con la capa física. Los diversos puertos e interfaces en un enrutador Cisco 1941 también son ejemplos de componentes físicos con conectores específicos y pines resultantes de los estándares.

## 3. Codificación

La codificación, o codificación de línea, es un método que se utiliza para convertir una transmisión de bits de datos en un «código» predefinido. Los códigos son grupos de bits utilizados para ofrecer un patrón predecible que pueda reconocer tanto el emisor como el receptor. En otras palabras, la codificación es el método o patrón utilizado para representar la información digital. Similar a la forma en que el código Morse codifica un mensaje con una serie de puntos y guiones.

Por ejemplo, en la codificación Manchester los **0** se representan mediante una transición de voltaje de alto a bajo y los 1 se representan como una transición de voltaje de bajo a alto. Un ejemplo de codificación Manchester se ilustra en la figura. La transición se produce en el medio de cada período de bit. Este tipo de codificación se usa en Ethernet de 10 Mbps. Las velocidades de datos más rápidas requieren codificación más compleja. La codificación Manchester se utiliza en estándares Ethernet más antiguos, como 10BASE-T. Ethernet 100BASE-TX usa codificación 4B/5B y 1000BASE-T usa codificación 8B/10B.

![Codificación Manchester](https://ccnadesdecero.es/wp-content/uploads/2017/11/Codificaci%C3%B3n-Manchester.png)

# Codificación Manchester: La transición se produce en el medio de cada período de bit.

## 4. Señalización

La capa física debe generar las señales inalámbricas, ópticas o eléctricas que representan los “1” y los “0” en los medios. La forma en que se representan los bits se denomina método de señalización. Los estándares de la capa física deben definir qué tipo de señal representa un “1” y qué tipo de señal representa un “0”. Esto puede ser tan simple como un cambio en el nivel de una señal eléctrica o de un pulso óptico. Por ejemplo, un pulso largo podría representar un 1 mientras que un pulso corto podría representar un 0.

Esto es similar al método de señalización que se utiliza en el código Morse, que puede utilizar una serie de tonos de encendido/apagado, luces o clics para enviar texto a través de cables telefónicos o entre barcos en el mar.

Las figuras muestran señalización

Haz clic en cada botón para ver ilustraciones de señalización para cable de cobre, cable de fibra óptica y medios inalámbricos.

-   [Cable de Cobre](https://ccnadesdecero.es/caracteristicas-capa-fisica/#)
-   [Cable de Fibra Óptica](https://ccnadesdecero.es/caracteristicas-capa-fisica/#)
-   [Medios Inalámbricos](https://ccnadesdecero.es/caracteristicas-capa-fisica/#)

# Señales eléctricas sobre cable de cobre.

![Señales eléctricas cable de cobre](https://ccnadesdecero.es/wp-content/uploads/2020/07/Se%C3%B1ales-el%C3%A9ctricas-cable-de-cobre.png)

## 5. Ancho de Banda

Los diferentes medios físicos admiten la transferencia de bits a distintas velocidades. La transferencia de datos generalmente se discute en términos de ancho de banda. El ancho de banda es la capacidad a la que un medio puede transportar datos. El ancho de banda digital mide la cantidad de datos que pueden fluir desde un lugar hacia otro en un período de tiempo determinado. El ancho de banda generalmente se mide en kilobits por segundo (kbps), megabits por segundo (Mbps) o gigabits por segundo (Gbps). En ocasiones, el ancho de banda se piensa como la velocidad a la que viajan los bits, sin embargo, esto no es adecuado. Por ejemplo, tanto en Ethernet a 10 Mbps como a 100 Mbps, los bits se envían a la velocidad de la electricidad. La diferencia es el número de bits que se transmiten por segundo.

Una combinación de factores determina el ancho de banda práctico de una red:

-   Las propiedades de los medios físicos
-   Las tecnologías seleccionadas para la señalización y la detección de señales de red

Las propiedades de los medios físicos, las tecnologías actuales y las leyes de la física desempeñan una función al momento de determinar el ancho de banda disponible.