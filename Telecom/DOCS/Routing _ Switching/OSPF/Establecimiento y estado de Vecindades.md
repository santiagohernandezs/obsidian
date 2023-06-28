Si se tienen dos routers conectados entre sí, estos deberán cumplir con una serie de requerimientos y parámetros para que puedan crear una adyacencia.

## Requerimientos
### Interfaces
- Ambas interfaces deben pertenecer a la misma red.
- El MTU en ambas interfaces debe ser el mismo.

### Parámetros
- Los contadores de Hello y Dead deben ser iguales
- El ID del área debe ser igual
- El Router-ID (RID) deben ser diferentes en ambos routers
- El tipo de autenticación debe ser la misma
- Las capabilidades activas

# Estado de Vecindades
- **Down**: Este es el primer estado de vecino OSPF. Significa que no ha recibido información del vecino, pero aún es posible enviar paquetes hello hacia él.
- **Attempt**: Este estado solamente es válido para los vecinos configurados manualmente en un entorno NBMA. En el estado Attempt, el router envía paquetes hello unicast cada intervalo de sondeo al vecino, de quien no se han recibido hellos dentro del intervalo muerto.
- **Init**: Este estado indica que el router ha recibido un paquete de Hello, pero el ID del router receptor no fue incluido en el paquete de Hello. Cuando un router recive un paquete de Hello de un vecino, debe indicar el ID del router remitente en su paquete de Hello como reconocimiento de que se recibió un paquete de Hello válido.
- **2-way**: Este estado indica que se a logrado un comunicación bidireccional entre los dos router, es decir, cada router a ha recivido el paquete de Hello del otro. Este estado se logra cuando el router que recibe el paquete de Hello ve su propio ID de router dentro del campo del vecino del paquete Hello recibido. En este estado el router decide si se vuelve adyacente a su vecino. En los medios Broadcast y en los NBMA, un router se llena solamente con el router designado (DR) y el router designado de respaldo (BDR). Permacenen en el estado bidireccional con los otros routers.
- **Exstart**: Una vez que se seleccionan el DR y el BDR, el proceso de intercambio de estados de enlace comienza entre los routers y sus DR y BDR. Cuando esto pasa se establece una relación maestro-esclavo (master-slave) entre los routers y su DR y BDR y eligen el número de secuencia inicial para la información adyacente. El router con el ID más alto se vuelve el maestro y comienza el intercambio, además se convierte en el único router capaz de cambiar el numero de secuencia.
- **Exchange**:  En el estado de intercambio, los routers OSPF intercambian paquetes de descripción de base de datos (DBD). Los descriptores de bases de datos contienen encabezados de anuncios de estados de enlaces (LSA) solamente y describen el contenido de la base de datos completa de estados de link.
- **Loading**: En este estado ocurre el intercambio real de la información del estado del link. De acuerdo con la información proporcionada por los DBDs, los routers envían paquetes de solicitud de estado de link. El vecino entonces proporciona la información de estado de link solicitada en paquetes de actualización de estado de link. Durante la adyacencia, si un router recibe un LSA obsoleto o perdido, solicita ese LSA enviando un paquete de solicitud de estado de link. Se reconocen todos los paquetes de actualización de estado de link.
- **Full**: En este estado, los routers son completamente adyacentes entre sí. Todos los LSA de router y red se intercambian y las bases de datos de los routers se sincronizan completamente.
**Nota**: El DR y el BDR que alcanza el estado FULL con cada router en el segmento visualizarán FULL/DROTHER cuando usted ingresa el comando show ip ospf neighbor en un DR o el BDR.