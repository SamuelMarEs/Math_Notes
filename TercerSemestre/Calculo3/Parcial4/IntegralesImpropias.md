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
Esto indica que ${}\lim_{ n \to \infty }S_{n}{}$ depende de la elección de ${}c_{ij}{}$, por lo tanto la función no es integrable.
Sin embargo, tenemos que 
$$
\int_{R}f(x,y)dA=\int_{0}^{1}\int_{0}^{1}f(x,y)dxdy=\int_{0}^{1}2dy=2.
$$


Supongamos que tenemos una región tipo 1 ${}D{}$, y una función ${}f:D\to \mathbb{R}{}$ continua y acotada excepto en los puntos frontera de ${}D{}$. Escribimos ${}D{}$ por ${}(x,y)\in \mathbb{R}^{2}{}$ tal que ${}a\leq x\leq b{}$ y ${}\phi_{2}(x)\leq y\leq \phi_{1}(x){}$.
Si elegimos ${}\delta,\eta>0{}$ y definimos 
$$
D_{\eta,\delta}=\{ (x,y)\in \mathbb{R}^{2}|a+\eta\leq x\leq b-\eta,\phi_{2}(x)+\delta\leq y\leq \phi_{1}(x)-\delta \},
$$
donde ${}\delta,\eta{}$ son lo suficientemente pequeños para ${}D_{\eta ,\delta}\subset D{}$. Así ${}f(x,y){}$ en ${}D_{\eta,\delta}{}$ es acotada y continua por lo que existe 
$$
\int_{D\eta,\delta}f(x,y)dA.
$$
Entonces definimos la ***integral impropia*** de ${}f{}$ sobre ${}D{}$ como 
$$
\lim_{ (\eta,\delta) \to (0,0) } \int_{D\eta,\delta}f(x,y)dA.
$$
(Siempre que el límite exista)
Notese que en ${}D_{\eta \delta}{}$ se cumple [[TeoremaDeFubini#^d82507|Fubini]], y por lo tanto podemos llegar a que 
$$
\lim_{ (\eta,\delta) \to (0,0) } \int_{D\eta,\delta}f(x,y)dA.=\lim_{ \eta \to 0 } \int_{a+\eta}^{b-\eta}\left[ \lim_{ \delta \to 0 } \int_{\phi_{2}+\delta}^{\phi_{1}-\delta}f(x,y)dy \right]dx.
$$
Si los límites existen, entonces esta es la integral iterada impropia.

#### Ejemplos:
1.- Si ${}f(x,y)=\frac{1}{\sqrt{ 1-x^{2}-y^{2} }}{}$, y ${}D{}$ es el círculo unitario ${}x^{2}+y^{2}\leq 1{}$. Calcular ${}\int_{D}fdA{}$ si existe.
**Sol:**

2.- Sea ${}f(x,y)=\frac{1}{x-y}{}$ y ${}D=\{ (x,y):0\leq x\leq 1,0\leq y\leq x \}{}$. Mostrar que ${}f{}$ no es integrable. (Dar una trayectoria para la cual el límite no exista).
**Sol:**
Notemos que en ${}x=y{}$ la función no está acotada (ni definida). Sea ${}0<\eta<1,0<\det <\eta{}$, definimos 
$$
D_{\eta \delta}=\{ (x,y)\varepsilon ta\leq x\leq 1-\eta,\delta\leq y\leq x-\delta \},
$$
entonces 
$$
\int_{D\eta \delta}fdA=\int_{\eta}^{1-\eta}\int_{\delta}^{x-\delta} \frac{1}{x-y}dydx,
$$
donde la integral respecto a ${}y{}$ es 
$$
\int_{\delta}^{x-\delta} \frac{1}{x-y}dy=-\ln(\delta)+\ln(x-\delta),
$$
y entonces tenemos 
$$
\int_{\eta}^{1-\eta}-\ln(\delta)+\ln(x-\delta)=-\ln(\delta)x+(x-\delta)\ln(x-\delta)-(x-\delta)|_{\eta}^{1-\eta},
$$
y a partir de esto llegamos al resultado 
$$
-\ln(\delta)[1-2\eta]+(1-\eta-\delta)\ln(1-\eta-\delta)-(1-\eta-\delta)-(\eta-\delta)\ln(\eta-\delta)+(\eta-\delta),
$$
donde si tomamos el limite cuando ${}\eta{}$ y ${}\delta{}$ tienden a cero, el único término que sobrevive es ${}-\ln(\delta)[1-2\eta]\to-\ln \delta{}$, que diverge para ${}\delta\to 0{}$.