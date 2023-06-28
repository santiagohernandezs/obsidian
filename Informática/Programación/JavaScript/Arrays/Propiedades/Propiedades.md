# get Array[@@especies]
La propiedad de acceso Array[@@especies] devuelve el constructor de `Array`
## Sintaxis
```js
Array[Symbol.species]
```
## Valor de Retorno
El constructor `Array`
## Descripción
La propiedad de acceso `species` devuelve el constructor predeterminado para objetos `Array`. Los constructores de subclase pueden anularlo para cambiar la asignación del constructor.
# Array.prototype[@@unscopables]
La propiedad de símbolo **`@@unscopable`** contiene nombres de propiedad que no se incluyeron en el estándar ECMAScript antes de la versión ES2015. Estas propiedades se excluyen de los enlaces de declaración `with`.
## Sintaxis
```js
arr[Symbol.unscopables]
```
## Descripción

Las propiedades de matriz predeterminadas que se excluyen de los enlaces `with` son: copyWithin, entries, fill, find, findIndex, includes, keys, y values.
# Array.prototype.length
La propiedad `length` de un objeto que es una instancia de tipo Array establece y retorna la cantidad de elementos en la matriz con un signo entero de 32bits 
## Valore de Retorno
Un signo entero de 32 bits siempre mayor al índice mayor de la matriz
## Descripción
El valor que retorna la propiedad length es un numero positivo menor que $2^{32}$
```js
let frutas = ['manzana', 'pera', 'uva', 'fresa'];
console.log(frutas.length)
```