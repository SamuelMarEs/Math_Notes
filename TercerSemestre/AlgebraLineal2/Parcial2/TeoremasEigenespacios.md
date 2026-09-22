#AlgebraLineal
#### Lema
Sea $T$ un operador lineal y $\lambda_{1},\dots,\lambda_{k}$ eigenvalores distintos de $T$. Para cada $i$, sea $v_{i}\in E_{\lambda i}$ el [[Eigenespacios|eigenespacio]] asociado al [[Eigenvectores_Eigenvalores|eigenvalor]] $i$.. Si 
$$
	v_{1}+v_{2}+\dots+v_{k}=0
$$
entonces $v_{i}=0$ para todo $i$.
##### Demostración:
Por contradicción.
Supongamos que para $1\leq i\leq m\leq k$ tenemos que $v_{i}\neq 0$ y además $v_{1}+v_{2}+\dots+v_{k}=0$, lo que implica que $\{ v_{1},\dots,v_{k} \}$ es un conjunto linealmente dependiente, lo cual contrdice que [[Diagonalizabilidad|teorema 5.5]].
Por lo tanto $v_{i}=0\forall i.\quad\square$

#### Teorema
Sea $T$ un operador lineal en un espacio vectorial $V$, y sean $\lambda_{1},\dots,\lambda_{k}$ eigenvalores distintos de $T.$ Para cada $i=1,2,\dots,k$, sea $S_{i}$ un subconjunto finito linealmente independiente del eigenespacio $E_{\lambda i}$. Entonces $S=S_{1}\cup S_{2}\cup\dots\cup S_{k}$ es un conjunto linealmente independiente de $V.$
##### Demostración:
Supongamos que $S_{i}=\{ v_{i 1},v_{i 2},\dots,v_{i n} \}$ con cardinalidad $\lvert S_{i} \rvert=n_{i}$. Entonces podemos definir a $S$ como 
$$
	S=\{ v_{ij}:1\leq i\leq k,1\leq j\leq n_{i} \}.
$$
Sea $w_{i}=\sum_{j=1}^{n_{i}}a_{ij}v_{ij}$, tenemos que $w_{i}\in E_{\lambda i}$. Sea $w_{1}+w_{2}+\dots+w_{k}=0$, para cualquier $i$, tenemos qe $w_{i}=0\implies\sum_{j=1}^{n_{i}}a_{ij}v_{ij}\implies a_{ij}=0$ por ser linealmente independientes todos los vectores.
Por lo tanto tenemos $S$ es linealmente independiente. $\quad\square$

#### Teorema 5.8
Sea $T$ un operador lineal en un espacio vectorial de dimensión finita $V$ tal que el polinomio característico se descompone sobre $F$. Sean $\lambda_{1},\dots \lambda_{k}$ eigenvalores de $T$.
- $T$ es diagonalizable si y sólo si la multiplicaidad de $\lambda_{i}$ es igual a $\text{dim}(E_{\lambda i})$ para toda $i$.
- Si $T$ es diagonalizable y $B_{i}$ es una base ordenada de $E_{\lambda i}$ para cada $i$, entonces $\beta=B_{1}\cup B_{2}\cup\dots\cup B_{k}$ es una base ordenada de $V$ que consiste de eigenvectores de $T.$
##### Demostración:
Para cada $i$, sea $m_{i}$ la multiplicidad de $\lambda_{i}$, y $d_{i}=\text{dim}(E_{\lambda i})$.
$\Rightarrow$ Supongamos que $T$ es diagonalizable, entonces existe una base de eigenvalores $\beta$. Para cada $i$, $B_{i}=\beta \cap E_{\lambda i}$ con $|B_{i}|=n_{i}$. Entonces $n_{i}\leq d_{i}$, y además por el [[Eigenespacios|teorema 2.7]], tenemos que $d_{i}\leq m_{i}$. Notemos que $m_{1}+m_{2}+\dots+m_{k}=n$ pues la suma de las multiplicidades debe ser el grado del polinomio característico. Además $n_{1}+n_{2}+\dots+n_{k}=n$ pues, por la forma en que construimos las bases, la suma de sus cardinalidades debe ser el tamaño de la base de $V$. Entonces $$
  	n\leq \sum_{i=1}^{k}d_{i}\leq \sum_{i=1}^{k}m_{i}= n,
  $$
es decir que $\sum m_{i}-d_{i}=0$, pero recordemos que $d_{i}\leq m_{i}$, es decir que tenemos una suma de términos no negativos, por lo tanto tenemos que necesariamente $m_{i}=d_{i}$.
$\Leftarrow$ Supongamos que $m_{i}=d_{i}$ para todo $i$. Vamos a demostrar que $T$ es diagonalizable y el segundo inciso. 
Para cada $i$ sea $B_{i}$ una base ordenada de $E_{\lambda i}$ y $\beta=B_{1}\cup B_{2}\cup\dots\cup B_{k}$. Por el teorema anterior, tenemos que $\beta$ es linealmente independiente. Además $\sum d_{i}=\sum m_{i}=n$, por lo tanto $\beta$ es una base de $V$, y por lo tanto $T$ es diagonalizable. $\quad\square$

