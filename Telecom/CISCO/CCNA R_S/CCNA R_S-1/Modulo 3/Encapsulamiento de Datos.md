# Segmentación del mensaje

Un método que consta en dividir los datos en parte más pequeñas y manejables para enviarlas por la red. La división del stream de datos en partes más pequeñas se denomina segmentación. La segmentación de mensaje tiene dos beneficios principales:

-   **Aumenta la velocidad** - Debido a que un flujo de datos grande en paqutes, se pueden enviar grandes cantidades de datos a través de la red sin atar un elnace de comunicaciones, al enviar partes individuales más pequeñas del origen al destino, se pueden intercalar muchas conversaciones diversas en la red. El proceso que se utiliza para intercalar las piezas de conversaciones en la red se denomina multiplexación.
-   La segmentación puede aumentar la confiabilidad de las comunicaciones de red. No es necesario que las partes separadas de cada mensaje sigan el mismo recorrido a través de la red desde el origen hasta el destino. En tal caso de que una ruta falle el mensaje puede redirecionarce y llegar a su host. Si un solo segmento no llega a su destino debido a una falla en la red o congestión de la red, solo ese segmento necesita ser retransmitido en lugar de volver a enviar toda la secuencia de datos.

# Secuenciación

Es la identificación de cada segmento (con un número de secuencia) el cual respeta un órden para que al momento de la multiplexación de los paquetes, estos lleguen al receptor y pueda reezamblarlos en el orden adecuado. TCP es responsable de secuanciar los segmentos individuales.

# Protocol Datagram Unit (PDU)

Es la manera que adopta una porción de datos en cualquier capa de unidad de protocolo

-   **Datos**: Término general que se utiliza en la capa de aplicación para la PDU.
-   **Segmento**: PDU de la capa de trasporte.
-   **Paquete**: PDU de la capa de red.
-   **Trama**: PDU de la capa de enlace de datos.
-   **Bits**: PDU de capa física que se utiliza cuando se transmiten datos físicamente por el medio.

**Nota**: Si el encabezado de transporte es TCP, entonces es un segmento. Si el encabezado de transporte es UDP, esntonces es un datagrama.