#Calculo 
Sea ${}f:B\to \mathbb{R}{}$ una función continua donde ${}B{}$ es un paralelepípedo recto 
$$
B=[a,b]\times[c,d]\times[u,v].
$$
![[Drawing 2026-11-17 11.01.07.excalidraw]]
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