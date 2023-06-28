> Identifica los aspectos de tu aplicación que varían y se páralos de los que se mantienen inalterables.

El objetivo principal de este principio es minimizar el efecto provocado por los cambios.

Se trata de aislar las partes del programa que varían, en módulos independientes, protegiendo el resto del código frente a efectos adversos.

## Encapsulación a nivel de método
Digamos que estamos creando un e-commerce. En alguna parte del código se encuentra un método llamado `getOrderTotal()` que calcula el total del pedido, con impuestos incluidos.

Por ende, podemos anticipar que el código relacionado con los impuestos tendrá que cambiar a futuro, ya sea, por factores de ubicación geográfica, o factores legales. Esto hará que tengas que cambiar el método `getOrderTotal()` bastante a menudo. Pero incluso el nombre del método sugiere que no le importa cómo se calcula el impuesto.

```
method getOrderTotal(order) is
	total = 0
	foreach item in order.lineItems
		total += item.price * item.quantity

	if(order.country == "US")
		total += total * 0.07 // IVA de Estados Unidos
	else if (order.country == "UE")
		total += total * 0.20 // IVA de Europeo

	return total
```

Puedes extraer la lógica de cálculo del impuesto aun método separado, escondiéndolo del método original.
```
method getOrderTotal(order) is
	total = 0
	foreach item in order.lineItems
		total += item.price * item.quantity

	total += total * getTaxRate(order.country)

	return total

method getTaxRate(country) is 
	if(country == "US")
		return 0.07 // IVA de Estados Unidos
	else if (country == "UE")
		return 0.20 // IVA de Europeo
	else
		return 0
```

Los cambios relacionados con el impuesto quedan aislados dentro de un único método. Además, si la lógica de cálculo del impuesto se complica demasiado, ahora es más sencillo moverla a una clase separada.

## Encapsulación a nival de la clase.
Con el tiempo puedes añadir más y más responsabilidades a un método que solía hacer algo sencillo. Estos comportamientos añadidos suelen venir con sus precios campos y métodos de ayuda que acaban nublando la responsabilidad principal del la clase contenedora. Si se extrae todo a una nueva clase se puede conseguir mayor claridad y sencillez.

![](https://i.imgur.com/BlHwyIu.png)

Los objetos de la clase Pedido delegan todo el trabajo relacionado con el impuesto a un objeto especial dedicado justo a eso.

![](https://i.imgur.com/vPsndLY.png)

## Programa a una interfaz, no a una implementación

	Programa a una interfaz, no a una implementación. Depende de abstracciones, no de clases concretas.

Un `Gato` que puede comer cualquier comida es más flexible que uno que sólo puede comer salchichas. Al primer gato le puedes dar sal chichas porque éstas son un subgrupo de “cualquier comida”, pero puedes extender el menú de ese gato con cualquier otra comida.

Cuando quieres hacer que dos clases colaboren, puedes comenzar por hacer una dependiente de la otra. Caramba, yo mismo suelo empezar haciendo eso. Sin embargo, hay otra forma más flexible de establecer la colaboración entre objetos:

1. Determina lo que necesita exactamente un objeto del otro: ¿Qué métodos ejecuta?
2. Describe esos métodos en una nueva interfaz o clase abstracta.
3. Haz que la clase que es una dependencia implemente esta interfaz.
4. Ahora, haz la segunda clase dependiente de esta interfaz en lugar de la clase concreta. Todavía puedes hacerlo funcionar con objetos de la clase original, pero ahora la conexión es mucho más flexible.

![](https://i.imgur.com/N0vIHTy.png)

Tras hacer este cambio, probablemente no notarás un beneficio inmediato. Por el contrario, el código se ha vuelto más complicado de lo que era antes. No obstante, si consideras que éste puede ser un buen punto de extensión para alguna funcionalidad adicional, o que otras personas que utilizan tu código pueden desear extenderlo aquí, entonces adelante con ello.

