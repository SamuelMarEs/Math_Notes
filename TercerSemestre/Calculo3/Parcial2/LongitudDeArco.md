#Calculo #Geometria 
Para $c:[a,b]\to\mathbb{R}^{n}$. Comencemos por tomar una partición del intervalo $[a,b]$ en $a=t_{0}, t_{1},\dots,t_{n}=b$, es decir los subintervalos 
$$
	[a,t_{1}],[t_{1},t_{2}],\dots,[t_{n-1},b], \quad\text{de longitud } \Delta w_{i}=t_{i+1}-t_{i}.
$$
Consideremos entonces los segmentos de recta que van entre $[c(a),c(t_{1})],[c(t_{1}),c(t_{2})],\dots,[c(t_{n-1},c(b))]$, cuya longitud es 
$$
	d(c(t_{i}),c(t_{i+1}))=\lvert \lvert c(t_{i})-c(t_{i+1}) \rvert  \rvert ,\quad\text{para }i=0,1,\dots,n-1.
$$
Sea $c(t)=(x_{1}(t),x_{2}(t),\dots,x_{n}(t))$, entonces tenemos que 
$$
	d(c(t_{i}),c(t_{i+1}))=\sqrt{ (x_{1}(t_{i})-x_{2}(t_{i+1}))^{2}+\dots+(x_{n}(t_{i})-x_{n}(t_{i+1}))^{2} }.
$$
Para el intervalo $[t_{i}, t_{i+1}]$, $i=0,\dots,n-1$, por el Teorema del Valor Medio, existe $\alpha_{i}\in[t_{i},t_{i+1}]$ tal que 
$$
	x_{j}(t_{i+1})-x_{j}(t_{i})=(t_{i+1}-t_{i})x'_{j}(\alpha_{i}),\quad\text{para }j=1,\dots,n.
$$
Entonces tenemos que 
$$
	\begin{align}
	d(c(t_{i}),c(t_{i+1}))&=\sqrt{ (\Delta w_{i} x_{1}'(\alpha_{i}))^{2}+\dots+(\Delta w_{i} x'_{n}(\alpha_{i}))^{2} } \\
	&= \Delta w_{i}\sqrt{ (x_{1}'(\alpha_{i}))^{2}+\dots+(x_{n}'(\alpha_{i}))^{2} } \\
	&=\Delta w_{i}\lvert \lvert c'(\alpha_{i}) \rvert  \rvert .
	\end{align}
$$
Entonces, podemos tomar la suma, y tenemos 
$$
	\sum_{i=0}^{n-1}d(c(t_{i}),c(t_{i+1}))=\sum_{i=0}^{n-1}\lvert \lvert c'(\alpha i) \rvert  \rvert \Delta w_{i},
$$
de modo que podemos ahora tomar el límite de la suma y obtener la integral definida: 
$$
	\lim_{ \Delta w_{i} \to 0 }\sum_{i=0}^{n-1}\lvert \lvert c'(\alpha i) \rvert  \rvert \Delta w_{i}=\int_{a}^{b}\lvert \lvert c'(t) \rvert  \rvert dt. 
$$

En base a esto, podemos definir la función 
$$
	s(t)=\int_{a}^{t}\lvert \lvert c'(\alpha) \rvert  \rvert d\alpha.
$$

