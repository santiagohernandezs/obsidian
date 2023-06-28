**Abstract Factory** es un patrón de diseño creacional que nos permite producir familias de objetos relacionados sin especificar sus clases concretas.
## Problema
Imagina que estás creando un simulador de tiendas de muebles. Tu código está compuesto por las clases que representan lo siguiente:
1. Una familia de productos relacionados: Silla, Sofá y Mesilla.
2. Algunas variantes de esta familia. Por ejemplo, los productos: Silla, Sofá y Mesilla, están disponibles en los siguientes variantes: Moderna, Victoriana y ArtDecó.

![](https://i.imgur.com/1XhFHCX.png)
 Necesitamos una forma de crear objetos de la misma familia. Los clientes se enfadan bastante cuando reciben muebles que no combinan. Además no queremos cambiar el código existente al añadir nuevos productos o familias de productos. 
## Solución
Lo que sugiere el patrón Abstract Factory es que declaremos de forma explicita interfaces  para cada producto diferente de las familias de productos para luego hacer que todos los productos pertenecientes a sus familias sigan esas interfaces. Por ejemplo, todas las variantes de sillas deberán implementar la interfaz `Silla`, todas las variables de mesas deberán implementar la interfaz de mesa.
![](https://i.imgur.com/DryU3vs.png)
El siguiente paso es declarar la fábrica abstracta. Una interfaz con una lista de métodos de creación para todos los productos que son parte de la familia de productos (por ejemplo, `crearSilla`, `crearSofá` y `crearMesilla`). Estos métodos deben devolver productos **abstractos** representados por las interfaces que extrajimos previamente: `Silla`, `Sofá`, `Mesilla`, etc.
![](https://i.imgur.com/sPrZlnE.png)
Ahora bien, ¿qué hay de las variantes de los productos? Para cada variante de una familia de productos, creamos una clase de fábrica independiente basada en la interfaz `FábricaAbstracta`. Una fábrica es una clase que devuelve productos de un tipo particular. Por ejemplo, la `FábricadeMueblesModernos` sólo puede crear objetos de `SillaModerna`, `SofáModerno` y `MesillaModerna`.

El código cliente tiene que funcionar con fábricas y productos a través de sus respectivas interfaces abstractas. Esto nos permite cambiar el tipo de fábrica que pasamos al código cliente, así como la variante del producto que recibe el código cliente, sin descomponer el propio código cliente.

Digamos que el cliente quiere una fábrica para producir una silla. El cliente no tiene que conocer la clase de la fábrica y tampoco importa el tipo de silla que obtiene. Ya sea un modelo moderno o una silla de estilo victoriano, el cliente debe tratar a todas las sillas del mismo modo, utilizando la interfaz abstracta `Silla`. Con este sistema, lo único que sabe el cliente sobre la silla es que implementa de algún modo el método `sentarse`. Además, sea cual sea la variante de silla devuelta, siempre combinará con el tipo de sofá o mesilla producida por el mismo objeto de fábrica.

Queda otro punto por aclarar: si el cliente sólo está expuesto a las interfaces abstractas, ¿cómo se crean los objetos de fábrica? Normalmente, la aplicación crea un objeto de fábrica concreto en la etapa de inicialización. Justo antes, la aplicación debe seleccionar el tipo de fábrica, dependiendo de la configuración o de los ajustes del entorno.
## Estructura
![](https://i.imgur.com/EQmFojF.png)
## Aplicabilidad
### Utiliza el patrón Abstract Factory cuando tu código deba funcionar con varias familias de productos relacionados, pero no desees que dependa de las clases concretas de esos productos, ya que puede ser que no los conozcas de antemano o sencillamente quieras permitir una futura extensibilidad.
El patrón Abstract Factory nos ofrece una interfaz para crear objetos a partir de cada clase de la familia de productos. Mientras tu código cree objetos a través de esta interfaz, no tendrás que preocuparte por crear la variante errónea de un producto que no combine con los productos que ya ha creado tu aplicación.
### Considera la implementación del patrón Abstract Factory cuando tengas una clase con un grupo de [métodos de fábrica](https://refactoring.guru/es/design-patterns/factory-method) que nublen su responsabilidad principal.
En un programa bien diseñado _cada clase es responsable tan solo de una cosa_. Cuando una clase lidia con varios tipos de productos, puede ser que valga la pena extraer sus métodos de fábrica para ponerlos en una clase única de fábrica o una implementación completa del patrón Abstract Factory.
## Ejemplo
```ts
type ProductStyle =
  | 'Vitorian'
  | 'Modern'

type ProductType =
  | 'Chair'
  | 'Table'

interface IChair {
  sitOn(): string
}

interface ITable {
  putOn(): string
}

interface IAbstractFactory {
  makeChair(): Chair
  makeTable(): Table
}

abstract class Chair implements IChair {
  abstract sitOn(): string
}

abstract class Table implements ITable {
  abstract putOn(): string
}

class VictorianChair extends Chair {
  name: ProductType = 'Chair'
  type: ProductStyle = 'Vitorian'
  
  sitOn(){
    return `You set on a ${this.type} ${this.name}`
  }
}
  
class ModernChair extends Chair{
  name: ProductType = 'Chair'
  type: ProductStyle = 'Modern'
  
  sitOn(){
    return `You set on a ${this.type} ${this.name}`
  }
}
  
class VictorianTable extends Table {
  name: ProductType = 'Table'
  type: ProductStyle = 'Vitorian'
  
  putOn(){
    return `You put the keys on the ${this.type} ${this.name}`
  }
}
  
class ModernTable extends Table {
  name: ProductType = 'Table'
  type: ProductStyle = 'Modern'
  
  putOn(){
    return `You put the keys on the ${this.type} ${this.name}`
  }
}
  
class VictorianFactory implements IAbstractFactory {
  makeChair(): Chair {
    return new VictorianChair()
  }
  
  makeTable(): Table{
    return new VictorianTable()
  }
}
  
class ModernFactory implements IAbstractFactory {
  makeChair(): Chair{
    return new ModernChair()
  }
  
  makeTable(): Table{
    return new ModernTable()
  }
}

function client(factory: IAbstractFactory){
  const chair = factory.makeChair()
  const table = factory.makeTable()
  
  console.log(chair.sitOn())
  console.log(table.putOn())
}
  
client(new VictorianFactory())
client(new ModernFactory ())
```
