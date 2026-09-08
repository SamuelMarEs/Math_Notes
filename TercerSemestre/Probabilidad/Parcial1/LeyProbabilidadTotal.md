#### Teorema
Sean $A,B_{1},B_{2},\dots,B_{n}$ eventos definidos sobre $\Omega$ tales que 
$$
	B_{i}\cap B_{j}=\emptyset\quad\forall i\neq j,\quad i,j=1,\dots,n
$$
y tenemos además que 
$$
	\bigcup_{i=1}^{n}B_{i}=\Omega.
$$
Es decir que $B_{1},\dots,B_{n}$ forman una partición de $\Omega$.
Entonces tenemos que 
$$
	\begin{align}
	P(A)&=\sum_{i=1}^{n}P(A|B_{i})P(B_{i}) \\
	&=P(A|B_{1})P(B_{1})+P(A|B_{2})P(B_{2})+\dots+P(A|B_{n})P(B_{n}).
	\end{align}
$$
Esto siempre y cuando $P(B_{i})>0\quad\forall B_{i}$.
##### Demostración:
Notese que todo evento $A$ se puede escribir de la forma 
$$
	A=(A\cap B_{1})\cup(A\cap B_{2})\cup\dots\cup(A\cap B_{n}).
$$
Esto implica que 
$$
	\begin{align}
	P(A)&=P\left( \bigcup_{i=1}^{n}A\cap B_{i} \right) \\
	&=\sum_{i=1}^{n}P(A\cap B_{i}) \\
	&=\sum_{i=1}^{n}P(A|B_{i})P(B_{i}).\quad\square
	\end{align}
$$
Esta última parte recordando la definición de [[ProbabilidadCondicional|probabilidad condicional]].

#### Ejemplos
1.- Supongamos que tenemos dos urnas llenas de pelotas. En la primera urna hay 5 pelotas rojas y 6 pelotas negras. En la segunda, hay 3 pelotas rojas y 10 pelotas negras.
Se elige una urna al azar y tomamos una pelota. ¿Cuál es la probabilidad de que la pelota sea roja?
**Sol:**
Sean los eventos $R=$ sacar pelota roja, $N=$ sacar pelota negra, $U_{1}=$ elegir urna 1, $U_{2}=$ elegir urna 2.
Entonces, tenemos una partición de nuestro espacio muestral en $U_{1}$ y $U_{2}$. Si supieramos que urna se eligió, calcular la probabilidad de sacar una pelota roja es fácil: $P(R|U_{1})=\frac{5}{11}$, y $P(R|U_{2})=\frac{3}{13}$. Además, sabemos que $P(U_{1})=P(U_{2})=\frac{1}{2}$.
Entonces, por la *ley de probabilidad total*, se sigue que 
$$
	\begin{align}
	P(R)&=P(R|U_{1})P(U_{1})+P(R|U_{2})P(U_{2}) \\
	&=\frac{5}{11} \frac{1}{2}+ \frac{3}{13} \frac{1}{2} \\
	&=\frac{1}{2}\left( \frac{5}{11}+\frac{3}{11} \right) \\
	&=\frac{49}{143}=0.34.
	\end{align}
$$

2.- Se tienen tres máquinas que producen tornillos. La producción de las máquinas 1,2, y 3 es el 60%, 30% y 10% de la producción total, respectivamente. Se sabe que cada cada máquina produce tornillos defectuosos con una probabilidad de $0.01, 0.05, 0.1$.
Si se toma un tornillo al azar para inspección, ¿qué tan probable es que esté defectuoso?
**Sol:**
Sean $M_{1},M_{2},M_{3}$ los eventos de elegir un tornillo de la máquina 1, 2 y 3 respectivamente. Sea además $D$ el evento de elegir un tornillo defectuoso. Tenemos las siguientes probabilidades:
$P(M_{1})=0.6,P(M_{2})=0.3,P(M_{3})=0.1$. Además de que sabemos la probabilidad de que el tornillo sea defectuoso dada la máquina de la que viene: $P(D|M_{1})=0.01, P(D|M_{2})=0.05, P(D|M_{3})=0.1$.
Entonces, por el teorema de probabilidad total, tenemos:
$$
	\begin{align}
	P(D)&=P(D|M_{1})P(M_{1})+P(D|M_{2})P(M_{2})+P(D|M_{2})P(M_{2}) \\
	&=(0.01)(0.6)+(0.05)(0.3)+(0.1)(0.1) \\
	&=0.031.
	\end{align}
$$

#Probabilidad #Teorema