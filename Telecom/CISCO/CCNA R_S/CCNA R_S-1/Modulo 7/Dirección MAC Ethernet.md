# Dirección MAC y hexadecimal

En redes, las direcciones IPv4 se representan utilizando el sistema de números de base decimal diez y el sistema de números base binaria 2. Las direcciones IPv6 y las direcciones Ethernet se representan utilizando el sistema de número de dieciséis base hexadecimal. Para entender hexadecimal, primero debe estar muy familiarizado con binario y decimal.

El sistema de numeración hexadecimal usa los números del 0 al 9 y las letras de la A a la F.

Una dirección MAC Ethernet consta de un valor binario de 48 bits. Hexadecimal se utiliza para identificar una dirección Ethernet porque un solo dígito hexadecimal representa cuatro bits binarios. Por lo tanto, una dirección MAC Ethernet de 48 bits se puede expresar utilizando sólo 12 valores hexadecimales.

La figura compara los valores decimales y hexadecimales equivalentes para el binario 0000 a 1111.

# Equivalentes decimales y binarios a los valores hexadecimales del 0 al F

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Valores-equivalente-binario-decimal-y-hexadecimal.png)

Dado que 8 bits (un byte) es un método de agrupación binaria común, los números binarios del 00000000 al 11111111 se pueden representar en hexadecimal como el rango del 00 al FF, como se muestra en la figura.

# Equivalentes decimales, binarios y hexadecimales seleccionados

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Decimal-Binario-y-Hexadecimal.png)

Cuando se usa hexadecimal, los ceros iniciales siempre se muestran para completar la representación de 8 bits. Por ejemplo, en la tabla, el valor binario 0000 1010 se muestra en hexadecimal como 0A.

Los números hexadecimales suelen ser representados por el valor precedido por **0x** (por ejemplo, 0x73) para distinguir entre valores decimales y hexadecimales en la documentación.

El hexadecimal también puede estar representado por un subíndice 16, o el número hexadecimal seguido de una H (por ejemplo, 73H).

Es posible que tenga que convertir entre valores decimales y hexadecimales. Si es necesario realizar dichas conversiones, generalmente, es más fácil convertir el valor decimal o hexadecimal a un valor binario y, a continuación, convertir ese valor binario a un valor decimal o hexadecimal, según corresponda.

# Dirección MAC de Ethernet

En una LAN Ethernet, cada dispositivo de red está conectado a los mismos medios compartidos. La dirección MAC se utiliza para identificar los dispositivos físicos de origen y destino (NIC) en el segmento de red local. El direccionamiento MAC proporciona un método para la identificación del dispositivo en la capa de enlace de datos del modelo OSI.

Una dirección MAC Ethernet es una dirección de 48 bits expresada con 12 dígitos hexadecimales, como se muestra en la figura. Debido a que un byte equivale a 8 bits, también podemos decir que una dirección MAC tiene 6 bytes de longitud.

El diagrama muestra que la dirección MAC se compone de 48 bits en total. Estos 48 bits se pueden dividir en doce grupos de 4 bits, o 12 dígitos hexadecimales. Combinando dos dígitos hexadecimales juntos hace un byte, por lo tanto, los 48 bits también son equivalentes a 6 bytes.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Direcci%C3%B3n-MAC-Ethernet.png)

Todas las direcciones MAC deben ser únicas para el dispositivo Ethernet o la interfaz Ethernet. Para garantizar esto, todos los proveedores que venden dispositivos Ethernet deben registrarse con el IEEE para obtener un código hexadecimal único de 6 (es decir, 24 bits o 3 bytes) denominado identificador único de organización (OUI).

Cuando un proveedor asigna una dirección MAC a un dispositivo o interfaz Ethernet, el proveedor debe hacer lo siguiente:

-   Utilice su OUI asignado como los primeros 6 dígitos hexadecimales.
-   Asigne un valor único en los últimos 6 dígitos hexadecimales.

Por lo tanto, una dirección MAC Ethernet consiste en un código OUI de proveedor hexadecimal 6 seguido de un valor asignado por el proveedor hexadecimal 6, como se muestra en la figura.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Composici%C3%B3n-Direcci%C3%B3n-MAC-OUI.png)

Por ejemplo, suponga que Cisco necesita asignar una dirección MAC única a un nuevo dispositivo. El IEEE ha asignado a Cisco un OUI de **00-60-2F**. Cisco configuraría entonces el dispositivo con un código de proveedor único como **3A-07-BC**. Por lo tanto, la dirección MAC Ethernet de ese dispositivo sería **00-60-2F-3A-07-BC.**

Es responsabilidad del proveedor asegurarse de que ninguno de sus dispositivos tenga asignada la misma dirección MAC. Sin embargo, es posible que existan direcciones MAC duplicadas debido a errores cometidos durante la fabricación, errores cometidos en algunos métodos de implementación de máquinas virtuales o modificaciones realizadas con una de varias herramientas de software. En cualquier caso, será necesario modificar la dirección MAC con una nueva NIC o realizar modificaciones a través del software.