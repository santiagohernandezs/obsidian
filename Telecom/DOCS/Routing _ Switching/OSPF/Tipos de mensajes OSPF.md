Cuando operamos con OSPF debemos tomar en cuanta los tipos de mensajes que de manera exclusiva posee este protocolo, el mismo como método para hacer adyacencias y actualizar los estados de los enlaces. Los cinco tipo de mensajes son los siguientes:
- Hello (1)
- DBD - Database Description (2)
- LSR - Link State Request (3)
- LSU - Link State Update (4)
- LSAck - Link State Acknowledge

## LSA
Unidad de dato que representa el estado local de un router o de una red. Para un router, esto incluye el estado de las interfaces y cada una de sus adyacencia. Cada estado de los enlaces es enviado a través dominio de rounting. La información de todos los LSA construyen la base de datos.

## Hello
Su función básica es la de descubrir nuevos vecinos y mantener las adyacencias operativas.

## DBD
Esta sumariza todas las adyacencias de los otros routers que se encuentran en la base de datos de cada uno de los routers.

## LSR
Este es una solicitud de otros routers de la DB del sus vecinos para el sumarizar las rutas en su propia BDm en el RFC-2328 se define como una descarga de la DB.

## LSU
Es un paquete que genera un router cuando uno de los LSA ha cambiado y este lo envia a todos sus vecinos quienes a su vez, actualizan su DB en el RFC-2328 se define como una actualización de la DB.

## LSAck
Es un paquete que envían los routers que significa que resivieron los LSA de sus vecinos. El RFC-2328 lo define como una reconocimeinto en forma de inundación.