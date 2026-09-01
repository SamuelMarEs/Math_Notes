#### Ejemplo
Una prueba de sangre detecta correctamente a una persona enferma con una probabilidad de 0.98.
Sean los eventos $T=$ test positivo, $E=$ persona enferma, $S=$ persona sana, $N=$ test negativo.
La probabilidad que conocemos es $P(T|E)=0.98$, esta es, la probabilidad de tener un test positivo dado que sabemos que tenemos la enfermedad. Sin embargo, ¿qué sucede si queremos saber la probabilidad de que tengamos la enfermedad, dado que tuvimos un test positivo? Es decir queremos $P(E|T)$.
Notemos que conocemos $P(N|E)=0.02$ (probabilidad de un test negativo dado que tenemos la enfermedad), $P(N|S)=0.98$ (probabilidad de un test negativo dado que no tenemos la enfermedad), $P(T|S)=0.02$ (probabilidad de un test positivo dado que no tenemos la enfermedad).
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


#Probabilidad #Teorema