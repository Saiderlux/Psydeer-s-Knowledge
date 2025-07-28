## Ejemplos
### Ejemplo 1
En una caja hay 5 esferas azules, 2 rojas y 1 verde. Si se sacan al azar dos esferas consecutivas, calcular la probabilidad de sacar una esfera azul y una verse. Con reemplazo y sin reemplazo.
Con reemplazo
$$A\text{ sacar una esfera azul, }B\text{ sacar una esfera verde}$$
$$P(A\cap B)=\left( \frac{5}{8 } \right)\left( \frac{1}{8} \right)=0.078\rightarrow 7.8\%$$
$$A\text{ sacar una esfera azul, }B\text{ sacar una esfera verde}$$
$$P(B\cap A)=\left( \frac{1}{8 } \right)\left( \frac{5}{8} \right)=0.078\rightarrow 7.8\%$$

$$P(AB)=P(A\cap B)+P(B\cap A)=0.156\rightarrow 15.6\%$$Sin reemplazo
$$A\text{ sacar una esfera azul, }B\text{ sacar una esfera verde}$$
$$P(A\cap B)=\left( \frac{5}{8 } \right)\left( \frac{1}{7} \right)=0.089\rightarrow 8.9\%$$
$$P(B\cap A)=\left( \frac{1}{8 } \right)\left( \frac{5}{7} \right)=0.089\rightarrow 8.9\%$$

$$P(AB)=P(A\cap B)+P(B\cap A)=0.178\rightarrow 17.8\%$$

¡¡LO TENGO!!

### Ejemplo 2

La señorita Andre Horta sabe que hay un 60% de probabilidad de que la empresa en la que trabaja abra una nueva sucursal en otra ciudad y si lo hace, la probabilidad de que ella sea nombrada gerente es del 70%. En cambio, si no se abre la nueva sucursal, la probabilidad de que sea nombrada gerente en otra sucursal es del 10%.

**Pregunta:** ¿Cuál es la probabilidad de que sea nombrada gerente en una sucursal de su empresa?

Para resolver este problema, utilizamos la **Ley de la Probabilidad Total**, que nos permite calcular la probabilidad de un evento considerando todas las vías en las que puede ocurrir.

- **$A$:** Se abre la nueva sucursal.  
- **$\lnot A$:** No se abre la nueva sucursal.  
- **$G$:** Andre Horta es nombrada gerente en una sucursal.

Los datos proporcionados en el problema son:

- Probabilidad de que se abra la sucursal:  
  $$P(A) = 0.60$$

- Probabilidad de que no se abra la sucursal:  
  $$P(\lnot A) = 1 - P(A) = 0.40$$

- Probabilidad de ser nombrada gerente si se abre la sucursal:  
  $$P(G \mid A) = 0.70$$

- Probabilidad de ser nombrada gerente si no se abre la sucursal:  
  $$P(G \mid \lnot A) = 0.10$$

 *2: Aplicar la Ley de la Probabilidad Total*

La fórmula de la probabilidad total para el evento $G$ es:

$$
P(G) = P(G \mid A) \cdot P(A) + P(G \mid \lnot A) \cdot P(\lnot A)
$$

Sustituimos en la fórmula:

$$
P(G) = (0.70 \times 0.60) + (0.10 \times 0.40)
$$


$$0.70 \times 0.60 = 0.42$$  
$$0.10 \times 0.40 = 0.04$$  

Sumamos los resultados:

$$
P(G) = 0.42 + 0.04 = 0.46
$$


La probabilidad de que Andre Horta sea nombrada gerente en una sucursal de su empresa es **46%**.



