#Calculo 
Ya conocemos la forma de integrar sobre un [[Integral_de_rectangulo|rectángulo]]. Si ahora queremos integrar una función ${}f(x,y){}$, podemos partir de su integral sobre el rectángulo ${}R{}$, y definir una nueva función 
$$
f^{*}(x,y)=\begin{cases}
f(x,y), & (x,y)\in D \\
0, & (x,y)\in R \setminus D
\end{cases}.
$$
Aquí, ${}D\subseteq \mathbb{R}^{2}{}$ es una región del plano que se puede definir de distintas formas.

#### Región Elemental
Definamos ${}D\subseteq \mathbb{R}^{2}{}$ de la siguiente forma: 
$$
D=\{ (x,y)\in \mathbb{R}^{2}|a\leq x\leq b,\phi_{1}(x)\leq y\leq \phi_{2}(x) \}.
$$
Otra opción es definir a ${}D{}$ de la forma 
$$
D=\{ (x,y)\in \mathbb{R}^{2}|c\leq y\leq d,\psi_{1}(y)\leq x\leq \psi_{2}(y) \}.
$$
Básicamente todas las curvas cerradas parametrizadas se pueden representar de ambas formas. 
Una región que se puede expresar de una o ambas formas se conoce como una región elemental.

#### Definición
Sea ${}f:D\to \mathbb{R}{}$, donde ${}D\subseteq \mathbb{R}^{2}{}$ es una región elemental, y ${}f{}$ es continua en ${}D{}$. Si ${}R{}$ es un rectángulo que contenga a ${}D{}$, definimos a 
$$
f^{*}(x,y)=\begin{cases}
f(x,y), & (x,y)\in D \\
0, & (x,y)\in R\setminus D
\end{cases}.
$$
Así, definimos 
$$
\int_{D}f(x,y)dA=\int_{R}f^{*}(x,y)dA.
$$

#### Teorema
Si ${}f:D\to \mathbb{R}{}$ es continua en ${}D\subseteq \mathbb{R}^{2}{}$, donde ${}D{}$ es una región elemental, entonces 
$$
\int_{D}f(x,y)dA=\int_{a}^{b}\int_{\phi_{1}(x)}^{\phi_{2}(x)}f(x,y)dydx\quad \text{o}\quad =\int_{c}^{d}\int_{\psi_{1}(y)}^{\psi_{2}(y)}f(x,y)dxdy.
$$
Si en particular tuviéramos que ${}f(x,y)=1{}$, tendríamos que 
$$
\int_{a}^{b}\int_{\phi_{1}(x)}^{\phi_{2}(x)}f(x,y)dydx=\int_{a}^{b}\phi_{2}(x)-\phi_{1}(x)dx=\text{Área de }D.
$$
##### Ejemplos:
1.- Calcular ${}\int_{T}(x^{3}y+\cos x)dA{}$ para ${}T=\left\{  (x,y)|0\leq x\leq \frac{\pi}{2},0\leq y\leq x  \right\}{}$. 
**Sol:** 
$$
\begin{aligned}
\int_{T}x^{3}y+\cos xdA&=\int_{0}^{\pi / 2}\int_{0}^{x}x^{3}y+\cos xdydx \\
&=\int_{0}^{\pi / 2} \frac{x^{5}}{2}+x\cos xdx \\
&=\left( \frac{x^{6}}{12} \right)+\cos x-x\sin x|_{0}^{\pi / 2} \\
&=\frac{(\pi / 2)^{6}}{12}-\frac{\pi}{2}-1.
\end{aligned}
$$
2.- Hallar el volumen del tetraedro acotado por ${}y=0,z=0,x=0{}$ y ${}y-x+z=1{}$.
**Sol**:
Tomemos la función ${}z=1+x-y{}$. Este plano intersecta al plano ${}x=0{}$ sobre la recta ${}z=1-y{}$, y al plano ${}y=0{}$ sobre la recta ${}z=1+x{}$ (contenidas sobre sus respectivos planos). La recta ${}z=1-y{}$ corta al eje ${}y{}$ en el punto ${}y=1{}$. Entonces tenemos ${}y\in[0,1]{}$. De igual forma, la recta ${}z=1+x{}$ corta al eje ${}x{}$ en ${}x=-1{}$, por lo tanto ${}x \in[0,-1]{}$. Entonces podemos definir a nuestra región como 
$$
D=\{ (x,y)|0\leq y\leq 1,y-1\leq x\leq 0 \},
$$
entonces la integral a resolver es 
$$
\begin{aligned}
\int_{D}1+x-ydA&=\int_{0}^{1}\int_{y-1}^{0}1+x-ydxdy \\
&= \int_{0}^{1}-(y-1)-\frac{(y-1)^{2}}{2}+y(y-1)dy \\
&=\int_{0}^{1}-y+1-\frac{(y-1)^{2}}{2}+y^{2}-ydy \\
&=-y^{2}+y-\frac{(y-1)^{3}}{6}+\frac{y^{3}}{3}|_{0}^{1} \\
&=-1+1-0+\frac{1}{3}-\frac{1}{6}=\frac{1}{6}.
\end{aligned}
$$

