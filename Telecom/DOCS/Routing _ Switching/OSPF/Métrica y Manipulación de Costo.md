OSPF utiliza el Ancho de banda (Bandwith, BW) como métrica para la toma de decisiones. Como referencia OSPF usa un BW de 100 Mbps para el cálculo del costo.

La formula para el cálculo del costo es el BW de referencia divido entre el BW de la interfaz

$$Costo = \frac{refBw}{intBw} = \frac{100 Mbps}{x}$$

Siempre y cuando el BW sea mayor a 100 Mbps el costo será de 1. Esto puede llegar a ser un incoveniente ya que al tener dos caminos uno con cableado Ethernet y otro con fibra óptica el algoritmo SPF no va a distinguir cual es la conexión con fibra y cual es la de ethernet, algo que puede ser molesto si queremos que el tráfico vaya por el cableado ethernet o lo contrario. Para ello alteraremos los costos, haciendo que la métrica sea más alta y con esto el algoritmo descartará la ruta a la cual le hemos subido el costo. Se realiza entrando en la interfaz y ejecutando el siguiente comando.

```
ip ospf cost x
```

Donde x es el numero de costo que quermos aplicar.

## Consideraciones
Cuando en nuestra red tenemos interfaces con una capacidad mayor a 100 Mbps puede traernos proeblemas si utilizamos 100 Mbps como BW de referencia. Por lo que, debemos cambiarlo simpre una clasificación más arriba de la mayor que se encuentre en la red. Para cmabiar el BW de referencia hacemos lo siguiente.

```
router ospf 1
	auto-cost reference-bandwith x
```

Donde x será el BW (expresado en Mbits por segundo)que queremos establecer como referencia.

**Nota**: Esta configuración se debe realizar en todos los routers dentro del mismo AS.