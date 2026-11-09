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
Sea ${}f:D\to \mathbb{R}{}$, donde ${}D\subseteq \mathbb{R}^{2}{}$ es una región elemental, y ${}f{}$ es continua en ${}D{}$. Si ${}R{}$ es un rectángulo que contenga a ${}D{}$