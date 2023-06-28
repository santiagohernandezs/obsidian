Una variable es un espacio en la memoria al que se le puede asignar un nombre y un valor, primero que todo tenemos que entender como funcionan las memorias.

|Address|Value|
|---|---|
|0x1000||
|0x1004||
|0x1008||

Las memorias se pueden representar como una tabla con dos columnas, la primera es la que contiene las direcciones con una longitud de 32 bits y que son útiles para acceder a los valores que estas contienen. Además, se le pueden asignar nombres y tipos para que el trabajo con ellas sea menos tedioso, a esto se le conoce como declaración de variable (siempre y cuando solo se hable de asignar nombre y tipo). Por ejemplo:

```ts
let name: str; //TypeScript
```

En estos dos ejemplos **declaramos** la variable *nombre* y le asignamos un **tipo** *string*

Una vez aclarado este primer punto, vamos a con la inicialización de las variables, aquí le asignamos su primer valor, **su valor inicial** y por ello se le reconoce de este manera, podemos realizar esta acción con el operador de asignación (=) y luego el valor que le queremos asignar a la variable.

```ts
let name: str;
name = 'Alejandro';
```

También podemos hacer las dos acciones en una misma instrucción, es decir, declarar e inicializar a la vez.
```ts
let name:str = 'Alejandro';
let lastName:str = 'Fernandez';
```

Una vez realizadas las declaraciones y asignaciones nuestra tabla se vería de la siguiente manera:

|Address|Value|
|---|---|
|name -> 0x1000|"Alejandro"|
|lastName -> 0x1004|"Fernandez"|

## Mutabilidad
Decimos que algo es inmutable cuando no puede cambiar. Por ello, una variable inmutable es aquella variable que su valor se puede modificar tras su inicialización. Por ello es importante tener en cuenta cuando nos encontramos con alguna variable u objeto inmutable en el código. Además, los objetos inmutables se denominan como *thread-safe* ya que, al no poder ser modificables, pueden ser accedidos de manera concurrente sin consecuencias. 
