#### Ejemplo
Una prueba de sangre detecta correctamente a una persona enferma con una probabilidad de 0.98.
Sean los eventos $T=$ test positivo, $E=$ persona enferma, $S=$ persona sana, $N=$ test negativo.
La probabilidad que conocemos es $P(T|E)=0.99$, esta es, la probabilidad de tener un test positivo dado que sabemos que tenemos la enfermedad. Sin embargo, ¿qué sucede si queremos saber la probabilidad de que tengamos la enfermedad, dado que tuvimos un test positivo? Es decir queremos $P(E|T)$.
Notemos que conocemos $P(N|E)=0.01$ (probabilidad de un test negativo dado que tenemos la enfermedad), $P(N|S)=0.98$ (probabilidad de un test negativo dado que no tenemos la enfermedad), $P(T|S)=0.02$ (probabilidad de un test positivo dado que no tenemos la enfermedad).
Nuestro problema es que queremos calcular la [[ProbabilidadCondicional|probabilidad condicional]], pero por así decirlo "al revés". Para esto existe el Teorema de Bayes.

#### Teorema de Bayes/Teorema de probabilidad inversa
Sea $A$ un evento y sean $B_{1},\dots,B_{n}$ una partición del espacio muestral $\Omega$. Entonces 
$$
	P(B_{i}|A)=\frac{P(A|B_{i})P(B_{i})}{\sum_{j=1}^{n}P(A|B_{j})P(B_{j})}.
$$
##### Demostración:
Por definición de probabilidad condicional sabemos que 
$$
	P(B_{i}|A)=\frac{P(B_{i}\cap A)}{P(A)},
$$
y basta multiplicar por $\frac{P(B_{i})}{P(B_{i})}$ para obtener que 
$$
	P(B_{i}|A)=\frac{P(B_{i}\cap A)}{P(A)}\frac{P(B_{i})}{P(B_{i})}=\frac{P(A|B_{i})P(B_{i})}{P(A)}.
$$
Entonces, por la [[LeyProbabilidadTotal|ley de probabilidad total]], sabemos que al tener nuestra partición, se cumple que 
$$
	P(A)=\sum_{j=1}^{n}P(A|B_{j})P(B_{j}),
$$
y por lo tanto tenemos que 
$$
	P(B_{i}|A)=\frac{P(A|B_{i})P(B_{i})}{\sum_{j=1}^{n}P(A|B_{j})P(B_{j})}.\quad\square
$$

#### Continuacion ejemplo
Tenemos los eventos $E=$ persona enferma, $S=$ persona sana, $T=$ test positivo, $N=$ test negativo.
Además conocemos las probabilidades $P(T|E)=0.99$, $P(N|E)=0.01$, $P(T|S)=0.02$, $P(N|S)=0.98$.
Si queremos la probabilidad de tener la enfermedad, dado que el test fue positivo, usamos el teorema de Bayes: 
$$
	P(E|T)=\frac{P(T|E)P(E)}{P(T)}.
$$
No conocemos la probabilidad de un test positivo por si sola, entonces, por la [[LeyProbabilidadTotal|ley de probabilidad total]], tenemos 
$$
	P(E|T)=\frac{P(T|E)P(E)}{P(T|E)P(E)+P(T|S)P(S)}.
$$
Entonces, la única información que nos falta es la probabilidad de estar enfermo o de estar sano.
Si suponemos que estamos tratando con una enfermedad muy rara, podemos suponer que $P(E)=\frac{1}{1000000}$, y por consiguiente $P(S)=\frac{999999}{1000000}$. 
Entonces tenemos que 
$$
	\begin{align}
	P(E|T)&=\frac{(0.99)(1 / 1000000)}{(0.99)(1 / 1000000)+(0.02)(999999 / 1000000)} \\
	&= 4.94\times 10^{-5}.
	\end{align}
$$
¿Cómo interpretamos esto? En este caso, dado que se esta tratando con una enfermedad MUY rara, es bastante probable que el test se hubiera equivocado.


#Probabilidad #Teorema