#Probabilidad 
#### Definición:
Sea $X$ una [[VariablesAleatorias|variable aleatoria]] discreta con [[FuncionDeProbabilidad|función de probabilidad]] $f(x)$ y valor esperado $\mu=E(X)<\infty$. La ***varianza*** de $X$ se define como 
$$
	Var(X)=\sum_{x}(x-\mu)^{2}P(X=x)=E[(X-\mu)^{2}].
$$
En general, la varianza se denota como $\sigma^{2}$.

La varianza indica, en promedio, qué tanto nos alejamos del centro de la distribución de probabilidad, $\mu$. Que tanto se aleja cada valor de la media.
Un valor grande de la varianza indica que hay mucha dispersión, y un valor pequeño indica que los valores se concentran muy cerca de $\mu$.

#### Proposición (Propiedades)
Sea $c$ una constante y sean $X$ y $Y$ v.a. discretas con varianza $\sigma^{2}_{x}$ y $\sigma^{2}_{y}$, respectivamente. Entonces:
a) $Var(cX)=c^{2}Var(x)=c\sigma_{x}^{2}$.
b) $Var(c)=0$.
c) $Var(cX+b)=c^{2}Var(X)=c^{2}\sigma_{x}^{2}$.
d) $Var(X+Y)=Var(X)+Var(Y)$ si $X$ y $Y$ son [[V.A.Independientes|independientes]].
e) $Var(X+Y)=Var(X)+Var(Y)-2Cov(X,y)$, dónde $Cov(X,Y)=E([X-E(X)][Y-E(Y)])$.
f) $Var(X)=E(X^{2})-[E(X)]^{2}$.


#### Definición:
La ***desviación estándar*** de una v.a. $X$ se define como 
$$
	sd(X)=\sqrt{ Var(X) }.
$$
Se suele denotar como $\sigma$, y es simplemente la raíz positiva de la varianza.

La desviación estándar se puede interpretar como el error promedio de predicción respecto al valor central.