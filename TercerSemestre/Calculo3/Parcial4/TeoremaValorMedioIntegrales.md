#Calculo #Teorema 
#### Teorema del valor medio para integrales:
Sea ${}f:D\to \mathbb{R}{}$ una función continua definida para ${}D\subseteq \mathbb{R}^{2}{}$ una [[Integral_sobre_Regiones|región elemental]]. Entonces existe un punto ${}(x_{0},y_{0})\in D{}$ tal que 
$$
f(x_{0},y_{0})=\frac{1}{A(D)}\int_{D}f(x,y)dA,
$$
donde ${}A(D){}$ denota el área de la región ${}D{}$.
##### Demostración:
Como ${}f{}$ es continua y ${}D{}$ compacto, existen ${}m{}$ y ${}M{}$ tales que ${}m\leq f(x,y)\leq M{}$ para todo punto ${}(x,y)\in D{}$. (Es decir ${}f{}$ está acotada).
Entonces tenemos que 
$$
\begin{aligned}
\int_{D}mdA&\leq \int_{D}f(x,y)dA&\leq \int_{D}MdA \\
m\cdot A(D)&\leq \int_{D}f(x,y)dA&\leq M\cdot A(D) \\
m&\leq \frac{1}{A(D)}\int_{D}f(x,y)dA&\leq M.
\end{aligned}
$$
Además, dado que la función ${}f{}$ es continua, por el teorema del valor intermedio existe un punto ${}(x_{0},y_{0})\in D{}$ tal que 
$$
f(x_{0},y_{0})=\frac{1}{A(D)}\int_{D}f(x,y)dA.\quad\square
$$
