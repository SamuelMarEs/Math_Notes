Una matriz $A$ es un arreglo ordenado que tiene operaciones.
- Sean $A=[a_{ij}]$ y $B=[b_{ij}]$, definimos la suma $+$ como 
$$
	A+B=[c_{ij}]\quad\text{donde}\quad c_ij=a_{ij}+b_{ij}.
$$
- Dos matrices $A$ y $B$ son iguales si y sólo si $a_{ij}=b_{ij}\quad \forall i,j$.
- Sea $F$ un campo, y $\lambda\in F$, definimos el producto escalar como 
$$
	\lambda A=[\lambda a_{ij}].
$$
- Definimos el producto interno entre $A\in M_{m\times n}$ y $B\in M_{n\times k}$ como $$
  	AB=\left[ \sum_{j=1}^{n}a_{ij}b_{ji} \right].
  $$
Algunas propiedades de los número reales se cumplen también con las matrices:
Sean $a,b,c\in F$ un campo, y sean $A,B,C$ matrices sobre $F$.
- Cerradura: $a+b\in F$. $A+B$ es una matriz.
- Conmutatividad: $a+b=b+a$. $A+B=B+A$.
- Asociatividad: $(a+b)+c=a+(b+c)$. $(A+B)+C=A+(B+C)$.
- Neutro aditivo: $\exists 0$ tal que $a+0=a$. Existe la matriz $\bar{0}=[0]$ tal que $A+\bar{0}=A$.
- Inverso aditivo: $\forall a\in F \quad\exists-a$ tal que $a+(-a)=0$. Existe una matiz $-A$ tal que $A+(-A)=\bar{0}$.

Un conjunto $K$ con una operación $*$ es un [[Grupos|grupo]] $(K,*)$ si satisface la cerradura, asociatividad, neutro aditivo e inverso aditivo. 
Si además satisface la conmutatividad, entonces es un *grupo abeliano*.

Un ***anillo*** es un conjunto no vacío $A$ con dos operaciones suma $(+)$ y multiplicación $(\cdot)$ tal que:
- $(A,+)$ es un grupo abeliano.
- El producto es asociativo.
- Distributividad $a(b+c)=ab+ac$ con la multiplicación y suma.
- Cerradura para el producto.
Si además, el anillo cumple que $\exists 1\in A$ tal que  $a\cdot 1=a$ (neutro multiplicativo), entonces es un ***anillo unitario***. Si el producto es conmutativo entonces es un ***anillo conmutativo***.

Un ***campo*** $F$ es un anillo conmutativo unitario donde todo elemento no cero tiene un inverso multiplicativo, es decir
- $(F,+)$ es un grupo abeliano.
- $(F- \{0\},\cdot)$ es un grupo abeliano.
- Existe la distributividad.
El campo es fundamental a la hora de definir un [[EspaciosVectoriales|espacio vectorial]], las matrices, y otros conceptos importantes.

#AlgebraLineal
