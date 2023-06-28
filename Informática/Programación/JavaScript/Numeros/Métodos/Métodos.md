# Number.isFinite()
Determina si el valor pasado es un número finito.
## Sintaxis
```txt
Number.isFinite(value)
```
## Parámetros
### `value`
El valor que será verificado
## Valor de Retorno
`true` si el valor es finito, de lo contrario `false`.
```js
console.log(Number.isFinite(1 / 0));
console.log(Number.isFinite(10 / 5));
console.log(Number.isFinite(0 / 0));
```
# Number.isInteger()
Este método determina si el valor pasado  es un entero.
## Sintaxis
```txt
Number.isInteger(value)
```
## Parámetros
### `value`
El valor que será verificado.
## Valor de Retorno
`true` si el valor dado es un entero. De lo contrario `false`.
```js
function fits(x, y) {
  if (Number.isInteger(y / x)) {
    return 'Fits!';
  }
  return 'Does NOT fit!';
}

console.log(fits(5, 10));
console.log(fits(5, 11));
```
# Number.isNaN()
Este método determina si el valor pasado es un `NaN` y retorna `false` si el valor del input no es un `NaN`
## Sintaxis
```txt
Number.isNaN(value)
```
## Parámetros
`value`
El valor que será verificado.
## Valor de Retorno
`true` si el valor es de tipo `NaN`. De lo contrario `false`.
```js
function typeOfNaN(x) {
  if (Number.isNaN(x)) {
    return 'Number NaN';
  }
  if (isNaN(x)) {
    return 'NaN';
  }
}

console.log(typeOfNaN('100F'));
console.log(typeOfNaN(NaN));
```
# Number.isSafeInteger()
Este método determina si el valor pasado es un numero 'seguro' en JavaScript
## Sintaxis
```txt
Number.isSafeInteger(testValue)
```
## Parámetros
### `testValue`
El valor que será verificado como número 'seguro'
## Valor de Retorno
`true` si el valor dado es un número 'seguro'. De lo contrario `false`.
```js
function warn(x) {
  if (Number.isSafeInteger(x)) {
    return 'Precision safe.';
  }
  return 'Precision may be lost!';
}

console.log(warn(Math.pow(2, 53)));
console.log(warn(Math.pow(2, 53) - 1));
```
# Number.parseFloat()
Este método analiza un argumento y devuelve un número de punto flotante. Si un número no se puede analizar a partir del argumento, devuelve `NaN`.
## Sintaxis
```txt
Number.parseFloat(string)
```
## Parámetros
### `string`
El valor a analizar. Si este argumento no es un string, entonces se convierte en una usando una operación abstracta `ToString`.
## Valor de Retorno
Un número de coma flotante convertido a partir del `string` dado.
```js
function circumference(r) {
  if (Number.isNaN(Number.parseFloat(r))) {
    return 0;
  }
  return parseFloat(r) * 2.0 * Math.PI ;
}

console.log(circumference('4.567abcdefgh'));
console.log(circumference('abcdefgh'));
```
# Number.parseInt()
Este método analiza el argumento y retorna un entero de la raíz o base especificada.
## Sintaxis
```txt
Number.parseInt(string,[ radix])
```
## Parámetros
### `string`
El valor que se va a analizar. Si el argumento no es un `string`, entonces será convertido con la operación abstracta `ToString`.
### `radix`
Un entero entre 2 y 36 que represente la raíz del string.
## Valor de Retorno
Un string analizado desde el string dado
```js
function roughScale(x, base) {
  const parsed = Number.parseInt(x, base);
  if (Number.isNaN(parsed)) {
    return 0;
  }
  return parsed * 100;
}

console.log(roughScale(' 0xF', 16));
console.log(roughScale('321', 2));
```
# Number.prototype.toExponential()
Este método retorna un `string` representando el objeto `Number` en notación exponencial.
## Sintaxis
```txt
toExponential()
toExponential(fractionDigits)
```
## Parámetros
### `fractionDigits`
Un entero es opcional que especifica el número de dígitos después del punto decimal. 
## Valor de Retorno
Un string representando el `Number` dado en notación exponencial con dígito antes del punto decimal.
```js
function expo(x, f) {
  return Number.parseFloat(x).toExponential(f);
}

console.log(expo(123456, 2));
console.log(expo('123456'));
console.log(expo('oink'));
```
# Number.prototype.toFixed()
El método `toFixed()` formatea un número usando la notación de punto fijo.
## Sintaxis
```txt
toFixed()
toFixed(digits)
```
## Parámetros
### `digits`
número de dígitos que aparecen después del punto decimal, debería ser entre 0 y 100.
## Valor de Retorno
Un string representando el número dado usando la notación de punto fijo.
```js
function financial(x) {
  return Number.parseFloat(x).toFixed(2);
}

console.log(financial(123.456));
console.log(financial(0.004));
```
# Number.prototype.toPrecision()
Este método retorna un string representando el objeto `Number` en la precisión especificada.
## Sintaxis
```js
toPrecision()
toPrecision(precision)
```
## Parámetros
### `precision`
Un entero especificando el numero de dígitos significantes.
## Valor de Retorno
Un string que representa un objeto `Number` en notación exponencial.
```js
function precise(x) {
  return x.toPrecision(4);
}

console.log(precise(123.456));
console.log(precise(0.004));
console.log(precise(1.23e5));
```
# Number.prototype.toString()
Este método retorna un `string` que representa un el número especificado.
## Sintaxis
```txt
toString()
toString(radix)
```
## Parámetro
Un entero entre 2 y 36 especificando la base a usar para representar el valor.
## Valor de Retorno
Un string representando el valor especificado.
```js
function hexColour(c) {
  if (c < 256) {
    return Math.abs(c).toString(16);
  }
  return 0;
}

console.log(hexColour(233));
console.log(hexColour('11'));
```
# Number.prototype.valueOf()
