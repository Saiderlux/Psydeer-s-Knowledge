La ecuación característica
El método es una ampliación del de orden 2
La ecuación diferencial
$$y^{(n)}+a_{n-1}y^{(n-1)}+...+a_{2}y''+a_{1}y'+a_{0}y=0$$
$$a_{1}(i=0,...,n-1)=ctes$$
Polinomio característico:
$$\lambda^{n}+a_{n-1}\lambda^{n-1}+...+a_{2}\lambda^{2}+a_{1}\lambda+a_{0}=0$$
## Casos
### Caso 1
n raíces reales diferentes $\lambda_{1},...,\lambda_{n}$
$$y=c_{1}e^{\lambda_{1}x}+c_{2}e^{\lambda_{2}x}+...+c_{n}e^{\lambda_{n}x}$$
### Caso 2
Raíces complejas a pares conjugados

$$\begin{cases} \lambda_{1}=a+bi\\
 \lambda_{2}=a-bi\\ \lambda_{3}=c+di\\
\lambda_{4}=c-di
\end{cases}$$
$y=c_{1}e^{ax}\cos{bx}+c_{2}e^{ax}\sin{bx}+c_{3}e^{cx}\cos{dx}+c_{4}e^{cx}\sin{dx}$
por cada par.
### Caso 3
$\lambda_{k}$ es una raíz de multiplicidad p. es decir en la ecuación característica sale $(\lambda-\lambda_{k})^{p}$
$$y=c_{1}e^{\lambda_{k}x}+c_{2}xe^{\lambda_{k}x}+c_{3}x^{2}e^{\lambda_{k}x}+...+c_{p}x^{p-1}e^{\lambda_{k}x}$$

## Ejemplo 1

## Ejemplo 2

```handwritten-ink
{
	"versionAtEmbed": "0.2.6",
	"filepath": "Tercer_Semestre/Ecuaciones diferenciales/ANEXOS/Ink/Writing/2024.11.25 - 12.14pm.writing"
}
```
## Ejemplo 3

```handwritten-ink
{
	"versionAtEmbed": "0.2.6",
	"filepath": "Tercer_Semestre/Ecuaciones diferenciales/ANEXOS/Ink/Writing/2024.11.25 - 12.18pm.writing"
}
```
## Ejemplo 4

```handwritten-ink
{
	"versionAtEmbed": "0.2.6",
	"filepath": "Tercer_Semestre/Ecuaciones diferenciales/ANEXOS/Ink/Writing/2024.11.25 - 12.19pm.writing"
}
```
## Ejemplo 5
$$y^{(4)}-4y'''+7y''-4y'+6y=0$$
$$\lambda^{4}-4\lambda^{3}+7\lambda^{2}-4\lambda+6=0$$
$6=3^{1}\cdot 2^{1}$
#$div (1+1)(1+1)=2\cdot 2=4$
$\pm6$
$\pm3$
$\pm2$
$\pm1$

$$\lambda_{1}=2+\sqrt{2}i$$
$$\lambda_{2}=2-\sqrt{2}i$$
$$\lambda_{3}=i$$
$$\lambda_{4}=-i$$
$$y=c_{1}e^{2x}\cos{\sqrt{2}x}+c_{2}e^{2x}\sin{\sqrt{2}x}+c_{3}\cos{x}+c_{4}\sin{x}$$

## Ejemplo 6
$$y^{(4)}+8y'''+24y''+32y'+16y=0$$
$$\lambda^{4}+8\lambda^{3}+24\lambda^{2}+32\lambda+16=0$$
$$(\lambda+2)^{4}=0$$
$\lambda_{1}=\lambda_{2}=\lambda_{3}=\lambda_{4}=-2$
Caso 3
$$y=c_{1}e^{-2x}+c_{2}xe^{-2x}+c_{3}x^{2}e^{-2x}+c_{4}x^{3}e^{-2x}$$
