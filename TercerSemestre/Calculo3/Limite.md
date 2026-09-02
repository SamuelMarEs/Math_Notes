Recordemos que, sea $f:R\to R$, decimos que $\lim_{ x \to a }f(x)=L$ si y sólo si 
$$
	\forall \varepsilon>0,\exists \delta>0:|x-a|<\delta\Rightarrow|f(x)-L|<\varepsilon.
$$
Además sabemos que 
$$
	\lim_{ x \to a }f(x)=L\Longleftrightarrow\lim_{ x \to a^{-} }f(x)=\lim_{ x \to a^{+} } f(x) = L  .
$$
La noción de que una [[Funciones|función]] tienda a algo cuando es de una variable es bastante intuitiva. Sin embargo, queremos generalizar esta noción de "acercarse" a otras dimensiones. 

##### Definición:
Sea $f:R^{n}\to R$ con dominio $A\subset R^{n}$, donde $A$ es un [[ConjuntosAbiertos|conjunto abierto]]. Sea $x_{0}\in A$ ó $x_{0}$ un punto en la frontera de $A$ y $N$ una vecindad de $b\in R$.
Decimos que $b$ es límite de $f$ cuando $x$ tiende a $x_{0}$ si existe una vecindad $U$ de $x_{0}$ tal que $x\neq x_{0}$, con $x\in U$ y $x\in A$ implica $f(x)\in N$, y escribimos 
$$
	\lim_{ x \to x_{0} } f(x)=b,
$$
es decir $\exists U\subset R^{n}$ tal que $x_{0}\in U$ y $f(U\setminus\{ x_{0} \})\subset N,\forall N$ tal que $b\in N$. 
