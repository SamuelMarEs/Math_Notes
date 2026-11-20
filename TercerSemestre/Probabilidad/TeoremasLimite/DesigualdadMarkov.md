#Probabilidad #Teorema
Al igual que la [[DesigualdadChebyshev|desigualdad de Chebyshev]], la desigualdad de Markov es un resultado importante, que de hecho se puede usar para demostrar la desigualdad mencionada anteriormente.
#### Desigualdad de Markov
Si ${}X{}$ es una v.a. con [[ValorEsperadoContinuo|esperanza]] ${}\mu{}$ finita, entonces 
$$
P(X\geq \varepsilon)\leq \frac{\mu}{\varepsilon}.
$$
##### Demostración:
Para el caso continuo, (para el caso discreto el procedimiento es análogo), tenemos que 
$$
\begin{aligned}
\mathbb{E}(X)=\mu&=\int_{-\infty}^{\infty}xf(x)dx \\
&\geq \int_{\varepsilon}^{\infty}xf(x)dx \\
&\geq \int_{\varepsilon}^{\infty}\varepsilon f(x)dx \\
&=\varepsilon \int_{\varepsilon}^{\infty}f(x)dx \\
&=\varepsilon P(X\geq \varepsilon), \\
\implies \mu&\geq \varepsilon P(X\geq\varepsilon) \\
\implies \frac{\mu }{\varepsilon}&\geq P(X\geq\varepsilon).\quad\square
\end{aligned}
$$
