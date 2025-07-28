La ecuación diferencial lineal no homogénea
$$L(y)=\phi(x)$$
$$y^{(n)}+a_{n-1}(x)y^{(n-1)}+...+a_{1}(x)y'+a_{0}(x)y=\phi(x)$$
Tiene la solución general
$$y=y_{p}+y_{h}$$
$y_{p} \rightarrow no homogenea$  
$y_{h} \rightarrow homogenea$, Coeficientes constantes polinomio característico orden 1, $I=e^{\int{p(x)dx}}$ 

EL método de coeficientes indeterminados funciona para hallar $y_{p}$ cuando te conduce $y_{h}$

Se inicia ensayando la forma partículas de $y_{p}$ hasta llegar a constantes arbitrarias, luego se sustituye $y_{p}$ para hallar las constantes.

**Solo funciona con coeficientes constantes. a:=ctes**

##### Modificaciones
Si cualquier término de $y_{p}$ es también un término de $y_{n}$, se debe multiplicar $y_{p}$ por $x^{m}$ hasta que ya no tengan términos en común.

##### Generalizaciones
Si $\phi(x)$ es la suma o diferencia de casos entonces $y_{p}$ también será la suma o diferencia de casos.
### _Forma simple del método_
#### **Caso 1** 
$$\phi(x)=p_{n}(x)$$ un polinomio en x de grado n.
Suponga $y_{p}=A_{n}x^{n}+A_{n-1}x^{n-1}+...+A_{1}x+A_{0}$
$A_{j}=ctes(j=0,...,n)$ que deben hallarse

#### **Caso 2**

$\phi(x)=e^{\alpha x}p_{n}(x)=cte, P_{n}(x)$ es como en caso 1

$y_{p}=e^{\alpha x}(A_{n}x^{n}+A_{n-1}x^{n-1}+...+A_{1}x+A_{0})$
$A_{i}=ctes$

#### **Caso 3**

$\phi (x)=e^{\alpha x}p_{n}(x)\sin{\beta x}$, $\alpha, \beta=ctes$  $p_{n}(x)=$ caso 1

$y_{p}=e^{\alpha x}\sin{\beta(x)}(A_{n}x^{n}+A_{n-1}x^{n-1}+...+A_{1}x+A_{0})+ e^{\alpha x}\cos{\beta x}(B_{n}x^{n}+B_{n-1}x^{n-1}+...+B_{1}x+B_{0})$
$A_{i}, B_{i}=ctes$

#### **Caso 4**

$\phi(x)=e^{\alpha x}p_{n}(x)\cos{\beta x},$  $\beta,\alpha=ctes$, $p_{n}(x)=$ caso 1
$y_{p}=$ igual al caso 3

Se inicia ensayando la forma particular de $y_{p}$ hasta llegar a constantes arbitrarias. Luego se sustituye $y_{p}$ para hallar las constates.
**Solo funciona con**