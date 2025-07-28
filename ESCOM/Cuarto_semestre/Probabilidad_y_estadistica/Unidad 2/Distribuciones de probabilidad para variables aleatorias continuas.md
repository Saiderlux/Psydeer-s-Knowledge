Distribución exponencial
La **distribución exponencial** es el modelo continuo clásico, para describir el tiempo de espera entre sucesos aislados que se producen de manera aleatoria pero con tasa media constante.

Ejemplo:
Tiempo de espera en ser atendido en la fila de las tortillas
Tiempo de vida de un componente
Tiempo necesario para cargar un camión

SI T es el tiempo (positivo) hasta que ocurre el siguiente suceso, escribimos
$T \sim Exp (\mu)$ o $T\sim Exp(\lambda)$

Donde
Tasa (rate) $\lambda>0$ \[Sucesos por unidad de tiempo\]
Media $\mu=\frac{1}{\lambda}$ \[Tiempo medio entre sucesos\] 

---
Se dice que $X$ tiene una distribución exponencial con parámetro $\lambda(\lambda>0)$ si la función de densidad de probabilidad de $X$ es
$f(x;\lambda)=\lambda e^{-\lambda x}$      $x>0$
$f(x;\mu)=\frac{1}{\mu}e^\frac{-x}{\mu}$ 

El valor esperado de una variable aleatoria exponencialmente distribuida $X$ es
$E(X)=\int^{\infty}_{0}x\lambda e^{-\lambda x}dx$ 
$\mu=\frac{1}{\lambda}$
$\sigma^{2}=\frac{1}{\lambda^{2}}$ 

---
## Ejemplos
### Ejemplo 1
El tiempo que tara para cargar un camión obedece a una distribución exponencial. La media del tiempo de espera para cargarlo es de 15 minutos
¿Cuál es la probabilidad de que la carga de un camión dure 6 minutos o menos?