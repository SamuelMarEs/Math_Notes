#AlgebraLineal 
#### Definición:
Un producto interno sobre un espacio vectorial $V$ es una operación binaria 
$$
	\langle,\rangle:V^{2}\to F
$$
tal que $\forall x,y,z\in V$ y $c\in F$,
a) $\langle x+z,y\rangle = \langle x,y\rangle+\langle z,y\rangle$.
b) $\langle cx,y\rangle = c\langle x,y\rangle$.
c) $\overline{\langle x,y\rangle}=\langle y,x\rangle$.
d) $\langle x,x\rangle \geq0\forall x\in V$.

#### Teorema 6.1 (propiedades):
1..- $\langle x,y+z\rangle = \langle x,y\rangle+\langle x, z\rangle$.
2.- $\langle x,cy\rangle=c\langle x,y\rangle$.
3.- $\langle x,0\rangle=\langle 0,x\rangle=0$.
4.- $\langle x, x\rangle=0\Longleftrightarrow x=0$. 
5.- $\langle x,y\rangle=\langle x,z\rangle \implies z=y$.
##### Demostración:
1.- $\langle x, y+z\rangle=\overline{\langle y+z, x\rangle}=\overline{\langle y,x\rangle+\langle z, x\rangle}=\overline{\langle y,x\rangle}+\overline{\langle z,x\rangle}=\langle x,y\rangle+\langle x,z\rangle$.
2.- 

#### Definición:
La ***norma*** o ***longitud*** de un vector $x\in V$ es 
$$
	\lvert \lvert x \rvert  \rvert =\sqrt{ \langle x,x\rangle }.
$$

#### Teorema 6.2:
1.- $\lvert \lvert cx \rvert \rvert=\lvert c \rvert\cdot\lvert \lvert x \rvert \rvert$.
2.- $\lvert \lvert x \rvert \rvert\geq 0\forall x\in V$, y $\lvert \lvert x \rvert \rvert=0 \iff x=0$.
3.- Desigualdad de Cauchy-Schwarz. $\lvert\langle x,y\rangle\rvert \leq \lvert \lvert x \rvert \rvert\cdot \lvert \lvert y \rvert \rvert$.
4.- Desigualdad del triángulo. $\lvert \lvert x+y \rvert \rvert\leq \lvert \lvert x \rvert \rvert+\lvert \lvert y \rvert \rvert$.

### Algunos productos internos
##### Producto interno estandar
Sean $x,y\in F^{n}$, entonces $$\langle x,y\rangle=\sum_{i=1}^{n}x_{i}\overline{y_{i}}$$
##### Producto interno de Frobenius
Sean $A,B\in M_{n\times n}$, entonces 
$$
	\langle A,B\rangle=\text{traza}(B^{*}A),
$$
dónde $B^{*}$ denota la matriz adjunta de $B$, es decir $(B^{*}_{ij})=\overline{(B_{ji})}$.

#### Definición:
Sea $V$ un espacio vectorial con producto interno. Decimos que $x$ y $y$ son ortogonales si $$\langle x,y\rangle=0.$$
