|Nombre|| Características |
|:---:|:---:|---|
|Broadcast|CISCO| - Elección del DR y BDR<br>- Topología  malla completa o malla parcial<br>- Contadores a 10 y 40 segundos|
|Point-to-point (PTP)|CISCO|- Para conexiones directas entre dos routers<br>- No se requiere elegir DR y BDR<br>- Contadores a 10 y 40 segundos|
|Non-broadcast|RFC|- Para redes Frame-Relay, ATM y X.25<br>- Si hay elección de DR y BDR<br>- Los vecinos hay que declararlos manualmente<br>- Topología de malla completa o malla parcial<br>- Contaodres a 30 y 120 segundos.|
|Point-to-multipoint|RFC|- Utilzadas en redes Frame-Relay con subinterfaces<br>- No hay elección de DR y BDR<br>- Si soporta los mensajes Broadcast y Multicast<br>- Topolgía malla parcial o estrella<br>- Contadores a 30 y 120 segundos|

