En este caso, el tamaño de la población es $N=20$, el tamaño de la muestra es $n=5$ y el número de éxitos (inyección de tinta $=E$) y las fallas ($F$) en la población son $M=12$ y $N-M=8$, respectivamente. Considérese el valor $x=2$. Como todos los resultados (cada uno consta de 5 solicitudes) son igualmente probables.

**Tradicionalmente**
*El primero es 12 de 20 y el segundo 11 de 19 porque nuestra x es solo 2, por eso después escogemos de los 8 que fallan*
$$\frac{12}{20}\left(\frac{11}{19}\right)\left(\frac{8}{18}\right)\left(\frac{7}{17}\right)\left(\frac{6}{16}\right)=0.024$$
*Esto es en el caso de que los primeros salgan de inyección y los siguientes sean fallas*
$$\text{E E F F F}$$
*Pero puede salir así*
$$\text{F F F E E}$$
$$\text{F E F E F}$$
*Entonces para considerar todas las posibles tenemos*
$$\frac{12}{20}\left(\frac{11}{19}\right)\left(\frac{8}{18}\right)\left(\frac{7}{17}\right)\left(\frac{6}{16}\right) \binom{5}{2}=0.024\cdot 10= 0.24\rightarrow 24\%$$
*En este caso es 5 porque es la n que nos dan y 2 porque estamos buscando específicamente 2 casos de éxitos*

---
La distribución hipergeométrica modela la probabilidad de obtener exactamente $x$ éxitos al extraer sin reemplazo $n$ elementos de una población finita de $N$ elementos que contiene $K$ éxitos en total.

Las suposiciones que conducen a la distribución hipergeométrica son las siguientes:
1. La población o conjunto que se va a muestrear se compone de $N$ individuos, objetos o elementos (una población finita).
2. Cada individuo puede ser caracterizado como éxito ($E$) o falla ($F$) y hay $M$ éxitos en la población.
3. Se selecciona una muestra de $n$ individuo sin reemplazo de tal modo que cada subconjunto de tamaño $n$ es igualmente probable de ser seleccionado.

$X ~ \text{Hipergeométrica}(N,K,n)$


| Símbolo | Significado |
| ------- | ----------- |
| N       |             |
|         |             |
|         |             |

---
## Ejemplos
### Ejemplo 1
Una caja contiene $N=20$ componentes, de los cuales $K=6$ son defectuosos. Se inspeccionan $n=5$ componentes al azar sin reposición.
$P(\text{ exactamente 2 defectuosos})=$

Población $N=20$ componentes
Defectuosos $K=6$
Buenos $N-K=14$
Se extraen $n=5$ sin reemplazo
*En este caso que sean defectuosos es nuestro caso de éxito, por lo tanto los primeros dos son las probabilidades de que salgan dos defectuosos*
$$\frac{6}{20}\left(\frac{5}{19}\right)\left(\frac{14}{18}\right)\left(\frac{13}{17}\right)\left(\frac{12}{16}\right)\binom{5}{3}$$
SI X es el número de éxitos ($E$) en una muestra completamente aleatoria de tamañó $n$ extraída de la población de compuesta de $M$ éxitos y ($N-M$) fallas, entonces la distribución de probabilidad de X llamada distribución hipergeométrica es
$$P(X=x)=h(x;n,M,N)=\frac{\binom{M}{x}\binom{N-M}{n-x}}{\binom{N}{n}}$$$\binom{M}{x}$: formas de elegir x éxitos
$\binom{N-M}{n-x}$: formas de elegir los $n-x$ fracasos
$\binom{N}{n}$: todas las muestras posibles de tamaño $n$

*Volviendo a la resolución*
$$\frac{6}{20}\left(\frac{5}{19}\right)\left(\frac{14}{18}\right)\left(\frac{13}{17}\right)\left(\frac{12}{16}\right)\binom{5}{3}=035$$
*Si lo hacemos con la formula*
$$\frac{\binom{6}{2}\binom{14}{3}}{\binom{20}{5}}=0.35$$
---
- **Binomial**: muestreo con reemplazo (o población muy grande); probabilidades idénticas en cada extracción.
- **Hipergeométrica**: muestreo sin reemplazo.
### Ejemplo 2

Durante un periodo particular una oficina de tecnología de la información de una universidad recibió 20 solicitudes de servicio de problemas con impresoras, de las cuales 8 eran impresoras láser y 12 eran modelos de inyección de tinta. Se tiene que seleccionar una muestra de 6 de estas solicitudes de servicio completamente al azar, de modo que cualquier subconjunto de tamaño 6 tenga la misma probabilidad de ser seleccionado como cualquier otro subconjunto. ¿Cuál es la probabilidad de que exactamente $x=2$ de las solicitudes de servicio fueran para impresoras de inyección de tinta?
$N=20$
$E= \text{tinta}=12$
$F=20-12=8$

$$\frac{\binom{12}{2}\binom{8}{4}}{\binom{20}{6}}=0.1191\rightarrow 11.91\%$$
---
### Ejemplo random

Tenemos 20 impresoras, 5 de laser, 11 de tinta y 4 de matriz de punto
$N=20$
$L=5$
$T=11$
$M=4\rightarrow E$
$N-E=16 \rightarrow F$
$$\frac{\binom{4}{4}\binom{16}{2}}{\binom{20}{6}}=0.1191\rightarrow 11.91\%$$
--- 
### Ejemplo 3
Se capturaro, etiquetaron y liberaron cinco individuos de una poblacción de animales que se piensa están al borde de la extinsión en una región para que se mezclen con la población. Después de haber tenido la oportunidad de mezclarse, se selecciona una muestra aleatoria de 10 de estos animales. Sea $X$ el número de animales etiquetados en la segunda muestra. Si en realidad hay 25 animales de este tipo en la región. ¿Cuál es la probabilidad de que
a) $X+2$?
b) $X\leq 2$?
Los valores de los parámetros son $n=10$, $M=5$ (cinco animales etiquetados en la población) y $N=25$, por lo tanto

$N=25$
$M=5$
$h=10$
$x=2$
$$\frac{\binom{5}{2}\binom{25-5}{10-2}}{\binom{25}{10}}=0.3853$$

---
## Media y varianza

La media y la varianza de la variable aleatoria hipergeométrica $X$ cuya función masa de probabilidad es 
$h(x;n,M,N)$
$E(X)=n\cdot \frac{M}{N}$
$V(X)=\frac{N-n}{N-1}\cdot n\cdot \frac{M}{N}\cdot (1- \frac{M}{N})$

| Símbolo | Significado                                             |
| ------- | ------------------------------------------------------- |
| N       | Tamaño total de la población                            |
| M       | Número de eleentos éxito en la población                |
| n       | Tamaño de la muestra (extracciones)                     |
| x       | Número de éxitos observados en la muestra (x=0,1,...,n) |

--- 
## Ejemplos 2
### Ejemplo 2.1
Un instructor que impartió dos secciones de estadística de ingeniería el semestre pasado, la primera con 20 estudiantes y la segunda con 30, decidió asignar un proyecto semestral.
Una vez que todos los proyectos le fueron entregados, el instructor los ordenó al azar antes de calificarlos. Considere los primero 15 proyectos calificados.

a. ¿Cuál es la probabilidad de que exactamente 10 de estos sean de la segunda sección?

$$P(X=10)=\frac{\binom{30}{10}\binom{50}{30}}{\binom{15}{10}}=0.206$$
b. ¿Cuál es la probabilidad de que por lo menos 10 de estos sean de la segunda sección?