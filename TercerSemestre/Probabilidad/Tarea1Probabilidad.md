Samuel Márquez Estrada

1.- Determine un espacio muestral para el experimento aleatorio consistente en:
   - Observar la posición de una partícula en un instante dado, la cual se mueve sin restricciones en un espacio tridimensional.
     **Sol:** $\Omega = \mathbb{R}^{3}$. Todas las coordenadas posibles de la partícula.
   - Registrar el número de personas que requieren hospitalización en el siguiente accidente automovilístico atendido por los servicios de emergencia de una localidad dada.
     **Sol:** $\Omega=\{ 0,1,2,\dots \}$. Enteros no negativos. Podrían ser 0 personas que requieran hospitalización, o si el accidente es muy grande, cualquier número entero de personas.
   - Lanzar un dado hasta que se obtiene un "6".
     **Sol:** $\Omega=\mathbb{N}$. El número de veces que se lanzó el dado.
     $\Omega =\{ (a_{1},a_{2},\dots,a_{n-1},6):n\in\mathbb{N}, a_{i}\in \{ 1,2,3,4,5 \} \}$. Todos los resultados posibles en $n$ lanzamientos para que salga el 6.
   - Registrar la fecha de cumpleaños de $n$ personas escogidas al azar.
     **Sol:** $\Omega=\{ (x_{1},x_{2},\dots,x_{n}):x_{i}\in \{ 1,2,\dots,365 \} \}$. Todas las posibles $n$-adas posibles con números del 1 al 365.
   - Observar la forma en la que $r$ personas que abordan un elevador en la planta baja de un edificio descienden en los pisos $1,2,\dots,n$.
     **Sol:** $\Omega=\{ (x_{1},1),(x_{2},2),\dots,(x_{n},n) \}$. Pares ordenados dónde $x_{i}$ es el número de personas que se bajan en el piso $i$, y $\sum_{i=1}^{n}x_{i}=r$.
   - Registrar la duración de una llamada telefónica escogida al azar.
     **Sol:** $\Omega=\mathbb{R}-\mathbb{R}^{-}=[0,\infty)$. El número de minutos (número no negativo) que duró la llamada.
   - Observar el número de años que le restan de vida a una persona escogida al azar dentro del conjunto de asegurados de una compañía aseguradora.
     **Sol:** $\Omega=\mathbb{Q}^{+}\cup \{ 0 \}$. El número de años en forma racional no negativa. 
     O $\Omega=\{ 0,1,\dots,130 \}$ igual el número de años.

2.- Considere el experimento aleatorio de lanzar dos dados distinguibles. Escriba explícitamente los resultados asociados a los siguientes eventos y determine su cardinalidad.
- $A=$"la suma de los dos resultados es 7."
  **Sol:** $$A=\{ (1,6),(6,1),(2,5),(5,2),(3,4),(4,3) \}.$$ $\#A=6$.
- $B=$"Uno de los dos dados cae en número impar y el otro en número par."
  **Sol:** $$\begin{align}
  B=\{ &(1,2),(2,1),(1,4),(4,1),(1,6),(6,1), \\
  &(3,2),(2,3),(3,4),(4,3),(3,6),(6,3), \\
  &(5,2),(2,5),(5,4),(4,5),(5,6),(6,5) \}.
  \end{align}$$
  $\#B=18$.
- $C=$"El resultado de un dado difiere del otro en, a lo sumo, una unidad."
  **Sol:** 
  $$
	\begin{align}
	C=\{ &(1,1),(2,2),(3,3),(4,4),(5,5), \\
	 &(6,6),(1,2),(2,1),(2,3),(3,2), \\
	 &(3,4),(4,5),(5,4),(5,6),(6,5)\}.
	\end{align}
  $$
  $\#C=15.$
- $D=$"El resultado de un dado difiere del otro en por lo menos cuatro unidades."
  **Sol:** 
  $$
	D=\{ (1,5),(1,6),(5,1),(6,1),(2,6),(6,2) \}.
  $$
  $\#D=6$.
- $E=A\cap B.$
  **Sol:** 
  $$
	A\cap B=A=\{ (1,6),(6,1),(2,5),(5,2),(3,4),(4,3) \}.
  $$
  $\#(A\cap B)=\#A=6.$
- $F=B^{c}$.
  **Sol:** 
  $$
	\begin{align}
	F=\{ &(1,1),(1,3),(3,1),(1,5),(5,1),(3,3), \\
	&(3,5),(5,3),(5,5),(2,2),(2,4),(4,2), \\
	&(2,6),(6,2),(4,4),(4,6),(6,4),(6,6)\}.
	\end{align}
  $$
  $\#F=18$.
- $G=C\cup D.$
  **Sol:** 
  $$
	\begin{align}
	G=\{ &(1,1),(2,2),(3,3),(4,4),(5,5), \\
	 &(6,6),(1,2),(2,1),(2,3),(3,2), \\
	 &(3,4),(4,5),(5,4),(5,6),(6,5), \\
	 &(1,5),(1,6),(5,1),(6,1),(2,6),(6,2)  \}.
	\end{align}
  $$
  $\#G=21$.

3.- **Señales.** Se transmiten cuatro señales consecutivas en un canal de comunicación. Debido al ruido que se presenta en el canal, cada señal se recibe bien o con distorsión. Defina el evento $D_{i}$ como aquél que indica que la $i$-ésima señal está distorsionada. Exprese los siguientes sucesos en términos de los eventos $D_{i}$.
- Sólo una señal está distorsionada.
  **Sol:** $$A=\bigcup_{i,j,k,l\in \{ 1,2,3,4 \}}D_{i}\cap D_{j}^{c}\cap D_{k}^{c}\cap D_{l}^{c}$$
  con $i\neq j\neq k\neq l$.
- Sólo dos señales están distorsionadas.
  **Sol:** $$B=\bigcup_{i,j,k,l\in \{ 1,2,3,4 \}} D_{i}\cap D_{j}\cap D_{k}^{c}\cap D_{l}^{c}$$ con $i\neq j\neq k\neq l$.
- Sólo hay dos señales distorsionadas y son consecutivas.
  **Sol:** 
  $$
	C=\bigcup D_{i}\cap D_{i+1}\cap D_{j}^{c}\cap D_{k}^{c}
  $$
  con $i\neq j\neq k$, $i\in \{ 1,2,3 \}$ y $j,k\in \{ 1,2,3,4 \}-\{ i,i+1 \}$.
- No hay dos señales consecutivas distorsionadas.
  **Sol:** $$D=(D_{1}^{c}\cap D_{2}^{c}\cap D_{3}^{c}\cap D_{4}^{c})\cup(A)\cup(B-C).$$
  O no hay ninguna señal distorsionada $(D_{1}^{c}\cap D_{2}^{c}\cap D_{3}^{c}\cap D_{4}^{c})$, o solo hay una $(A)$, o hay dos no consecutivas $(B-C)$.
- Por lo menos hay dos señales consecutivas distorsionadas.
  **Sol:** $$E=C\cup(\bigcup_{i,j,k,l\in \{ 1,2,3,4 \}} D_{i}\cap D_{j}\cap D_{k}\cap D_{l}^{c})\cup(D_{i}\cap D_{j}\cap D_{k}\cap D_{l}).$$ Hay solo dos consecutivas distorsionada $(C)$, o hay tres distorsionadas, o hay cuatro distorsionadas.


4.- Considere el experimento aleatorio de escoger al azar dos números $x$ y $y$ del intervalo unitario $(0,1)$. El espacio muestral $\Omega$ para este experimento es entonces el producto cartesiano $(0,1)\times(0,1)$. Represente en un plano cartesiano este espacio muestral e identifique los siguientes eventos:
- $A=\{ (x,y)\in \Omega : x>1 / 2,y<1 / 2\}$.
- $B=\{ (x,y)\in \Omega : x<2y\quad\text{ó}\quad y<1 /2 \}$.
- $C=\{ (x,y)\in \Omega : x^{2}+y^{2}<1\}-\{ (x,y)\in \Omega : y<x \}$.
- $D=\{ (x,y)\in \Omega : |x-y|<1 / 4\quad\text{ó}\quad |1-x-y|<1 / 4\}$.
**Sol:**
![[Tarea1Proba]]

5.- Sean $A,B$ dos eventos cualesquiera de un experimento aleatorio con espacio muestral finito y equiprobable. Demuestre que la definición de probabilidad clásica satisface las siguientes propiedades:
- $P(\emptyset)=0$.
  **Sol:** $P(\emptyset)=\frac{\#\emptyset}{\#\Omega}=\frac{0}{\#\Omega}=0.\quad\square$
- $P(\Omega)=1$.
  **Sol:** $P(\Omega)=\frac{\#\Omega}{\#\Omega}=1.\quad\square$
- $P(A)\geq 0$ para cualquier evento $A$.
  **Sol:** Si $A=\emptyset$, entonces $P(A)=0$. De lo contrario, $\#A>0$, y por lo tanto $P(A)=\frac{\#A}{\#\Omega}>0$. Entonces tenemos que $P(A)\geq 0$ para todo $A.\quad\square$
- $P(A^{c})=1-P(A)$.
  **Sol:** $$1=P(\Omega)=P(A\cup A^{c})=\frac{\#(A\cup A^{c})}{\#\Omega}=\frac{\#A+\#A^{c}}{\#\Omega}=P(A)+P(A^{c})\implies P(A^{c})=1-P(A).\quad\square$$
- Si $A\subset B$ entonces $P(A)\leq P(B)$.
  **Sol:** Sea $A\subset B$, entonces $\#A\leq\#B$, por lo tanto $P(A)=\frac{\#A}{\#\Omega}\leq \frac{\#B}{\#\Omega}=P(B).\quad\square$
- $P(A\cup B)=P(A)+P(B)$ cuando $A,B$ son ajenos.
  **Sol:** Sean $A,B$ ajenos, entonces 
  $$
	P(A\cup B)=\frac{\#(A\cup B)}{\#\Omega}=\frac{\#A+\#B}{\#\Omega}=\frac{\#A}{\#\Omega}+\frac{\#B}{\#\Omega}=P(A)+P(B).\quad\square
  $$ 
- $P(A\cup B)=P(A)+P(B)-P(A\cap B)$.
  **Sol:** Sean $A,B$ cualesquiera eventos, entonces 
  $$
	P(A\cup B)=\frac{\#(A\cup B)}{\#\Omega}=\frac{\#A+\#B-\#(A\cap B)}{\#\Omega}=P(A)+P(B)-P(A\cap B).\quad\square
  $$

6.- El juego de una feria consiste en pedirle a un jugador que arroje al azar 4 monedas equilibradas, una a la vez. Suponga que las monedas son de una unidad monetaria y están marcadas con "cara" y "cruz". Si algún lanzamiento cae "cara", la moneda es recogida por el jugador y se le entrega una moneda adicional de la misma denominación como premio. Por otro lado, el jugador pierde cualquier moneda que caiga "cruz". Determine el número posible de monedas que el jugador puede tener al final del juego y las probabilidades de cada uno de estos resultados.
**Sol:** El jugador puede quedar con
- 0 monedas si pierde los 4 lanzamientos. Evento $A$.
- 2 monedas si gana solo un lanzamiento. Evento $B$.
- 4 monedas si gana dos lanzamientos. Evento $C$.
- 6 monedas si gana tres lanzamientos. Evento $D$.
- 8 monedas si gana los cuatro lanzamientos. Evento $E$.
Tenemos entonces que $\Omega=\{ x\in\mathbb{Z}_{2}^{4} \}$ con $\#\Omega=2^{4}=16$.
$P(A)=\frac{1}{16}=P(E)$ pues solo hay una forma de perder 4 lanzamientos, o de ganarlos.
$P(B)=\frac{1}{4}=P(D)$ pues hay $\begin{pmatrix}4 \\  1\end{pmatrix}=4$ formas de solo ganar un lanzamiento o de ganar tres (que es lo mismo que solo perder uno).
Por último, $P(C)=\frac{3}{8}$ pues hay $\begin{pmatrix}4 \\  2\end{pmatrix}=6$ formas de ganar 2 lanzamientos de moneda.

7.- Se escogen dos números $x$ y $y$ al azar dentro del intervalo unitario $[0,1]$. ¿Cuál es la probabilidad de que la suma de estos números sea mayor a uno y que, al mismo tiempo, la suma de sus cuadrados sea menor a uno?
**Sol:** Este problema se puede resolver con probabilidad geométrica. El espacio muestral $\Omega=[0,1]\times[0,1]$ cuya área es 1. Solo queda calcular el área del evento $A=\{ (x,y):x^{2}+y^{2}<1\quad\text{y}\quad x+y>1 \}$. Esta es el área acotada entre las gráficas de las curvas $x^{2}+y^{2}=1$ y $y=1-x$,  o también se puede ver como el área de un cuarto de círculo de radio 1, área $=\frac{\pi}{4}$, menos el área del triángulo formado por $y=1-x$ y los ejes coordenados, que es un triángulo de base 1 y altura 1, con área $=\frac{1}{2}$. Entonces $\text{área}(A)=\frac{\pi-2}{4}$, y por lo tanto 
$$
	P(A)=\frac{(\pi-2) /4}{1}=\frac{\pi-2}{4}\approx 0.28.
$$


8.- Un pasajero llega en autobús a la estación de trenes. La hora de llegada del autobús es aleatoria entre las 9:00 y las 10:00 hrs. Por otro lado, el tren que debe tomar el pasajero parte de la estación también al azar entre las 9:00 y las 10:00 hrs. El pasajero podrá subirse al tren si el autobús llega por lo menos cinco minutos antes de que el tren parta. ¿Cuál es la probabilidad de que el pasajero aborde el tren?
**Sol:** Nuestro espacio muestral es $\Omega =[0,60]\times[0,60]$ que son pares ordenados, con la primera coordenada la hora a la que llega el autobús (expresado como minutos después de las 9:00), y la segunda, la hora a la que sale el tren.
Nuestro evento es $A=\{ (x,y):y-x>5 \}$. El área de $\Omega$ es $60\times 60=360$, mientras que el área de $A$ es el área de un triángulo que corta al eje $y$ en $y=5$, y queremos que se detenga en $y=60$, es decir en $x=55$. Por lo tanto, es un triángulo de altura 55 y base 55. Entonces la probabilidad del evento $A$ esta dada por:
$$
	P(A)=\frac{55^{2}}{60^{2}}=\left( \frac{55}{60} \right)^{2}=\left( \frac{11}{12} \right)^{2}=\frac{121}{144}\approx0.84.
$$

9.- **Triángulos 1.** Se escogen dos números $x$ y $y$ al azar de manera independiente uno del otro, dentro del intervalo $[0,\ell]$. Calcule la probabilidad de que las longitudes $x,y$ y $\ell$ formen un triángulo. 
**Sol:** Nuestro espacio muestral es $\Omega=[0,\ell]\times[0,\ell]$. Nuestro evento es $A=\{ (x,y):x+y>\ell \}$. El área de este evento está dada por un triángulo de altura y base $\ell$, por lo tanto tenemos que
$$
	P(A)=\frac{\text{área}(A)}{\text{área}(\Omega)}=\frac{\ell^{2} / 2}{\ell^{2}}=\frac{1}{2}=0.5
$$

10.- Sean $A,B$ dos eventos cualesquiera de un experimento aleatorio. Demuestre que la definición de probabilidad frecuentista satisface las siguientes propiedades:
- $P(\emptyset)=0$.
  **Sol:** Sea $n_{\emptyset}$ el número de ocurrencias de ningún evento en $n$ experimentos, entonces $n_{\emptyset}=0$ para cualquier $n$, pues algo tiene que ocurrir, por lo tanto $$P(\emptyset)=\lim_{ n \to \infty } \frac{n_{\emptyset}}{n}=0.\quad\square$$
- $P(\Omega)=1$.
  **Sol:** Sea $n_{\Omega}$ el número de ocurrencias de cualquier evento en $n$ experimentos, entonces $n_{\Omega}=n$, y por lo tanto $$P(\Omega)=\lim_{ n \to \infty } \frac{n}{n}=1.\quad\square$$
- $P(A)\geq 0$ para cualquier evento $A$.
  **Sol:** Un evento $A$ no puede ocurrir una cantidad negativa de veces. Si no ocurre ninguna vez, entonces $n_{A}=0$, de lo contrario, $n_{A}>0$, por lo tanto tenemos que $\frac{n_{A}}{n}\geq 0$ para cualquier $n$, es decir que $$P(A)=\lim_{ n \to \infty } \frac{n_{A}}{n}\geq 0.\quad\square$$
- $P(A^{c})=1-P(A)$.
  **Sol:** Si el evento $A$ ocurrió $n_{A}$ veces en $n$ experimentos, entonces $A^{c}$ ocurrió $n_{A^{c}}=n-n_{A}$ veces, por lo tanto $$P(A^{c})=\lim_{ n \to \infty } \frac{n_{A^{c}}}{n}=\lim_{ n \to \infty }  \frac{n-n_{A}}{n}=1-\lim_{ n \to \infty } \frac{n_{A}}{n}=1-P(A).\quad\square$$
- Si $A\subset B$ entonces $P(A)\leq P(B)$.
  **Sol:** Sea $A\subset B$, entonces cada vez que ocurre $A$, también está ocurriendo $B$, por lo tanto $n_{A}\leq n_{B}\implies \frac{n_{A}}{n}\leq \frac{n_{B}}{n}$, entonces 
  $$
	\lim_{ n \to \infty } \frac{n_{A}}{n}\leq \lim_{ n \to \infty } \frac{n_{B}}{n}\implies P(A)\leq P(B).\quad\square
  $$
- $P(A\cup B)=P(A)+P(B)$ cuando $A,B$ son ajenos.
  **Sol:** Sean $A$ y $B$  eventos ajenos, entonces no pueden ocurrir al mismo tiempo, por lo tanto $A\cup B$ ocurre $n_{A\cup B}=n_{A}+n_{B}$ veces, y por lo tanto 
  $$
	P(A\cup B)=\lim_{ n \to \infty } \frac{n_{A\cup B}}{n}=\lim_{ n \to \infty } \frac{n_{A}+n_{B}}{n}=\lim_{ n \to \infty } \frac{n_{A}}{n}+\lim_{ n \to \infty } \frac{n_{B}}{n}=P(A)+P(B).\quad\square
  $$
- $P(A\cup B)=P(A)+P(B)-P(A\cap B)$.
  **Sol:** Sean $A$ y $B$ dos eventos cualesquiera. Entonces ambos eventos ocurren las veces que ocurre $A$ y las veces que ocurre $B$ por separado, pero al contar las veces que ocurrió $A$, también contamos las veces que ocurrió $B$ al mismo tiempo. Por lo tanto tenemos que $n_{A\cup B}=n_{A}+n_{B}-n_{A\cap B}$, y por lo tanto 
  $$
	P(A\cup B)=\lim_{ n \to \infty } \frac{n_{A\cup B}}{n}=\lim_{ n \to \infty } \frac{n_{A}+n_{B}-n_{A\cap B}}{n}=P(A)+P(B)-P(A\cap B).\quad\square
  
  $$
  

#Probabilidad