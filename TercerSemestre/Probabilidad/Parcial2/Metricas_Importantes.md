#Probabilidad 
# Momentos
#### Definición:
Sea $X$ una [[VariablesAleatorias|v.a.]] discreta. Decimos que el $n$-ésimo momento de $X$ es $E(X^{n})$, para $n=1,2,\dots$, de modo que $E(X)$ es el primer momento, $E(X^{2})$ el segundo momento, y así sucesivamente.
Recordemos que el [[ValorEsperado|valor esperado]] está dado como 
$$
	E(X^{n})=\sum_{x}x^{n}P(X=x).
$$
Si bien puede ser que podamos calcular todos los momentos, no todos son interpretables. Algunos de los momentos de una v.a. están asociados a características de la distribución de proabilidad.
- El primer momento $E(X)$ está relacionado con el "centro" de la [[FuncionDeProbabilidad|función de probabilidad]].
- El segundo momento $E(X^{2})$, está relacionado con la variabilidad de la función de probabilidad, pues está ligado a la [[Varianza_DesviacionEstandar|varianza]].
- El tercer momento $E(X^{3})$ contiene información sobre la simetría de la pdf.
- El cuarto momento $E(X^{4})$ se relaciona con la *Kortosis*, es decir, el peso de la distribución en los extremos (colas de la distribución).

Existen variantes de los momentos "simples". Por ejemplo :
- $E[(X-\mu)^{n}]$ se conoce como el $n$-ésimo momento central.
- $E(|X|^{n})$ el $n$-ésimo momento absoluto.
- $E(|X-\mu|^{n})$ el $n$-ésimo momento absoluto central.
- $E[(X-c)^{n}]$ el $n$-ésimo momento generalizado.

# Moda
Si $X$ es una [[VariablesAleatorias|v.a.]] discreta con [[FuncionDeProbabilidad|función de probabilidad]] $f$, la moda de $X$ es el valor de la v.a. en el que se alcanza la máxima probabilidad.
![[Excalidraw/Moda]]
La moda de una v.a. no tiene que coincidir necesariamente con el [[ValorEsperado|valor esperado]] $E(X)$, salvo que la distribución $f(x)$ sea simétrica.

# Cuantiles
#### Definición:
Sea $p\in (0,1]$. En ***cuantil*** $p$ de la v.a. $X$ o de su [[FuncionDeDistribucion|función de distribución]] $F(x)$ es un número $c_{p}$ que cumple ser el valor más pequeño tal que 
$$
	F(c_{p})\geq p.
$$
Es decir, de forma barroca, se puede pensar en un cuántil como el primero valor de la variable aleatoria donde se alcanza un nivel de probabilidad.
##### Ejemplo
Suponga que $X$ es una v.a. discreta con pdf dada por la siguiente tabla:

| x    | 0    | 1    | 2    | 3    | 4    | 5   |
| ---- | ---- | ---- | ---- | ---- | ---- | --- |
| f(x) | 0.05 | 0.1  | 0.15 | 0.45 | 0.15 | 0.1 |
| F(x) | 0.05 | 0.15 | 0.30 | 0.75 | 0.90 | 1   |
Supongamos que queremos encontral el cuantil de nivel 0.5, es decir $c_{0.5}$. Pues es el valor de $x$ para el cual $F(c_{0.5})\geq 0.5$, que para este caso es $c_{0.5}=3$. 
Supongamos que $X$ representa el número de hijos de una pareja seleccionada al azar en una población. ¿Cómo podríamos interpretar $c_{0.5}$?
Pues el cuantil nos está diciendo que el 50% de la población tiene 3 o menos hijos. (Aunque realmente es el 75% de la población, pero el cuantil en este caso lo está asegurando para el 50%).
Esto sirve para saber cuando un evento es raro o atípico.

Si consideramos tres niveles para $p:$ 0.25, 0.5, 0.75, los cuantiles $c_{0.25},c_{0.5},c_{0.75}$ se conocen como *cuartiles*, pues dividen a la función de distribución en 4 pedazos.
Si en lugar de tomar tres niveles, tomamos 10 niveles, es decir 
$$
	c_{0.1},c_{0.2},\dots,c_{0.9},
$$
estos se conocen como *deciles*.
También podemos considerar dividir los valores de nuestra variable en 100 partes: 
$$
	c_{0.01},c_{0.02},c_{0.03},\dots,c_{0.99},
$$
estos se conocen como *percentiles*.
