## Propósito
Factory Method o también llamado Método Fábrica es un diseño creacional que brinda una interfaz para crear objetos en una superclase, a la vez que permite a las subclases alterar el tipo de de objetos que se crean.

## Problema
Imagina que estás creando una aplicación de gestión de logística. La primera versión de tu aplicación solo es capaz de manejar el transporte en camión, por lo que la mayor parte de tu código se encuentra dentro de la clase `Camion`.

Al cabo de un tiempo se vuelve bastante popular. Cada día recibes decenas de peticiones de empresas de transporte marítimo para que incorpores la logística por mar a la aplicación.
![](https://i.imgur.com/iPdNl18.png)
Estupendo, ¿verdad? Pero, ¿qué pasa con el código? En este momento, la mayor parte de tu código está acoplado a la clase `Camión`. Para añadir barcos a la aplicación habría que hacer cambios en toda la base del código. Además, si más tarde decides añadir otro tipo de transporte a la aplicación, probablemente tendrás que volver a hacer todos estos cambios.

Al final acabarás con un código bastante sucio, plagado de condicionales que cambian el comportamiento de la aplicación dependiendo de la clase de los objetos de transporte.
## Solución
El patrón Factory Method sugiere que, en lugar de llamar al operador `new` para construir objetos directamente, se invoque a un método _fábrica_ especial. No te preocupes: los objetos se siguen creando a través del operador `new`, pero se invocan desde el método fábrica. Los objetos devueltos por el método fábrica a menudo se denominan _productos_.
![](https://i.imgur.com/WDRfodj.png)
Por ejemplo, tanto la clase `Camión` como la clase `Barco` deben implementar la interfaz `Transporte`, que declara un método llamado `entrega`. Cada clase implementa este método de forma diferente: los camiones entregan su carga por tierra, mientras que los barcos lo hacen por mar. El método fábrica dentro de la clase `LogísticaTerrestre` devuelve objetos de tipo camión, mientras que el método fábrica de la clase `LogísticaMarítima` devuelve barcos.
![](https://i.imgur.com/mHmHjST.png)
El código que utiliza el método fábrica (a menudo denominado código _cliente_) no encuentra diferencias entre los productos devueltos por varias subclases, y trata a todos los productos como la clase abstracta `Transporte`. El cliente sabe que todos los objetos de transporte deben tener el método `entrega`, pero no necesita saber cómo funciona exactamente.
## Estructura
![](https://i.imgur.com/QQTv6c6.png)
## Aplicabilidad
### Utiliza el método fábrica cuando no conozcas de antemano las dependencias y los tipos de exactos de los objetos con los que de deba funcionar de tu código.

El patrón de fábrica separa el código de construcción de producto del código que hace uso del producto. Por ello, es más fácil extender el código de construcción de producto de forma independiente al resto del código.
### Utiliza el Factory Method cuando quieras ofrecer a los usuarios de tu biblioteca o framework, una forma de extender sus componentes internos.

La herencia es probablemente la forma más sencilla de extender el comportamiento por defecto de una biblioteca o un framework. La solución es reducir el código que construye componentes en todo el framework a un único patrón Factory Method y permitir que cualquiera sobrescriba este método además de extender el propio componente.
### Utiliza el Factory Method cuando quieras ahorrar recursos del sistema mediante la reutilización de objetos existentes en lugar de reconstruirlos cada vez.
## Pros y contras
### Pros
- Evitas un acoplamiento fuerte entre el creador y los productos concretos.
- *Principio de responsabilidad única*. Puedes mover el Código de creation de producto a un lugar del programa, haciendo que el código sea más fácil de mantener.
- *Principio de abierto/cerrado*. Puedes incorporar nuevos tipos de productos en el programa sin descomponer el código cliente existente.
### Contras
- Puede ser que el código se complique, ya que debes de incorporar una multitud de nuevas subclases para implementar el patrón. La situación ideal sería introducir el patrón en una jerarquía existente de clases creadoras.
## Ejemplo en Código
```ts
interface IConnection {
  newConnection(): string
}

interface DbConfig {
  newConnection(): string
}

class PostgreSql implements DbConfig{
  private name: string = 'postgresql'
  private host: string = '127.0.0.1'
  private user: string = 'root'
  private password: string = 'admin'
  
  newConnection() {
    return `connected to db with this info 
    name:${this.name}
    host:${this.host}
    user:${this.user}
    passeword:${this.password}
    `
  }
}

class MySql implements DbConfig{
  private name: string = 'mysql'
  private host: string = '127.0.0.1'
  private user: string = 'root'
  private password: string = 'admin'
  
  newConnection() {
    return `connected to db with this info 
    name:${this.name}
    host:${this.host}
    user:${this.user}
    passeword:${this.password}
    `
  }
}

abstract class ConnectionFactory {
  public abstract factoryMethod(): IConnection;
  
  createConnection():string {
    const connection = this.factoryMethod()
    return `${connection.newConnection()}`;
  }
}

class PostgresqlConnection extends ConnectionFactory {
  factoryMethod() {
    return new PostgreSql()
  }
}

class MysqlConnection extends ConnectionFactory {
   factoryMethod() {
    return new MySql()
  } 
}

function client(factory: ConnectionFactory) {
  console.log(factory.createConnection());
}

client(new PostgresqlConnection())
client(new MysqlConnection())
```
