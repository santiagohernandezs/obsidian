# Roles de Routers
|Rol|Característica|
|:---:|---|
|Designated Router (DR)|- Posee la dirección multicast 224.0.0.6.<br> - Todos los routers envían sus LSR a la 224.0.0.6.<br> - Todos los routers reciben los LSU solamente del DR por la 224.0.0.5.|
|Backup Designated Router (BDR)|- Posee la dirección multicast 224.0.0.6.<br> - Actuará como backup en caso de que el DR se caiga.|

# Criterios para elegir al DR
Se evaluan lo siguientes criterios de manera secuencial

1. El router con la prioridad más alta.
2. El router con el RID más alto.
3. El router con la dirección IP más alta en la Loopback.
4. El router con la dirección más alta en cualquiera de las interfaces físcias.