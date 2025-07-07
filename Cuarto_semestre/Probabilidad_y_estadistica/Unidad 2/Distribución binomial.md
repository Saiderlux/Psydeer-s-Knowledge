Existen muchos experimentos que se ajustan exacta o aproximadamente a la siguiente lista de experimentos.
1. El Experimento consta de una secuencia de $n$ experimentos más pequeños llamados ensayos, donde $n$ se fija antes del experimento.
2. Cada ensayo puede dar por resultado uno de los mismo dos resultados posibles, los cuales se denotan como éxito ($E$) y falla ($F$).
3. Los ensayos son independientes, de modo que el resultado en cualquier ensayo particular no influye  en el resultado de cualquier otro ensayo.
4. La probabilidad de éxito es constante de un ensayo a otro; esta probabilidad se denota por $p$. Por ello, la probabilidad de fracaso será $1-p$

## Ejemplos
### Ejemplo 1
El color de las semillas de chícharo lo determina un solo lugar geométrico genético. SI los dos alelos en este lugar geométrico son AA o Aa (el genotipo),entonces el chícharo será amarillo (el fenotipo) y si el alelo es aa, el chícharo será verde. Suponga que aparean 20 semillas Aa y se cruzan las dos semillas en cada uno de los diez pares para obtener diez nuevos genotipos. Designe a cada nuevo genotipo como éxito ($E$ ) si es aa y falla ($F$) si es lo contrario

Entonces con esta identificación se $S$ y $F$, el experimento es binomial con $n=10$ y $p=P$ (genotipo aa). Si es igualmente probable que cada miembro del par contribuya con a o A, entonces $p=P(a)=P(a)=(\frac{1}{2})(\frac{1}{2}=\frac{1}{4})$

### Ejemplo 2
Para un experimento binomial, sea $p$ la probabilidad de un "éxito" y $1-p$ la probabilidad de un "fracaso en un solo ensayo; entonces la probabilidad de obtener $x$ éxitos en n ensayos, está dada por la función de probabilidad $f(x)$
$$F(x)=P(X=x)=()p^{x}(1-p)^{n-x}  \text{ para } x=0,1,2...n$$
### Ejemplo 3
La probabilidad de que un alumno se gane un punto extra es de 0.8 a partir de un volado, si quedan los últimos 5 alumnos, ¿Cuál será la probabilidad de que solo a 2 de ellos se ganen el punto extra?

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Proba/ANEXOS/ANEXOS/Ink/Drawing/2025.4.8 - 9.08am.drawing",
	"width": 864,
	"aspectRatio": 1.2953523238380809
}
```
$n= \text{número de ensayos}$
$p=\text{probabilidad de éxito}$
$X\sim B(n,p)$
$X\sim B(5,0.8)$
$x=0,1,2,3,4,5$
$f(x)=P(X=x)=\binom{n}{v}p^{x}(1-p)^{n-x}$

$$\binom{n}{x}=\frac{n!}{x!(n-x)!}=\frac{5!}{2!(5-2)!}= \frac{20}{2}=10$$

$$\binom{5}{2}(0.8)^{2}(1-0.8)^{5-2}=0.0512 \rightarrow 5.12\%$$
### Ejemplo 3
Considere un experimento binomial con 10 ensayos y $p=0.9$
1) LA probabilidad de obtener 9 éxitos
2) La probabilidad de obtener 9 o más éxitos
$n=10$
$P=0.9$
$X\sim B(10,0.9)$
$x=0,1,2,3,4,5,6,7,8,9,10$ 

**1)**
$$\binom{n}{x}=\frac{10!}{9!(1)!}=10$$
$$f(x)=P(X=9)=10(0.9)^{9}(1-0.9)^{10-9}=0.387 \rightarrow 38.7\%$$

**2)**
$$P(X\geq 9)=P(X=9)+P(X=10)$$
$$f(10)=P(X=10)=0.3487$$
$$P(X\geq 9)= 0.3847+0.3487=0.7361\rightarrow 73.61\%$$
### Ejemplo 4
