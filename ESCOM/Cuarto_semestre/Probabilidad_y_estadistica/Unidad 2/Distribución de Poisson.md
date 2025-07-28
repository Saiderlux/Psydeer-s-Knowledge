Simeón Denis Poisson
La distribución de Poisson es un modelo de probabilidad discreto que describe el número de veces que ocurre un evento durante un intervalo fijo de tiempo. EL intervalo puede ser espacio, área, volumen u otra medida. Cuándo se cumplen estas condiciones:
1. Independencia: Los eventos ocurren de manera independiente entre sí.
2. Tasa constante: La media de ocurrencia ($\lambda, \mu$, o $E[X]$) es constante en todo intervalo.
3. Eventos raros o individuales: la probabilidad de más de un suceso simultáneo es prácticamente nula.
Se dice que una variable aleatoria de $X$ tiene una distribución de Poisson con parámetro $\lambda$ ($\lambda >0$) si la función masa de probabilidad de $X$ es:
$$f(x)=P(X=x)=p(x;\lambda)=\frac{e^{\lambda}\lambda^{x}}{x!}$$ $x=0,1,2,...$
$f(x)=P(X=x) \text{ probabilidad de x ocurrencias en un intervalo}$
$X=\text{número de sucesos observados}$
$\lambda= \text{media o tasa de sucesos por intervalo}$
$e\approx 2.71828$


En la enfermería de la escom se rescibe un promedio de $\mu=4$ pacientes al día. Sabiendo que el número de pacientes que llegan un díá sigue una distribución de Poisson, calcular:
A) la probabilidad de que lleguen tres pacientes en un día
$f(x)=P(X=x)=p(x;\lambda)$

$$\lambda=4$$
$$x=3$$
$f=3=\frac{e^{-4}4^{3}}{3!}=0.1954=19.54\%$