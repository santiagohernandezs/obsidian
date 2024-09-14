# La conexión física

Una conexión física se puede definir como una conxión por cable o una conexión inalámbrica mediante ondas de radio.

Tanto en las empresas como en los hogares, podemos conseguir estos dos tipos de conexiones, dependiendo de lo que las personas necesiten en el momento se conectarán de manera alámbrica o inalámbrica, siendo la alámbrica por medio de cables que se conectan con un Switch o la inalámbrica donde los usuarios se conectan por ondas de radio a un Access Point (AP) lo que les permite más movilidad.

# Router Inalámbrico

![](https://ccnadesdecero.es/wp-content/uploads/2017/11/Router-inal%C3%A1mbrico.png)

Estos son los componentes de un Access Point:

1.  Las antenas inalámbricas (Estas están integradas dentro del router)
2.  Varios puertos de switch de Ehternet
3.  Un puerto Ethernet

# Conexión por cable al router inalámbrico

![](https://ccnadesdecero.es/wp-content/uploads/2017/11/Conexi%C3%B3n-por-cable.png)

## Tarjetas de interfaz de red

Las tarjetas de interfaz de red (NIC) conectan un dispositivo a la red. Las NIC de Ehternet se usan para una conexión por cable, mientras que las NIC de Wireless Local Area Network (WLAN) se usan para las conexiones inalámbrica. Los dispositivos finales pueden tener una o dos de estas tarjetas.

## Conexión por cable utilizando una NIC Ethernet

No todas las conexiones físicas son iguales, en términos del nivel de rendimiento, cuando se conecta a una red.

![](https://ccnadesdecero.es/wp-content/uploads/2017/11/Conexi%C3%B3n-con-NIC-Ethernet.png)

# La capa física

La capa física del modelo OSI proporciona los medios para transportar los bits que forman una trama de capa de enlace de datos a través de los medios de red. Esta capa acepta una trama completa de la capa de enlace de datos y la codifica como una serie de señales que se transmiten a los medios locales. Los bits codificados que comprenden una trama son recibidos por un dispositivo final o un dispositivo intermedio.

Haga clic en en la figura para ver un ejemplo del proceso de encapsulación. La última parte de este proceso muestra los bits que se envían a través del medio físico. La capa física codifica las tramas y crea las señales eléctricas, ópticas o de ondas de radio que representan los bits en cada trama. Estas señales se envían por los medios, una a la vez.

![](https://ccnadesdecero.es/wp-content/uploads/2017/11/Proceso-de-encapsulaci%C3%B3n-capa-f%C3%ADsica.png)

La capa física del nodo de destino recupera estas señales individuales de los medios, las restaura a sus representaciones en bits y pasa los bits a la capa de enlace de datos en forma de trama completa.