Es un método alternativo más general que el de coeficientes indeterminados.
Para encontrar la solución de la ecuación diferencial lineal no homogénea
$$L(y)=\phi(x)$$
Una vez que se conoce la solución de la homogénea.
Si $y_{1}, y_{2},...,y_{n}$ son n soluciones l.i de la ecuación diferencial lineal homogénea
$$L(y)=0$$
La solución general de la homogénea es 
$$y_{n}=c_{1}y_{1}+c_{2}y_{2}+...+c_{n}y_{n}$$
Variación de parámetros
Una solución particular $y_{p}$ de $L(y)=\phi(x)$ es $$y_{p}=v_{1}y_{1}+v_{2}y_{2}+...+v_{n}y_{n}$$
$y_{i}=$ solución de la homogénea
$v_{i}=$ funciones desconocidas de x a determinar, $v_{i}=v_{i}(x)$
$i=1,2,...,n$ 
Para hallar las $v_{i}$ necesito resolver el sistema de ecuaciones lineales
$$\begin{cases} v_{1}'y_{1}+v_{2}'y_{2}+...+v_{n}'y_{n}&=0 \\ v_{1}'y_{1}'+v_{2}'y_{2}'+...+v_{n}'y_{n}'&=0  \\ \vdots  \\
v_{1}'y^{(n-2)}_{1}+v_{2}'y^{(n-2)}_{2}+...+v_{n}'y^{(n-2)}_{n}&=0  \\
v_{1}'y^{(n-1)}_{1}+v_{2}'y^{(n-1)}_{2}+...+v_{n}'y^{(n-1)}_{n}&=0
\end{cases}
$$
Resolver para los $v_{i}'$ luego integrar para hallar las $v_{i}$ olvidando las constantes de integración, porque buscamos una solución particular

Para el caso de orden $n=3$
$$\begin{cases}v'_{1}y_{1}+v_{2}'y_{2}+v_{3}'y_{3}=0 \\
v'_{1}y_{1}'+v_{2}'y_{2}'+v_{3}'y_{3}'=0 \\
v'_{1}y_{1}''+v_{2}'y_{2}''+v_{3}'y_{3}''=\phi(x)\end{cases}$$
$n=2$
$$\begin{cases}v'_{1}y_{1}+v_{2}'y_{2}=0 \\
v'_{1}y_{1}'+v_{2}'y_{2}'=\phi(x) \end{cases}$$
$n=1$
$$\begin{cases}v_{1}'y_{1}=\phi(x)\end{cases}$$
### Alcance del método
El método de variación de parámetros puede aplicarse a todas las ecuaciones diferenciales lineales (coeficientes variables).
Es más poderoso que coeficientes indeterminados porque ese método solo se aplica a ecuación diferencial lineal con coeficientes constantes y ciertas formas de $\phi(x)$.
En caso de que se puedan aplicar las 2, se preferirá variación de parámetros.
