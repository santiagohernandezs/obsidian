Los switches utilizan uno de los siguientes métodos de reenvío para el switching de datos entre puertos de la red:

-   **Switching de almacenamiento y envío**: Este método de reenvío de trama recibe [[La Trama]] completa y calcula el CRC. Si la CRC es válida, el switch busca la dirección de destino, que determinala interfaz de salida . Luego la trama se reenvía al puerto correcto.
-   **Switching por método de corte**: Este método de reenvío de tramas reenvía la trama antes de que se reciba por completo. Como mínimo debe leer la dirección de destino para que la trama se pueda enviar.

Una gran ventaja del store-and-forward (almacenamiento y reenvío), es que determina si la trama tiene errores antes de reenviarla. Cuando se detecta un errore en la trama, el switch la descarta. El proceso de descarte de las tramas con errores reduce el ancho de banda consumido por datos dañados: Store-and-forwarding se requiere para que el análisis de calida de servicio (QoS) en las redes convergentes, donde se necesita una clasificación de la trama para predecir el orden de prioridad del tráfico.

# Switching por método de corte

En este tipo de switching, el switch actúa sobre los datos apenas los recibe, incluso si la transmición no se complet. El switch almacena la cantidad suficiente de trama como para leer la dirección MAC de destino para que pueda determinar a qué puerto debe reenviar los datos. La dirección MAC de destino se encuentra en los primeros 6 bytes de la trama después del preámbulo. El switch busca la dirección MAC de destino en la tabla de switching, determina el puerto de la interfaz de salida y reenvía la trama a su destino mediante el puerto de switch designado. El switch no lleva a cabo ninguna verificación de errores en la trama.

## Variantes del método cut-through switching

-   **Switching de reenvío rápido** - Este método ofrece el nivel de latrencia más bajo. **Fast-Forward switching** reenvía el paquete inmdeiata emnte después de leer la dirección, es posible que la trama contenga errores. El fat-forwar-switching es el método de corte más típico.
-   **Switching libre de fragmentos** - En este método, el switch almacena los pimeros 64 bytes de la trama antes de reenviarla, ya que, la mayoría de los errores y colisiones de red se producen en los primeros 64 bytes de la trama. Es un punto medio entre alta latencia y alata integridad. El **fragment-free switching** se puede ver como un punto medio entre el **store-and-forward switching** y el **fast-forward switching**.