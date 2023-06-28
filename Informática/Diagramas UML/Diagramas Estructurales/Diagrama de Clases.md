Este diagrama, el más común en el desarrollo de software, se usa para representar el diseño lógico y físico de un sistema, y muestra sus clases. Este diagrama ofrece una imagen de las diferentes clases y la forma en la que se interrelacionan, y cada clase posee tres compartimientos:
- Sección superior: Nombre de la clase.
- Sección central: Atributos de la clase.
- Sección inferior: Métodos u operaciones de la clase.
![](https://i.imgur.com/eVUu6Fm.png)

Cada uno de los atributos y métodos tienen a su lado el tipo de valor que poseen retornan.

Si el nombre de la clase está en itálica significa que es una clase abstracta.
## Políticas
Dentro de la clase podemos especificar cuales serán las políticas de acceso a las propiedades y métodos lo que en OOP se conoce como ***encapsulamiento***, la notación es la siguiente:

|Símbolo|Valor|
|:--:|:--:|
|+|Public|
|-|Private|
|#|Protected|
|~|Package Local|
![](https://i.imgur.com/6ulBuB6.png)

## Relaciones entre Clases
Las clases pueden tener algo en común o interacción entre ellas. Para ello, se usan los siguiente símbolos:
![](https://i.imgur.com/XE9IrgM.png)
### Asociación
Sirve para asociar dos clases, si tenemos dos clases que interactúan una con la otra se produce una asociación. También se puede especificar la cantidad de objetos que forman parte de la relación y estas son:
- Relaciones Uno a Uno (1)
- Relaciones Uno a Muchos (1..\*)
- Relaciones Muchos a Muchos (\*)
### Herencia
Sirve para indicar la línea de herencia de las clases partiendo desde el hijo apuntando hacia su padre.
![](https://i.imgur.com/DrrKL22.png)
### Realization
Lo normal es que se utiliza para definir las relación que existe entre un objeto y una interfaz de manera que se pueda ver cuales de ellos son los que las implementan.
![](https://i.imgur.com/DWCstAI.png)
### Dependencia
Rara, pero también usada. Sirve cuando un objeto usa valores en las que ninguno de sus campos tiene. De hecho, son valores pertenecientes a otras clases por lo que **dependen** de otras clases para funcionar.
![](https://i.imgur.com/Lo9hmDD.png)
### Agregación
Una relación que funciona cuando una clase cobra sentido agregando otras clases dentro de ella. Por ejemplo, la estación de trabajo (workspace) de un programador está compuesta por una silla, un escritorio, y una computadora. Haciendo una agregación de estas clases podemos hacer la clase estación de trabajo, de manera que si esta última es eliminada seguiremos teniendo las mismas clases que las contenían.
![](https://i.imgur.com/kHhTpze.png)
### Composición
Es bastante parecido a la agregación solo que en este tipo de relación las clases que conforman la clase "agregadora" son destruidas cuando la clase "agregadora" es detruida, cosa que no pasa en la agregación.
![](https://i.imgur.com/R1lxtYt.png)
