#Probabilidad #Teorema
Esta es una de las desigualdades más importantes a ver:
#### Desigualdad de Chebyshev
Sea ${}X{}$ una v.a. con media ${}\mu{}$ y desviación estándar ${}\sigma{}$, ambas finitas. Entonces, para todo ${}\varepsilon >0{}$ se cumple 
$$
P(\lvert X-\mu \rvert \geq \varepsilon)\leq \frac{\sigma^{2}}{\varepsilon^{2}}.
$$
Este resultado nos está dando una cota superior para la distancia entre los valores de una variable y su valor esperado.
##### Demostración
Sea ${}X{}$ una v.a. continua con función de densidad ${}f(x){}$. Partimos de la definición de varianza 
$$
\begin{aligned}
\sigma^{2}=\mathrm{Var}(X)&=\int_{-\infty}^{\infty}(x-\mu)^{2}f(x)dx \\
&\geq \int_{x:\lvert x-\mu \rvert >\varepsilon}(x-\mu)^{2}f(x)dx \\
&\geq \int_{x:\lvert x-\mu \rvert >\varepsilon}\varepsilon^{2}f(x)dx \\
&=\varepsilon^{2}\int_{x:\lvert x-\mu \rvert >\varepsilon}f(x)dx \\
&=\varepsilon^{2}P(\lvert X-\mu \rvert >\varepsilon), \\
\implies \sigma^{2}&\geq \varepsilon^{2}P(\lvert X-\mu \rvert >\varepsilon) \\
\implies P(\lvert X-\mu \rvert >\varepsilon)&\leq \frac{\sigma^{2}}{\varepsilon^{2}}.\quad\square
\end{aligned}
$$

Para que la desigualdad tenga sentido, es necesario que ${}\varepsilon>\sigma^{2}{}$, ya que, de lo contrario, la desigualdad únicamente nos estaría diciendo que 
$$
P(\lvert X-\mu \rvert >\varepsilon)\leq 1,
$$
lo cual es trivial por la definición de una [[ProbabilidadAxiomatica|medida de probabilidad]].
