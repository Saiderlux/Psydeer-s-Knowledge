Para los siguientes 4 modelos recurrentes, determine su modelo equivalente sin recurrencia mediante el método de sustitución.

## Ejercicio 01:
$$T(n)=4T(n-2)+T(n-1)+T(n-3)+3T(n-4)$$
con $$T(n)=1 \text{ para toda } n<=4$$
Podemos reescribirla como:
$$T(n)-T(n-1)-4T(n-2)-T(n-3)-3T(n-4)=0$$
Sustituyendo $T(n)=x^{k}$ y $k=4$
 $$T(n)=x^{4}$$
$$x^{4}-x^{3}-4x^{2}-x-3=0$$
Y tenemos que:
$$r_{1}=2.739379857$$
$$r_{2}=-1.67341383$$
$$r_{3}=-0.032983013+0.80829809i$$
$$r_{3}=-0.032983013-0.80829809i$$
Entonces, como son raíces distintas tenemos
$$T(n)=c_{1}(2.739379857)^{n}+c_{2}(-1.67341383)^{n}+c_{3}(-0.032983013+0.80829809i)^{n}+c_{4}(-0.032983013-0.80829809i)^{n}$$
Y tenemos que, para n=0, n=1, n=2, n=3, T(n)=1
$$\begin{cases} c_1 \cdot (2.73937987)^1 + c_2 \cdot (-1.673413883)^1 + c_3 \cdot (-0.032983013 + 0.80829809i)^1 + c_4 \cdot (-0.032983013 - 0.80829809i)^1 = 1 \\[10pt] c_1 \cdot (2.73937987)^2 + c_2 \cdot (-1.673413883)^2 + c_3 \cdot (-0.032983013 + 0.80829809i)^2 + c_4 \cdot (-0.032983013 - 0.80829809i)^2 = 1 \\[10pt] c_1 \cdot (2.73937987)^3 + c_2 \cdot (-1.673413883)^3 + c_3 \cdot (-0.032983013 + 0.80829809i)^3 + c_4 \cdot (-0.032983013 - 0.80829809i)^3 = 1 \\[10pt] c_1 \cdot (2.73937987)^4 + c_2 \cdot (-1.673413883)^4 + c_3 \cdot (-0.032983013 + 0.80829809i)^4 + c_4 \cdot (-0.032983013 - 0.80829809i)^4 = 1 \end{cases}$$

Resolviendo este sistema, obtenemos los valores de $c_1, c_2, c_3$ y $c_4$ para expresar la solución no recurrente de $T(n)$.

$$c_1 \approx 0.0456, \quad c_2 \approx -0.1212, \quad c_3 \approx -0.7956 - 0.3834i, \quad c_4 \approx -0.7956 + 0.3834i $$
Por lo tanto, sustituyendo tenemos:
$$T(n) = 0.0456 \cdot (2.73937987)^n - 0.1212 \cdot (-1.673413883)^n - (0.7956 + 0.3834i) \cdot (-0.032983013 + 0.80829809i)^n - (0.7956 - 0.3834i) \cdot (-0.032983013 - 0.80829809i)^n$$
Dado que el término dominante en esta expresión es $(2.73937987)^n$ la cota asintótica de $T(n)$ es:

$$T(n) = \Theta((2.73937987)^n)$$

Esto indica que el crecimiento de $T(n)$ es exponencial en función de $n$.
### Código utilizado para calcular los valores de las constantes
```python
import numpy as np

# Valores de las raíces
r1 = 2.73937987
r2 = -1.673413883
r3 = -0.032983013 + 0.80829809j
r4 = -0.032983013 - 0.80829809j

# Matriz del sistema de ecuaciones para n=1, 2, 3, 4
A = np.array([
    [r1*1, r21, r31, r4*1],
    [r1*2, r22, r32, r4*2],
    [r1*3, r23, r33, r4*3],
    [r1*4, r24, r34, r4*4]
], dtype=complex)

# Vector de resultados para T(1) = T(2) = T(3) = T(4) = 1
b = np.array([1, 1, 1, 1], dtype=complex)

# Resolver el sistema de ecuaciones lineales
x = np.linalg.solve(A, b)
x
```

## Ejercicio 2:
$$T(n)=T(n-1)+3$$
Con $$T(0)=4$$
Podemos reescribirla como 
$$T(n)-T(n-1)=3$$
Con $k=1$,   $b=1$,   $d=0$
$$(x-1)(x-1)^{1}=0$$
$$r_{1}=1, \text{  } r_{2}=1$$
$$T(n)=c_{1}n^{2-1}1^{n}+c_{2}n^{1-1}1^{n}$$
$$T(n)=nc_{1}+c_{2}$$
Ahora, tenemos que para $T(0)=4$, por lo tanto sustituimos $\rightarrow T(0)=c_{2}=4$
$$\begin{align} 
T(1)&=T(0)+3+T(1)=4+3=7 \\
T(1)&=nc_{1}+c_{2}=7\\
T(1)&=nc_{1}+4=7 \rightarrow c_{1}=3
\end{align}
$$
Lo cual, sustituyendo, nos da como resultado:
$$T(n)=3n+4$$
Dado que el término dominante de la expresión es 3n, la cota asintótica de T(n) es:
$$\Theta (n)$$



## Ejercicio 3.
$$T(n)=-5T(n-1)-6T(n-2)+(42)(4^{n})$$
Con $$T(0)=18 \text{ y } T(1)=61$$
Podemos reescribirla como:
$$T(n)+5T(n-1)-6T(n-2)=42(4^{n})$$
Tenemos que $T(n)=x^{k}$, $k=2$, $b=4$ y $d=0$
Así, nos queda:
$$\begin{align}
(x^{2}+5x+6)(x-4)&=0\\
(x+3)(x+2)(x-4)&=0\\
\end{align}
$$
Lo que nos deja con:
$$\begin{align}
r_{1}&=-3\\ r_{2}&=-2 \\r_{3}&=4
\end{align}
$$
Entonces, sustituyendo:
$$T(n)=c_{1}(-3)^{n}+c_{2}(-2)^{n}+c_{3}(4^{n})$$
Considerando que $T(0)=18$, tenemos que:
$$\begin{align}
T(0)&=c_{1}+c_{2}+c_{3}=18\\
T(1)&=-3c_{1}-2c_{2}+4c_{3}=61
\end{align}
$$
Como nos queda un sistema de 3x2, podemos calcular el valor de la función en T(2) para tener un sistema 3x3 y que sea más sencillo de resolver. 
$$\begin{align}
T(2)&=-5T(2-1)-6T(2-2)+42(4^{2})\\
T(2)&=-5T(1)-6T(0)+42(16)\\
T(2)&=-5(61)=6(18)+42(16)=259\\
T(2)&=9c_{1}+4c_{2}+16c_{3}=259
\end{align}
$$
Así tenemos el sistema de ecuaciones:
$$\begin{cases} 
c_{1}+c_{2}+c_{3}=18\\
-3c_{1}-2c_{2}+4c_{3}=61 \\
9c_{1}+4c_{2}+16c_{3}=259
\end{cases}$$
Resolviendo este sistema, obtenemos los valores de $c_1, c_2, c_3$, para expresar la solución no recurrente de $T(n)$.
$$c_1 =-1, \quad c_2 = 3, \quad c_3=16$$
Por lo tanto, sustituyendo tenemos:
$$T(n)=-(-3)^{n}+3(-2)^{n}+16(4)^{n}$$Dado que el término dominante en esta expresión es $(4)^n$ la cota asintótica de $T(n)$ es:$$\Theta(4^{n})$$
## Ejercicio 4
$$T(n)=5T(n-2)+3T(n-1)$$
Con $$T(1)=2 \text{ y } T(2)=-3$$
Tenemos $T(n)=x^{k}$ y $k=2$
Podemos reescribirla como:
$$T(n)-3T(n-1)-5T(n-2)=0$$
Lo cual podemos sustituir como:
$$x^{2}-3x-5=0$$
Lo cual nos deja con sus raíces:
$$\begin{align}
r_{1}&=4.192582404\\
r_{2}&=-1.192582404
\end{align}
$$
Así, tenemos que:
$$T(n)=c_{1}(4.192582404)^{n}+c_{2}(-1.192582404)^{n}$$

Y tenemos que $T(1)=2$ y $T(2)=-3$, entonces, sustituyendo:
$$\begin{align}
T(1)&=c_{1}(4.192582404)+c_{2}(-1.192582404)=2\\ 
T(2)&=c_{1}(17.57774721)+c_{2}(-1.422252789)=-3
\end{align}
$$
Así, tenemos el sistema de ecuaciones:
$$\begin{cases}   c_{1}(4.192582404)+c_{2}(-1.192582404)&=2\\ 
c_{1}(17.57774721)+c_{2}(1.422252789)&=-3
\end{cases}$$
Resolviendo este sistema, obtenemos los valores de $c_1, c_2$, para expresar la solución no recurrente de $T(n)$.
$$\begin{align}
c_{1}&=-0.02723191063\\
c_{2}&=-1.772768089
\end{align}
$$
Así, la función no recurrente T(n) es:
$$T(n)=-0.02723191063(4.192582404)^{n}-1.772768089(-1.192582404)^{n}$$
Dado que el término dominante en esta expresión es $(4.192582404)^n$ la cota asintótica de $T(n)$ es:$$\Theta((4.192582404)^{n})$$
## Ejercicio 5.
$$T(n)=3T(n-2)-2T(n-3)$$
Con $$T(0)=-1 \text{,  } T(1)=4 \text{ y }T(2)=8$$Podemos reescribirlo como:
$$T(n)-3T(n-2)+2T(n-3)=0$$
Tenemos $T(n)=x^{k}$ y $k=3$
Lo que nos deja con:
$$x^{3}-3x+2=0$$
De la que obtenemos las siguientes raíces: $$\begin{align}
r_{1}&=-2\\
r_{2}&=1\\
r_{3}&=1
\end{align}$$
Ahora, tenemos que $T(0)=-1$, $T(1)=4$ y $T(2)=8$, por lo tanto:
$$\begin{align}
T(0)&=c_{2}+c_{3}=-1\\
T(2)&=c_{1}+c_{2}-2c_{3}=4\\
T(2)&=2c_{1}+c_{2}+4c_{3}=8\\
\end{align}$$
Lo cual nos deja con el sistema de ecuaciones:
$$\begin{cases}
c_{2}+c_{3}&=-1\\
c_{1}+c_{2}-2c_{3}&=4\\
2c_{1}+c_{2}+4c_{3}&=8\\
\end{cases}$$
El cual nos deja con las constantes:
$$\begin{align}
c_{1}&=4.666666667\\
c_{2}&=0.8888888889\\
c_{3}&=0.111111111111
\end{align}
$$
Lo que nos deja con la función no recurrente T(n):
$$T(n)=\frac{14}{3}n-\frac{8}{9}-\frac{1}{9}(-2)^{n}$$
