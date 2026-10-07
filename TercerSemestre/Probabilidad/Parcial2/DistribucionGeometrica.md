#Probabilidad 
Suponga que se tienen ensayos [[DistribucionBernoulli|Bernoulli]] que se pueden repetir infinitamente. Suponga que cada repetición es independiente y que la probabilidad de éxito no cambia.
Sea $X$ la [[VariablesAleatorias|v.a.]] que indica el número de fallos (fracasos) hasta que ocurre el primer éxito. Entonces $X$ puede tomar valores $\{ 0,1,2,\dots \}$.
La [[FuncionDeProbabilidad|función de probabilidad]] de $X$ está dada por la siguiente función: 
$$
	f(x)=P(X=x)=\begin{cases}
	p(1-p)^{x}, & x=0,1,2,\dots \\
	0 & \text{otro caso.}
	\end{cases}
$$
A este tipo de v.a. se les conoce como ***variables geométricas*** de parámetro $p$, y se denotan por 
$$
	X\sim\text{Geom}(p).
$$
Se puede demostrar que 
$$
	E(X)=\frac{1-p}{p},\quad Var(X)=\frac{1-p}{p^{2}}.
$$
Esta distribución es muy útil para estudiar procesos de muestreo donde la probabilidad de éxito es muy pequeña.

##### Ejemplo
Se sabe, por estudios previos, que el 5% de cierta población de ratas presenta una mutación con un gen específica. Se quiere repetir el experimento para corroborar los resultados. ¿Cuál es el número esperado de ratas que se necesitan para observar 1 que tenga la mutación? ¿Qué tan probable es que 20 ratas no tengan la mutación? ¿Qué tan probable es que la rata 51 sea la primera en tener la mutación?
**Sol:**
Sea $X$ el número de ratas examinadas sin mutación hasta que aparezca una con la mutación. Suponemos que $X\sim\text{Geom}(p)$ con $p=0.05$.
La primera pregunta nos está preguntando el [[ValorEsperado|valor esperado]] de $X$, pero sumar 1 (porque el valor esperado por si solo nos da el número de ratas sin la mutación, pero la pregunta es el número de ratas para que haya una con la mutación, por eso añadimos la rata extra con la mutación).
Esto es 
$$
	E(X)+1=\frac{1-p}{p}+1=\frac{0.95}{0.05}+1=20.
$$
La segunda pregunta nos pide la probabilidad de que 20 ratas no tengan la mutación, es decir 
$$
	P(X=20)=p(1-p)^{20}=0.05(0.95)^{20}\approx0.017.
$$
Por último, nos pide la probabilidad de que la rata 51 sea la primera en presentar la mutación, es decir 
$$
	P(X=51)=0.05(0.95)^{51}\approx0.003.
$$

***Note:*** Sabemos que $X$ es una variable aleatoria geométrica si cuenta el número de fallos hasta el primer éxito. 
Podemos definir otra variable aleatoria $Y=X+1$ que sería el número de **ensayos** hasta el primer éxito. La diferencia es que $X$ solo cuenta las fallas, y que $Y$ cuenta las fallas más el evento exitoso (por eso +1).
Entonces tendríamos que 
$$
	E(Y)=E(X+1)=E(X)+1.
$$
