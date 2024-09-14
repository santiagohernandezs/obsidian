# Direcciones binarias e IPv4

Las direcciones IPv4 comienzan como binarias, una serie de solo 1 y 0. Estos son difíciles de adminsitrar, por lo que los administradores de red deben convertirlos a decimales.

Binario es un sistema de numeración que consta de 0 y 1 llamados bits. En constraste, el sistema de numeración decimal consta de 10 dígitos desde el 0 al 9.

Es importante que comprender el sistema binario, ya que los hosts, los servidores y los dispositivos de red usan el direccionamiento binario. Específicamente, usan el direccionamiento binario. Específicamente, usan direcciones IPv4 binarias, com se muetra en la figura, para identificarse entre sí.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Direcciones-binarias-e-IPv4.png)

Cada dirección consta de una cadena de 32 bits dividos en cautro secciones denominadas octetos. Cada octeto contiene 8 bits (o 1 byte) separados por un punto. Por ejemplo la PC1 de la ilustración se le asignó la dirección IPv4 11000000.10101000.00001010.00001010. La dirección de gateway predeterminado sería de la interfaz Gigabit Ethernet del R1, 11000000.10101000.00001010.00000001.

Binario funciona bien con host y dispositivos de red. Sin embargo, es muy difícil para los humanos trabajar con ellos.

Para facilitar el uso por parte de las personas, las direcciones IPv4 se expresan conmúnmente en noteción decimal punteada. A la PC1 se le asigna la dirección IPv4 192.168.10.10, y su gateway predeterminado es 192.168.10.1, como se muestra en la figura.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Direcciones-decimales-en-IPv4.png)

---

# Conversión entre sistemas de numeración binarios y decimales.


**Nota: Siempre debemos tomar en cuenta lo siguiente:**

-   Las direcciones IPv4 están formadas por 32 bit, cada uno separados en cuatro grupos de 8 bits cada uno.
-   8 bits es iguala 1 byte, por lo que una IPv4 es de 32 bits o 4 bytes.
-   Las direcciones IPv4 son utilizan el sistema binarrio y son representadas con el sistema decimal para un uso más fácil.

---

# Notación de posición binaria

Para aprender a convertir de sistema binario a decimal, es necesario entender la notación de posición. El término "notación de posición" significa que un dígito representa diferentes valores según la "posición" que el dígito ocupa en la secuencia de números. Ya conoce el sistema de numeración más común, el sistema de notación decimal (de base 10).

El sistema de notación posicional decimal funciona como se describe en la tabla.



Las viñetas siguientes describen cada fila de la tabla.

-   Fila 1, Radix es la base numérica. La notación decimal se basa en 10, por lo tanto, la raíz es 10.
    
-   Fila 2, Posición en número considera la posición del número decimal que comienza con, de derecha a izquierda, 0 (1ª posición), 1 (2ª posición), 2 (3ª posición), 3 (4ª posición). Estos números también representan el valor exponencial utilizado para calcular el valor posicional en la cuarta fila.
    
-   Fila 3 calcula el valor posicional tomando la raíz y elevándola por el valor exponencial de su posición en la fila 2.**Nota:** n es = 1.
    
    0
    
-   El valor posicional de la fila 4 representa unidades de miles, cientos, decenas y unos.
    

Para usar el sistema de posición, una un número dado con su valor de posición. El ejemplo en la tabla ilustra cómo se usa la notación posicional con el número decimal 1234.



En contraste, la notación posicional binaria opera como se describe en la tabla.



Las viñetas siguientes describen cada fila de la tabla.

-   Fila 1, Radix es la base numérica. La notación binaria se basa en 2, por lo tanto, el radix es 2.
    
-   Fila 2, Posición en número considera la posición del número binario que comienza con, de derecha a izquierda, 0 (1ª posición), 1 (2ª posición), 2 (3ª posición), 3 (4ª posición). Estos números también representan el valor exponencial utilizado para calcular el valor posicional en la cuarta fila.
    
-   Fila 3 calcula el valor posicional tomando la raíz y elevándola por el valor exponencial de su posición en la fila 2.**Nota:** n es = 1.
    
    0
    
-   El valor posicional de la fila 4 representa unidades de uno, dos, cuatro, ocho, etc.
    

El ejemplo en la tabla ilustra cómo un número binario 11000000 corresponde al número 192. Si el número binario fuera 10101000, el número decimal correspondiente sería 168.



---

# Convertir binario a decimal

Para convertir una dirección IPv4 binaria a su equivalente decimal punteada, divida la dirección IPv4 en cuatro octetos de 8 bits. A continuación, aplique el valor de posición binario al primer octeto del número binario y calcule según corresponda.

Por ejemplo, suponga que 11000000.10101000.00001011.00001010 es la dirección IPv4 binaria de un host. Para convertir la dirección binaria a decimal, comience con el primer octeto, como se muestra en la tabla. Introduzca el número binario de 8 bits en el valor de posición de la fila 1 y, después, calcule para producir el número decimal 192. Este número entra en el primer octeto de la notación decimal punteada.



A continuación, convertir el segundo octeto de 10101000 como se muestra en la tabla. El valor decimal resultante es 168 y entra en el segundo octeto.



Convertir el tercer octeto de 00001011 como se muestra en la tabla.



Convertir el cuarto octeto de 00001010 como se muestra en la tabla. Esto completa la dirección IP y produce 192.168.11.10.



---

# Conversión de sistema decimal a binario

También es necesario comprender cómo convertir una dirección IPv4 decimal punteada a una binaria. La tabla de valores de posición binarios es una herramienta útil.

## 128

¿Es el número decimal del octeto (n) igual o mayor que el bit más significativo (**128**)?

-   Si no es, introduzca el binario **0** en el valor posicional **128**.
-   Si es, agregue un binario **1** en el valor posicional **128** y reste **128** del numero decimal.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Conversi%C3%B3n-Decimal-a-Binaria-128.png)

## 64

¿Es el número decimal del octeto (n) igual o mayor que el siguiente bit más significativo (**64**)?

-   Si no es, introduzca el binario **0** en el valor posicional **64**.
-   Si es, agregue un binario **1** en el valor posicional **64** y reste **64** del numero decimal.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Conversi%C3%B3n-Decimal-a-Binaria-64.png)

## 32

¿Es el número decimal del octeto (n) igual o mayor que el siguiente bit más significativo (**32**)?

-   Si no es, introduzca el binario **0** en el valor posicional **32**.
-   Si es, agregue un binario **1** en el valor posicional **32** y reste **32** del numero decimal.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Conversi%C3%B3n-Decimal-a-Binaria-32.png)

## 16

¿Es el número decimal del octeto (n) igual o mayor que el siguiente bit más significativo (**16**)?

-   Si no es, introduzca el binario **0** en el valor posicional **16**.
-   Si es, agregue un binario **1** en el valor posicional **16** y reste **16** del numero decimal.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Conversi%C3%B3n-Decimal-a-Binaria-16.png)

## 8

¿Es el número decimal del octeto (n) igual o mayor que el siguiente bit más significativo (**8**)?

-   Si no es, introduzca el binario **0** en el valor posicional **8**.
-   Si es, agregue un binario **1** en el valor posicional **8** y reste **8** del numero decimal.

~[](https://ccnadesdecero.es/wp-content/uploads/2020/03/Conversi%C3%B3n-Decimal-a-Binaria-8.png)

## 4

¿Es el número decimal del octeto (n) igual o mayor que el siguiente bit más significativo (**4**)?

-   Si no es, introduzca el binario **0** en el valor posicional **4**.
-   Si es, agregue un binario **1** en el valor posicional **4** y reste **4** del numero decimal.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Conversi%C3%B3n-Decimal-a-Binaria-4.png)

## 2

¿Es el número decimal del octeto (n) igual o mayor que el siguiente bit más significativo (**2**)?

-   Si no es, introduzca el binario **0** en el valor posicional **2**.
-   Si es, agregue un binario **1** en el valor posicional **2** y reste **2** del numero decimal.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Conversi%C3%B3n-Decimal-a-Binaria-2.png)

# 1

¿Es el número decimal del octeto (n) igual o mayor que el último bit más significativo (**1**)?

-   Si no es, introduzca el binario **0** en el valor posicional **1**.
-   Si es, agregue un binario **1** en el valor posicional **1** y reste **1** del numero decimal.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Conversi%C3%B3n-Decimal-a-Binaria-1.png)

---

# Ejemplo de conversión de sistema decimal a binario

Para poder comprender el proceso, considere la dirección IP 192.168.11.10.

El primer octeto número 192 se convierte a binario utilizando el proceso de notación posicional explicado anteriormente.

Es posible omitir el proceso de resta con números decimales menores o más pequeños. Por ejemplo, observe que es bastante fácil calcular el tercer octeto convertido a un número binario sin pasar realmente por el proceso de resta (8 + 2 = 10). El valor binario del tercer octeto es 00001010.

El cuarto octeto es 11 (8 + 2 + 1). El valor binario del cuarto octeto es 00001011.

La conversión de sistema binario a decimal puede parecer un desafío inicialmente, pero con la práctica resulta más fácil.

# Paso 1

11

¿El primer octeto número 192 es igual o mayor que el bit de orden alto 128?

-   Sí es, por lo tanto, añadir un 1 al valor posicional de orden alto a un representar 128.
-   Resta 128 de 192 para producir un resto de 64.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Decimal-a-Binario-Paso-1.png)

## Paso 2

¿El resto 64 es igual o mayor que el siguiente bit de orden alto 64?

-   Es igual, por lo tanto, agregue un 1 al siguiente valor posicional de alto orden.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Decimal-a-Binario-Paso-2.png)

## Paso 3

Dado que no hay resto, introduzca binario **0** en los valores posicionales restantes.

-   El valor binario del primero octeto es **11000000**.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Decimal-a-Binario-Paso-3.png)

## Paso 4

¿El segundo número de octetos es **168** igual o mayor que el bit de orden alto **128**?

-   Si, esto es cierto, por lo tanto agregue un **1** al valor posicional de alto orden para representar **128**.
-   Reste **128** de **168** para producir un resto de **40**.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Decimal-a-Binario-Paso-4.png)

## Paso 5

¿El resto es **40** igual o mayor que el siguiente bit de orden alto **64**?

-   No, no lo es, por lo tanto, ingrese un **0** binario en el valor posicional 64.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Decimal-a-Binario-Paso-5.png)

## Paso 6

¿El resto es **40** igual o mayor que el siguiente bit de orden alto **32**?

-   Si, esto es cierto, por lo tanto agregue un **1** al valor posicional de alto orden para representar **32**.
-   Reste **32** de 40 para producir un resto de **8**.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Decimal-a-Binario-Paso-6.png)

## Paso 7

¿El resto es **8** igual o mayor que el siguiente bit de orden alto **16**?

-   No, no lo es, por lo tanto, introduzca un 0 binario en el valor posicional.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Decimal-a-Binario-Paso-7.png)

## Paso 8

¿El resto es **8** igual o mayor que el siguiente bit de orden alto **8**?

-   Si, esto es cierto, por lo tanto agregue un **1**.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Decimal-a-Binario-Paso-8.png)

## Paso 9

Dado que no hay resto, introduzca binario **0** en los valores posicionales restantes.

-   El valor binario del segundo octeto es **10101000**.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Decimal-a-Binario-Paso-9.png)

## Paso 10

El valor binario del tercer octeto es.00001010

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Decimal-a-Binario-Paso-10.png)

## Paso 11

El valor binario del cuarto octeto es. 00001011

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Decimal-a-Binario-Paso-11.png)

---

# Direcciones IPv4

Como se mencionó antes, las computadoras y los routers solo entienden binario, mientras que los humanos trabajan en decimal. Es importante conocer a fondo estos dos sistemas de numeración y cómo se utilizan en redes.

## Dirección en formato decimal punteado

192.168.10.10 es una dirección IP asignada a una computadora.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Formato-decimal-punteado.png)

## Octetos

La dirección se compone de cuatro octetos diferentes.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Ejemplo-Direcci%C3%B3n-IPv4-Decimal-y-Binario.png)

## Dirección de 32 bits

La computadora almacena la dirección como el flujo de datos total de 32 bits.

![](https://ccnadesdecero.es/wp-content/uploads/2020/03/Direcci%C3%B3n-IP-formato-32-bits.png)