##### Definición:
Sea $\Omega$ un [[PrincipiosDeProbabilidad|espacio muestral]] de cardinalidad finita y equiprobable. 
La probabilidad clásica de un evento $A$ definido sobe $\Omega$ está dada de la siguiente manera: 
$$
	P(A)=\frac{\#A}{\#\Omega}.
$$
Esta fue la primera forma de probabilidad que se definió formalmente.

##### Ejercicio:
¿Cuál es la probabilidad de encontrar al menos dos personas con la misma fecha de cumpleaños en un grupo de $n$ personas?
##### Solución:
Para este problema, conviene calcular la probabilidad de que los $n$ individuos tengan fechas de cumpleaños distintas. 
Sea $\Omega=\{ 1,2,\dots,365 \}$ ($\#\Omega=365$) todos los cumpleaños posibles.
Si tomamos una persona al azar y anotamos su cumpleaños. Sea $A=$ otra persona tiene un cumpleaños distinto, entonces tenemos $\# A = 364$ (quitamos el cumpleaños de la pesrona anterior), y entonces $P(A)=\frac{364}{365}$. 
Sea $B=$ las dos personas no comparten cumpleaños, entonces tenemos que
$$
	P(B)=\frac{365}{365}\cdot \frac{364}{365}.
$$
Podemos repetir este proceso $n$ veces.
Sea $N=n$ personas no comparten un cumpleaños, entonces podemos calcular la probabilidad como 
$$
	P(N)=\frac{365! / (365-n)!}{365^{n}}.
$$
De esta forma, podemos calcular la probabilidad que originalmente queríamos. Sea $K$ la probabilidad de que al menos dos personas compartan cumpleaños, entonces $K^{c}=N$, y por lo tanto $P(K)=1-P(K^{c})=1-P(N)$, es decir que 
$$
	P(K)=1-P(N)=\frac{365!}{365^{n}(365-n)!}.
$$

##### Ejemplo
Se lanzan dos dados indistinguibles y se suman los resultados. En un juego de apuestas, gana quien acierte la suma. ¿Cuáles son los mejores números para apostar?
##### Solución:
Primero definimos nuestro espacio muestral $\Omega =\{ \{ (1,1),(1,2),\dots,(1,6),(2,2),\dots,(2,6),(3,3),\dots,(4,4),\dots,(5,5),(6,6) \}$, con $\#\Omega =21$.
Entonces podemos calcular las probabilidades de cada suma:
$$
	\begin{align}
	P(\text{suma=2})&=P(\{ (1,1) \})=\frac{1}{21}, \\
	P(\text{suma=3})&=P(\{ (1,2) \})=\frac{1}{21}, \\
	P(\text{suma=4})&=P(\{ (2,2),(1,3) \})=\frac{2}{21}, \\
	P(\text{suma=5})&=P(\{ (2,3),(1,4) \})=\frac{2}{21}, \\
	P(\text{suma=6})&=\frac{3}{21}, \\
	P(\text{suma=7})&=\frac{3}{21}, \\
	P(\text{suma=8})&=\frac{3}{21}, \\
	\text{etc.}
	\end{align}
$$
Como después del 8 se repiten los primeros 4 resultados, entonces los mejores números son 6, 7 y 8.


#Probabilidad