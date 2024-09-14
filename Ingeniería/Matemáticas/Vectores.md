En matemática y física, un vector  es cualquier ente matemático que se puede representar mediante un segmento de recta orientado dentro del espacio euclidiano.

## Espacio vectorial
Es una estructura algebraica creada a partir de un conjunto no vacío, una operación interna y una operación externa que te satisface 8 propiedades fundamentales. A los elementos de un espacio vectoriales se les llama vectores y a los elementos del cuerpo se les conoce como escalares.
## Notación
Dado un espacio vectorial $V$ sobre un cuerpo $K$, se distinguen los elementos de $V$ y los de $K$.
Los elementos de $V$ suelen denotarse por $u,v,w$ y son llamados **vectores**, también son denotados como $\vec{u}, \vec{v}, \vec{w}$. Mientras que los elementos de $K$ se denotan como $a,b,\alpha,\beta$ y son llamados **escalares**. 
## Definición
Un espacio vectorial sobre un cuerpo $K$ es un conjunto no vacío, digamos $V$, dotado de dos operaciones para las cuales será cerrado: 
### Suma
$$
\begin{align}
V \times V &\to V \\
(u,v)&\mapsto u+v
\end{align}
$$
Operación interna tal que:
Tenga la propiedad conmutativa:
$$u+v=v+u,\hspace{,2cm} \forall u,v \in V$$
Tenga la propiedad asociativa:
$$
u+(v+w)=(u+v)+w, \hspace{,2cm} \forall u,v,w \in V
$$
Exista el elemento neutro:
$$
	\exists e \in V: u + e=u,\forall u
$$
Exista el elemento opuesto:
$$
\forall u \in V, \exists - u \in V:u+(-u)=e
$$
### Producto
Tenga la propiedad asociativa:
$$
a \cdot(b \cdot u) = (a \cdot b) \cdot u, \hspace{.2cm} \forall a,b \in K, \hspace{.2cm} \forall u \in V
$$ 
Exista el elemento neutro:
$$
\exists e \in K:e \cdot u = u, \hspace{.2cm} \forall u \in V
$$
Tenga la propiedad distributiva respecto de la suma vectorial:
$$
a \cdot (u+v)= a\cdot u + a \cdot v,\hspace{.2cm} \forall a \in K, \hspace{.2cm} \forall u,v \in V
$$
Tenga la propiedad distributiva respecto de la suma escalar:
$$
(a+b) \cdot u= a\cdot u + b \cdot u,\hspace{.2cm} \forall a,b \in K, \hspace{.2cm} \forall u \in V
$$
