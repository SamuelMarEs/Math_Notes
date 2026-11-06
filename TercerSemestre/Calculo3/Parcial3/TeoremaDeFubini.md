#Calculo #Teorema
#### Definición:
Una función ${}f{}$ es integrable sobre ${}R{}$ si el límite 
$$
\lim_{ \lVert P \rVert   \to 0 }S_{n} =\lim_{ n \to \infty } S_{n}
$$
existe y es igual a 
$$
\iint_{R}fdA
$$
independientemente de los puntos que se tomen.

#### Teorema:
Sea ${}f:R\to \mathbb{R}{}$ acotada y definida en el rectángulo, y supongamos que los puntos donde ${}f{}$ es discontinua están formados por una unión finita de gráficas de funciones continuas.
Entonces ${}f{}$ es integrable.

#### Lema:
Sea ${}h(x,y)\geq 0{}$ en ${}R{}$, entonces 
$$
\int_{R}h(x,y)dA\geq0.
$$
##### Demostración:
Sea ${}S_{n}(h){}$ la suma de Riemann de ${}h{}$, como ${}h\geq 0{}$ en ${}R{}$ y ${}\Delta A_{ij}>0{}$, entonces ${}h(x,y)\Delta A_{ij}\geq 0{}$, es decir cada término de la suma de Riemann es positivo, de modo que 
$$
S_{n}(h)=\sum_{i,j}h(x_{i},y_{j})\Delta A_{ij}\geq 0\implies \lim_{ n \to \infty } S_{n}(h)\geq 0. \quad\square
$$

#### Propiedades
1.- Linealidad. Sean ${}f,g{}$ funciones integrables en el rectángulo ${}R{}$, entonces 
$$
\int_{R}(f+g)(x,y)dA=\int_{R}fdA+\int_{R}gdA.
$$
2.- Homogeniedad. Si ${}f{}$ es integrable en ${}R{}$ y ${}c{}$ es una constante, entonces 
$$
\int_{R}cf(x,y)dA=c\int_{R}f(x,y)dA.
$$
3.- Monotonia. Si ${}f(x,y)\geq g(x,y){}$ para todo ${}(x,y)\in R{}$, entonces 
$$
\int_{R}fdA\geq \int_{R}gdA.
$$
4.- Aditividad. Si ${}R_{i}{}$ con ${}i=1,\dots,M{}$ son rectángulos ajenos entre sí, tal que ${}f{}$ es integrable en cada ${}R_{i}{}$. Si ${}Q=\bigcup_{i=1}^{M}R_{i}{}$ es un rectángulo, entonces 
$$
\iint_{Q}f(x,y)dA=\sum_{i=1}^{M}\iint_{R_{i}}f(x,y)dA.
$$

##### Demostración:
1.- Sea ${}P{}$ una partición de ${}R{}$, tomemos 
$$
\begin{aligned}
S_{n}(f+g)=\sum_{i,j}(f+g)(x_{i},y_{j})\Delta A_{ij}&=\sum_{i,j}f(x_{i},y_{j})\Delta A_{ij}+g(x_{i},y_{j})\Delta A_{ij} \\
&= S_{n}(f)+S_{n}(g),
\end{aligned}
$$
donde tenemos que si ${}\lVert P \rVert\to 0{}$ o ${}n\to \infty{}$ se tiene que 
$$
\lim_{ n \to \infty } S_{n}(f+g)=\lim_{ n \to \infty } S_{n}(f)+\lim_{ n \to \infty } S_{n}(g).\quad\square
$$

2.- Construimos a 
$$
S_{n}(cf)=\sum_{i,j}cf(x_{i},y_{j})\Delta A_{ij}=c\sum_{ij}f(x_{i},y_{j})\Delta A_{ij}=cS_{n}(f).
$$
De este modo solo resta tomar el límite para obtener que 
$$
\lim_{ n \to \infty } S_{n}(cf)=c\lim_{ n \to \infty } S_{n}(f).\quad\square
$$

3.- Tomando el lema demostrado anteriormente, basta definir a ${}h(x,y)=f(x,y)-g(x,y){}$, y como ${}f(x,y)\geq g(x,y){}$, se mantiene que ${}h(x,y)\geq 0{}$. Por lo tanto tenemos que 
$$
\iint_{R}h(x,y)dA=\iint_{R}f(x,y)-g(x,y)dA=\iint_{R}f(x,y)dA-\iint_{R}g(x,y)dA\geq 0,
$$
por lo que se sigue de forma directa que 
$$
\iint_{R}f(x,y)dA\geq \iint_{R}g(x,y)dA.\quad\square
$$
4.- Tomemos una partición ${}P{}$ tal que las fronteras de ${}R_{i}{}$ son parte de la partición.


### Teorema de Fubini
Sea ${}f{}$ una función continua con dominio rectangular ${}R=[a,b]\times[c,d]{}$. Entonces 
$$
\int_{R}f(x,y)dA=\int_{a}^{b}\int_{c}^{d}f(x,y)dydx=\int_{c}^{d}\int_{a}^{b}f(x,y)
$$