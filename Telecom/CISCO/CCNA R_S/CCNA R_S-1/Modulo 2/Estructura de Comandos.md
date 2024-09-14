# Estructura básica de los comandos de IOS

Este tema cubre la estructura básica de los comandos para Cisco IOS. Un administrador de red debe conecer la estructura de comandos básica del IOS par apoder usar la CLI.

![](https://ccnadesdecero.es/wp-content/uploads/2020/07/Estructura-B%C3%A1sica-Comandos-de-IOS.png)

-   **Palabra clave (Keyword)** - Esto es un parámetro específico definido en el sistema operativo (en la figura, **ip protocols**).
-   **Argumento** - Esto no está predefinido; es un valor o variable definida por el usuario (en la figura, **192.168.10.5**).

# Comprobación de la sintaxis del comando de IOS

Un comando puede tener uno o más argumentos. La sintaxis proporciona el patrón o el formato que se debe utilizar cuando se introduce un comando.

|Convención|Descripción|
|:---:|:---:|
|negrita|El texto en negrita indica los comandos y las palabras clave que ingresa literalmente como se muestra.|
|cursiva|El texto en cursiva indica los argumentos para los cuales el usuario proporciona el valor.|
|[x]|Los corchetes indican un elemento opcional (palabra clave o argumento).|
|{x}|Las llaves indican un elemento obligatorio (palabra clave o argumento).|
|[ x { y \| z }]|Las llaves y las líneas verticales entre corchetes indican que se requiere dentro de un elemento opcional. Los espacios se utilizan para delinear claramente partes del comando.|



Por ejemplo, la sintaxis para utilizar el **description** comando es **description** _string._ El argumento es un valor _string_ proporcionando por el usuario. **description** El comando se usa típicamente para identificar el propósito de una interfaz. Por ejemplo, al ingresar el comando, `switch(config-if)#  description Connects to the main headquarter office switch`, se describe dónde se encuantra el otro dispositivo al final de la conexión.

Los siguientes ejemplos muestran algunas convenciones utilizadas para registrar y usar comandos de IOS:

-   **ping** _ip-address_ - El comando es **ping** y el argumento definido por el usuario es el _ip-address_ del dispositivo de destino. Por ejemplo, **ping 10.10.5.2**.
-   **traceroute** _ip-address_ - El comando es **traceroute** y el argumento definido por el usuario es el _ip-address_ del dispositivo de destino. Por ejemplo, **traceroute 8.8.8.8**.

Si un comando es complejo con múltiples argumentos, puede verlo representado así:

```cisco
switch(config-if)# **switchport port-security aging** { **static** | **time** *time* | **type** { **absolute** | **inactivity**}}
```

# Ayuda sensible

La ayuda contextual proporciona al usuario una lista de comandos y argumentos asociados con dichos comandos en el modo actual de red, es decir, determina la mejor opción, palabra clave o argumento está disponible para el comando introducido y muestra una lista de los comando disponibles en el modo actual.