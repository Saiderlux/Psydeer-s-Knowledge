Se resuelve con una sustitución
$$\frac{dy}{dx}+p(x)y=f(x)\cdot y^{n}$$
$$n \in \mathbb{R}$$
si $n=0, n=1 \rightarrow$ lineal
$n \neq 2$ sustituyo
$$u=y^{1-n}$$
$\rightarrow$ La ecuación es lineal

##### Ejemplo
Resolver Bernoulli
$$x\cdot \frac{dy}{dx}+y=x^{2}y^{2}$$
$$\frac{dy}{dx}+\frac{1^{y}}{x}=xy^{2}\rightarrow \text {Bernoulli}$$
Sustituyendo.
$$n=1$$
$$u=y^{1-n}=y^{1-2}=y^{-1}=\frac{1}{y} $$
$$u=\frac{1}{y}$$
$$\rightarrow y=\frac{1}{u}=u^{-1}$$
$$\rightarrow \frac{dy}{dx}=-u^{-2}\cdot \frac{du}{dx}$$
Sustituyendo
$$-u^{-2}\cdot \frac{du}{dx}+\frac{1}{x}\frac{1}{u}=x(\frac{1}{u})^{2}$$
$$\frac{-1}{u^{2}}\frac {du}{dx}+\frac{1}{x}\frac{1}{u}=\frac{x}{u^{2}}$$
Multiplico por $-u^{2}$
$$\frac{du}{dx}-\frac{1}{x}u=-x$$
$$I=e^{\int p(x)dx}=e^{-\int \frac{1}{x}dx}=e^{- \ln{|x|}}$$
