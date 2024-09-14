# Number.EPSILON
La propiedad `Number.EPSILON` representa la diferencia entre 1 y el número de coma flotante más pequeño mayor a 1.
## Valor
$2^{-52}$, o aproximadamente $2.2204460492503130808472633361816E-16$
## Descripción
`Number.EPSILON` es la diferencia entre 1 y el siguiente número más alto representable en el formato de Number, debido a que el formato de doble precisión de coma flotante solo tiene 52 bits para representar el mantissa y el menor bit tiene un significado de $2^{-52}$
```js
const result = Math.abs(0.2 - 0.3 + 0.1);

console.log(result);
console.log(result < Number.EPSILON);
```
# Number.MAX_SAFE_INTEGER
La propiedad estática `Number.MAX_SAFE_INTEGER` representa el valor máximo 'seguro' de un entero en JavaScript ($2^{53} - 1$).
## Valor
$9,007,199,254,740,991$ o ~9 mil billones.
```js
const x = Number.MAX_SAFE_INTEGER + 1;
const y = Number.MAX_SAFE_INTEGER + 2;

console.log(Number.MAX_SAFE_INTEGER);
console.log(x);
console.log(x === y);
```