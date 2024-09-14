Al establecer métodos de autenticación esto hará que en los mensages "Hello" integren en su encabezado un método de autenticación con una contraseña dentro de esta, si el vecino no cuenta con los mísmos métodos de autenticación y la misma contraseña pues dropeará los paquetes y se declararán los vecinos Down.

Existen tres tipos de autenticación:
- Texto plano
- MD5
- SHA

## Texto plano
Es el tipo de autenticación 1 y este se propaga en la red con un formato de **texto plano** lo que no puede ser tan seguro para usos que van más allá de una maqueta de prueba. 

```
ip ospf authentication
ip ospf authentication-key cisco123
```

## MD5
Es el tipo de autenticación 2 y este se propaga en la red de manera encriptada 

```
ip ospf authentication message-digest
ip ospf message-digest-key 1 md5 cisco123
```

## SHA
El tipo de autenticación tipo 3. Esta permite tener autenticación en integridad en los datos con una misma función. Para esto necesitamos crear un llavero (key chain)

```
key chain x
key 1
key-string cisco123
cryptographic-algorithm hmac-sha-{ 1 | 256 | 384 | 512 }
```

Donde *x* es el nombre del "key chain".

Luego, nos dirigimos a las interfaces y habilitamos el modo de autenticación en cada una de ellas, indicando el "key chain" que queremos utilizar.

```
inter g0/0
ip ospf authentication hey-chain x
```

