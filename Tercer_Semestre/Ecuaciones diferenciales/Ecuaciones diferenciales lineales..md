## Definición 
### Teorema de la solución única
Una ecuación diferencial de orden n tiene la forma $$b_{n}(x)\cdot y^{(n)}+b_{n-1}(x)\cdot y^{(n-1)}+ ...b_{2}(x)\cdot y''+b_{1}(x)\cdot y^{'}+b_{0}(x)\cdot y=g(x)$$

```handwritten-ink
{
	"versionAtEmbed": "0.2.6",
	"filepath": "Tercer_Semestre/Ecuaciones diferenciales/ANEXOS/Ink/Writing/2024.11.4 - 12.21pm.writing"
}
```
### Teorema
COnsidere el problema de valor inicial dado por la ecuación anterior y las condiciones iniciales
$y(x_{0})=c_{0}$
$y'(x_{1})=c_{1}$
$y''(x_{2})=c_{2}$

$y^{(n)}(x_{n})=c_{n}$

Si $g(x)$ y $b_{i}(x)$ son continuos en algún intervalo que contiene a $x_{0}$ y $b_{n}(x) \neq 0 \rightarrow$ El problema de valor inicial tiene solución única.

Si dividimos por $b_{n}(x)$

```handwritten-ink
{
	"versionAtEmbed": "0.2.6",
	"filepath": "Tercer_Semestre/Ecuaciones diferenciales/ANEXOS/Ink/Writing/2024.11.4 - 12.28pm (2).writing"
}
```
Si $\Phi(x)=0$ la ecuación se dice homogénea
Si $\Phi(x)\neq 0$ La ecuacióñ se dice no homogénea

Si $a_{i}$ son constantes $\rightarrow$ la ecuación tiene coeficientes constantes
Si $a_{i}$ no son constantes $\rightarrow$ la ecuación tiene coeficientes variables

### Operador diferencial lineal
Definamos el operador diferencial lineal $\mathcal L(y)$ 
$\mathcal L(y)=y^{(n)}+a_{n-1}(x)y^{(n-1)}+...+a_{2}(x)y''+a_{1}(x)y'+a_{0}(x)y$
$a_{i}(x)$ son continuos
	$\rightarrow$ la ecuación diferencial se escribe
	$$\mathcal L(y)=\Phi(x)$$
Si la ecuación es homogénea $\rightarrow \Phi(x)=0$ 
$$\mathcal L(y)=0$$
### Teorema
El operador $\mathcal L(y)$ es lineal.

```handwritten-ink
{
	"versionAtEmbed": "0.2.6",
	"filepath": "Tercer_Semestre/Ecuaciones diferenciales/ANEXOS/Ink/Writing/2024.11.4 - 12.42pm.writing"
}
```
### Teorema 
#### Principio de superposición 
Si $y_{1}$ y $y_{2}$ son dos soluciones de $\mathcal L(y)=0$
$\rightarrow c_{1}y_{1}+c_{2}y_{2}$ también es solución 

Es lineal 
$$\begin{align} \mathcal L(c_{1}y_{1}+c_{2}y_{2})=\\
&(c_{1}y_{1}+c_{2}y_{2})^{(n)}+a_{n-1}(x)(c_{1}y_{1}+c_{2}y_{2})^{(n-1)} +... \\
&+a_{2}(x)(c_{1}y_{1}+c_{2}y_{2})''+a_{1}(x)(c_{1}y_{1}+c_{2}y_{2})'+a_{0}(x)(c_{1}y_{1}+c_{2}y_{2})=\\

(c_{1}y_{1})

\end{align}$$


```handwritten-ink
{
	"versionAtEmbed": "0.2.6",
	"filepath": "Tercer_Semestre/Ecuaciones diferenciales/ANEXOS/Ink/Writing/2024.11.4 - 12.44pm.writing"
}
```

Si $y_{1}$ y $y_{2}$ son soluciones, $\mathcal L(y)=0$
$\mathcal L(y_{1})=0$
$\mathcal L(y_{2})=0$
$\mathcal L(c_{1}y_{1}+c_{2}y_{2})=c_{1}\mathcal L(y_{1})+c_{2}\mathcal L(y_{2})=0+0=0$

##### Ejemplo
Diga el orden y si es lineal o no
a) $2xy''+c^{2}y'-(\sin{x})y=2$ 
Orden =2
$b_{2}(x)=2x$
$b_{1}(x)=x^{2}$
$b_{0}(x)=-\sin{x}$
$g(x)=2$

Es lineal. (no depende de y ni de y(n))

b) $yy'' +xy'+y=x^{2}$
orden =3
$b_{3}(x)=y$
$b_{2}(x)=0$
$b_{1}(x)=x$
$b_{0}=1$
$g(x)=x^{2}$

Como $b_{3}(x)$ depende de $y$
No es lineal

##### Ejemplo 5
Problema de valor inicial
$$y'=2\sqrt{|y|}$$
$$y(0)=0$$
TIene dos soluciones $y=x|x|$ & $y=0$ ¿Van en contra del teorema de solución única?

No porque el teorema sollo se aplica a lineales y esta no es lineal

##### Ejemplo 6
Halle todas las soluciones del problema de valor inicial
$$y''+e^{x}y'+(x+1)y=0$$
$$y(1)=0$$
$$y'(1)=0$$
$b_{2}(x)=1$
$b_{1}(x)=e^{x}$
$b_{0}(x)=(x+1)$
$\Phi(x)=0$
Es lineal si la dependencia de x
Aplico teorema de solución único
$y=0$ es una solución por inspección, por lo tanto por el teorema de solución única es la única