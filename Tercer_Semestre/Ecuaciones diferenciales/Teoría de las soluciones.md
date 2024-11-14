## Dependencia lineal
Un conjunto de funciones ${y_{1}(x), y_{2}(x),...,y_{n}(x)}$ es linealmente dependiente en $a<=x<=b$ si $\exists n$ constantes $c_{1},c_{2},...,c_{n}$ no todas cero tales que
$$c_{1}y_{1}(x)+c_{2}y_{2}(x)+...+c_{n}y_{n}(x)=0$$
#### Ejemplo 1
El conjunto ${x, 5x, \sin{x}}$ es linealmente dependiente en $[-1,1]$ ya que $\exists n$ constantes $c_{1},c_{2},c_{3},c_{4}$ tales que
$$(-5)(x)+(1)(5x)+(0)(1)+0\sin {x}$$
$c_{1},c_{2}\neq 0$ por lo tanto son linealmente dependientes

## Independencia lineal
El conjunto ${y_{1}(x),y_{2}(x),...,y_{n}(x)}$ es linealmente independiente; no es linealmente dependiente, i.e. si todas las constantes $c_{1}=c_{2}=...=c_{n}=0$
## Soluciones linealmente independientes: El Wronskiano
### Teorema 1.
La ecuación diferencial lineal homogénea de orden n
$$\mathcal L(y)=0$$
tiene siempre $n$ soluciones linealmente independientes.
Si $y_{1}(x),y_{2}(x),y_{3}(x),...,y_{n}(x)$ son esas soluciones, entonces la solución general de $\mathcal L(y)=0$
es:
$$y(x)=c_{1}y_{1}(x)+c_{2}y_{2}(x)+...+c_{n}y_{n}(x)$$
i.e. la solución general es una combinación lineal de las $n$ soluciones.
$c_{1},c_{2},...,c_{n}$ son constantes arbitrarias.
#### Ejemplo 2
Dos soluciones de $y''+4y=0$ (segundo orden, debe tener dos soluciones)
son:
$y_{1}(x)=\sin{2x}$
$y_{2}(x)=\cos{2x}$
Estas soluciones son linealmente independientes.

Esto implica que la solución general es:
$$\begin{align} 
y(x)&=c_{1}y_{1}(x)+c_{2}y_{2}(x)\\
&=c_{1}\sin{2x}+c_{2}\cos{2x}
\end{align}$$
## Wronskiano
### Definición
Sea un conjunto de funciones $z_{1}(x),z_{2},...,z_{n}(x)$ en $a\leq x\leq b$ cada una de las cuales tiene n-1 derivadas. El determinante 

$$W(z_{1},z_{1},...,z_{n})=\begin{vmatrix} z_{1} & z_{2} & \cdots & z_{n} \\ z'_{1} & z'_{2} & \cdots & z'_{n} \\ z''_{1} & z''_{2} & \cdots & z''_{n} \\ \vdots & \vdots & \ddots & \vdots \\ z^{(n-1)}_{1} & z^{(n-1)}_{2} & \cdots & z^{(n-1)}_{n} \end{vmatrix}$$
Se llama el Wronskiano del conjunto de funciones.
Google Wronsky
#### Ejemplo 3
El Wronskiano del conjunto ${{x,x^{2},x^{3}}}$ es:
$$w(x,x^{2},x^3)=
\begin{vmatrix} 
x & x^{2} & x^{3}\\ 
\frac{d}{dx}(x) & \frac{d}{dx}(x^{2}) & \frac{d}{dx}(x^{3})\\ 
\frac{d^{2}}{dx^{2}}(x) & \frac{d^{2}}{dx^{2}}(x^{2}) & \frac{d^{2}}{dx^{2}}(x^{3})\\  
\end{vmatrix}
 $$
 
```handwritten-ink
{
	"versionAtEmbed": "0.2.6",
	"filepath": "Tercer_Semestre/Ecuaciones diferenciales/ANEXOS/Ink/Writing/2024.11.6 - 13.03pm.writing"
}
```

### Teorema 2.
Si $y_{1}(x),y_{2}(x),...,y_{n}(x)$ son $n$ soluciones para la ecuación diferencial lineal homogénea de orden n
$$\mathcal L(y)=0$$
$\rightarrow$ El conjunto de solución es linealmente independiente en $a\leq x\leq b$  si y solo si $W(x)\neq 0$
#### Ejemplo 4.
Las dos soluciones $$\begin{align}y_{1}(x)=\sin{2x}\\y_{2}(x)=\cos{2x}\end{align}$$
de $y''+4y=0$
Son linealmente independientes ya que:
$$W(\sin{2x},\cos{2x})=
\begin{vmatrix} 
\sin{2x} & \cos{2x}\\
2\cos{2x} & -2\sin{2x}
\end{vmatrix}
$$
$$\begin{align}
&=-2\sin^{2}{2x}-2\cos^{2}{2x}\\
&=-2(\sin^{2}{2x}+\cos^{2}{2x})\\
&=-2\\
-2\neq 0
\end{align}
$$
Son linealmente independientes

###### Nota:
Los coeficientes de $\mathcal L(y)=0$ deben ser continuos en el intervalo para aplicar este teorema del Wronskiano.

Considere la ecuación diferencial no homogénea $$\mathcal L(y)=\Phi (x)$$una solución de esta ecuación se llama solución particular $y_{p}$
La solución de la homogénea $$\mathcal L(y)=0$$
se llama $y_{n}$
### Teorema 3.
La solución general de la ecuación 
$$\mathcal L(y)=\Phi(x)$$
es
$$y(x)=y_{n}+y_{p}$$
