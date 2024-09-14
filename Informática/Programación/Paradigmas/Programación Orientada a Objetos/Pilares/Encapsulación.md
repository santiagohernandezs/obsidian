La *encapsulación* es la capacidad que tiene un objeto de es conder partes de su estado y comportamiento de otros objetos, exponiendo únicamente una interfaz limitada al resto del programa. *Encapsular* algo significa hacerlo privado y, por ello, accesible únicamente desde dentro de los métodos de su propia clase. Existe un modelo un poco menos restrictivo llamado protegido que hace que un miembro de una clase también esté disponible para las subclases.

En los lenguajes modernos de programación orientada a objetos, el mecanismo de la inter faz (declarado normalmente con la palabra clave interface o protocol ) te permite definir **contratos de interacción** entre objetos.

Imagina que tienes una interfaz `TransporteAéreo` con un método `vuelo(origen, destino, pasajeros)`.

![](https://i.imgur.com/lhXvwAm.png)

Al diseñar un simulador de transporte aéreo, puedes restringir la clase Aeropuerto para que sólo funcione con objetos que implementan la interfaz `TransporteAéreo`. Después de esto, tendrás la certeza de que cualquier objeto pasado a un objeto del aeropuerto, ya sea un `Avión` , un `Helicóptero` o hasta un maldito `GrifoDomesticado` si quieres, podrá aterrizar o despegar de este tipo de aeropuerto.

Puedes cambiar la implementación del método `volar()` en esas clases del modo que quieras. Siempre y cuando la firma del método sea la misma que se declaró en la interfaz, todas las instancias de la clase `Aeropuerto` pueden funcionar bien con tus objetos voladores.