Samuel Márquez Estrada

##### Sección 6.1 Friedberg
3.- En $C([0,1])$, sea $f(t)=t$ y $g(t)=e^{t}$. Calcule $\langle f,g\rangle$, $\lvert \lvert f \rvert \rvert$, $\lvert \lvert g \rvert \rvert$, y $\lvert \lvert f+g \rvert \rvert$. Verifique entonces la desigualdad de Cauchy Schwarz y la desigualdad triangular. El producto interno definido como: 
$$
	\langle f,g\rangle=\int_{0}^{1}f(t)g(t)dt
$$
**Sol:**
$$
	\begin{align}
	\langle f,g\rangle=\int_{0}^{1}te^{t}dt=te^{t}|_{0}^{1}-\int_{0}^{1}e^{t}dt=(te^{t}-e^{t})|_{0}^{1}=1.
	\end{align}
$$
$$
	\lvert \lvert f \rvert  \rvert =\sqrt{ \int_{0}^{1}t^{2}dt }=\frac{1}{\sqrt{ 3 }}.
$$
$$
	\lvert \lvert g \rvert  \rvert =\sqrt{ \int_{0}^{1}e^{2t}dt }=\sqrt{\frac{1}{2}(e^{2}-1) }
$$
$$
	\lvert \lvert f+g \rvert  \rvert =\sqrt{ \int_{0}^{1}(t+e^{t})^{2}dt }= \sqrt{ \int_{0}^{1}t^{2}dt+\int_{0}^{1}2te^{t}+\int_{0}^{1}e^{2t} }=\sqrt{ \frac{1}{3}+2+\frac{1}{2}(e^{2}-1) }.
$$

6.- Pruebe los incisos b, c, d, e, del Teorema 6.1.
b) $\langle x,cy\rangle=\overline{c}\langle x,y\rangle$.
c) $\langle x,0\rangle=\langle 0,x\rangle=0$.
d) $\langle x, x\rangle=0\Longleftrightarrow x=0$. 
e) $\langle x,y\rangle=\langle x,z\rangle\forall x\in V \implies z=y$.
**Sol:**
b) $\langle x,cy\rangle=\overline{\langle cy, x\rangle}=\overline{c\langle y,x\rangle}=\overline{c}\overline{\langle y,x\rangle}=\overline{c}\langle x,y\rangle$.
c) $\langle x,0\rangle=\langle x,0y\rangle=0\langle x,y\rangle=0=0\langle y,x\rangle=\langle 0y, x\rangle=\langle 0,x\rangle$.
d) Por el inciso c), $x=0\implies\langle x,x\rangle=0$. Sea $\langle x,x\rangle=0$, vamos a demostrar por contradicción que entonces $x=0$. Supongamos $x\neq 0$, entonces $\langle x,x\rangle>0$, lo cual contradice la hipótesis inicial. Por lo tanto $x=0$.
e) Observemos que $\langle x,y\rangle=\langle x,z\rangle\implies\langle x,y\rangle-\langle x,z\rangle=0\implies \langle x, y-z\rangle=0$. Fijemos en particular $x=y-z$, es decir que $\langle y-z,y-z\rangle=0$, y por d) esto implica que $y-z=0$, i.e. $y=z$.

7.- Pruebe los incisos a y b del Teorema 6.2.
a) $\lvert \lvert cx \rvert \rvert=\lvert c \rvert\cdot\lvert \lvert x \rvert \rvert$.
b) $\lvert \lvert x \rvert \rvert\geq 0\forall x\in V$, y $\lvert \lvert x \rvert \rvert=0 \iff x=0$.
**Sol:**
a) $\lvert \lvert cx \rvert \rvert=\sqrt{ \langle cx, cx\rangle }=\sqrt{ c^{2}\langle x,x\rangle }=\lvert c \rvert\cdot \lvert \lvert x \rvert \rvert$.
b) Dado que $\langle x,x\rangle\geq 0$, entonces su raíz cuadrada es también no negativa. Más aún, el producto interno solo es cero si $x=0$, por lo tanto la raíz solo es cero en ese caso.

8.- Argumente porque los siguientes no son productos internos sobre sus espacios vectoriales correspondientes:
a) $\langle(a,b),(c,d)\rangle=ac-bd$ sobre $R^{2}$.
b) $\langle A,B\rangle=\text{tr}(A+B)$ sobre $M_{2\times 2}(R)$.
c) $\langle f(x), g(x)\rangle=\int_{0}^{1}f'(t)g(t)dt$ sobre $P(R)$.
**Sol:**
a) No cumple la propiedad d) del Teorema 6.1. Basta tomar $(1,1)$ y $(1,1)$, y vemos que ninguno es el vector cero, sin embargo su producto interno es cero.
b) No satisface el axioma b), puesto que $\text{tr}(cA+B)\neq c\cdot\text{tr}(A+B)$.
c) Si tomamos $f(t)=1=g(t)$, entonces $f'(t)=0$, por lo que el producto interno es cero, aún si el polinomio no es el polinomio cero, i.e. no se cumple la propiedad d) del Teorema 6.1.

11.- Pruebe la ley del paralelogramo de un producto interno sobre $V$. Es decir, pruebe que 
$$
	\lvert \lvert x+y \rvert  \rvert ^{2}+\lvert \lvert x-y \rvert  \rvert ^{2}=2\lvert \lvert x \rvert  \rvert^{2}+2\lvert \lvert y \rvert  \rvert ^{2}\quad\forall x,y\in V. 
$$
¿Qué nos dice esta ecuación sobre los paralelogramos en $R^{2}$?
**Sol:**


24.- Sea $V$ un espacio vectorial complejo con producto interno $\langle\cdot,\cdot\rangle$. Sea $[\cdot,\cdot]$ una función real tal que $[x,y]$ es la parte real del número complejo $\langle x,y\rangle$ para todos $x,y\in V$. Pruebe que $[\cdot,\cdot]$ es un producto interno para $V$, donde $V$ es un espacio vectorial sobre $R$. Pruebe, además, que $[x,ix]=0$ para todo $x\in V$.
**Sol:**


26.- Pruebe que las siguientes son normas sobre el espacio vectorial dado:
a) $V=R^{2}$: $\lvert \lvert (a,b) \rvert \rvert=\lvert a \rvert+\lvert b \rvert$ para todo $(a,b)\in V$.
b) $V=C([0,1])$: $\lvert \lvert f \rvert \rvert=\max_{t\in[0,1]}\lvert f(t) \rvert$ para toda $f\in V$.
c) $V=C([0,1])$: $\lvert \lvert f \rvert \rvert=\int_{0}^{1}\lvert f(t) \rvert dt$ para toda $f\in V$.
d) $V=M_{m\times n}(F)$: $\lvert \lvert A \rvert \rvert=\max_{i,j}\lvert A_{ij} \rvert$.
**Sol:**
a)
b)
c)
d)

