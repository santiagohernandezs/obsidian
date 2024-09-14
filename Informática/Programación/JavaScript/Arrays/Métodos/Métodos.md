# Array.prototype.at()
El método `at()` recibe un valor numérico y devuelve el elemento en esa posición, permitiendo así valores positivos y negativos.
## Sintaxis
```txt
at(index)
```
```js
const numbers = [23, 34, 764, 65, 14, 9];
let positive = numbers.at(2);
let negative = numbers.at(-2);

console.log(positive, negative);
```
# Array.prototype.concat()
El método `concat()` se usa para unir dos o más arrays. Este método no cambia los arrays existentes, sino que devuelve un nuevo array.
## Sintaxis
```txt
var nuevo_array = viejo_array.contact(valor1[, valor2[, ...[, valorN]]]) 
```
## Parámetros
### `Valor N`
Arrays y/o valores a concatenar el nuevo array.
## Valor de Retorno
Una nueva instancia de `Array`
## Descripción
El método `concat` crea un nuevo array que consta de los elementos del objeto que lo llama, seguido, en orden de ingreso, por los elementos de cada parámetro. Este método no altera el `this` del array original ni en ninguno de los que fueron ingresados como parámetros, sino que devuelve una copia superficial (shallow copy) que contiene copias de los mismos elementos de los arrays originales combinados. Los elementos de los arrays son copiados de la siguiente manera:
- Referencias a Objetos (no el objeto real): `concat` copia las referencias del objeto en el nuevo array. Ambos, el array original y el nuevo array refieren al mismo objeto.
- Tipos de datos como strings, numbers y booleans (**no objetos `String`, `Number`, `Boolean`**): `concat` copia los valores de los strings, numbers and booleans en el nuevo array.
## Ejemplo
```js
const array1 = ['a', 'b', 'c'];
const array2 = ['d', 'e', 'f'];
const array3 = array1.concat(array2);

console.log(array3);
```
# Array.prototype.entries()
El método `entries()` retorna un nuevo objeto `Array Iterator` que contiene los clave/valor para cada índice de la matriz.
## Sintaxis
```txt
arr.entries()
```
## Valor de Retorno
Un nuevo objeto iterador `Array`
## Ejemplo
```js
var a = ['a', 'b', 'c'];
var iterator = a.entries();

console.log(iterator)

for (let i of iterator){
	console.log(i);
}
```
# Array.prototype.every()
Determina si todos los elementos de un array cumplen con la condición.
## Sintaxis
```txt
arr.every(callback(element[, index[, array]])[, thisArg])
```
## Parámetros
### `callback`
Una función para probar cada elemento y recibe tres argumentos:
- `currentValue` (requiered): El elemento actual del arreglo que está siendo procesado.
- `index` (Optional): El índice del elemento actual del arreglo que está siendo procesado.
- `array` (Optional): El arreglo sobre el cual fue llamado `every`.
- `thisArg` (Optional): Valor como para usar `this` cuando se ejecute `callback`
## Valor de Retorno
`true` si el callback devuelve un valor de truthy para cada elemento de la matriz; de lo contrario, false.
## Descripción
El método every ejecuta una función callback por cada elemento del arreglo hasta que encuentre uno que lo haga retornar un valor falso, de lo contrario devolverá verdadero, trabaja como el cuantificador matemático "para todos"
```js
const array1 = [1, 27, 39, 29, 10, 13];

console.log(array1.every(x => x < 40));
```
# Array.prototype.fill()
El método `fill()` convierte lo valores de un array en valores estáticos, empezando desde el índice 0 (por defecto) hasta el final del array (`array.length` por defecto)
## Sintaxis
```txt
fill(value)
fill(value, start)
fill(value, start, end)
```
## Parámetros
### `value`
Es el valor que tomará para llenar los elementos del array; si este es un objeto, cada elemento referenciará a ese objeto
### `start`
Indica el comienzo de la porción afectada (dónde se comenzará a llenar)
### `end`
Indica el final de la porción que será afectada (dónde terminará de llenar)
## Valor de Retorno
El array modificado llenado con el `value`
## Descripción
El método `fill()` es un método que muta el array. No cambia el length `this`, pero cambia el contenido del `this`.
```js
const array = [1, 2, 3, 4, 5, 6, 7, 8, 9];
console.log(array.fill(1))
console.log(array.fill(0, 4))
console.log(array.fill(7, 4, 8))
```
# Array.prototype.filter()
Este es un método que crea un shallow copy de una porción de un array dado. Este filtra todo el array y devuelve solo los elementos que solo pasen el test implementado.
## Sintaxis
```txt
// Arrow function
filter((element) => { /* … */ })
filter((element, index) => { /* … */ })
filter((element, index, array) => { /* … */ })

// Callback function
filter(callbackFn)
filter(callbackFn, thisArg)

// Inline callback function
filter(function (element) { /* … */ })
filter(function (element, index) { /* … */ })
filter(function (element, index, array) { /* … */ })
filter(function (element, index, array) { /* … */ }, thisArg)
```
## Parámetros
### `callbackFn`
Una función que se ejecuta por cada elemento del array debería retornar el valor de truthy para que el elemento se encuentre en el array resultante.
- `element` : el elemento que está siendo procesado.
- `index` : el índice del elemento que está siendo procesado.
- `array` : el array donde `filter()` fue llamado.
### `thisArg` (opcional)
Un valor para utilizar como `this` cuando se ejecute `callbackFn`
## Valor de Retorno
Un shallow copy de una porción del array dado, conteniendo solo los elementos del array que cumplieron con la implementación. Si ninguna cumplió con ella el array estará vacío.
```js
const array = [1,0,0,1,1,1,0];

console.log(array)
console.log(array.filter(x => x === 1));
```
# Array.prototype.find()
El método `find()` retorna el primer elemento del array que cumpla con la implementación; si ninguno cumple con ella `undefined` será el valor retornado.
## Sintaxis
```txt
// Arrow function
find((element) => { /* … */ })
find((element, index) => { /* … */ })
find((element, index, array) => { /* … */ })

// Callback function
find(callbackFn)
find(callbackFn, thisArg)

// Inline callback function
find(function (element) { /* … */ })
find(function (element, index) { /* … */ })
find(function (element, index, array) { /* … */ })
find(function (element, index, array) { /* … */ }, thisArg)
```
## Parámetros
### `callbackFn`
Una función que se ejecuta por cada elemento del array, debe retornar el valor de truthy para indicar que un elemento ha sido encontrado.
- `element` : el elemento que está siendo procesado en el array.
- `index` : el índice del elemento que está siendo procesado en el array.
- `array` : el array donde `find()` donde fue llamado.
### `thisArg` (opcional)
Un valor para utilizar como `this` cuando se ejecute `callbackFn`.
## Valor de Retorno
El primer elemento del array que cumpla con la implementación, de lo contrario devolverá `undefined`.
# Descripción
Es un método iterativo que recorre el array de manera creciente (su variación sería el método `findLast()` el cual recorre el array desde el último elemento, o sea, de manera decreciente) y este llama un callback por cada elemento del array hasta que el callback retorne un valor truthy. `find()` retorna el elemento y para de iterar el array. Si `find()` no retorna un valor truthy, retornará `undefined`. 
```js
const array = ['foo', 'bar', 'buz'];

console.log(array.find(word => word.startsWith('b')))
console.log(array.findLast(word => word.startsWith('b')))
```
# Array.prototype.findIndex()
El método `findIndex()` retorna el índice del array del primer elemento que cumpla con la implementación, muy similar al método `find()` solo que en vez de devolver un boolean este devuelve un numero.
## Parámetros
### `callbackFn`
Una función que se ejecuta por cada elemento del array, debe retornar el valor de truthy para indicar que un elemento ha sido encontrado.
- `element` : el elemento que está siendo procesado en el array.
- `index` : el índice del elemento que está siendo procesado en el array.
- `array` : el array donde `find()` donde fue llamado.
### `thisArg` (opcional)
Un valor para utilizar como `this` cuando se ejecute `callbackFn`.
## Valor de Retorno
El índice del primer elemento del array que cumpla con la implementación, de lo contrario retornará `-1`.
## Descripción
Es un método iterativo que recorre el array de manera creciente (su variación sería el método `findLastIndex()` el cual recorre el array desde el último elemento, o sea, de manera decreciente) y este llama un callback por cada elemento del array hasta que el callback retorne un valor truthy. `find()` retorna el índice elemento y para de iterar el array. Si `find()` no retorna un valor truthy, retornará `-1`. 
```js
const array = [3, 37, 41, 68, 47, 12]

console.log(array.findIndex(x => x > 40))
console.log(array.findLastIndex(x => x > 40))
```
# Array.prototype.flat()
El método `flat()` crea un nuevo con todos los sub arreglos concatenados recursivamente hasta la profundidad especificada.
## Sintax
```txt
flat()
flat(depth)
```
## Parámetros
### `depth`
El nivel de aplanado que se aplicará al array para reducir el número de arrays  concatenados.
## Valor de Retorno
El nuevo array aplanado.
## Descripción
El método `flat()` es un método de copiado. Por lo que no altera el `this` del array, por ende realiza una copia superficial (shallow copy) que contiene los mismos elementos del array original.
```js
const array = [1, 2, 3, [4, 5, [6, 7, [8, 9]]]]

console.log(array.flat(1))
console.log(array.flat(2))
console.log(array.flat(3))

console.log(array)
```
# Array.prototype.flatMap()
El método `flatMap()` retorna un nuevo array, array resultante de aplicar un `callback` por cada uno de los elementos del array y luego aplanándolos con una profundidad de uno. A groso modo, `flatMap()` es idéntico a un `map()` seguido de un `flat()` de profundidad 1 (`arr.map(...args).flat()`), pero este método es un poco más eficiente que aplicar ambos métodos uno luego de otro.
## Sintaxis
```txt
// Arrow function
flatMap((element) => { /* … */ })
flatMap((element, index) => { /* … */ })
flatMap((element, index, array) => { /* … */ })

// Callback function
flatMap(callbackFn)
flatMap(callbackFn, thisArg)

// Inline callback function
flatMap(function (element) { /* … */ })
flatMap(function (element, index) { /* … */ })
flatMap(function (element, index, array) { /* … */ })
flatMap(function (element, index, array) { /* … */ }, thisArg)

```
## Parámetros
### `callback`
Una función que se ejecutará por cada uno de los elementos del array. Debe retornar un array conteniendo nuevos elementos del nuevo array o un solo valor no-array para ser añadido al nuevo array.
Esta función es llamada con los siguientes parámetros:
- `element` : El elementos que está siendo procesado en el array.
- `index` : El índice del elemento que está siendo procesado en el array.
- `array` : El array donde `flatMap()` fue llamado.
### `thisArg` (Opcional)
Un valor para usar como `this` cuando el `callback` se ejecute.
## Valor de Retorno
Un nuevo array con los elementos resultantes de la aplicación del `callback` y `flat()` en cada uno de los elementos.
## Descripción
El método `flatMap()` es un método iterativo. Es idéntico a un `map(callback, thisArg)` seguido de un `flat()`.
```js
const array = [1, 2, [3], [4, 5], 6, []];

console.log(array.flatMap(num => num))
```
# Array.prototype.forEach()
El método `forEach()` ejecuta una función por cada elemento del array.
## Sintaxis
```txt
// Arrow function
forEach((element) => { /* … */ })
forEach((element, index) => { /* … */ })
forEach((element, index, array) => { /* … */ })

// Callback function
forEach(callbackFn)
forEach(callbackFn, thisArg)

// Inline callback function
forEach(function (element) { /* … */ })
forEach(function (element, index) { /* … */ })
forEach(function (element, index, array) { /* … */ })
forEach(function (element, index, array) { /* … */ }, thisArg)
```
## Parámetros
### `callback`
Una función que se ejecuta por cada elemento del array. Su valor de retorno
La función es llamada con tres argumentos:
- `element` : El elemento del array que está siendo procesado.
- `index` : El índice del elemento que está siendo procesado.
- `array` : El array donde `forEach()` fue llamado.
### `thisArg`
Un valor para usar como `this` cuando el `callback` se ejecute.
## Valor de Retorno
`undefined`
## Descripción
El método `forEach()` es un método iterativo. Llama a un `callback` por cada elemento del array en orden ascendente. A diferencia de `map()`, `forEach()` siempre retorna `undefined`
y no se puede encadenar. Es un método que no muta el array original pero el `callback` que contiene sí puede
```js
const array = ['a', 'b', 'c'];

array.forEach(element => console.log(element));
```
# Array.prototype.from()
El método `array.from()` crea una nueva instancia de `Array` de una copia superficial desde un iterable o un «array-like object».
## Sintaxis
```txt
Array.from(arrayLike)

// Arrow function
Array.from(arrayLike, (element) => { /* … */ })
Array.from(arrayLike, (element, index) => { /* … */ })

// Mapping function
Array.from(arrayLike, mapFn)
Array.from(arrayLike, mapFn, thisArg)

// Inline mapping function
Array.from(arrayLike, function (element) { /* … */ })
Array.from(arrayLike, function (element, index) { /* … */ })
Array.from(arrayLike, function (element) { /* … */ }, thisArg)
Array.from(arrayLike, function (element, index) { /* … */ }, thisArg)

```
## Parámetros
### `arrayLike`
Un iterable o un objeto array-like para convertir en un array.
### `mapFn`
Una función map que funciona como el `Array.map()`.
### `thisArg`
Un valor para usar como `this` cuando el `mapFn` se ejecute.
## Valor de Retorno
Una nueva instancia de `Array`.
## Descripción
`Array.from()` permite crear arrays desde:
- Objetos iterables: tales como `Map` y `Set`.
- Objetos "Array-like": objetos con la propiedad de `length`
Este método nunca crea un array escaso. Por lo que si el objeto "Arra-like" faltan algunas propiedades, esas mismas propiedades serán reflejadas en un nuevo array como `undefined`. Esta tiene un parámetro opcional `mapFn`, que permite ejecutar una función por cada elemento del array.
# Array.prototype.includes()
El método `includes()` determina si el array contiene o **incluye** un valor entre sus elementos, retornando `true` o `false` según como sea necesario 
## Sintaxis
```txt
includes(searchElement)
includes(searchElement, fromIndex)
```
## Parámetros
### `searchElement`
El valor que se va a buscar en el array.
### `fromIndex` (Opcional)
El índice del array en donde debe empezar a buscar
## Valor de Retorno
Si el valor que se buscaba se encuentra en el array el valor de retorno será `true`, de lo contrario `false`.
## Descripción
El método `includes()` compara el `seacrhElement` con los elementos del array usando el algoritmo SameValueZero.
```js
let myArray = [1, 2, 3, 4, 5, 6];

console.log(myArray.includes(2))
console.log(myArray.includes(9))
```
# Array.prototype.indexOf()
El método `indexOf()` retorna el índice del elemento en un array (retornará el índice del primer elemento que haga match)
## Sintaxis
```txt
indexOf(searchElement)
indexOf(searchElement, fromIndex)
```
## Parámetros
### `searchElement`
El valor que se va a buscar en el array.
### `fromIndex` (Opcional)
El índice del array en donde debe empezar a buscar
## Valor de Retorno
El índice del primer elemento que encuentre en el array, de lo contrario retornará `-1`
## Descripción
El método `indexOf()` compara el `seacrhElement` con los elementos del array usando el algoritmo SameValueZero.
```js
let myArray = [1, 2, 3, 4, 5, 6];

console.log(myArray.indexOf(4))
console.log(myArray.indexOf(9))
```
## Array.prototype.isArray()
Este es un método estático que determina si el valor que le pasamos como parámetro es una `Array`.
## Sintaxis
```txt
Array.isArray(value)
```
## Parámetros
### `value`
El valor que será verificado.
## Valor de Retorno
Si `value` es un `Array` el valor de retorno será `true`, de lo contrario retornará `false`. Además si `value`es una instancia de `TypedArray` el valor de retorno será `false`.
## Descripción
El método `isArray()` verifica si el valor que le pasamos es un `Array`. No verifica la cadena prototípica de los valores. Devolverá true si el valor es un array literal y proviene del constructor `Array`.
```js
const myArray = [1, 'a', true];
const emptyArray = [];

console.log(Array.isArray(myArray));
console.log(Array.isArray(emptyArray));
console.log(Array.isArray(new Array(5)));
console.log(Array.isArray(new Int16Array([14,32])));
```
# Array.prototype.join()
El método `join()` crea y retorna un nuevo array concatenando todos los elementos del array o de un objeto "array-like", separados por comas o cualquier otro **`string` separador**.
## Sintaxis
```txt
join()
join(separator)
```
## Parámetros
### `separator`
Un `string` específico para separar cada par o cada elemento adyacente en el array. Por defecto el separador es una coma (",").
## Valor de Retorno
Un `string` con todos los elementos del array unidos. Si `arr.length` es `0` , entonces el valor de retorno será un string vacío.
## Descripción
Las conversiones a `string` de todos los elementos del array son unidas en un solo string.
Si un elemento es `undefined`, `null`, es convertido en un `string` vacío en vez de `"null"` o `"undefined"`.
```js
const elements = ['Fire', 'Air', 'Water'];

console.log(elements.join());
console.log(elements.join(''));
console.log(elements.join('-'));
```
# Array.prototype.keys()
`keys()` es un método que retorna un objeto `Array` iterador que contiene las keys de cada índice en el array.
## Sintaxis
```txt
keys()
```
## Valor de Retorno
Un nuevo objeto `Array` Iterador.
```js
const array1 = ['a', 'b', 'c'];
const iterator = array1.keys();

for (const key of iterator) {
  console.log(key);
}
```
# Array.prototype.map()
El método map crea un nuevo array lleno con los resultados de la llamada de la función que se ejecuta por cada elemento del array.
## Sintaxis
```txt
// Arrow function
map((element) => { /* … */ })
map((element, index) => { /* … */ })
map((element, index, array) => { /* … */ })

// Callback function
map(callbackFn)
map(callbackFn, thisArg)

// Inline callback function
map(function (element) { /* … */ })
map(function (element, index) { /* … */ })
map(function (element, index, array) { /* … */ })
map(function (element, index, array) { /* … */ }, thisArg)
```
## Parámetros
### `callback`
Una función que se ejecutará por cada uno de los elementos del array. Debe retornar un array conteniendo nuevos elementos del nuevo array o un solo valor no-array para ser añadido al nuevo array.
Esta función es llamada con los siguientes parámetros:
- `element` : El elementos que está siendo procesado en el array.
- `index` : El índice del elemento que está siendo procesado en el array.
- `array` : El array donde `flatMap()` fue llamado.
### `thisArg` (Opcional)
Un valor para usar como `this` cuando el `callback` se ejecute.
## Valor de Retorno
Un nuevo array con los elementos resultantes de la aplicación del `callback` y `flat()` en cada uno de los elementos.
## Valor de Retorno
Un nuevo `Array` con cada elemento siento resultado del `callback function`.
## Descripción
El método `map()` es un método iterativo. Y llama al callback que le fue proveído por cada elemento en el array y construye un nuevo array con los resultados.
```js
const array1 = [1, 4, 9, 16];

const map1 = array1.map(x => x * 2);

console.log(map1)
```
# Array.prototype.of()
El método `of()` es un método estático que crea un nuevo `Array` desde un numero variable de argumentos. 
## Sintaxis
```txt
Array.of(element0)
Array.of(element0, element1)
Array.of(element0, element1, ..., elementN)
```
## Parámetros
### `elementN`
Elementos usados para crear el array.
## Valor de Retorno
Una nueva instancia de `Array`
## Descripción
La diferencia entre `Array.of()` y el constructor `Array()` está en el manejo del/los argumentos. `Array.of(7)` crea un array con un solo elemento, `7`. `Array(7)` crea un array vacío con un `length` de `7`.
```js
console.log(Array.of(7));
console.log(Array(7));
```
```js
console.log(Array.of('foo', 2,'bar', true));
console.log(Array.of());
```
# Array.prototype.pop()
El método `pop()` remueve el último elemento del array, cambiando el `length` del array y retorna el elemento que se retiró.
## Sintaxis
```txt
pop()
```
## Valor de Retorno
El elemento que se removió del array. `undefined` si el array está vacío.
```js
const plants = ['broccoli', 'cauliflower', 'cabbage', 'kale', 'tomato'];
console.log(plants.pop());
console.log(plants);
```
# Array.prototype.push()
El método `push()` añade uno o más elementos al final de un array y retorna el nuevo `length` del array.
# Sintaxis
```txt
push(element0)
push(element0, element1)
push(element0, element1, /* … ,*/ elementN)
```
## Parámetros
### `elementN`
Los elementos para añadir al final del array.
## Valor de Retorno
El nuevo `length` del array.
```js
const animals = ['pigs', 'goats', 'sheep'];
const count = animals.push('cows');

console.log(count);
console.log(animals);
```
# Array.prototype.reduce()
El método `reduce()` ejecuta un "reducer" creado por el usuario y este se ejecuta en cada elemento del array, en orden y pasando como valor de retorno el calculo del anterior elemento.
## Sintaxis
```txt
// Arrow function
reduce((accumulator, currentValue) => { /* … */ })
reduce((accumulator, currentValue, currentIndex) => { /* … */ })
reduce((accumulator, currentValue, currentIndex, array) => { /* … */ })

reduce((accumulator, currentValue) => { /* … */ }, initialValue)
reduce((accumulator, currentValue, currentIndex) => { /* … */ }, initialValue)
reduce((accumulator, currentValue, currentIndex, array) => { /* … */ }, initialValue)

// Callback function
reduce(callbackFn)
reduce(callbackFn, initialValue)

// Inline callback function
reduce(function (accumulator, currentValue) { /* … */ })
reduce(function (accumulator, currentValue, currentIndex) { /* … */ })
reduce(function (accumulator, currentValue, currentIndex, array) { /* … */ })

reduce(function (accumulator, currentValue) { /* … */ }, initialValue)
reduce(function (accumulator, currentValue, currentIndex) { /* … */ }, initialValue)
reduce(function (accumulator, currentValue, currentIndex, array) { /* … */ }, initialValue)

```
## Parámetros
### `callbackFn`
Una función que se ejecuta por cada elemento del array. El valor de retorno se convierte en el valor del parámetro `accumulator` en la siguiente llamada del `callbackFn` 
### `acumulator`
El valor resultante de la previa llamada al `callback`.
### `currentValue`
El valor del elemento actual.
### `currentIndex`
El índice del elemento actual.
###  `array`
El array en el que `reduce()` fue llamado.
### `initialValue`
El valor en el que el `accumulator` es inicializado la primera vez que el callback es llamado.
```js
const array1 = [1, 2, 3, 4];

const initialValue = 0;
const sumWithInitial = array1.reduce(
  (accumulator, currentValue) => accumulator + currentValue,
  initialValue
);

console.log(sumWithInitial);
```
# Array.prototype.reverse()
El método `reverse()` pone del revés un array y retorna una referencia al mismo array.
## Sintaxis
```txt
reverse()
```
## Valor de Retorno
Una referencia al array original, pero ahora del revés.
## Descripción
El método `reverse()` transpone los elementos del array, mutándolo y retornando una referencia al array.
```js
const array1 = ['one', 'two', 'three'];
console.log('array1:', array1);

const reversed = array1.reverse();
console.log('reversed:', reversed);

console.log('array1:', array1);
```
# Array.prototype.shift()
El método `shift()` elimina el primer elemento del array y retorna el elemento removido.
## Sintaxis
```txt
shift()
```
## Valor de Retorno
El elemento que se eliminó del array, `undefined` si el array está vacío.
```js
const array1 = [1, 2, 3];
const firstElement = array1.shift();

console.log(array1);
console.log(firstElement);
```
# Array.prototype.slice()
El método `slice()` retorna un shallow copy o una porción del array en un nuevo array seleccionado desde `start` a `end`.
## Sintaxis
```txt
slice()
slice(start)
slice(start, end)
```
## Parámetros
### `start`
Un índice base cero que indica dónde comenzará la extracción.
### `end`
Un índice base cero que indica dónde finalizará la extracción.
## Valor de retorno
Un nuevo Array conteniendo los elementos extraídos.
## Descripción
`slice()` es un método que no muta el array original, ya que realiza un shallow copy de este.
```js
const animals = ['ant', 'bison', 'camel', 'duck', 'elephant'];

console.log(animals.slice(2));
console.log(animals.slice(2, 4));
console.log(animals.slice(1, 5));
```
# Array.prototype.some()
El parámetro `some()` verifica si en el array existe al menos un elemento que pase la prueba implementada.
## Sintaxis
```txt
// Arrow function
some((element) => { /* … */ })
some((element, index) => { /* … */ })
some((element, index, array) => { /* … */ })

// Callback function
some(callbackFn)
some(callbackFn, thisArg)

// Inline callback function
some(function (element) { /* … */ })
some(function (element, index) { /* … */ })
some(function (element, index, array) { /* … */ })
some(function (element, index, array) { /* … */ }, thisArg)
```
## Parámetros
### `callback`
Una función que se ejecutará por cada uno de los elementos del array. Debe retornar un array conteniendo nuevos elementos del nuevo array o un solo valor no-array para ser añadido al nuevo array.
Esta función es llamada con los siguientes parámetros:
- `element` : El elementos que está siendo procesado en el array.
- `index` : El índice del elemento que está siendo procesado en el array.
- `array` : El array donde `flatMap()` fue llamado.
### `thisArg` (Opcional)
Un valor para usar como `this` cuando el `callback` se ejecute.
## Valor de Retorno
`true` si el callback retorna un valor `truthy` para al menos un elementos en el array. De lo contrario `false`.
```js
const array = [1, 2, 3, 4, 5];
const even = (element) => element % 2 === 0;

console.log(array.some(even));
```
# Array.prototype.sort()
El método `sort()` ordena los elementos de un array y retorna la referencia del mismo array, pero ahora ordenado. El ordenado por defecto es ascendente.
## Sintaxis
```txt
// Functionless
sort()

// Arrow function
sort((a, b) => { /* … */ } )

// Compare function
sort(compareFn)

// Inline compare function
sort(function compareFn(a, b) { /* … */ })
```
## Parámetros
### `compateFn`
Especifica una función que define el ordenamiento. Si se omite, los elementos del array son convertidos en strings y luego son ordenados de acuerdo a cada carácter.
## Valor de Retorno
La referencia al array original pero con la diferencia de que ya está ordenado.
# Array.prototype.splice
El método `splice()` cambia el contenido de un array removiendo o reemplazando los elementos existentes y/o añadiendo nuevos elementos.
## Sintaxis
```txt
splice(start)
splice(start, deleteCount)
splice(start, deleteCount, item1)
splice(start, deleteCount, item1, item2, itemN)
```
## Parámetros
### `start`
Índice base cero que indica el comienzo de la porción del array que cambiará.
### `deleteCount`
Un número entero indicando el numero de elementos del array que serán removidos a partir de `start`. Si `deleteCount` es omitida o su valor es mayor o igual que el número de elementos del array después del `start`, todo los elementos serán eliminados.
### `item1`, ..., `itemN`
Los elementos que serán añadidos al array empezando desde `start`.
## Valor de Retorno
Un array conteniendo los elementos removidos.
```js
const myArray = [1,2,3,4,5];
myArray.splice(1, 0, 1.5);
console.log(myArray);

const res = myArray.splice(3, 2);
console.log(res)
console.log(myArray)
```
# Array.prototype.toLocaleString()
Este método retorna un string representando los elementos del array. Lo elementos son convertidos a strings usando su método `toLocalString` y estos strings son separados por un `locale-specific String` (Como una coma ","). 
## Sintaxis
```txt
toLocaleString()
toLocaleString(locales)
toLocaleString(locales, options)
```
## Parámetros
### `locales`
Un string con un BCP 47 como etiqueta de lenguaje o un array  de tales strings.
### `options`
Un objeto que configura las propiedades.
## Valor de Retorno
Un string que representa los elementos del array.
```js
const array1 = [1, 'a', new Date('21 Dec 1997 14:12:00 UTC')];
const localeString = array1.toLocaleString('en', { timeZone: 'UTC' });

console.log(localeString);
```
# Array.prototyep.toString()
El método `toString()` retorna un string que representa el array y sus elementos.
## Sintaxis
```txt
toString()
```
## Valor de Retorno
Un string que representa el array y sus elementos.
## Descripción
El objeto `Array` sobrescribe el método `toString` de `Object`.
