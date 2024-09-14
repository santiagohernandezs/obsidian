## Propósito
**Facade** es un patrón de diseño estructural que proporciona una interfaz simplificada a una biblioteca, un framework o cualquier otro grupo complejo de clases.
![](https://i.imgur.com/JQQWThY.png)
## Problema
Imagina que debes lograr que tu código trabaje con un amplio grupo de objetos que pertenecen a una sofisticada biblioteca o framework. Normalmente, debes inicializar todos esos objetos, llevar un registro de las dependencias, ejecutar los métodos en el orden correcto y así sucesivamente.

Como resultado, la lógica de negocio de tus clases se vería estrechamente acoplada a los detalles de implementación de las clases de terceros, haciéndola difícil de comprender y mantener.
## Solución
Una fachada es una clase que proporciona una interfaz simple a un subsistema que contiene muchas partes móviles. Una fachada puede proporcionar una funcionalidad limitada en comparación con trabajar directamente con el subsistema. Sin embargo, tan solo incluye las funciones realmente importantes para los clientes.

Tener una fachada resulta útil cuando tienes que integrar tu aplicación con una biblioteca sofisticada con decenas de funciones, de la cual sólo necesitas una pequeña parte.

Por ejemplo, una aplicación que sube breves vídeos divertidos de gatos a las redes sociales, podría potencialmente utilizar una biblioteca de conversión de vídeo profesional. Sin embargo, lo único que necesita en realidad es una clase con el método simple `codificar(nombreDelArchivo, formato)`. Una vez que crees dicha clase y la conectes con la biblioteca de conversión de vídeo, tendrás tu primera fachada.
## Analogía en el mundo real
![](https://i.imgur.com/fSRQ9Lp.png)
Cuando llamas a una tienda para hacer un pedido por teléfono, un operador es tu fachada a todos los servicios y departamentos de la tienda. El operador te proporciona una sencilla interfaz de voz al sistema de pedidos, pasarelas de pago y varios servicios de entrega.
## Estructura
![](https://i.imgur.com/q13TKmL.png)
1.  El patrón **Facade** proporciona un práctico acceso a una parte específica de la funcionalidad del subsistema. Sabe a dónde dirigir la petición del cliente y cómo operar todas las partes móviles.
2.  Puede crearse una clase **Fachada Adicional** para evitar contaminar una única fachada con funciones no relacionadas que podrían convertirla en otra estructura compleja. Las fachadas adicionales pueden utilizarse por clientes y por otras fachadas.
3.  El **Subsistema Complejo** consiste en decenas de objetos diversos. Para lograr que todos hagan algo significativo, debes profundizar en los detalles de implementación del subsistema, que pueden incluir inicializar objetos en el orden correcto y suministrarles datos en el formato adecuado.
4. El **Cliente** utiliza la fachada en lugar de invocar directamente los objetos del subsistema.
## Aplicabilidad
### Utiliza el patrón Facade cuando necesites una interfaz limitada pero directa a un subsistema complejo.
A menudo los subsistemas se vuelven más complejos con el tiempo. Incluso la aplicación de patrones de diseño suele conducir a la creación de un mayor número de clases. Un subsistema puede hacerse más flexible y más fácil de reutilizar en varios contextos, pero la cantidad de código de configuración que exige de un cliente, crece aún más. El patrón Facade intenta solucionar este problema proporcionando un atajo a las funciones más utilizadas del subsistema que mejor encajan con los requisitos del cliente.

### Utiliza el patrón Facade cuando quieras estructurar un subsistema en capas.
Crea fachadas para definir puntos de entrada a cada nivel de un subsistema. Puedes reducir el acoplamiento entre varios subsistemas exigiéndoles que se comuniquen únicamente mediante fachadas.
## Pros y Contras
### Pros
- Puede aislar tu código de la complejidad de un subsistema.
### Contras
- Una fachada puede convertirse en un **objeto todopoderoso** acoplado a todas las clases de una aplicación.
## Ejemplo
```ts
class AudioConverter {
  convertAudio(){
    return 'Audio converted.'
  }
}

class VideoConverter {
  convertVideo(){
    return 'Video Converted'
  }
}

class Facade {
  protected audioConverter: AudioConverter
  protected videoConverter: VideoConverter
  
  constructor(audioConverter?: AudioConverter, videoConverter?: VideoConverter){
    this.audioConverter = audioConverter || new AudioConverter()
    this.videoConverter = videoConverter || new VideoConverter()
  }
  
  operation(){
    let result = 'Facade initializes subsystems: \n'
    result += this.audioConverter.convertAudio() + this.videoConverter.convertVideo()
    return result
  }
}

function clientCode(facade: Facade) {
    console.log(facade.operation());
}

const audioConverter = new AudioConverter()
const videoConverter = new VideoConverter()
const facade = new Facade(audioConverter, videoConverter)

clientCode(facade)
```