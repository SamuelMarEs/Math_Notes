#Calculo 
Sea ${}f:B\to \mathbb{R}{}$ una función continua donde ${}B{}$ es un paralelepípedo recto 
$$
B=[a,b]\times[c,d]\times[u,v].
$$
![[RegionDeIntegracionEnR3]]
Tomemos una partición de ${}B{}$ en paralelepípedos ${}B_{ijk}{}$ con ${}i,j,k=1,\dots,n{}$. Tomamos ${}c_{ijk}\in B_{ijk}{}$ un punto en cada paralelepípedo, y ${}\Delta V=\Delta x\Delta y\Delta z{}$ el volumen de cada ${}B_{ijk}{}$, ${}i,j,k=1,\dots,n{}$. Entonces definimos la siguiente suma 
$$
S_{n}=\sum_{i=1}^{n}\sum_{j=1}^{n}\sum_{k=1}^{n}f(c_{ijk})\Delta V=\sum_{i,j,k}f(c_{ijk})\Delta V
$$
para a partir de esta definir la integral triple:
#### Definición:
Sea ${}f:\mathbb{R}^{3}\to \mathbb{R}{}$ una función acotada y definida en ${}B{}$. Si ${}\lim_{ n \to \infty }S_{n}{}$ existe, le llamamos la triple integral de ${}f{}$ sobre ${}B{}$. 
$$
\lim_{ n \to \infty } S_{n}=\int_{B}f(x,y,z)dV=\iiint_{B}f(x,y,z)dxdydz.
$$

Si ${}f{}$ es continua en ${}B{}$ entonces es integrable sobre ${}B{}$. Además, se cumple el [[TeoremaDeFubini|Teorema de Fubini,]] es decir, podemos intercambiar el orden de integración.

##### Ejemplos
1.- Sea ${}B=[0,1]\times\left[ -\frac{1}{2},0 \right]\times\left[ 0, \frac{1}{3} \right]{}$ y sea ${}f(x,y,z)=(x+2y+3z)^{2}{}$, entonces 
$$
\int_{B}f(x,y,z)dV=\int_{0}^{1 / 3}\int_{-1 / 2}^{0}\int_{0}^{1}(x+2y+3z)^{2}dxdydz,
$$
y haciendo un cambio de variable es fácil ver que esto es
$$
\int_{0}^{1 / 3}\int_{- 1 / 2}^{0} \frac{(1+2y+3z)^{3}}{3}- \frac{(2y+3z)^{3}}{3}dydz,
$$
donde la integral de cada término se puede resolver mediante otro cambio de variable como 
$$
\int_{0}^{1 / 3} \frac{1}{24} [(3z+1)^{4}-2(3z)^{4}+(3z-1)^{4}]dz,
$$
y nuevamente haciendo todas las cuentas mediante sustitución por ${}u{}$ y etc etc, llegamos a que esto es 
$$
\frac{1}{24} \frac{1}{15}[(3z+1)^{5}-2(3z)^{5}+(3z-1)^{5}]|_{0}^{1 / 3}=\frac{1}{12}.
$$
