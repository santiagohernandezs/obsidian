La herencia es probablemente la forma más obvia y sencilla de reutilizar código entre clases. Tienes dos clases con el mismo código. Creas una clase base común para estas dos clases y colocas dentro el código similar. 

Lamentablemente, la herencia tiene sus contras, que a menudo no resultan aparentes hasta que tu programa tiene toneladas de clases y cambiarlo todo resulta muy complicado. Aquí una lista con todos esos problemas.
- **Una subclase no puede reproducir la interfaz de la superclase**. Tienes que implementar todos los métodos abstractos de la clase padre, incluso aunque no vas a usarlos.
- **Al sobrescribir métodos debes asegurarte que el nuevo comportamiento sea compatible con el de la clase**. Es importante porque los objetos de la subclase pueden pasarse a cualquier código que espere objetos de la superclase y no quieres que ese código se rompa.
- **La herencia rompe la encapsulación de la superclase** porque los detalles internos de la clase padre se hacen disponibles para la subclase. Puede darse una situación opuesta en la que un programador hace una superclase conozca algunos detalles de las subclases, con el objetico de que las siguientes extensiones sean más sencillas.
- **Las subclases están fuertemente acopladas a superclases.** Cualquier cambio en una superclase puede descomponer las subclases.
- **Intentar reutilizar código mediante la herencia puede conducir a la creación de jerarquía de herencia paralelas.** Normalmente, la herencia sucede en un única dimensión. Pero cuando hay dos o más dimensiones, debes crear muchas combinaciones de clases, hinchando la jerarquía de clases hasta un tamaño ridículo.

Existe una alternativa a la herencia llamada composición. Mientras que la herencia representa la relación “is a” (es un/ a) entre clases (un auto es un medio de transporte), la composición se basa en la relación “tiene un/a” (un auto tiene un motor).

Imagina que debes crear una aplicación de un catálogo para un fabricante de automóviles. La empresa fabrica autos y camiones; pueden ser eléctricos o de gasolina; todos los mode los pueden tener controles manuales o piloto automático.

![](https://i.imgur.com/iZadp8h.png)

Como puedes ver, cada parámetro adicional resulta en la multiplicación del número de subclases. Hay mucho código duplicado entre subclases porque una subclase no puede extender dos clases al mismo tiempo. Puedes resolver este problema con la composición. En lugar de que los objetos de auto implementen un comportamiento por su cuenta, pueden delegarlo a otros objetos.

La ventaja adicional es que puedes sustituir un comporta miento durante el tiempo de ejecución. Por ejemplo, puedes sustituir un objeto de motor vinculado a un objeto de auto asignando simplemente un objeto de motor distinto al auto.

![](https://i.imgur.com/BDjlXoe.png)
