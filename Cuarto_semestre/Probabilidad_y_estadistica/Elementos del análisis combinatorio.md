 Cuando se presentan experimentos cuyos espacios muestrales contienen tantos elementos que enlistarlos ya no es practico, se hace uso del análisis combinatorio.
También sirve cuando no necesitamos conocer a detalle cuales son los elementos del evento o espacio muestral, más bien necesitamos saber cuantos son.
## Permutaciones
En las combinaciones *importa el orden*, por lo que si tenemos un evento $\{AB,BA\}$ los dos elementos, aunque tienen los mismos objetos, se consideran diferentes por el orden.
Una permutación difiere de otra si el orden o el contenido del arreglo es diferente.
En general, si quiero permutar $k$ de  $n$ elementos tendría
$$P^{n}_{k}=\frac{n!}{(n-k)!}$$
## Combinaciones
Es un arreglo de objetos de objetos distintos donde *no importa el orden*.
Una combinación difiera de otra solo si el contenido es diferente.
Tenemos que el número de combinaciones al tomar $k$ de $n$ elementos está dado por:
$$C^{n}_{k}=\binom{n}{k}=\frac{n!}{k!(n-k)!}$$
## Ejemplos de permutaciones
### Ejemplo 1
¿Cuántos anagramas son posibles con las palabras CASA, MISISIPI ó MANTARRAYA?
	**CASA**
- **Letras y repeticiones:**
    
    - C: 1
        
    - A: 2
        
    - S: 1
        
- **Cálculo:**
    $$
   \text{Anagramas} = \frac{4!}{2!} = \frac{24}{2} = 12
    $$
    **MISISIPI**

- **Letras y repeticiones:**  
    La palabra se descompone en los siguientes caracteres: M, I, S, I, S, I, P, I
    
    - M: 1
        
    - I: 4
        
    - S: 2
        
    - P: 1
        
- **Cálculo:**
    $$
    \text{Anagramas} = \frac{8!}{4! \cdot 2!} = \frac{40320}{24 \cdot 2} = \frac{40320}{48} = 840
    $$
    **MANTARRAYA**

- **Letras y repeticiones:**  
    La palabra se descompone en: M, A, N, T, A, R, R, A, Y, A
    
    - M: 1
        
    - A: 4
        
    - N: 1
        
    - T: 1
        
    - R: 2
        
    - Y: 1
        
- **Cálculo:**
    $$
    \text{Anagramas} = \frac{10!}{4! \cdot 2!} = \frac{3628800}{24 \cdot 2} = \frac{3628800}{48} = 75600
    $$
### Ejemplo 2
¿Cuántos números de 3 cifras diferents se pueden formar con los digitos 1,2,3?
*Sin repetir número*
$$6\rightarrow 3!$$
1- 123
2- 132
3- 213
4- 231
5- 312
6- 321

*Repitiendo número*
$27 \rightarrow 3^{3}$
$$n^{k}$$
$$n = \text{digitos que tenemos}$$
$$k = \text{Cantidad de números que se quieren en cada permutación}$$
### Ejemplo 3
Cuántos números de 3 cifras diferentes se pueden formar con 1,2,3,4,5,6,7? 
*Sin repetir números*
$$\frac{7!}{(7-3)!}=\frac{(7)(6)(5)(4)!}{4!}=(7)(6)(5)=210$$
*Repitiendo números*
$7^{3}=343$

### Interpretación de los resultados
| Tipo de permutación                      | Fórmula                                                 | Condiciones                                     |
| ---------------------------------------- | ------------------------------------------------------- | ----------------------------------------------- |
| Sin repetición (orden importa)           | $$ P(n, k) = \frac{n!}{(n - k)!} $$                     | Sin repetir, seleccionando $k$ elementos de $n$ |
| Con repetición permitida (orden importa) | $$ P_{\text{rep}}(n, k) = n^k $$                        | Puedes repetir elementos                        |
| Todos los elementos, con repeticiones    | $$ \frac{n!}{n_1! \cdot n_2! \cdot \dots \cdot n_k!} $$ | Algunos elementos se repiten (caso anagramas)   |
## Combinaciones: Extras
Subconjuntos ordenados
$$\binom{n}{k}=\frac{P_{k,n}}{{k!}}=\frac{n!}{k!(n-k)!}$$
Nos importa no tener combinaciones con los mismo elementos, más no el orden de las combinaciones.

## Ejemplos de combinaciones
### Ejemplo 1
Un consejo estudiantil, supongamos que 3 de los 7 representantes tienen que ser seleccionados para que asistan a unas convenciones de programación. EL orden de selección no es importante
$n=7$
$k=3$
$$\binom{7}{3}=\frac{7!}{3!(7-3)!}=24$$

## Coeficiente binomial
Se tiene un conjunto con 6 objetos diferentes $\{A,B,C,D,E,F\}$ de los cuales se desea escoger 2 (sin importar el oren de elección). Existen 15 formas de efectuar tal elección.
$$<<\text{combinaciones de }n \text{ en } k>> \text{, o simplemente }<<n\text{ en }k>>$$
## Ejemplos de coeficiente binomial
### Ejemplo 1
Una mano de bridge (cartas de póker) se compone de 13 cartas seleccionadas de entre un mazo de 52 cartas sin importar el orden
$$_{n}C_{k}=\frac{52!}{13!(52-13)!}=6.350135596×10^{11}$$
### Ejemplo 2
Como existen 13 cartas de cada palo (figuras), el número de mano compuestas de tréboles y/o espadas \[Nada de cartas rojas] es:
$$_{n}C_{k}=\frac{26!}{13!(26-13)!}=10,400,600$$
