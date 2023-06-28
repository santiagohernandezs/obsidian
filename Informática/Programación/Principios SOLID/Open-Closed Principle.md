Las clases deben estar abiertas a la extensión pero cerradas a la modificación.

La idea fundamental de este principio es evitar que el código existente se descomponga cuando implementas nuevas funciones.

Una clase está *abierta* si puedes extenderla, crear una subclase y hacer lo que quieras con ella (añadir nuevos métodos o campos, sobrescribir el comportamiento base, etc.). Algunos lenguajes de programación te permiten restringir en mayor medida la extensión de una clase con palabras clave como `final`. Después de esto, la clase ya no está abierta. Al mismo tiempo, la clase está *cerrada* (también se dice *completa*) si está lista al 100% para que otras clases la utilicen; su interfaz está claramente definida y no se cambiará en el futuro.

La clases pueden estar *al mismo tiempo* abiertas (para la extensión) y cerradas (para la modificación).

Cuando una clase se ha desarrollado, probado, revisado e incluido en un framework o utilizada en una aplicación de cualquier otro modo, es arriesgado intentar juguetear con su código. En lugar de cambiar directamente el código de la clase, puedes crear una sub-clase y sobrescribir las partes de la clase original que quieras que se comporten de otra forma. Lograrás tu objetivo sin descomponer clientes existentes de la clase original.

## Ejemplo
Tienes una aplicación de comercio electrónico con una clase `Pedido` que calcula los costos de envío, y todos los métodos de envío están incrustados dentro de la clase. Si necesitas añadir un nuevo método de envío, tienes que cambiar el código de la clase `Pedido` , arriesgándote a descomponerlo.

![](https://i.imgur.com/UPN1kwz.png)

Puedes resolver el problema aplicando el patrón Strategy. Empieza extrayendo métodos de envío y colocándolos dentro de clases separadas con una interfaz común.

![](https://i.imgur.com/GXvkyik.png)

Ahora, cuando necesites implementar un nuevo método de envío, puedes derivar una nueva clase de la interfaz `Envíos` sin tocar el código de la clase `Pedido` . El código cliente de la clase `Pedido` vinculará los pedidos con un objeto de envío de