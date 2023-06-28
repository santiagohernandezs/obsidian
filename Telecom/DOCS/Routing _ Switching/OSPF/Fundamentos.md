Es un protocolo **de estandar libre** que fue desarrolado en el año 1987 por el IETF, actualemnte existen dos RFC para OSPF
- RFC 2328 versión 2 para IPv4
- RFC 5340 versión 3 para IPv6

Este es un protocolo basado en el estado de los enlaces y siendo más específicos este toma en cuenta el ancho de banda del enlace como referencia para poder operar. Este funciona mediante el Algoritmo SPF (Djikstra).

Este tiene una distancia administrativa de 110 y su numero de protocolo es el 89

## Direcciones Multicast
- Dirección IP multicast SPF - 224.0.0.5 (SPF)
- Dirección IP multicast DR/BDR - 224.0.0.6 (DR/BDR)
- Dirección MAC multicast SPF - 01-00-5E-00-00-05 (SPF)
- Dirección MAC multicast DR/BDR - 01-00-5E-00-00-06 (DR/BDR)
- ECMP 4 por defecto, con un máximo de 32