
Calcular el valor esperado y la varianza de una variable aleatoria de Bernoulli (p)

$$\mu \sum xP(x)$$
$$\mu=0P(0)+1P(1)$$
$$\mu= 0 +P(1)$$
$$\mu = P(1)$$
*Varianza*
$v=\sum x^{2}P(x)-\mu^{2}$ 

$$v=0^{2}P(0)+1^{2}P(1)-P(1)^{2}$$
$$v=P(1)-P(1)^{2}$$

$$F(x)=P(X<=x)\case$$

### Ejemplos

1.
Espacio de muestra
S S S $\frac{1}{8}$ *
S S A $\frac{1}{8}$ *
S A S $\frac{1}{8}$ *
S A A $\frac{1}{8}$
A S S $\frac{1}{8}$ *
A S A $\frac{1}{8}$
A A S $\frac{1}{8}$
A A A $\frac{1}{8}$
Definimos con que ganamos: Sol

|          | 0             | 1             |
| -------- | ------------- | ------------- |
| $P(X-x)$ | $\frac{4}{8}$ | $\frac{4}{8}$ |
|          | $\frac{7}{8}$ | $\frac{1}{8}$ |
$$f(x)=\begin{cases}
\frac{7}{8}, & \text{si } x = 0, \\
\frac{1}{8}, & \text{si } x = 1.
\end{cases}
$$ Si la moneda está cargada
$$S=0.25$$

```handdrawn-ink

{
	"versionAtEmbed": "0.3.4",
	"filepath": "Cuarto_semestre/Probabilidad_y_estadistica/ANEXOS/Ink/Drawing/2025.4.7 - 11.23am.drawing",
	"width": 712,
	"aspectRatio": 1.1807628524046434
}
```
$$SSS=(0.25)(0.25)(0.25)=\frac{1}{64}$$
$$f(x)=\begin{cases} \frac{63}{64} & x=0\\ \\
\frac{1}{64} & x=1
\end{cases}$$
### Ejemplos
La probabilidad de que un alumno se gane un punto extra es de 0.8 a partir de un volado. Si quedan los últimos 3 alumnos, ¿Cuál será la probabilidad de que solo a 2 de ellos se ganen el punto extra?


| Dorantes | Horta | Rocha |
| -------- | ----- | ----- |
| Si       | Si    | No    |
| SI       | No    | Si    |
| No       | Si    | Si    |

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Proba/ANEXOS/Ink/Drawing/2025.4.8 - 8.51am.drawing",
	"width": 878,
	"aspectRatio": 2.398907103825137
}
```
$P(2)=0.384$


