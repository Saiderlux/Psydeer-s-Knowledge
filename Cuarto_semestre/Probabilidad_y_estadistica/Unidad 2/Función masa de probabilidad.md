
La **función de masa de probabilidad** es una función matemática que describe la probabilidad de que una **variable aleatoria discreta** tome un valor específico.

## Definición formal

Sea $X$ una **variable aleatoria discreta**. La función de masa de probabilidad de $X$ es una función:

$$
f(x) = P(X = x)
$$

donde $f(x)$ asigna a cada valor posible $x$ la **probabilidad** de que $X$ tome ese valor.

## Propiedades

1. **No negatividad:**  
   $$
   f(x) \geq 0 \quad \text{para todo } x
   $$

2. **Suma total de 1:**  
   $$
   \sum f(x) = 1
   $$

3. Probabilidad de que cada valor especifico : $f(x)$ asigna una probabilidad a cada valor posible de $x$ 

## Ejemplos
### Ejemplo 1
Supón que $X$ representa el resultado de lanzar un dado justo. Entonces la fmd es:

$$
f(x) = \begin{cases}
\frac{1}{6} & \text{si } x \in \{1, 2, 3, 4, 5, 6\} \\
0 & \text{en otro caso}
\end{cases}
$$

Cada valor tiene probabilidad igual a $\frac{1}{6}$, y la suma de las probabilidades es 1.

---
### Ejemplo 2
Lanzamiento de 3 veces una moneda
$X=\text{\# de soles}$
$$f(x) = \begin{cases}
\frac{1}{8} & \text{si } x =\{0,3\} \\
\frac{3}{8} & \text{si }x=\{1,2\}
\end{cases}$$
### Ejemplo 3
Utilizando la función de masa de probabilidad (FMD) para el lanzamiento de un dado de 6 caras, se tiene que los valores posibles de \(X\) son:  
$$
\{1, 2, 3, 4, 5, 6\}
$$

La función de masa de probabilidad se define como:
$$
P(X = x) = \frac{1}{6}, \quad x \in \{1,2,3,4,5,6\}
$$

**Pregunta:** ¿Cuál es la probabilidad de obtener un número mayor que 4?
Para obtener un número mayor que 4, se deben considerar los valores:
$$
\{5, 6\}
$$

Cada uno de estos resultados tiene una probabilidad de:
$$
\frac{1}{6}
$$

Por lo tanto, la probabilidad total es la suma de las probabilidades de los eventos individuales:
$$
P(X > 4) = P(X=5) + P(X=6) = \frac{1}{6} + \frac{1}{6} = \frac{2}{6} = \frac{1}{3}
$$