Samuel Márquez Estrada
#### Sección 6.2 Friedberg
2.- En cada parte, aplicar el proceso Gram-Schmidt a los subconjuntos $S$ del espacio de producto interno $V$ para obtener una base ortogonal para $\mathrm{span}(S)$. Después, normaliza los vectores de la base para obtener una base ortonormal $\beta$ para $\mathrm{span}(S)$. Calcula los coheficientes de Fourier para cualquier vector relativo a $\beta$. Usa el Teorema 6.5 para verificar tu resultado.
a) $V=R^{3}$, $S=\{ (1,0,1),(0,1,1),(1,3,3) \}$, y $x=(1,1,2)$.
b) $V=R^{3}$, $S=\{ (1,1,1),(0,1,1),(0,0,1) \}$, y $x=(1,0,1)$.
c) $V=P_{2}(R)$ con producto interno $\langle f(x),g(x)\rangle=\int_{0}^{1}f(t)g(t)dt$, $S=\{ 1,x,x^{2} \}$, y $h(x)=1+x$.
d) $V=\mathrm{span}(S)$, $S=\{ (1,i,0),(1-i,2,4i) \}$, y $x=(3+i,4i,-4)$.
e) $V=R^{4}$, $S=\{ (2,-1,-2,4),(-2,1,-5,5),(-1,3,7,11) \}$, y $x=(-11,8,-4,18)$.
f) $V=R^{4}$, $S=\{ (1,-2,-1,3),(3,6,3,-1),(1,4,2,8) \}$, y $x=(-1,2,1,1)$.
g) $V=M_{2 \times 2}(R)$, $S=\left\{ \begin{pmatrix}3 & 5 \\  -1 & 1\end{pmatrix} , \begin{pmatrix}-1 & 9 \\  5 & -1\end{pmatrix}, \begin{pmatrix}7 & -17 \\  2 & -6\end{pmatrix}\right\}$, y $A=\begin{pmatrix}-1 & 2 \\  -4 & 8\end{pmatrix}$.
h) $V=M_{2\times 2}(R)$, $S=\left\{ \begin{pmatrix}2 & 2 \\  2 & 1\end{pmatrix} , \begin{pmatrix}11 & 4 \\  2 & 5\end{pmatrix}, \begin{pmatrix}4 & -12 \\  3 & -16\end{pmatrix}\right\}$, y $A=\begin{pmatrix}8 & 6 \\  25 & -13\end{pmatrix}$.
i) $V=\mathrm{span}(S)$ con producto interno $\langle f,g\rangle=\int_{0}^{\pi}f(t)g(t)dt$, $S=\{ \sin t, \cos t, 1, t \}$, $h(t)=2t+1$.
j) $V=C^{4}$, $S=\{ (1, i, 2-i, -1),(2+3i, 3i, 1-i, 2i),(-1+7i,6+10i,11-4i,3+4i) \}$, y $x=(-2+7i,6+9i,9-3i,4+4i)$.
k) $V=C^{4}$, $S=\{ (-4,3-2i,i,1-4i),(-1-5i,5-4i,-3+5i,7-2i),(-27-i,-7-6i,-15+25i,-7-6i) \}$, y $x=(-13-7i, -12+3i, -39-11i,-26+5i)$.
l) $V=M_{2 \times 2}(C), S=\left\{ \begin{pmatrix}1-i & -2-3i \\  2+2i & 4+i\end{pmatrix}, \begin{pmatrix}8i & 4 \\  -3-3i & -4+4i\end{pmatrix}, \begin{pmatrix}-25-38i & -2-13i \\  12-78i & -7+24i\end{pmatrix} \right\}$, y $A=\begin{pmatrix}-2+8i & -13+i \\  10-10i & 9-9i\end{pmatrix}.$
m) $V=M_{2 \times 2}(C), S=\left\{ \begin{pmatrix}-1+i & -i \\  2-i & 1+3i\end{pmatrix}, \begin{pmatrix}-1-7i & -9-8i \\  1+10i & -6-2i\end{pmatrix}, \begin{pmatrix}-11-132i & -34-31i \\  7-126i & -71-5i\end{pmatrix} \right\}$ y $A=\begin{pmatrix}-7+5i & 3+18i \\  9-6i & -3+7i\end{pmatrix}$.

4.- Sea $S=\{ (1,0,i),(1,2,1) \}$ en $C^{3}$. Calcula $S^{\perp}$.

5.- Sea $S_{0}=\{ x_{0} \}$, donde $x_{0}$ es un vector no cero en $R^{3}$. Describe $S_{0}^{\perp}$ geométricamente. Ahora supón que $S=\{ x_{1},x_{2} \}$ es un subconjunto linealmente independiente de $R^{3}$. Describe $S^{\perp}$ geométricamente.

7.- Sea $\beta$ una base del subespacio $W$ de un espacio de producto interno $V$, y sea $z\in V$. Demuestra que $z\in W^{\perp}$ si y sólo si $\langle z,v\rangle=0$ para todo $v\in \beta$.

19.- En cada una de las siguientes partes, encuentra la proyección ortogonal del vector dado sobre el subespacio $W$ del espacio de producto interno $V$.
a) $V=R^{2}$, $u=(2,6)$, y $W=\{ (x,y):y=4x \}$.
b) $V=R^{3}$, $u=(2,1,3)$, u $W=\{ (x,y,z):x+3y-2z=0 \}$.
c) $V=P(R)$ con producto interno $\langle f(x),g(x)\rangle=\int_{0}^{1}f(t)g(t)dt$, $h(x)=4+3x-2x^{2}$ y $W=P_{1}(R)$.

21.- Sea $V=C([-1,1])$ con producto interno $\langle f,g\rangle=\int_{-1}^{1}f(t)g(t)dt$ y sea $W$ el subespacio $P_{2}(R)$, visto como un espacio de funciones. Use la base ortonormal obtenida en el ejemplo 5 para calcular la "mejor" (más cercana) aproximación polinomial de segundo grado de la función $h(t)=e^{t}$ en el intervalo $[-1,1]$.

22.- Sea $V=C([0,1])$ con producto interno $\langle f,g\rangle=\int_{0}^{1}f(t)g(t)dt$. Sea $W$ es subespacio generado por el conjunto linealmente independiente $\{ t, \sqrt{ t } \}$.
a) Encuentra una base ortonormal de $W$.
b) Sea $h(t)=t^{2}$. Usa la base ortonormal para encontrar la "mejor" (más cercana) aproximación de $h$ en $W$.

