### Sección 2.4 Friedberg
2.- Para cada una de las siguientes transformaciones, determina si son invertibles y justifica tu respuesta.

3.-

8.-

12.-

14.-

15.-

### Sección 2.5 Friedberg
2.- Para cada uno de los siguientes pares de bases ordenadas $\beta$ y $\beta'$ para $R^{2}$, encuentre la matriz de cambio de base que cambia las coordenadas $\beta'$ en coordenadas $\beta$.
- $\beta=\{ e_{1},e_{2} \},\beta'=\{ (a_{1},a_{2}),(b_{1},b_{2}) \}$.
- $\beta=\{ (-1,3),(2,-1) \},\beta'=\{ (0,10),(5,0) \}$.
- $\beta=\{ (2,5),(-1,-3) \},\beta'=\{ (e_{1},e_{2}) \}$.
- $\beta=\{ (-4,3),(2,-1) \},\beta'=\{ (2,1),(-4,1) \}$.

3.- Para cada uno de los siguientes pares de bases ordenadas $\beta$ y $\beta'$ para $P_{2}(R)$, encuentre la matriz de cambio de base que cambia las coordenadas $\beta'$ en coordenadas $\beta$.
- $\beta=\{ x^{2},x,1 \},\beta'=\{ a_{2}x^{2}+a_{1}x+a_{0},b_{2}x^{2}+b_{1}x+b_{0},c_{2}x^{2}+c_{1}x+c_{0} \}$.
- $\beta=\{ 1,x,x^{2} \},\beta'=\{  a_{2}x^{2}+a_{1}x+a_{0},b_{2}x^{2}+b_{1}x+b_{0},c_{2}x^{2}+c_{1}x+c_{0}  \}$.
- $\beta = \{ 2x^{2}-x,3x^{2}+1,x^{2} \},\beta'=\{ 1,x,x^{2} \}$.
- $\beta=\{ x^{2}-x+1,x+1,x^{2}+1 \},\beta'=\{ x^{2}+x+4,4x^{2}-3x+2,2x^{2}+3 \}$.
- $\beta=\{ x_{2}-x,x_{2}+1,x-1 \},\beta'=\{ 5x^{2}-2x-3,-2x^{2}+5x+5,2x^{2}-x-3 \}$.
- $\beta=\{ 2x^{2}-x+1,x^{2}+3x-2,-x^{2}+2x+1 \}, \beta'=\{ 9x-9,x^{2}+21x-2,3x^{2}+5x+2 \}$

4.- Sea $T$ un operador lineal sobre $R^{2}$ definido como 
$$
	T\begin{pmatrix}
	a \\
	b
	\end{pmatrix}=\begin{pmatrix}
	2a+b \\
	a-3b
	\end{pmatrix},
$$
sea $\beta$ la base ordenada estándar para $R^{2}$, y sea $\beta'=\left\{ \begin{pmatrix}1 \\  1\end{pmatrix},\begin{pmatrix}1 \\  2\end{pmatrix} \right\}$. Use el Teorema 2.23 y el hecho de que 
$$
	\begin{pmatrix}
	1 & 1 \\
	1 & 2
	\end{pmatrix}^{-1}=\begin{pmatrix}
	2 & -1 \\
	-1 & 1
	\end{pmatrix}
$$
para encontrar $[T]_{\beta'}$

5.- Sea $T$ el operador lineal sobre $P_{1}(R)$ definido como $T(p(x))=p'(x)$, la derivada de $p(x)$. Sea $\beta=\{ 1,x \}$ y $\beta'=\{ 1+x,1-x \}$. Use el Teorema 2.23 y el hecho de que 
$$
	\begin{pmatrix}
	1 & 1 \\
	1 & -1
	\end{pmatrix}^{-1}=\begin{pmatrix}
	2 & -1 \\
	-1 & 1
	\end{pmatrix}
$$
para encontrar $[T]_{\beta'}$.

6.- Para cada matriz $A$ y base ordenada $\beta$, encuentra $[L_{A}]_{\beta}$. También, encuentra una matriz invertible $Q$ tal que $[L_{A}]_{\beta}=Q^{-1}AQ$.
- $A=\begin{pmatrix}1 & 3 \\  1 & 1\end{pmatrix}$ y $B=\left\{ \begin{pmatrix}1 \\  1\end{pmatrix},\begin{pmatrix}1 \\  2\end{pmatrix} \right\}$.
- $A=\begin{pmatrix}1 & 2 \\  2 & 1\end{pmatrix}$ y $B=\left\{ \begin{pmatrix}1 \\  1\end{pmatrix},\begin{pmatrix}1 \\  -1\end{pmatrix} \right\}$.
- $A=\begin{pmatrix}1 & 1 & -1 \\  2 & 0 & 1 \\  1 & 1 & 0\end{pmatrix}$ y $B=\left\{ \begin{pmatrix}1 \\  1 \\  1\end{pmatrix},\begin{pmatrix}1 \\  0 \\  1\end{pmatrix},\begin{pmatrix}1 \\  1 \\  2\end{pmatrix} \right\}$.
- $A=\begin{pmatrix}13 & 1 & 4 \\ 1 & 13 & 4 \\  4 & 4 & 10\end{pmatrix}$ y $B=\left\{ \begin{pmatrix}1 \\  1 \\  -2\end{pmatrix},\begin{pmatrix}1 \\  -1 \\  0\end{pmatrix},\begin{pmatrix}1 \\  1 \\  1\end{pmatrix} \right\}$.

11.- Sea $V$ un espacio vectorial de dimensión finita con bases ordenadas $\alpha, \beta, \gamma$. 
- Pruebe que si $Q$ y $R$ son las matrices de cambio de base de $\alpha$ en $\beta$, y $\beta$ en $\gamma$, respectivamente, entonces $RQ$ es la matriz de cambio de base de $\alpha$ en $\gamma$.
- Pruebe que si $Q$ cambia las coordenadas $\alpha$ en coordenadas $\beta$, entonces $Q^{-1}$ cambia las coordenadas $\beta$ en coordenadas $\alpha$.
