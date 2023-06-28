## Conceptos Básicos de POO
La programación orientada a objetos (POO) es un paradigma basado en el concepto de envolver bloques de información en "lotes" llamados **[[Objetos]]**, en estos lotes se almacena todas sus características y comportamiento. Estos objetos se construyen a partir de un grupo de "planos" definidos por el programador, que son denominados **clases**.

### Objetos, clases
Las clases son lo que denotamos como planos, por ende las clases crean un especie de molde o modelo que reúne una cantidad finita de elementos y que definen tanto las características y el comportamiento de un objeto, objeto que será producto de la clase. Por ejemplo si queremos usar un plano para que en nuestro programa se creen gatos haríamos una clase "Gato" bastante similar a la siguiente.

![](https://i.imgur.com/vvjkYC0.png)

Cada gato tiene varios atributos estándar: nombre, sexo, edad, peso, color, comida favorita, etc. Estos son los *campos* de la clase. Además, todos los gatos se comportan de forma similar: respiran, comen, corren, duermen y maúllan. Estos son los métodos de la clase. Colectivamente, podemos referirnos a los campos y los métodos como los *miembros* de su clase. La información almacenada dentro de los campos del objeto suele denominarse *estado*, y todos los métodos del objeto definen su *comportamiento*.

![](https://i.imgur.com/2KmxQfH.png)

## Jerarquías de clase
Es muy habitual que un programa real contenga más de una clase y es por ello, que algunas de estas clases pueden estar organizadas en **jerarquías de clase**. Esta es **La relación que existe entre superclases y subclases**. Dichas relaciones pueden basarse en la herencia de métodos y campos e incluso en la modificación de alguno de esos métodos.

Digamos que tu vecino tiene un perro llamado Fido. Resulta que perros y gatos tienen mucho en común: nombre, sexo, edad y color, son atributos tanto de perros como de gatos. Los perros pueden respirar, dormir y correr igual que los gatos, por lo que podemos definir la clase base `Animal` que enumerará los atributos y comportamientos comunes.

![](https://i.imgur.com/HY1XNGv.png)

Una clase padre, como la que acabamos de definir, se denomina **superclase**. Sus hijas son las subclases. Las subclases heredan el estado y el comportamiento de su padre y se limitan a definir atributos o comportamientos diferentes. Por lo tanto la clase `Gato` contendrá el método `maullar()` y la clase `Perro`, el método `ladrar()`. Las subclases pueden sobrescribir el comportamiento de los métodos que heredan de clases padre. Una subclase puede sustituir completamente el comportamiento por defecto o limitarse a mejorarlo con material adicional.

## Los pilares de la POO
La programación orientada a objetos se basa en cuatro pi lares, conceptos que la diferencian de otros paradigmas de programación.
- [[Abstracción]]
- [[Polimorfismo]] 
- [[Encapsulación]] 
- [[Herencia]] 