#Calculo 
Sea ${}R{}$ un rectángulo ${}[0,1]\times[0,1]{}$ y ${}f:R\to \mathbb{R}{}$ dada por 
$$
f(x,y)=\begin{cases}
\frac{1}{\sqrt{ x }}, & x\neq 0 \\
0, & x=0
\end{cases}.
$$
Si vemos la suma de Riemann 
$$
S_{n}=\sum_{i=0}^{n-1}\sum_{j=0}^{n-1}f(c_{ij})\Delta x\Delta y
$$
podremos notar que para puntos fijos cercanos a ${}(0,0){}$ y ${}n{}$ fijo, podemos tomar ${}c_{ij}{}$ cada vez más cerca a ${}(0,0){}$ tal que ${}S_{n}\to \infty{}$.
Esto indica que ${}\lim_{ n \to \infty }S_{n}{}$ depende de ${}c_{ij}{}$