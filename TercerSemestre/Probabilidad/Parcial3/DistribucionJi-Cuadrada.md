#Probabilidad 
#### Definición:
Sea ${}X{}$ una [[V.A.Continuas|v.a. continua]] que sólo toma valores positivos, con función de densidad dada por 
$$
f(x)=\frac{1}{\Gamma(n/2)}\left( \frac{1}{2} \right)^{n / 2}x^{n/2 -1}e^{-x/2},\quad x>0,n\geq 0.
$$
A este tipo de variable se le conoce como distribución ${}\mathcal{X}^{2}{}$ con ${}n{}$ grados de libertad. (Ji o Chi cuadrada). Los grados de libertad se pueden ver como las “opciones” que tenemos. Por ejemplo, si queremos elegir una gorra, y tenemos seis gorras, tenemos seis grados de libertad.

Se puede demostrar que si ${}X\sim \mathcal{X}^{2}_{(n)}{}$
- ${}\mathbb{E}(X)=n{}$,
- ${}\mathrm{Var}(X)=2n{}$.
#### Proposición
Si ${}X{}$ es una [[DistribucionNormal|v.a.]] ${}\mathcal{N}(0,1){}$, entonces ${}X^{2}\sim \mathcal{X}^{2}_{(1)}{}$, es decir, sigue una distribución ji-cuadrada con un grado de libertad.
#### Proposición
Si ${}X_{1},X_{2}{}$ son v.a. ${}\mathcal{X}^{2}{}$ con ${}n{}$ y ${}m{}$ grados de libertad, respectivamente, entonces $${}X_{1}+X_{2}\sim \mathcal{X}^{2}_{(n+m)}.{}$$
#### Ejemplo. Pruebas de independencia
Sean ${}X{}$ y ${}Y{}$ dos variables aleatorias categóricas nominales (nominales significa sin orden). Tomemos por ejemplo 
$$
x=\begin{cases}
1, & \text{la persona juega videojuegos} \\
0, & \text{si no}
\end{cases},\quad y=\begin{cases}
1, & \text{buen desempeño académico} \\
2, & \text{desempeño regular} \\
3, & \text{desempeño bajo}
\end{cases}.
$$
¿Son ${}X{}$ y ${}Y{}$ independientes?
Tomemos una muestra de ${}n{}$ individuos, asignando a cada individuo una categoría en ${}x{}$ y una en ${}y{}$. Después hacemos un conteo de cuántos individuos pertenecen a cada categoría.
Sabemos que ${}X,Y{}$ son independientes si ${}P(X=i,Y=j)=P(X=i)P(Y=j){}$.
¿Qué debería pasar con los conteos si hubiera independencia?
Tomamos ${}o_{ij}={}$“número observado de personas con la condición ${}X=i,Y=j{}$”, y tomamos además ${}e_{ij}={}$“el número esperado de personas con la condición ${}X=i,Y=j{}$ bajo el supuesto de independencia”.
Si definimos $${}X^{2}=\sum_{i}\sum_{j} \frac{(o_{ij}-e_{ij})^{2}}{e_{ij}},{}$$
entonces se puede mostrar que ${}X^{2}\sim \mathcal{X}^{2}_{(2)}{}$.
Lo que buscamos entonces es que el valor observado de ${}X^{2}{}$ tenga una probabilidad alta dada la distribución ${}\mathcal{X}^{2}{}$.