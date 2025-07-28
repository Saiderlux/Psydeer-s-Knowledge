Para los siguientes 6 algoritmos, determine la cota de complejidad O (cota superior ajustada) bajo el principio del peor caso de cada algoritmo. Indique a detalle el procedimiento de obtención de la cota.
### Código 1.
```Python
 Busqueda (A[],i,val){
	if(i<e)
		return -1
	if(A[i]=val)
		return i
	return Busqueda(A[],i-1,val)	
 }
```
Este algoritmo realiza una búsqueda lineal, asumo que empieza desde el último índice del arreglo, ya que $i$ disminuye en cada llamada recursiva. Además asumo que e=0 ya que sería el límite inferior para $i$ que es 0 ya que desde ese número se indexan los arreglos.
Como es una búsqueda lineal, el peor caso sería que val esté en la posición e ó que directamente no se encuentre en el arreglo.

Para este algoritmo, tomaré como operaciones básicas: aritméticas y comparaciones.

Basado en el análisis del peor caso, la función recursiva que describe el número de operaciones que realiza el algoritmo es:
$$T(n)=T(n-1)+3$$
Y $$T(0)=2$$
Ahora, despejando el modelo recurrente tenemos:
$$T(n)-T(n-1)=3 \rightarrow \text{No homogenea}$$
Y tenemos que $k=1$, $b=1$, $d=0$ y $T(n)=x^{k}=x$
Lo cual nos deja con:
$$(x-1)(x-1)=0$$
Calculando sus raíces tenemos: $r_{1}=1, r_{2}=1$
Así
$$\begin{align}T(n)&=c_{1}n(1)^{n}+c_{2}(1)^{n}\\T(n)&=c_{1}n+c_{2}\end{align}$$
Y tenemos que $T(0)=2$
$$T(0)=c_{1}\cdot 0+c_{2}=2$$
$$c_{2}=2$$
Y $T(1)=T(1-1)+3=T(0)+3=5$
$$\begin{align}T(1)&=c_{1}\cdot 1+2=5\\
&=c_{1}=3
\end{align}$$
Por lo tanto, la función no recurrente es:
$$T(n)=3n+2 \in O(n)$$
### Código 2.
```cpp
int coef(int n, int l){
	if(k==0||k==n)
		return 1;
	else if(k>0 && k<n)
		return coef(n-1,k-1)+coef(n-1,k)
}
```
El código creo que calcula el coeficiente binomial

El peor caso ocurre cuando $n$ y $k$ son valores grandes y, debido a la recursión, el cálculo se vuelve redundante y se repiten llamadas para los mismos valores.
Basado en el análisis recursivo tenemos, 4 comparaciones y 4 aritméticas para el peor caso y el return de la llamada recursiva:
$$T(n,k)=T(n-1,k-1)+T(n-1,k)+8$$
Para $T(0,0)$ tenemos:
$$T(0,0)=3$$
La relación de recurrencia tiene una estructura de árbol binario. En cada nivel de recursión, se generan dos subproblemas, lo cual nos está indicando un crecimiento exponencial.
Cómo estamos considerando el peor caso, observamos que al realizar cálculos redundantes la complejidad queda exponencial, dándonos así:
$$O(2^{n})$$

### Código 3.
```Python
Palindromo(cadena){
	if(longitud(cadena)==1)
		return TRUE
	if(primer_caracter(cadena)!=ultimo_caracter(cadena))
		return FALSE
	cadena=remover_primer_ultimo_caracter(cadena)
	return Palindromo(cadena)	
}
```
Este algoritmo, lo que hace es ir acortando la cadena en cada uno de sus extremos y los va comparando para verificar si es un palíndromo. El peor caso es cuando la cadena efectivamente es un palíndromo, teniendo así que cortar toda la cadena hasta que quede de longitud 1.
Como en cada llamada recursiva se corta en ambos extremos la cadena y considerando que tenemos 4 comparaciones y considerando que remover_primer_ultimo_caracter() es lineal tenemos:
$$T(n)=T(n-2)+3$$
Y para $T(0)$ y $T(1)$ tenemos:
$$T(0)=2, T(1)=2$$
Ya que solo realiza una comparación y retorna directamente, aunque es un poco ambiguo ya que no tenemos esta condición explícitamente.
Ahora, despejando tenemos:
$$T(n)-T(n-2)=3$$
La cual es no homogénea.
Así tenemos $k=2$, $b=1$, $d=0$ y $T(n)=x^{k}=x^{2}$, lo cual nos deja con:
$$(x^{2}-1)(x-1)=0$$
Para el cual tenemos las raíces:
$$\begin{align}
r_{1}&=1\\
r_{2}&=-1\\
r_{3}&=1
\end{align}$$
De lo cual obtenemos:
$$T(n)=c_{1}(n)+c_{2}+c_{3}(-1)^{n}$$
$$T(0)=c_{1}(0)+c_{2}+c_{3}(-1)^{0}=2$$
$$T(0)=c_{2}+c_{3}=2$$
$$T(1)=c_{1}+c_{2}-c_{3}=2$$
Y para $T(2)$ tenemos : $T(2)=T(0)+3=2+3=5$
Entonces:
$$T(2)=2c_{1}+c_{2}+c_{3}(-1)^{2}=2c_{1}+c_{2}+c_{3}=5$$
Realizando el sistema de ecuaciones:
$$\begin{cases}  c_{2}+c_{3}&=2\\
c_{1}+c_{2}-c_{3}&=2\\
2c_{1}+c_{2}+c_{3}&=5\\

\end{cases}$$
Así tenemos:
$c_{1}=\frac{3}{2}$,  $c_{2}=\frac{5}{4}$,  $c_{3}=\frac{3}{4}$
Obteniendo la función no recurrente $T(n)=\frac{3}{2}n+ \frac{5}{4}+ \frac{3}{4}(-1)^{n}\in O(n)$
$$\text{  }
$$

### Código 4.
```Pseudocódigo
SubAlgoritmo Volados(n,cadena)
	Si n!=0
		Volados(n-1,concatenar(cadena,'S'))
		Volados(n-1,concatenar(cadena,'A'))
	SiNo
		Mostrar cadena
	Finsi
FinSubAlgoritmo
```
El algoritmo Volados genera todas las posibles combinaciones de una secuencia de longitud n compuesta de las letras 'S' y 'A'. 
Para el análisis consideré asignaciones, aritméticas y comparaciones. El peor caso es cuando se se hacen todas las llamadas recursivas.

Tenemos que $$T(n)=2T(n-1)+6$$
Entonces $$T(0)=2$$
Y además: $$T(1)=2T(0)+6=4+6=10$$
Despejando tenemos $$T(n)-2T(n-1)=6$$
Que es no homogénea, por lo consiguiente obtenemos $k=1$, $b=1$, $d=0$ y $T(n)=x^{k}=x$
Así:
$$(x-2)(x-1)=0$$
Y obtenemos las raíces $r_{1}=2$, $r_{2}=1$
Entonces tenemos: 
$$T(n)=2^{n}c_{1}+c_{2}$$
Para $T(0)$ tenemos:
$$T(0)=c_{1}+c_{2}=2$$
Y para $T(1)$ tenemos:
$$T(1)=2c_{1}+c_{2}=10$$
Así obtenemos el sistema de ecuaciones:
$$\begin{cases}  c_{1}+c_{2}&=2\\ 2c_{1}+c_{2}&=10\\

\end{cases}$$
Lo que nos da las constantes $c_{1}=8$ y $c_{2}=-6$
Obteniendo así la función recursiva $$T(n)=8(2^{n})-6 \in O(2^{n})$$
### Código 5.
```Python
int Producto(int a, int b){
	if(b==0)
		return 0;
	else
		return a+Producto(a,b-1)
}
```
El programa calcula el producto de a y b usando sumas sucesivas, realizando b sumas de a cuando b es positivo. La función es equivalente a a×b. Y su peor caso es el caso promedio, donde se realizan todas las recursiones.
Las operaciones básicas que consideré son asignaciones, comparaciones y aritméticas

Tenemos entonces: $$T(n)=T(n-1)+3$$
También tenemos que para $T(0)$ y $T(1)$:
$$T(0)=2$$
$$T(1)=T(0)+3=2+3=5$$
Por consiguiente tenemos:
$$T(n)-T(n-1)=3$$
Así tenemos que $k=1, b=1, d=0$ y $T(n)=x^{k}=x$
Con lo cual obtenemos:
$$(x-1)(x-1)=0$$
Con esto obtenemos las raíces $r_{1}=1$ y $r_{2}=1$
Con estas raíces obtenemos:
$$T(n)=c_{1}+c_{2}n$$
Así tenemos que: $$T(0)=c_{1}+c_{2}(0)=c_{1}=2$$
$$T(1)=c_{1}+c_{2}=2+c_{2}=5$$
Así $$c_{2}=3$$
Con lo cual obtenemos la función no recurrente:
$$T(n)=2+3n \in O(n)$$

### Código 6.
```Python
DecABin(n){.
	if(n>1)
		DecABin(n/2)
		Mostrar(n%2)
}
```

El algoritmo convierte un número decimal a su representación binaria. Su peor caso es cuando es cuando la entrada es de n muy grandes.
Para su análisis considere las aritméticas, comparaciones y asignaciones.
Así tenemos la función recursiva no lineal: 
$$T(n)=T(n/2)+2$$
Y tenemos que:
$$T(0)=1$$
$$T(1)=1$$
Cómo es no lineal utilizaré el teorema maestro. Con base en eso tenemos:
$a=1$, $b=2$ con $f(n)=2$ con $n^{\log_{a}{b}}$ 
Y tenemos que $\log_{b}{a}=\log_{2}{1}=0$
Entonces $n^{\log_{b}{a}}=1$

Como $f(n)=2$ es constante, tenemos el caso 1 del teorema maestro, donde $f(n)=O(n^{\log_{b}{a}-\epsilon})$ 
Ahora, aplicando el caso 2 tenemos que $$T(n)=\Theta(n^{\log_{b}{a}}=\Theta(n^{0})=\Theta(1))$$
Tal que $$T(n)=\Theta(lg {n})$$