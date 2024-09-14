# Introducción
OSPF (Open Shortest Path First) es un protocolo (IGP, Interios Gateway Protocol) basado en Link-State (Estado de enlace) o Tecnología SPF, hecho para desenvolverse en el campo de TCP/IP. El hecho de que es clasificado como un IGP significa que este intercambia la información de enrutamiento entre routers que pertenecen a un sistema autónomo.

Los paquetes IP de las rutas OSPF están solamente basados en la IP de destino que se encuentra en el encabezado IP y estos son enrutados tal cual y como están si involucrar ninguna mécanica extra que altere el contenido del este mientras se translada por el sistema autónomo. OSPF es un protocolo de enrutamiento dinámico, lo que significa que detecta de manera rápida los cambios topológicos dentro del sistemá autónomo y al mismo tiempo calcula el nuevo camino más rápido.

En un protocolo basado en el estado de enlaces cada router contiene una base de datos que describe la topolgía del sistema autónomo esta es llamada como **link-satate database** 

# Definiciones
## Router
Un protocolo de capa tres de intercambio de paquetes. Llamado la mayoría de veces de manera formal como **gateway** en la literatura IP.

## Sistema Autónomo (AS)
Un conjunto de routers que comparten iformación entre sí por medio de un protocolo de routing en común. Abreviado en inglés como AS (Autonomous System).

## Interior Gateway Protocol (IGP)
El protocolo de routing hablado por varios routers que pertenecen a un AS. Cada AS tiene un IGP.

## Router-ID (RID)
Un número de 32 bits asignado a cada router con OSPF habilitado. Este tiene el objetivo de identificar al router dentro del AS.

##  Networks

### Point-to-point Network (PTP Network)
Una red que admite un par de router conectados entre sí, donde la conexión o red va de un punto a otro.

### Broadcast Network
Redes que admiten más de dos routers conectados entre sí y que tienen la característica de poder envíar un solo mensaje a todos los routers conectados.

### Non-broadcast Network
Redes que admiten más de dos routers conectados entre sí, pero no comparten la funcionalidad de las redes broadcast.

## Interface
Una conexión entre un router y una de sus redes adjuntas a el. Una inerfaz contiene un estado que se obtiene del nivel inferior subyacente protocolos y el propio protocolo de enrutamiento. Una interfaz tiene asociada consigo una IP y una mascara de red y esta tambien es referida como link.

## Neighbor Routers
Dos routers que tienen sus interfaces en una red en común. Estos son descubiertos por el "Hello".

## Adjacency
Una relación formada entre dos router vecinos "Neighbor Routers" con el proposito de que estos intercambién información.

## Link State Advertisement (LSA)
Unidad de datos que que describe el estado local de un router o de una red. Para el router este describe el estado de las interfaces y sus adyacencias.

## Hello Protocol
Parte del Protocolo OSPF el cual se encarga de descubrir y mantener adyacencias.

## Flooding
Parte de OSPF que distribuye y sincroniza los LSAs entre routers.

## Designed Router
Todas las redes Broadcarst y las Non-broadcast deben de tener un router designado. Este genera un LSA para toda la red y tiene responsabilidades especiales. Automáticamente estos son elegidos por el protocolo "Hello".

# Contenido
- [[Fundamentos]]
- [[Tipos de mensajes OSPF]]
- [[Establecimiento y estado de Vecindades]]
- [[Configuración Inicial]]
- [[Métodos de Autenticación]]
- [[OSPF Multiprocesos XE]]
- [[Métrica y Manipulación de Costo]]
- [[Tipos de Redes]]
- [[Redes Multiacceso (DR-BDR)]]

#ospf