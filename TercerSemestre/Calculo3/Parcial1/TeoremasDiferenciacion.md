#### Teorema:
Sea $f:R^{n}\to R^{m}$ y $U\subset R^{n}$ [[Limite|abierto]]. Si $f$ es [[Diferenciacion|diferenciable]] en $(a_{1},\dots,a_{n})\in U$, entonces es [[Continuidad|continua]] en $(a_{1},\dots,a_{n})$.
##### Demostración:
Supongamos que $f$ es diferenciable en $\bar{a}$. Es decir 
$$
	\lim_{ \bar{x} \to \bar{a} } \frac{\lvert \lvert f(\bar{x})-f(\bar{a})-Df(\bar{a})\begin{pmatrix}
	x_{1}-a_{1} \\
	x_{2}-a_{2} \\
	\vdots \\
	x_{n}-a_{n}
	\end{pmatrix} \rvert  \rvert }{\lvert \lvert \bar{x}-\bar{a} \rvert  \rvert } .
$$
Sea $\hbar=\bar{x}-\bar{a}$, entonces eso es lo mismo que 
$$
	\lim_{ \bar{h} \to \bar{0}  } \frac{\lvert \lvert f(\bar{h}+\bar{a})-f(\bar{a})-Df(\bar{a})\bar{h} \rvert  \rvert }{\lvert \lvert \bar{h} \rvert  \rvert } .
$$
Recordemos además la definición de [[Limite|limite]]: 
$$
	\forall\varepsilon>0,\exists \delta>0:0<\lvert \lvert \bar{h} \rvert  \rvert<\delta\implies \frac{\lvert \lvert f(\bar{h}+\bar{a})-f(\bar{a})-Df(\bar{a})\bar{h} \rvert  \rvert }{\lvert \lvert \bar{h} \rvert  \rvert }<\varepsilon.
$$
Tomemos en particular $\varepsilon=1>0,\exists \delta_{1}>0$ tal que si $\lvert \lvert \bar{h} \rvert \rvert<\delta_{1}$ entonces 
$$
	\lvert \lvert f(\bar{h}-\bar{a})-f(\bar{a})-Df(\bar{a})\bar{h} \rvert  \rvert<\lvert \lvert \bar{h} \rvert  \rvert.  
$$
Entonces 
$$
	\begin{align}
	\lvert \lvert f(\bar{a}+\bar{h})-f(\bar{a}) \rvert  \rvert
	&=\lvert \lvert f(\bar{a}+\bar{h})-f(\bar{a})-Df(\bar{a})\bar{h}+Df(\bar{a})\bar{h} \rvert  \rvert  \\
	&\leq \lvert \lvert f(\bar{a}+\bar{h})-f(\bar{a})-Df(\bar{a})\bar{h} \rvert  \rvert +\lvert \lvert Df(\bar{a})\bar{h} \rvert  \rvert  \\
	&\leq \lvert \lvert \bar{h} \rvert  \rvert+ M\lvert \lvert \bar{h} \rvert  \rvert &=\lvert \lvert \bar{h} \rvert  \rvert (M+1).
	\end{align}
$$
($M$ como definido en la [[TareaDiferenciacion|tarea de diferenciación]]).
Sea $\varepsilon'>0$ y definamos $\delta=\min\{ \delta_{1}, \varepsilon' / (M+1) \}$. Si $\lvert \lvert \bar{h} \rvert \rvert<\delta$, entonces tenemos que 
$$
	\lvert \lvert f(\bar{a}+\bar{h})-f(\bar{a}) \rvert  \rvert <\lvert \lvert \bar{h} \rvert  \rvert (M+1)< \frac{\varepsilon'}{M+1}(M+1)=\varepsilon'.
$$
Por lo tanto $$\lim_{ \bar{h} \to \bar{0} }f(\bar{a}+\bar{h})-f(\bar{a})=\bar{0}\implies \lim_{ \bar{h} \to \bar{0} } f(\bar{a}+\bar{h})=f(\bar{a}),$$
recordamos que $\bar{x}=\bar{h}+\bar{a}$, entonces tenemos que $$\lim_{ \bar{x} \to \bar{a} }f(\bar{x})=f(\bar{a}).\quad\square$$

#### Teorema:
Sea $f:R^{n}\to R^{m}$, $\bar{a}\in R^{n}$ y $U$ una vecindad de $\bar{a}$. Si las derivadas parciales $\frac{\partial f_{i}}{\partial x_{j}}$ existen, y $f$ son continuas en $U$, para $i=1,\dots,m$, $j=1,\dots,n$. 
Entonces $f$ es diferenciable en $\bar{a}$.
##### Demostración (para $f:R^{2}\to R$):
![[Teroema2Diferenciacion]]




#Calculo