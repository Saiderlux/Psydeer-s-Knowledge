La distribución Gamma es un modelo continuo que generaliza la exponencial: describe el tiempo hasta que ocurren $k$ sucesos (o la suma de $k$ tiempos exponenciales independientes) en un proceso de Poisson con tasa constante.

En probabilidad la distribución gamma se utiliza comúnmente en estudios de supervivencia de fiabilidad o para modelar las probabilidades relacionadas con los tiempos de espera.

Función gamma
$$\Gamma(\alpha)=\int^\infty_{0}x^{\alpha-1}e^{-x}dx $$

Las propiedades más importantes de la función gamma son:

$$\Gamma(1)=1$$
$$\Gamma(n)=(n-1)!, \text{ }n\in\mathbb{N}$$
$$\Gamma\left(\frac{1}{2}\right)=\sqrt{\pi}$$
---

Se dice que una variable aleatoria continua $X$ tiene una distribución gama si la función de densidad de probabilidad de $X$ es

$$f(x,\alpha,\beta)=\begin{cases} \frac{1}{\beta^{\alpha}\Gamma(\alpha)}x^{\alpha-1}e^\frac{-x}{\beta} & x\geq0\\ 0 &\text{de lo contrario }x\\
\end{cases}$$

Donde los parámetros $\alpha$ y $\beta$ satisfacen $\alpha>0$, $\beta>0$. La distribución gamma estándar tiene $\beta=1$, así que da la función de densidad de probabilidad de una variable aleatoria estándar.

---
**Particularidad (exponencial)**

si $\alpha=1$
$$f(x)=\frac{1}{\beta^{1}\Gamma(1)}x^{1-1}e^\frac{-x}{\beta}$$
$$=\frac{1}{\beta} e^\frac{-x}{\beta}$$

| Propiedad       | Valor (forma-escala)   |
| --------------- | ---------------------- |
| Media E[X]      | $\alpha\beta$          |
| Varianza Var(X) | $\alpha\beta^2$        |
| MGF $M_{X}(t)$  | $(1-\beta t)^{\alpha}$ |

| FOrma            | Parametros                                                           | dfp f(x) (para x>0)                                                              |
| ---------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| ($\alpha,\beta$) | $\alpha>0$ (parametro de forma)<br>$\beta>0$ (paramteo de escala)    | $$f(x)=\frac{x^{\alpha-1}e^{\frac{-x}{\beta}}}{{\beta^{\alpha}}\Gamma(\alpha)}$$ |
| (k, $\lambda$)   | k>0 (forma) (k=$\gamma$)<br>$\lambda>0$ (tasa) ($\lambda=1/{\beta}$) | <br>$$f(x)=\frac{\lambda^{k}x^{k-1}e^{-\lambda x}}{\Gamma(k)}$$                  |

---

Cuando usarla
- Modelar tiempos de vida con aceleración o etapas (ej. sistemas de reserva).
- Suma de variables exponenciales (esperas en colas, total de lluvia acumulada)
- Prior conjugado de la Poisson en estadística bayesiana (familia Gamma-Poisson)


--- 
## Ejemplos
### Ejemplo 1

Las averías de una máquina ocurren a $\lambda=0.02$ fallas/hora.
¿Distribución del tiempo hasta la 3ra falla?

Para P(X<100)

$$f(x)=\frac{\lambda^{k}x^{k-1}e^{-\lambda x}}{\Gamma(k)}$$
k>0 (forma) (k=$\alpha$)
$\lambda>0$ (tasa) ($\lambda=\frac{1}{\beta}$)

$$\frac{0.02^{3}x^{3-1}e^{-0.002x}}{2}$$
$$T(k)=(k-1)!$$
$$=(3-1)!$$
$$2!=2$$
### Ejemplo 2
En base a datos previos se sabe que la longitud de tiempo en meses, entre las quejas de clientes por cierto producto puede ser descrita con la distribución gamma con parámetros $\alpha=2$ y $\beta=2$

$$\frac{x^{\alpha-1}e^\frac{-x}{\beta}}{\beta^{\alpha}\Gamma(\alpha)}$$

A) ¿Qué probabilidad hay de que se presente una queja en más de 20 meses?

$$\frac{x^{2-1}e^\frac{-x}{2}}{2^{2}(2-1)!}$$
$$=\frac{x^{1}e^\frac{-x}{2}}{4(1)}=\frac{xe^\frac{x}{2}}{2}$$

$$\int^{\infty}_{20}\frac{xe^\frac{-x}{2}}{4}dx$$

0.0027
B) ¿Cuál es la probabilidad de recibir una queja entre 15 y 18 meses?

---

SI X tiene una distribución gamma con parámetros $\alpha$ y $\beta$ entonces con cualquier x>0, la función de distribución acumulativa de X es:

$P(X\leq x)=F(x;\alpha,\beta)=F(\frac{x}{\beta};\alpha)$

Donde $F(.;\alpha)$ es la función gama incompleta

$f(x;\alpha)=\begin{cases}\frac{x^{\alpha-1}e^{-x}}{\Gamma(\alpha)} \\0 \end{cases}$ 

---
### Ejemplo 3
Sean X una variable aleatoria con distribución gamma $\alpha=5, \beta=2$ calcule
$P(10<x<15.2)$
$P(X>18.3)$

$\frac{x^{\alpha-1}e^{\frac{-x}{\beta}}}{\beta^{\alpha}\Gamma(\alpha)}$ 
$\Gamma(\alpha)=(\alpha-1)!$

1.
$\Gamma(alpha)=(\alpha-1)!=4!=24$
$P(10<x,15.2)=\int^{15.2}_{10} \frac{x^{5-1}e^{\frac{-x}{2}}}{2^{5}\cdot24}dx=\frac{1}{768}\int^{15.2}_{10}x^{4}e^{\frac{-x}{2}}dx$ 

Se calcula la integral

$=\frac{e^{\frac{x}{2}}}{384}(-x^{4}-8x^{3}-48x^{2}-192x-384)|^{15.2}_{10}$ 

$=0.3256\rightarrow 32.56\%$



**CUANDO SE DICE QUE TENEMOS UNA DISTRIBUCIÓN GAMMA ESTÁNDAR $\beta$=1**


### Ejemplo 4

Si X tiene una distribución gamma  estándar con 7 evalúe lo siguiente

a. P(X<=5)
b. P(X<5)
c. P(X>8)
d. P(3<=X<=8)
e. P(3<X<8)
f. P(X>4 o X>6)
