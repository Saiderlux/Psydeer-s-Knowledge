$$P(X=x)=p(1-p)^{x-1}$$
$X= \text{ número de ensayos hasta el primer éxito}$
$p= \text{ probabilidad de éxito en cada ensayo}$
$\text{ Esperanza(media) } E[X]=\frac{1}{p}$ 
$\text{ Varianza Var(X) }= \frac{1-p}{p^{2}}$ 

Suponiendo que tenemos un dado de las vegas
$\frac{1}{6}=0.166$
La probabilidad no cambia
$\frac{1}{6}+ \frac{1}{6} + \frac{1}{6} + \frac{1}{6} + \frac{1}{6} + \frac{1}{6} \rightarrow \text{ Por lo menos saldrá una vez el número 5}$

## EJemplo
Si la probabilidad de que un tirador experto de en el blanco del 95%
¿Cuál es la probabilidad de que falle por primera vez en su décimo quinto disparo?
$x=15$
$p=0.05$
$P(X=x)=(1-0.05)^{14}(0.95)=0.024$

¿Cuál es la probabilidad de que falle 1 de 15 disparos?
$P(X=x)=\binom{n}{x}=p^{x}(1-p)^{n-x}$
$P(X=x)=\binom{15}{1}=(0.05(0.95)^{15-1}=0.365$

## Ejemplo más perrillo

La probabilidad de calibrar un transductor en un instrumento electrónico de acuerdo con las especificaciones del sistema de medida es de 0.6. Asumiendo que los intentos de calibración son independientes ¿Cuál es la probabilidad de que cuando mucho tres intentos de calibración sean requeridos para satisfacer las especificaciones?
$P(1)=(0.6)(0.4)^{0}=0.6$
$P(2)=(0.6)(0.4)^{1}=0.24$
$P(3)=(0.6)(0.4)^{2}=0.096$

$P(x\leq 3)=1-q^{x}=1-(0.4)^{3}=0.936$


## Ejemplo
Si suponemos que el número de años que transcurren antes de que falle un transformador sigue una distribución geométrica con $p=0.00459$ ¿Cuál es la probabilidad de que falle durante los primeros 5 años?