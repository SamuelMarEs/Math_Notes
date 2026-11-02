#AlgebraLineal 
#### Definición:
Sea ${}T{}$ un operador lineal sobre un espacio de producto interno ${}V{}$. Decimos que ${}T{}$ es hermitiano (o auto-adjunto) si ${}T=T^{*}{}$. De forma análoga, una matriz real o compleja ${}A{}$ es hermitiana (auto-adjunta) si ${}A=A^{*}{}$.

No es difícil ver que, si ${}\beta{}$ es una base ortonormal, entonces ${}T{}$ es hermitiano si y sólo si ${}[T]_{\beta}{}$ es hermitiana. Si se tiene que ${}F=\mathbb{R}{}$, entonces decir que una matriz es hermitiana es lo mismo a decir que la matriz es simétrica.
#### Lema
Sea ${}T{}$ un operador auto-adjunto sobre un espacio de producto interno de dimensión finita ${}V{}$. Entonces:
a) Todo eigenvalor de ${}T{}$ es real.
b) Supongamos que ${}V{}$ es un espacio vectorial sobre ${}\mathbb{R}{}$. Entonces el polinomio característico de ${}T{}$ se descompone sobre ${}\mathbb{R}{}$.
##### Demostración:
a) Supongamos que ${}T(x)=\lambda x{}$ para ${}x\neq 0{}$. Dado que un operador auto-adjunto también es un [[TercerSemestre/AlgebraLineal2/Parcial4/OperadoresNormales|operador normal]], tenemos que 
$$
\lambda x=T(x)=T^{*}(x)=\overline{\lambda}(x).
$$
Es decir que ${}\lambda=\overline{\lambda}{}$, por lo tanto ${}\lambda{}$ es real.
b) Sean ${}n=\mathrm{dim}(V){}$, ${}\beta{}$ una base ortonormal de ${}V{}$, y ${}A=[T]_{\beta}{}$. Entonces ${}A{}$ es auto-adjunta. Sea ${}T_{A}{}$ el operador lineal sobre ${}\mathbb{C}^{n}{}$ definido como ${}T_{A}(x)=Ax{}$ para todo ${}x \in \mathbb{C}^{n}{}.$ Podemos notar que ${}T_{A}{}$ es auto-adjunto pues ${}[T_{A}]_{\gamma}=A{}$, donde ${}\gamma{}$ es la base canónica de ${}\mathbb{C}^{n}{}$. Entonces, por el inciso ${}A{}$, todo eigenvalor de ${}T_{A}{}$ es real, y por lo tanto su polinomio característico se descompone sobre los reales. Sin embargo, el polinomio característico de ${}T_{A}{}$ es el mismo que el de ${}A{}$