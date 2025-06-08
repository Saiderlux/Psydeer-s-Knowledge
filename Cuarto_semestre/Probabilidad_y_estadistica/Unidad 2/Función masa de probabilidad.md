
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
### Ejemplo 4
Sea $X$ la suma de los valores obtenidos al lanzar 2 dados justos de 6 caras. ¿Cuál es la probabilidad de cada combinación que se puede producir de cada valor?
Si se lanzan 2 dados justos de 6 caras, el total de resultados posibles es  
$$
6 \times 6 = 36
$$  
La variable aleatoria $$X$$, que representa la suma de los valores obtenidos, puede tomar valores de $$2$$ $$a$$ $$12$$ La función de masa de probabilidad se define como:  
$$
P(X = x) = \frac{\text{número de combinaciones que dan } x}{36}
$$

A continuación se listan las combinaciones para cada valor y su probabilidad:

- **Para $$X = 2$$:**  
  Combinaciones: $$ (1,1) $$  
  $$P(X=2)=\frac{1}{36}$$

- **Para $$X = 3$$:**  
  Combinaciones: $$ (1,2), (2,1) $$  
  $$P(X=3)=\frac{2}{36}$$

- **Para $$X = 4$$:**  
  Combinaciones: $$ (1,3), (2,2), (3,1) $$  
  $$P(X=4)=\frac{3}{36}$$

- **Para $$X = 5$$:**  
  Combinaciones: $$ (1,4), (2,3), (3,2), (4,1) $$  
  $$P(X=5)=\frac{4}{36}$$

- **Para $$X = 6$$:**  
  Combinaciones: $$ (1,5), (2,4), (3,3), (4,2), (5,1) $$  
  $$P(X=6)=\frac{5}{36}$$

- **Para $$X = 7$$:**  
  Combinaciones: $$ (1,6), (2,5), (3,4), (4,3), (5,2), (6,1) $$  
  $$P(X=7)=\frac{6}{36}$$

- **Para $$X = 8$$:**  
  Combinaciones: $$ (2,6), (3,5), (4,4), (5,3), (6,2) $$  
  $$P(X=8)=\frac{5}{36}$$

- **Para $$X = 9$$:**  
  Combinaciones: $$ (3,6), (4,5), (5,4), (6,3) $$  
  $$P(X=9)=\frac{4}{36}$$

- **Para $$X = 10$$:**  
  Combinaciones: $$ (4,6), (5,5), (6,4) $$  
  $$P(X=10)=\frac{3}{36}$$

- **Para $$X = 11$$:**  
  Combinaciones: $$ (5,6), (6,5) $$  
  $$P(X=11)=\frac{2}{36}$$

- **Para $$X = 12$$:**  
  Combinaciones: $$ (6,6) $$  
  $$P(X=12)=\frac{1}{36}$$

---

### Función de masa de probabilidad

Se puede expresar de la siguiente manera:

$$
f(x) =
\begin{cases}
\frac{1}{36} & \text{si } x = 2 \\
\frac{2}{36} & \text{si } x = 3 \\
\frac{3}{36} & \text{si } x = 4 \\
\frac{4}{36} & \text{si } x = 5 \\
\frac{5}{36} & \text{si } x = 6 \\
\frac{6}{36} & \text{si } x = 7 \\
\frac{5}{36} & \text{si } x = 8 \\
\frac{4}{36} & \text{si } x = 9 \\
\frac{3}{36} & \text{si } x = 10 \\
\frac{2}{36} & \text{si } x = 11 \\
\frac{1}{36} & \text{si } x = 12 \\
0 & \text{en otro caso}
\end{cases}
$$

---
