#Probabilidad 
#### Definición
Si $X$ es una [[V.A.Continuas|v.a. continua]] con función de densidad $f(x)$, entonces 
$$
	\mathbb{E}(X)=\int_{-\infty}^{\infty}xf(x)dx,
$$
suponiendo que la integral converge. En caso de que no, decimos que la función no tiene valor esperado.
De forma similar al [[ValorEsperadoDiscreto|valor esperado discreto]], se la esperanza se puede ver como el promedio ponderado de la variable aleatoria.
Un poco más enfocado a v.a. continuas, el valor esperado es el el centro de masa (centroide) de la pdf.

##### Ejemplo
1.- Sea $X$ una v.a. continua con pdf dada por 
$$
	f(x)=\begin{cases}
	1, & x\in(0,1) \\
	0, & \text{en otro caso}
	\end{cases}.
$$
Encontrar $\mathbb{E}(X)$. Para esto tenemos que encontrar la siguiente integral 
$$
	\mathbb{E}(X)=\int_{-\infty}^{\infty}xf(x)dx=\int_{0}^{1}xdx=\frac{x^{2}}{2}|_{0}^{1}=\frac{1}{2}.
$$

2.- Sea $X$ una v.a. continua con pdf dada por 
$$
	f(x)=\begin{cases}
	e^{-x}, & x>0 \\
	0, & \text{en otro caso}
	\end{cases}.
$$
Encontrar la esperanza de $X$.
**Sol:**
$$
    \mathbb{E}(X)=\int_{0}^{\infty}xe^{-x}dx=\dots=1.
$$

#### Resultados
Los mismos resultados que se cumplen para el valor esperado de una v.a. discreta se mantienen para el valor esperado de una v.a. continua.
- $E(c)=c$;
- $E(X+c)=E(X)+c$;
- $E(aX+b)=aE(X)+b$;
- $E(\psi(X))=\int_{-\infty}^{\infty}\psi(x)f(x)dx$;
- $E(X+Y)=E(X)+E(Y)$;
- $E(X,Y)=E(X)E(Y)$ si $X$ y $Y$ son [[Independencia_V.A_Continuas|independientes]];
- $E(\psi(X)\psi(Y))=E(\psi(X))E(\psi(Y))$ si $X$ y $Y$ son independientes;
- $E(X)=\int_{-\infty}^{\infty}(1-F(x))dx$. <- TAREA