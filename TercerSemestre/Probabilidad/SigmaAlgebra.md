##### Definición:
Una colección $\mathcal{F}$ de subconjuntos de $\Omega$ (i.e. $\mathcal{F}\subset 2^{\Omega}$) se conoce como una ***álgebra*** si
1. $\Omega\in\mathcal{F}$.
2. Si $A\in\mathcal{F}$ entonces $A^{c}\in \mathcal{F}$.
3. Si $A_{1},A_{2},\dots,A_{n}\in\mathcal{F}$ entonces $\bigcup_{i=1}^{n}A_{i}\in\mathcal{F}$.

##### Definición:
Sea $\mathcal{F}$ una *álgebra*, si esta además cumple que, si $A_{1},A_{2},\dots\in\mathcal{F}$ entonces 
$$
	\bigcup_{i=1}^{\infty}A_{i}\in\mathcal{F},
$$
entonces decimos que $\mathcal{F}$ es una ***sigma álgebra*** ($\sigma$-álgebra).

##### Ejemplos:
1. $\mathcal{F}=\{ \Omega,\emptyset \}$ es una $\sigma$-álgebra.
2. $\mathcal{F}=\{ \Omega, A, A^{c},\emptyset \}$ es una $\sigma$-álgebra.
3. $\mathcal{F}=2^{\Omega}$ el conjunto potencia es una $\sigma$-álgebra.

### Sigma álgebra de Borel
La $\sigma$-álgebra de Borel de $\mathbb{R}$, denotada por $\mathcal{B}(\mathbb{R})$ es la mínima $\sigma$-álgebra de subconjuntos de $\mathbb{R}$ generada por los interalos $(-\infty,x]$. Esto se denota por 
$$
	\mathcal{B}(\mathbb{R})=\sigma \{ (-\infty,x]:x\in\mathbb{R} \}.
$$
A los elementos de $\mathcal{B}(\mathbb{R})$ se les conoce como conjuntos de Borel o borelianos.


##### Ejercicio:
Sean $A$ y $B$ dos eventos en $\mathcal{F}$ una $\sigma$-álgebra. Demostrar que:
1.  $\emptyset\in\mathcal{F}$.
**Sol:**
  Por definición $\Omega\in\mathcal{F}$, y por lo tanto $\emptyset=\Omega^{c}\in\mathcal{F}$.
  
2. $A\cap B\in\mathcal{F}$.
**Sol:**
  Como $A,B\in\mathcal{F}$, entonces $A^{c},B^{c}\in\mathcal{F}$, por lo tanto $A^{c}\cup B^{c}\in\mathcal{F}$, y por lo tanto 
  $$
	A\cap B=(A^{c}\cup B^{c})^{c}\in\mathcal{F}.
  $$
  
3. $A-B\in\mathcal{F}$.
**Sol:**
  Podemos reescribir $A-B=A\cap B^{c}$, y por hipótesis $B^{c}\in\mathcal{F}$, por lo tanto, por el inciso anterior, $A-B=A\cap B^{c}\in\mathcal{F}$.
  
4. $A\cup B^{c}\in\mathcal{F}$.
**Sol:**
  Como $B\in\mathcal{F}$, entonces $B^{c}\in\mathcal{F}$, y como es una sigma álgebra, es cerrada bajo uniones finitas, por lo tanto $A\cup B^{c}\in\mathcal{F}$.
  
5. $A\Delta B\in\mathcal{F}$.
**Sol:**
  $A\Delta B=(A- B)\cup(B- A)$. Por el inciso 3 $(A- B),(B-A)\in\mathcal{F}$, entonces como $\mathcal{F}$ es una sigma álgebra, la unión es cerrada, por lo tanto tenemos que $A\Delta B=(A- B)\cup(B- A)\in\mathcal{F}$.
  
6. $A-(A\cap B)\in\mathcal{F}$.
**Sol:**
  Por el segundo inciso $(A\cap B)\in\mathcal{F}$, entonces por el inciso 3 tenemos que $A-(A\cap B)\in\mathcal{F}$.



#Probabilidad