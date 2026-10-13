#AlgebraLineal 
#### Definición:
Una base $\{ v_{1},v_{2},\dots v_{n} \}$ de un espacio vectorial $V$ es una base ortonormal si satisface que:
- Todos los vectores son [[ProductoInterno|ortogonales]] dos a dos. $v_{i}\perp v_{j},\forall i\neq j,\quad i,j=1,2,\dots,n$.
- Todos los vectores son unitarios. Es decir que $\lvert \lvert v_i \rvert \rvert=1,\forall i=1,\dots,n$.

#### Teorema 6.3
Sea $V$ un espacio vectorial con [[ProductoInterno|producto interno]] $\langle\cdot,\cdot\rangle$, y sea $S=\{ v_{1},v_{2},\dots,v_{k} \}$ un conjunto ortogonal (todos los vectores son ortogonales 2 a 2). Si $w\in \mathrm{span}(S)$, entonces 
$$
	w=\sum_{i=1}^{k} \frac{\langle w,v_{i}\rangle}{\lvert \lvert v_{i} \rvert  \rvert^{2} }v_{i}.
$$
##### Demostración:
Sea $w\in \mathrm{span}(S)$, por definición existen escalares tales que 
$$
	w=\sum_{i=1}^{k}c_{i}v_{i}.
$$
Observemos que el producto interno de $w$ con cualquier vector de $S$ está dado por 
$$
	\langle w,v_{i}\rangle=\left\langle  \sum_{j=1}^{k}c_{j}v_{j},v_{i} \right\rangle=\sum_{j=1}^{k} c_{j}\langle v_{j},v_{i}\rangle=c_{i}\langle v_{i}, v_{i}\rangle.
$$
pues como el conjunto es ortogonal, tenemos que los términos de la suma con $i\neq j$ tienen que $\langle v_{i},v_{j}\rangle=0$.
Con esto concluimos que 
$$
	c_{i}=\frac{\langle w,v_{i}\rangle}{\langle v_{i},v_{i}\rangle}=\frac{\langle w, v_{i}\rangle}{\lvert \lvert v_{i} \rvert  \rvert ^{2}}.\quad\square
$$
##### Corolario
Si además $S$ es una [[BasesOrtonormales|ortonormal]], entonces los coeficientes son únicamente el producto interno $\langle w,v_{i}\rangle$.




