# Object.assign()
El método estático `Object.assign()` copia todos los "enumerable own properties" desde uno o más *objetos fuentes* a un *objeto objetivo*. Este retorna el *objeto objetivo* modificado.
## Sintaxis
```txt
Object.assign(target, ...sources)
```
## Parámetros
### `target`
El objeto *objetivo*, al que se le aplicarán los valores de los *objetos fuentes*.
### `sources`
Los *objetos fuente* son aquellos que contienen las propiedades que serán aplicadas al *objeto objetivo*
## Valor de Retorno
El *objeto objetivo*
## Descripción
Las propiedades en el *objetivo* son sobrescritas por las propiedades en las *fuentes* si tienen la misma `key`.
```js
const target = { a: 1, b: 2 };
const source = { b: 4, c: 5 };
const returnedTarget = Object.assign(target, source);

console.log(target);
console.log(returnedTarget === target);
```
## Object.create()
El método estático `Object.create()` crea un nuevo objeto, usando un objeto existente como el prototipo para el nuevo objeto creado.
## Sintaxis
```txt
Object.create(proto)
Object.create(proto, propertiesObject)
```
## Parámetros
### `proto`
El objeto que será usado como el prototipo del nuevo objeto creado.
### `propertiesObject`
Si es especificado y no `undefined`, un objeto cuyas propiedades numerables propias especifica descriptores de propiedad  para ser agregadas al objeto recién creado, con los nombres de propiedad correspondiente.
## Valor de Retorno
Un nuevo objeto con prototipo de objeto y propiedades especificadas.
```js
const person = {
  isHuman: false,
  printIntroduction: function() {
    console.log(`My name is ${this.name}. Am I human? ${this.isHuman}`);
  }
};

const me = Object.create(person);

me.name = 'Matthew';
me.isHuman = true;

me.printIntroduction();
```
# Object.defineProperties()
El método estático `Object.defineProperties()` define nuevas o modifica propiedades directas de un objeto, retornando el objeto.
## Sintaxis
```txt
Object.defineProperties(obj, props)
```
## Parámetros
### `obj`
El objeto en el que definiremos o modificaremos las propiedades.
### `props`
Un objeto cuyas keys representan los nombres de las propiedades que serán definidas o modificadas y cuyos valores son objetos describiendo las sus propiedades.
