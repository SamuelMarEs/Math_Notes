#### Problema
Entre $n$ puntos del plano, $u(n)$ es el máximo númeo de pares separados exactamente por una unidad.

**Lo que Erdös esperaba:** Conjeturó que, ara cualquier constante $\varepsilon>0$, 
$$
	u(n)\in O(n^{1+\varepsilon}).
$$
La mejor [[Complejidad|cota superior]] conocida es
$$
	u(n)\in O(n^{4 / 3}).
$$

En **mayo de 2026** se probó que 
$$
	\exists \delta>0\text{ fijo }: u(n)\in \Omega(n^{1+\delta})\quad\text{para infinitos }n.
$$
##### ¿Por qué esto refuta la conjetura?
La conjetura debía cumplirse para cualquier $\varepsilon>0$. Como $\delta$ es fijo, podemos elegir $\varepsilon<\delta$. Entonces $n^{1+\delta}$ crece más rápido que $n^{1+\varepsilon}$, contradiciendo la cota propuesta por Erdös. El orden exacto $\Theta(u(n))$ aún se desconoce. Tampoco conocemos una fórmula general para $u(n)$.

Este resultado fue encontrado no por un matemático, si no por ***ChatGPT***.


#Algoritmos 