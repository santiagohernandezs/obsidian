# Desición de envío de paquetes del router

¿Qué sucede cuando llega un paquete a la interfaz de un router?

EL router examina la dirección IP de destino dle paquete y busca en su tabla de enrutamiento oara determinar donde reenviar el paquete. La tabla de enrutramiento contiene la lista de todlas las direcciones de red conocidas (prefijos) y a dónde reenviar el paquete. Estas entradasse conocen como entradas de ruta o rutas. El router El router enviará el paquete utilizando la mejor entrada de ruta conocida (más larga).

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Decisi%C3%B3n-reenv%C3%ADo-de-paquetes-Router.png)

1.  El paquete llega a la interfaz Gigabgit Ethernet 0/0/0 del router R1. R1 desencapsula el encabezado Ehternet de la capa 2 y el trailer.
2.  El router R1 examina la dirección IPv4 de destino del paquete y busca la mejor coincidencia en su tabla de enrutamiento IPv4. La entrada de ruta indica que este paquete se reenviará al router R2.
3.  El router R1 encapsula el paquete en un nuevo encabezado Ehternet y trailer, y reenvía el paquete al siguiente router de salto R2

La siguiente tabla muestra la información pertinente de la tbaal de ruteo R1.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Tabla-de-enrutamiento-de-Router-IP.png)

# Tabla de enrutamiento IP del router

La tabla de enrutamiento dle router contiene entradas de ruta de red que enumeran todos los posibles destinos de red conocidos.

La trabla de enrutamiento almacena tres tipos de entradas de ruta:

1.  **Redes conectadas directamente** - estas entradas de ruta son inetrfaces de router activas. Los router agragan una ruta conectada directamente cunado una interfaz se configura con una dirección IP y se activa. Cada interfaz de router está conectada a un segmento de red diferente. En la figura, las redes conectadas directamente en la tabal de enrutameinto IPv4 R1 serían 192.168.10.0/24 y 209.165.200.224/30.
2.  **Redes remotas** - estas entradas de ruta de red están conectadas a otrso routers. Los routers aprenden acerca de las redes remotas ya sea mediante la configuración explícita de un administrador o mediante el intercambio de infromación de ruta mediante un protocolo de enrutamiento dinámico. En la figura, la red remota en la tabla de enrutamiento IPv4 R1 sería 10.1.1.0/24.
3.  **Ruta predeterminada** - Al igual que un host, la mayoría de los router tmabién incluyen una entrada de ruta predeterminada, un puerta de eblace de último recurso. Al ruta predeterminada se utiliza cuando no hay un mejor coincidencia (más larga) en la tabla de enrutamiento IP. En la figura, la tabal de enrutamiento IPv4 R1 probablementeincluirá una ruta predeterminada para reenviar todos los paquetes al router 2.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Enrutamiento-Est%C3%A1tico-manual.png)

Un router puede descubirr redes remotas de dos maneras:

-   **Manualmente** - Las redes se ingresan manuelamente en la tabal de rutas mediante rutas estáticas.
-   **Dinámicamente** - Las rutas remotas se aprenden automáticamente mediante un protocolo de enrutamiento dinámico.

# Enrutamiento Estático

Las rutas estáticas son entradas de ruta que se configuran manualmente. La figura muestra un ejemplo de una ruta estática que se configuró manualmente en el router R1. La ruta estática incluye la dirección de red remota y la dirección IP del router de salto siguiente.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Ruta-est%C3%A1tica-con-cambio-topolog%C3%ADa.png)

Si hay un cambio en la topología de la red, la ruta estática no se actualiza automáticamente y debe reconfigurarse manualmente. Por ejemplo, en la figura R1 tiene una ruta estática para llegar a la red 10.1.1.0/24 a través de R2. Si esa ruta ya no está disponible, R1 tendría que reconfigurarse con una nueva ruta estática a la red 10.1.1.0/24 a través de R3. Por lo tanto, el router R3 necesitaría tener una entrada de ruta en su tabla de enrutamiento para enviar paquetes destinados a 10.1.1.0/24 a R2.

El diagrama es una topología de red que muestra un vínculo fallido en una ruta estática. El host PC1, con una dirección de.10, está conectado a un conmutador en la red 192.168.10.0/24 que está conectado a la interfaz G0/0/0 del enrutador R1 con una dirección de .1. R1 está conectado al router R2 y al router R3 que también se dirigen conectados. R2 está conectado a un switch en la red 10.1.1.0/24 al que está conectado el PC2 host, dirección .10. Se ha configurado una ruta estática en R1 que apunta a R2 como el salto siguiente. Una X roja indica que este enlace ha fallado.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Enrutamiento-Din%C3%A1mico-con-OSPF.png)

El enrutamiento estático tiene las siguiente características

-   Una ruta estática debe configurarse manualmente.
-   El administrador necesita volver a configurar una ruta estática si hay un cambio en la topología y la ruta estática ya no es viable.
-   Una ruta estática es apropiada para una red pequeña y cuando hay pocos o ninguno de los enlaces redundantes.
-   Una ruta estática se usa comúnmente con un protocolo de enrutamiento dinámico para configurar una ruta predeterminada.

# Enrutamiento dinámico

Un protocolo de enrutamiento dinámico permite a los routers aprender automáticamente sobre redes remotas, incluida una ruta predeterminada, de otros routers. Los routers que usan protocolos de enrutamiento dinámico comparten automáticamente la información de enrutamiento con otros routers y compensan cualquier cambio de topología sin que sea necesaria la participación del administrador de la red. Si se produce un cambio en la topología de red, los routers comparten esta información mediante el protocolo de enrutamiento dinámico y actualizan automáticamente sus tablas de enrutamiento.

Los protocolos de enrutamiento dinámico incluyen OSPF y Enhanced Interior Gateway Routing Protocol (EIGRP). La figura muestra un ejemplo de routers R1 y R2 que comparten automáticamente información de red mediante el protocolo de enrutamiento OSPF.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Ruta-din%C3%A1mica-con-cambio-topolog%C3%ADa.png)

La configuración básica sólo requiere que el administrador de red habilite las redes conectadas directamente dentro del protocolo de enrutamiento dinámico. El protocolo de enrutamiento dinámico hará automáticamente lo siguiente:

-   Detectar redes remotas.
-   Mantener información de enrutamiento actualizada.
-   Elija el mejor camino hacia las redes de destino
-   Intente encontrar una nueva mejor ruta si la ruta actual ya no está disponible

Cuando un router se configura manualmente con una ruta estática o aprende acerca de una red remota dinámicamente mediante un protocolo de enrutamiento dinámico, la dirección de red remota y la dirección de salto siguiente se introducen en la tabla de enrutamiento IP. Como se muestra en la figura, si hay un cambio en la topología de red, los routers se ajustarán automáticamente e intentarán encontrar una nueva mejor ruta.