- Sean X y Y variables aleatorias continuas. Una función de densidad de probabilidad conjunta f(x,y) de estas dos variables es una función que satisface $f(x,y)\geq0$ y $\int^{\infty}_{\infty}\int^{\infty}_{\infty}f(x,y)dxdy=1$ Entonces para cualquier conjunto $A$ en dos dimensiones
- $P[(X<Y)\int A]=\int_{A}\intf(x,y)dx dy$
- EN particular si A es el rectángulo $\{(x,y):a\leq c\leq b,c\leq y\leq d\}$, entonces
- $P[(X,Y)\in A]=P(a\leq X\leq b, c\leq Y\leq d)=\int_{a}^{b}\int^{d}_{c}f(x,y)dy dx$
---

- Sea $$f(x,y)=\begin{cases}kx & \text{ si }0\leq x \leq 1, x\leq y \leq 2-x\\ 0 & \text{de lo contrario} \end{cases}$$
- Hallar K para que $f(x,y)$ sea una FDP conjunta 
- $\int_{0}^{1}\int^{2-x}_{x}kx\text{ }dy\text{ } dx$    
- $\int_{0}^{1}kxy|^{2-x}_{x}dx$  
- $\int_{0}^{1}kx(2-x-x)dx=\int_{0}^{1}kx(2-2x)dx$
- $k\int_{0}^{1}2x-2x^{2}dx$  
- $k[\frac{2x^{2}}{2}- \frac{2x^{3}}{3}]^{1}_{0}=k\left(1- \frac{2}{3}\right)=\frac{k}{3}$ 
 ---
## Ejemplos  

1. Un banco dispone tanto de una ventanilla para automovilistas como de una ventanilla normal. En un día seleccionado al azar sea $X$ la proporción de tiempo que la ventanilla para automovilistas está en uso (por lo menos un cliente está siendo atendido o está esperando ser atendido) y $Y$ la proporción del tiempo que la ventanilla normal está en uso. ENtonces el conjutno de valores posibles de $(X,Y)$ es el rectángulo $D=\{(x,y):0\leq x\leq 1\}$ suponga que la función de densidad de probabilidad conjunta de $(X,Y)$ está dada por
$$f(x,y)=\begin{cases} \frac{6}{5}(x+y^{2}) & 0\leq x \leq 1, & 0\leq y \leq 1 \\ 0 &\text{de lo contrario}  \end{cases}$$
**Resultado 1**