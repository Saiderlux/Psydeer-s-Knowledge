Podemos resolver la ecuación diferencial de 2do orden homogénea
$$a_{2}(x)y''+a_{1}(x)y'+a_{0}(x)y=0$$
a partir de una primera solución $y_{1}$ en un intervalo I. $y_{1}$ es una solución no trivial. Buscamos a una 2da solución $y_{2}$ .
1. $y_{1}$ & $y_{2}$
si $y_{1}$ y $y_{2}$ no son l.d. son l.i. 
$\rightarrow$ $y_{2}=cy_{1} (c \neq cte)$ múltiplos
Pero como son l.i. no son múltiplos constantes $$y_{2}=u(x)y,(li)$$
$u(x)$ no es constante

Tengo que hallar $u(x)$ sustituyendo $y_{2}$ en la ecuación diferencial.

## Ejemplo 1
2da solución por reducción de orden
Si $y_{1}=e^{x}$ es solución de $y''-y=0$
en $(-\infty,\infty)$ halle $y_{2}$ 

Solución 
Para que sean l.i. 
$$y_{2}=u(x)y_{1}=u(x)e^{x}$$
$$y'_{2}=u(x)e^{x}+e^{x}u'(x)$$
$$y''_{2}=u(x)e^{x}+e^{x}u'(x)+e^{x}u''(x)+e^{x}u'(x)$$
Sustituyendo en la ecuación
$$y''-y=0$$
$$u(x)e^{x}+e^{x}u'(x)+e^{x}u''(x)+e^{x}u'(x)-u(x)e^{x}=0$$
$$e^{x}[u''(x)+2u'(x)]=0$$
$$e^{x}\neq \forall x$$


```handwritten-ink
{
	"versionAtEmbed": "0.2.6",
	"filepath": "Tercer_Semestre/Ecuaciones diferenciales/ANEXOS/Ink/Writing/2024.11.13 - 18.42pm.writing"
}
```
$$\rightarrow u''(x)+2u'(x)=0$$
Ahora hagamos la sustitución
$$w=u'(x)$$
$$w'=u''(x)$$
$$w'+2w=0$$
Ecuación diferencial lineal homogénea 1er orden
Factor integrante es:
$$I=e^{\int p(x)dx}=e^{\int2dw}=e^{2w}$$
$$\frac{d}{dx}[e^{2x}w]=0$$
$$\int {d[e^{2x}w]}=0\int dw +c$$
$$e^{2x}w=c_{1}$$
$$w=\frac{c}{e^{2x}}=c_{1}e^{-2x}$$
Sustituyendo
$$u'=w=c_{1}e^{-2x}$$
$$\frac{dy}{dx}=c_{1}e^{-2x}$$
$$\int dy=\frac{-1}{2}\int c_{1}e^{-2x}(-2)dx$$
$$u=\frac{-1}{2}c_{1}e^{-2x}+c_{2}$$

Peeero
$$y_{2}=uy_{1}$$
$$y_{2}=[\frac{-c_{1}}{2}e^{-x}+c_{2}e^{x}]$$
$c_{1}=0$, $c_{2}=1$
$$y_{2}\rightarrow e^{x}=y_{1}$$
$$W(e^{x},e^{-x})=-2\neq 0$$
Son linealmente independientes $y_{1}$ y $y_{2}$ 

## Caso general: Fórmula
Ecuación diferencial de 2do orden lineal homogénea
$$a_{2}(x)y''+a_{1}(x)y'+a_{0}(x)y=0$$
divido todo por $a_{2}(x)$
$$y''+ \frac{a_{1}(x)}{a_{2}(x)}y'+\frac{a_{0}(x)}{a_{2}(x)}y=0$$
$$y''+P(x)y'+Q(x)y=0$$
$P(x),Q(x)$ son continuas en un intervalo I.
Sea $y_{1}$ una solución de la ecuación diferencial, $y_{1}(x)\neq 0$ la segunda solución es $$y=u(x)y_{1}$$

```handwritten-ink
{
	"versionAtEmbed": "0.2.6",
	"filepath": "Tercer_Semestre/Ecuaciones diferenciales/ANEXOS/Ink/Writing/2024.11.13 - 19.04pm.writing"
}
```

Sustituyendo en la ecuación diferencial

```handwritten-ink
{
	"versionAtEmbed": "0.2.6",
	"filepath": "Tercer_Semestre/Ecuaciones diferenciales/ANEXOS/Ink/Writing/2024.11.13 - 19.06pm.writing"
}
```
