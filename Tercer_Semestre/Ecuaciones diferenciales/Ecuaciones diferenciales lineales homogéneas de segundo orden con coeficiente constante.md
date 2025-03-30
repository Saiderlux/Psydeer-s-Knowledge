## I. Ecuación característica
Correspondiente a la ecuación diferencial 
$$y''+a_{1}y'+a_{0}y=0$$
$$a_{1}, a_{0}= ctes$$
$\exists$ la ecuación característica, polinomio característico
$$\lambda^{2}+a_{1}\lambda+a_{0}=0$$
Reemplazo $$y''\rightarrow \lambda^{2}$$$$y'\rightarrow \lambda$$
$$y\rightarrow 1$$
Es una ecuación algebraica de segundo grado
$$\begin{align}
\lambda^{2}+a_{1}\lambda+a_{0}=0\\
(\lambda-\lambda_{1})(\lambda-\lambda_{2})=0
\end{align}$$
Factorizar $$\begin{align}
\lambda=\lambda_{1}\\
\lambda=\lambda_{2}
\end{align}$$
Solución en términos de raíces características dependiendo de los valores de $\lambda_{1}$ y $\lambda_{2}$ se tienen tres casos:
### Caso 1.
$\lambda_{1}$ y $\lambda_{2}$ son reales y diferentes.
Dos soluciones l.i son $e^{\lambda_{1}x}$ y $e^{\lambda_{2}x}$ y la solución general es:
$$Y=c_{1}e\lambda^{_{1}x}+c_{2}e^{\lambda_{2}x}$$
en el caso en que $\lambda_{1}=-\lambda_{2}$ la solución es:
$$y=k_{1}\cosh{\lambda_{1}x}+k_{2}\sinh{\lambda_{1}x}$$
$k_{1}=c_{1}+c_{2}$
$k_{2}=c_{1}-c_{2}$
$\cosh{\lambda_{1}x}=\frac{1}{2}(e^{\lambda_{1}x}+e^{-\lambda_{1}x})$
$\sinh{\lambda_{1}x}=\frac{1}{2}(e^{\lambda_{1}x}-e^{-\lambda_{1}x})$ 

### Caso 2.
2 raíces complejas
Si $\lambda_{1}=a+ib$ como las raíces complejas aparecen a pares $\rightarrow \lambda_{2}=a-ib$ (Complejo conjugado).
Dos soluciones l.i son $e^{(a+ib)x}, e^{(a-ib)x}$. La solución general es
$$y=d_{1}e^{(a+ib)x}+d_{2}e^{(a-ib)x}$$
transformaremos usando la identidad de Euler
$$\begin{align}
e^{ibx}=\cos{bx}+i\sin{bx}\\
e^{-ibx}=\cos{bx}-i\sin{bx}
\end{align}$$
Sustituyendo
$$\begin{align}
y&=e^{ax}[d_{1}e^{ibx}+d_{2}e^{-ibx}]\\
y&=e^{ax}[d_{1}(\cos{bx}+i\sin{bx})+d_{2}(\cos{bx}-i\sin{bx})] \\
y&=e^{ax}[d_{1}\cos{bx}+d_{1}i\sin{bx}+d_{2}\cos{bx}-d_{2}i\sin{bx}]\\
y&=e^{ax}[(d_{1}+d_{2})\cos{bx}+(d_{1}-d_{2})i\sin{bx}]\\
y&=e^{ax}[c_{1}\cos{bx}+c_{2}\sin{bx}]
\end{align}
$$
### Caso 3.
$\lambda_{1}=\lambda_{2}$
Dos soluciones l.i. son $e^{\lambda_{1}x}, xe^{\lambda_{1}x}$
$\rightarrow$ la solución es
$$y=c_{1}e^{\lambda_{1}x}+c_{2}xe^{\lambda_{1}x}$$
