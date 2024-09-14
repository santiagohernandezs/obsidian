En el cálculo diferencial y análisis matemático, la derivada de una función es la razón de cambio instantánea con la que varía el valor de dicha función matemática, según se modifique el valor de su variable independiente.

![Imgur|450](https://imgur.com/tWXLvwD.png)

Un ejemplo de uso de las derivadas aparece al estudiar el movimiento: Si una función representa la posición de un objeto respecto al tiempo, su derivada es la velocidad de dicho objeto para todos los momentos. Se interpreta geométricamente como la pendiente de una recta tangente a la gráfica de la función en un dicho punto.

Es uno de los conceptos más básicos en el análisis matemático además de las integrales definidas e indefinidas, las sucesiones e incluso, el concepto de límite. La derivada es un concepto que tiene variadas aplicaciones. Se aplica en aquellos casos donde es necesario medir la rapidez con que se produce el cambio de una magnitud o situación.

![](https://imgur.com/uFqB1vu.gif)

## Derivada de una función

Dada una función $f$, se puede definir una nueva función que, en cada punto $x$, toma el valor de la derivada $f'(x)$. Esta función se denota $f'$ y se denomina función derivada de $f$ o simplemente derivada de $f$. Esto es, derivada de $f$ es la función dada por:
$$f'(x)=\lim_{h \to 0}\frac{f(x+h)-f(x)}{h}$$
Esta función sólo está definida en los puntos del dominio de $f$ donde el límite existe; en otras palabras, el dominio de $f'$ está contenido en el de $f$.
### Ejemplos
Considere la función cuadrática $f(x)=x^2$ definida para todo $x\in \mathbb{R}$. Se trata de calcular la derivada de esta función aplicando la definición.
$$

\begin{align}
f'(x)&=\lim_{h \to 0}\frac{(x+h)^2-x^2}{h}\\
&=\lim_{h \to 0}\frac{x^2+2xh+h^2-x^2}{h}\\
&=\lim_{h \to 0}\frac{2xh+h^2}{h}\\
&=\lim_{h \to 0}(2xh+h)\\
&=2x
\end{align}
$$
Para el caso general $g'(x)=\lim_{h\to0}\frac{(x+h)^n-x^n}{h}$.
Teniendo entendido el teorema del binomio:
$$
(x+h)^n=\sum_{k=0}^{n}=
\left(\frac{n}{0}\right)x^n +
\left(\frac{n}{1}\right)x^{n-1}h +
\left(\frac{n}{2}\right)x^{n-2}h^2 +
\dots +
\left(\frac{n}{n-1}\right)xh^{n-1} +
\left(\frac{n}{n}\right)h^n

$$
Tenemos;
$$
\begin{align}
g'(x)&=\lim_{h \to 0} \frac{
\left(\frac{n}{0}\right)x^n +
\left(\frac{n}{1}\right)x^{n-1}h +
\left(\frac{n}{2}\right)x^{n-2}h^2 +
\dots +
\left(\frac{n}{n-1}\right)xh^{n-1} +
\left(\frac{n}{n}\right)h^n -
x^n
}{
h
}\\
&=\lim_{h \to 0} \frac{
x^n+nx^{n-1}h+\frac{n(n-1)}{2}x^{n-2}h^2+\dots+nxh^{n-1}+h^n-x^n \\
}{
h
}\\
&=\lim_{h \to 0} \frac{
x^n+h(nx^{x-1}+\frac{n(n-1)}{2}x^{n-2}+\dots+nxh^{n-2}+h^{n-1})-x^n
}{
h
}
\\
&=\lim_{h \to 0}nx^{n-1}+\frac{n(n-1)}{2}x^{n-2}h+\dots+nxh^{n-2}+h^{n-1}=nx^{n-1}
\end{align}
$$
# Continuidad y diferenciabilidad 
## La continuidad es necesaria
Para que una función sea derivable en un punto es necesario que también sea continua en ese punto: Intuitivamente, si la gráfica de una función está rota en un punto, no hay una manera clara de trazar una recta tangente a la gráfica. Más precisamente, esto se debe a que, si una función $f$ no es continua en un punto $a$ , entonces la diferencia entre el valor $f(a)$ y el valor en un punto cercano $f(a+h)$ no va a tender a 0 a medida que la distancia $h$ entre los dos puntos tiende a 0; de hecho, el límite $\lim_{h\to0}f(a+h)-f(a)$ no tiene por qué estar bien definido si los dos límites laterales no son iguales. Tanto si este límite no existe como si existe pero es distinto de 0, el cociente diferencial $\frac{f(a+h) - f(a)}{h}$ no tendrá un límite definido.

Como ejemplo, lo que ocurre cuando una función no es continua, se puede considerar la función de Heaviside, definida como:
$$
f(x) =
\begin{cases}
1, & \text{if $x \ge 0$} \\
0, & \text{if $x \lt 0$}
\end{cases}
$$
Esta función no es continua en $x=0$, el valor del función en este punto es 1, pero todos puntos a su izquierda de la función vale 0.

![](https://imgur.com/xMw3aM5.png)
## La continuidad no es suficiente

**La relación no funciona a la inversa**, el que una función sea continua no garantiza su derivabilidad. Es posible que los límites laterales sean iguales pero las derivadas laterales no; en este caso concreto la función presenta un punto anguloso en dicho punto.
Un ejemplo es la función valor absoluto $f(x)=|x|$
$$
|x| =
\begin{cases}
x, & \text{if $x \ge 0$} \\
-x, & \text{if $x \lt 0$}
\end{cases}
$$
Esta función es continua en el punto $x=0$: en este punto la función toma el valor 0, y para valor 0, y para valores de $x$ infinitamente cercanos.
# Notaciones
Existen distintas formas de nombrar una derivada. siendo $f$ una función, se escribe a la derivada de la función $f$ respecto al valor $x$ en varios modos.
## Notación de Lagrange
La notación más simple para diferenciación. Consiste en denotar la derivada de una función $f(x)$ como $f'(x)$ que se lee *f prima de x*. Esta notación se extiende a derivadas de orden superior, dando lugar a $f''(x)$  que se lee *f segunda de x* para la derivada segunda así sucesivamente. La derivada cuarta y siguientes se pueden denotar de dos formas: 
- con números romanos: $f^{IV}(x)$ 
- con números entre paréntesis: $f^{(4)}(x)$ 
Esta última opción da lugar también a la notación $f^{(n)}(x)$ par denotar la n-ésima de $f$.
## Notación de Leibniz
Otra notación común para la diferenciación. Para la función derivada de $f$, se escribe:
$$
\frac{d(f(x))}{dx}
$$
También puede encontrarse como:
$$\frac{dy}{dx}, \frac{df}{dx}, \frac{d}{dx} f(x)$$
Se lee como *derivada de $y$ ($f$ o $f$ de $x$)* con respecto a $x$. Esta notación tiene la ventaja de sugerir a la derivada de una función con respecto a otra como un cociente de diferenciales.
Con esta notación, se puede escribir la derivada de $f$  en el punto $a$ de dos modos diferentes:

![](https://i.imgur.com/9pbZzrK.png)
Si $y = f(x)$, se pude escribir la derivada como:
$$
\frac{dy}{dx}
$$
Y las derivadas sucesivas se expresan como:
$$
\frac{d^n f}{dx^n}, \frac{d^n y}{dx^n}
$$
Para la enésima derivada de $f$ o de $y$ respectivamente, Históricamente, esto viene del hecho que, por ejemplo, la tercera derivada es:
$$
\frac{
	d\left(\frac{
			d\left(\frac{
			d(f(x))
			}{
			dx
			}\right)
		}{
		dx
		}\right)
	}{
	dx
	}
$$
Lo cual se puede describir como:
$$
\left(\frac{d}{dx}\right)^3(f(x))=\frac{d^3}{(dx)^3}(f(x))
$$
La notación de Leibniz es muy útil, por cuanto permite especificar la variable de diferenciación (en el denominador); lo cual es pertinente en caso de diferenciación parcial. También facilita recordar la regla de la cadena, porque los términos «d» parecen cancelarse simbólicamente:
$$
\frac{dy}{dx}=\frac{dy}{du}\cdot\frac{du}{dx}
$$
## Notación de Newton
La notación de Newton para la diferenciación respecto al tiempo, era poner un punto arriba del nombre de la función:
$$
\begin{align}
\dot x = x'(t)\\
\ddot x= x''(t)
\end{align}
$$
Y así sucesivamente. Se lee *punto $x$* o  *$x$ punto*. Actualmente está en desuso en el área de matemáticas puras, sin embargo se sigue usando en áreas de la física como la mecánica, donde otras notaciones de la derivada se pueden confundir con la notación de velocidad relativa. Se usa para definir la derivada temporal de una variable.
# Cálculo de la derivada
La derivada de una función, **en principio**, puede ser calculada a partir de la definición, expresando el cociente de diferencias y calculando si límite. Sin embargo, salvo para unos pocos casos esto puede resultar una terea tediosa. Para ello existen fórmulas precalculadas para las derivadas para las derivadas de las funciones más simples, mientras que para las funciones más complicadas se utilizan una serie de reglas que permitan reducir el problema al cálculo de la derivada de funciones más sencillas. Por ejemplo, para calcular la derivada de la función $cos(x)^2$ bastaría con conocer la derivada de $x^2$, la derivada de $cos(x)$, y cómo derivar una composición de funciones.
## Derivadas de funciones elementales
La mayor parte de los cálculos de derivadas requieren tomar eventualmente la derivada de algunas funciones comunes. La siguiente tabla incompleta proporciona algunas de las más frecuentes funciones de una variable real usadas y sus derivadas.
![Imgur](https://imgur.com/dSNaLjW.png)

# Aplicación de las derivadas
## Pendiente
