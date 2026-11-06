#Calculo #Teorema
#### Definición:
Una función ${}f{}$ es integrable sobre ${}R{}$ si el límite 
$$
\lim_{ \lVert P \rVert   \to 0 }S_{n} =\lim_{ n \to \infty } S_{n}
$$
existe y es igual a 
$$
\underset{R}{\int \int}fdA
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
S_{n}(h)=\sum_{i,j}h(x_{i},y_{j})\Delta A_{ij}\geq 0
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
3.- Si ${}f(x,y)\geq g(x,y){}$ para todo ${}(x,y)\in R{}$, entonces 
$$
\int_{R}fdA\geq \int_{R}gdA.
$$
##### Demostración:
1.- Sea ${}P{}$ una partición de ${}R{}$, tomemos 
$$
\begin{aligned}
S_{n}(f+g)=\sum_{i,j}f+g(x_{ij},y_{ij})\Delta A_{ij}&=\sum_{i,j}f(x_{ij},y_{ij})\Delta A_{ij}+g(x_{ij},y_{ij})\Delta A_{ij} \\
&= S_{n}(f)+S_{n}(g),
\end{aligned}
$$
donde tenemos que si ${}\lVert P \rVert\to 0{}$ o ${}n\to \infty{}$ se tiene que 
$$
\lim_{ n \to \infty } S_{n}(f+g)=\lim_{ n \to \infty } S_{n}(f)+\lim_{ n \to \infty } S_{n}(g).\quad\square
$$

2.- 

3.- 