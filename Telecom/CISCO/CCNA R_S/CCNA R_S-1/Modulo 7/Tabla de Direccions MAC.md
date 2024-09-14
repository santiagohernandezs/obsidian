# Fundamento de los switches

Un switch Ethernet de capa 2 usa direcciones MAC de capa 2 para tomar decisiones de reenvío. Es completamente inconsceinte de los datos que se llevan en la porción de la trama, tal como un paquete del IPv4, un mensaje ARP o un paquete ND del IPv6. El switch toma sus desiciones de servicios de enlace en las direcciones MAC de Ethernet de la capa 2.

Un **switch** Ethernet examina su tabla de direcciones MAC para tomar una decisión de reenvío para cada trama, a diferencia de los **hubs** Ethernet heredados que repiten bits en todos los puertos excepto el puerto entrante. La tabla muestra la tabla de direcciones MAC que aún no ha aprendido las direcciones MAC para las cuatro PC conectadas.

---

# Switch, Aprendiendo y Reenviando

El switch arma la tabal de direcciones MAC de manera dinámica después de examinar las direcciones MAC de origne recibida en un puerto. El switch reenvía las tramas después de buscar una coincidencia entre la dirección MAC de origen de la trama y una entrada de la tabal de direcciones MAC.

## Aprender

### Examinar la dirección MAC de Origen

Se revisa cada trama que ingresa a un switch para obtener información nueva. Esto se realiza examinando la dirección MAC de origen de la trama y el número de puerto por el que ingresó al switch. Si la dirección MAC no exite, se agrega a la tabal, junto con el número de puerto de entrada. Si la direcciónMAC no existe, el switch actualiza el temporizador de actualización en la tabla durante cinco minutos.

En la figura, por ejemplo, la PC-A está enviando una trama Ethernet a la PC-D. La tabla muestra que el switch agrega la dirección MAC para PC-A a la tabla de direcciones MAC.

## Reenviar

### Buscar dirección MAC de destino

Si la dirección MAC de destino es una dirección de unicast, el switch busca una coincidencia entre la dirección MAC de destino de la trama y una entrada en la tabal de direcciones MAC. Si la dirección MAC de destino en la tabla, reenvía la trama por el puertoespecíficado. Si la dirección MAC de destino no está en la tabla, el switch reenvía a todos los puertos, excepto el de entrada: esto de conoce como unicast descnocida.


# Filtrado de tramas

A medida que un switch recibe tramas de diferentes dispositivos, puede completar la tabla de direcciones MAC examinando la dirección MAC de cada trama. Cuando la tabla de direcciones MAC del switch contiene la dirección MAC de destino, puede filtrar la trama y reenviar un solo puerto.