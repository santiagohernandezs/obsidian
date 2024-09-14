# Fundamentos de la comunicación

Dado que una red puede tener diversas formas, tamaños y funciones; es necesario tener en cuenta que deben existir ciertos métodos de comunicación, así como nosotros los humanos tenemos métodos para intercambiar información y lograr una comunicación.

Todos los métodos de comunicación tienen tres elementos en común:

-   **Los orígenes de los mensajes** - Los orígenes de los mensajes son las personas o los dispositivos electrónicos que deben enviar un mensaje a otras personas o dispositivos.
-   **Destino del mensaje(receptor)** - El destino recibe el mensaje y lo interpreta.
-   **Canal** - Está formado por los medios que proporcionan el camino por el que el mensaje viaja desde el origne hasta el destino.

# Protocolos de enrutmaiento.

Para poder comunicarnos con alguien ya sea cara a cara o a través de una red, necesitamos unas reglas (protocolos) por las cuales regirnos, especificando el método de comunicación en cuestión.

# Establecimiento de reglas

Antes de comunicarse entre sí, las personas deben utilizar reglas o acuerdos establecidos que rijan la conversación. Considere este mensaje, por ejemplo:

```plaintext
Humanos comunicaciones las entre los gobiernan reglas. Es muydifícilcomprender mensajes que no están correctamente formateados y quenosiguen las reglas y los protocolos establecidos. La estructura de la gramática, el lenguaje, la puntuación y la oración hace que la configuración humana sea comprensible para muchos individuos diferentes.
```

Observe cómo es difícil leer el mensaje porque no está formateado correctamente. Debe escribirse usando reglas (es decir, protocolos) que son necesarias para una comunicación efectiva. El ejemplo muestra el mensaje que ahora está correctamente formateado para el lenguaje y la gramática.

```plaintext
Las reglas gobiernan las comunicaciones entre los humanos. Es muy difícil comprender mensajes que no están correctamente formateados y que no siguen las reglas y los protocolos establecidos. La estructura de la gramática, el idioma, la puntuación y la oración hacen que la configuración sea humanamente comprensible para muchos individuos diferentes
```

Los protocolos deben tener en cuenta los siguientes requisitos para entregar correctamente un mensaje que sea comprendido por el receptor:

-   Un emisor y un receptor identificados.
-   Idioma y gramática común.
-   Velocidad y momento de entrega.
-   Requisitos de confirmación o acuse de recibo.

# Requisitos de protocolo de red.

Además de compartir muchos de estos fundamentos, los protocolos de red incluyen los siguientes requisitos:

-   Codificación de los mensajes.
-   Formato y encapsulamiento del mensaje.
-   Tamaño del mensaje.
-   Sincronización del mensaje.
-   Opciones de entreda del mensaje.

# Codificación del mensaje.

Uno de los primeros pasos para enviar un mensaje es codificarlo. La codificación es el proceso mediante el cual la información se convierte en otra forma aceptable para la transmisión. La decodificación revierte este proceso para interpretar la idea.

La codificación entre hosts debe tener el formato adecuado para el medio. El host emisor, primero convierte en bits los mensajes enviados a través de la red. Cada bit está codificado en un patrón de voltajes en cables de cobre, luz infrarroja en fibras ópticas o microondas para sistemas inalámbricos. El host de destino recibe y decodifica las señales para interpretar el mensaje.

# Formato y encapsulamieto del mensaje.

Cuando se envía un mensaje desde el origen hacia el destino, se debe utilizar un formato o estructura específicos. Los formatos de los mensajes dependen del tipo de mensaje y el canal que se utilice para entregar el mensaje.

**Analogía**

Un ejemplo común de requerir el formato correcto en las comunicaciones humanas es cuando se envía una carta. Haga clic en Reproducir en la figura para ver una animación de formato y encapsulación de una letra.

El sobre tiene la dirección del emisor y la del receptor, cada una escrita en el lugar adecuado del sobre. Si la dirección de destino y el formato no son correctos, la carta no se entrega.

El proceso que consiste en colocar un formato de mensaje (la carta) dentro de otro formato de mensaje (el sobre) se denomina encapsulamiento. La desencapsulación ocurre cuando el destinatario invierte el proceso y la carta se saca del sobre.

![](https://ccnadesdecero.es/wp-content/uploads/2020/07/Demo-Formato-de-Mensaje.gif)

**Red**

Semejante a enviar una carta,Un mensaje que se envía a través de una red de computadoras sigue reglas de formato específicas para que pueda ser entregado y procesado.

Protocolo de Internet (IP) es un protocolo con una función similar a la del ejemplo sobre. En la figura, los campos del paquete de Protocolo de Internet versión 6 (IPv6) identifican el origen del paquete y su destino. IP es responsable de enviar un mensaje desde el origen del mensaje al destino a través de una o más redes.

![](https://ccnadesdecero.es/wp-content/uploads/2020/07/Encapsulaci%C3%B3n-Mensaje-Red.png)

# Tamaño del mensaje

### Analogía

Cuando las personas se comunican, los mensajes que envían, normalmente, están divididos en fragmentos más pequeños u oraciones. El tamaño de estas oraciones se limita a lo que la persona que recibe el mensaje puede procesar por vez, como se muestra en la figura. También hace que sea más fácil para el receptor leer y comprender.

### Red

De manera similar, cuando se envía un mensaje largo de un host a otro a través de una red, es necesario separarlo en partes más pequeñas. Las reglas que controlan el tamaño de las partes, o tramas que se comunican a través de la red, son muy estrictas. También pueden ser diferentes, de acuerdo con el canal utilizado. Las tramas que son demasiado largas o demasiado cortas no se entregan.

Las restricciones de tamaño de las tramas requieren que el host de origen divida un mensaje largo en fragmentos individuales que cumplan los requisitos de tamaño mínimo y máximo. El mensaje largo se enviará en tramas independientes, cada trama contendrá una parte del mensaje original. Cada trama también tendrá su propia información de direccionamiento. En el host receptor, las partes individuales del mensaje se vuelven a unir para reconstruir el mensaje original.

# Sincronización del mensaje

El tiempo de los mensajes también es muy importante en las comunicaciones de red. El tiempo de los mesajes incluyen lo siguiente:

-   **Control de flujo** - Este es el proceso de gestión de la velocidad de transmisión de datos. La sincronización también afecta la cantidad de información que se puede enviar y la velocidad con la que puede entregarse. Por ejemplo, Si una persona habla demasiado rápido, la otra persona tendrá dificultades para escuchar y comprender el mensaje. En la comunicación de red, existen protocolos de red utilizados por los dispositivos de origen y destino para negociar y administrar el flujo de información.
-   **Tiempo de espera de repsueta (Response Timeout)** - Si una persona hace una pregunta y no escucha una respuesta antes de un tiempo aceptable, la persona supone que no habrá ninguna respuesta y reacciona en consecuencia. La persona puede repetir la pregunta o puede continuar la conversación. Los hosts de las redes tienen reglas que especifican cuánto tiempo deben esperar una respuesta y qué deben hacer si se agota el tiempo de espera para la respuesta.
-   **El método de acceso** - Determina en qué momento alguien puede enviar un mensaje. Al dos personas hablando al mismo tiempo, se produce una "colisión de información" y es necesario que las dos retrocedan y comiencen de nuevo. Del mismo modo, cuando un dispositivo desea transmitir en una LAN inalámbrica, es necesario que la tarjeta de interfaz de red (NIC) WLAN determine si el medio inalámbrico está disponible.

# Opciones de entrega del mensaje.

Un mensaje se puede entregar de diferentes maneras.

### Analogía

En algunos casos, una persona desea comunicar información a un solo individuo. Otras veces, esa persona puede necesitar enviar información a un grupo de personas simultáneamente o, incluso, a todas las personas de un área.

### Red

Las comunicaciones de red tienen opciones de entrega similares para comunicarse. Como se muestra en la figura, hay tres tipos de comunicaciones de datos:

-   **Unicast** - La informcaión se transmiten a un único dsipositivo final.
-   **Multicast** -La información se trasnmite a uno o varios dsipositivos finales.
-   **Transmisión** - La información se transmite a todos los dispositivos finales.