# Direcciones IP

El uso de la direcciones IP es el principal medio por que los equipos se puedan identificar entre sí y para establecer comunicación entre ellos. Cada terminal de red se debe configurar con direcciones IP. Los ejemplos de dispositovos finales incluyen estos:

-   PC.
-   Impresoras de red.
-   Teléfonos VoIP.
-   Cámaras de seguridad.
-   teléfonos inteligentes.
-   Dispositivos portátiles móviles.

La estructura de una dirección IPv4 se denomina notación decimal punteada y se representa con cuatro decimales entre 0 y 255. Las direcciones IPv4 son números asignados a dispositivos individuales conectados a una red.

La mascara de subred IPv4 es un valor de 32 bits que separa la porción de red de la porción de host. Junto con la dirección IPv4, la mascara de subred determina a qué subred pertenece el dispositivo.

Las direcciones IPv6 tienen una longitud de 128 bitd y se escriben como una cadena de valores hexadecimales. Cada cuatro bits está representado por un sólo dígito hexadecimal; para un total de 32 valores hexadecimales. Los grupos de cuatro dígitos están separados por dos puntos (:). Las direcciones IPv6 no distinguen entre mayúsculas y minúsculas.

# Interfaces y puertos

Las comunicaciones entre los dispositivos depende de la disponibilidad de las interfaces y del cableado. Cada interfaz tiene especificaciones o estándares que la definen. Los tipos de medios de red incluyen los cables de cobre de par trenzado, los cables de fibra óptica, los cables coaxiales o la tecnología inalámbrica, como se muestra en la figura.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Tipos-de-medios-de-red.png)

Existen varios tipos de medios cada uno con sus ventajas y desventajas, ya que, no todos disponen de las mimas características. Estas son algunas de las diferencias entre varios tipos de medios:

-   La distancia a través de la cual los medios puedne transportar una señal correctamente.
-   El ambiente en el cual se instalará el medio.
-   La cantida de datos y la velocidad a la que se deben transmitir.
-   El costo de los medios y de la instalación.

# Configuración de interfaz virtual de switch

Para acceder al switch de manera remota, se deben configurar una dirección IP y una máscara de subred en la SVI. Para configurar una SVI en un switch, utilice el comando de **interface vlan 1** configuración global. La Vlan 1 no es una interfaz física real, sino una virtual. A continuación, asigne una dirección IPv4 mediante el comando **ip address** _ip-address_ _subnet-mask_ de la configuración de interfaz. Finalmente, habilite la interfaz virtual utilizando el comando de **no shutdown** configuración de la interfaz.
```cisco
Sw-Floor-1# configure terminal Sw-Floor-1(config)# interface vlan 1 Sw-Floor-1(config-if)# ip address 192.168.1.20 255.255.255.0 Sw-Floor-1(config-if)# no shutdown Sw-Floor-1(config-if)# exit Sw-Floor-1(config)# ip default-gateway 192.168.1.1
```