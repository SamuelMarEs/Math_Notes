##### Definición:
Sean $A$ y $B$ dos eventos definidos sobre el [[PrincipiosDeProbabilidad|espacio muestral]] $\Omega$ tales que $P(B)>0$. La ***probabilidad condicional*** de $A$ dado $B$ está dada por 
$$
	P(A|B)=\frac{P(A\cap B)}{P(B)}.
$$
Esto se lee como la probabilidad de $A$ dado $B$ o condicional a $B$.

##### Ejemplo:
Sea $\Omega=\{ 1,\dots,6 \}$ para el experimento de lanzar un dado. Sean $A=$ par, $B=$ impar, $C=$ primo, $D=\{ 2 \}$.
Entonces tenemos que $P(A)=P(B)=P(C)=\frac{1}{2}$ y $P(D)=\frac{1}{6}$.
Si queremos calcular, por ejemplo, la probabilidad de que el dado caiga en 2, dado que sabemos que cayó en par, calculariamos:
$$
	P(D|A)=\frac{P(D\cap A)}{P(A)}=\frac{P(\{ 2 \})}{1 / 2}=\frac{1 / 6}{1 / 2}=\frac{1}{3}.
$$
Otro ejemplo, sería la probabilidad de que salga impar, dado que cayó par, tenemos 
$$
	P(B|A)=\frac{P(B\cap A)}{P(A)}=\frac{P(\emptyset)}{P(A)}=0.
$$

***NOTA:*** La probabilidad condicional de un evento $A$ dado $B$ puede ser igual, mayor o menor a la probabilidad del evento $A$ sin condicionar.

Vamos a demostrar que la medida de probabilidad condicional cumple los [[ProbabilidadAxiomatica|axiomas de Kolmogorov]].
1. $P(\Omega|A)=1$.
   **Sol:**
   $P(\Omega|A)=\frac{P(\Omega \cap A)}{P(A)}=\frac{P(A)}{P(A)}=1.$
2. $P(A|B)\geq 0$.
   **Sol:**
   Sabemos que $P(A|B)=\frac{P(A\cap B)}{P(B)}$ dónde $P(A\cap B)\geq0$ y $P(B)\geq 0$, por lo tatno el cociente es no negativo.
3. $P\left( \bigcup_{i=1}^{\infty}A_{i}|B \right)=\sum_{i=1}^{\infty}P(A_{i}|B)$ siempre que $A_{i}\cap A_{j}=\emptyset$ para $i\neq j$.
   Para el caso de aditividad por pares 
   $$
	\begin{align}
	P(A_{1}\cup A_{2}|B)=\frac{P((A_{1}\cup A_{2})\cap B)}{P(B)}&=\frac{P((A_{1}\cap B)\cup(A_{2}\cap B)}{P(B)} \\
	&=\frac{P(A_{1}\cap B)+P(A_{2}\cap B)}{P(B)} \\
	&=P(A_{1}|B)+P(A_{2}|B).
	\end{align}
   $$

### Regla del producto
Sean $A_{1},\dots,A_{n}$ eventos tales que $P(A_{1}\cap A_{2}\cap\dots \cap A_{n})\geq 0$. Demuestre que 
$$
	P(A_{1}\cap A_{2}\cap\dots A_{n})=P(A_{1})P(A_{2}|A_{1})P(A_{3}|A_{1}\cap A_{2})\dots(P(A_{n}|A_{1}\cap\dots \cap A_{n-1})).
$$
##### Demostración:
Tenemos que 
$$
	\begin{align}
	P(A_{1})P(A_{2}|A_{1})\dots(P(A_{n}|A_{1}\cap\dots \cap A_{n-1}))= \\
	P(A_{1}) \frac{P(A_{2}\cap A_{1})}{P(A_{1})} \frac{P(A_{3}\cap A_{2}\cap A_{1})}{P(A_{1}\cap A_{2})}\dots \frac{P(An\cap A_{1}\cap\dots \cap A_{n-1})}{P(A_{1}\cap \dots \cap A_{n-1})},
	\end{align}
$$
los términos se cancelan de forma telescópica y solo sobrevive 
$$
	P(A_{1}\cap A_{2}\cap\dots \cap A_{n}).
$$


#Probabilidad