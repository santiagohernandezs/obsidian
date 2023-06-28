> Una clase sólo debe tener una razón para cambiar

Intenta hacer cada clase responsable de una única parte de la funcionalidad proporcionada por el software, y haz que esa responsabilidad quede totalmente encapsulada por la clase. 

La idea es reducir la complejidad. A medida que el programa crece las clases se vuelven tan grandes que ya no son tan fáciles de recordar sus detalles. La navegación por el código se ralentiza cada vez más y hay que recorrer clases enteras para encontrar algo específico. De hecho, si una clase hace demasiadas cosas al cambiar algo dentro de esta clase puede que las otras cosas cambie, haciendo que la tarea de hacer un mínimo cambio se convierte en hacer más de dos o tres, entorpeciendo el flujo de trabajo. 

## Ejemplo
La clase `Empleado` tiene varias razones para cambiar. La primera razón puede estar relacionada con eel trabajo principal de la clase: gestionar información de los empleados. Pero hay otra razón: el formato del informe de horas de trabajo puede cambiar con el tiempo, lo que te obliga a cambiar el código de la clase.

![](https://i.imgur.com/s0qIuQT.png)

Resuelve el problema moviendo el comportamiento relacionado con la impresión de informes de horas de trabajo a una clase separada. Estee cambio te permite mover otros elementos relacionados con el informe a la nueva clase.

![](https://i.imgur.com/oPxaclO.png)

