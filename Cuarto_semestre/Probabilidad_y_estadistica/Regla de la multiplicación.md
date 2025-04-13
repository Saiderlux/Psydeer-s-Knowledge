La **regla de la multiplicación** permite calcular la probabilidad de que ocurran dos eventos simultáneamente. Se distinguen dos casos, según si los eventos son dependientes o independientes.
## 1. Eventos Dependientes

Cuando la ocurrencia de $B$ depende de que ocurra $A$, se usa la [[Probabilidad condicional]]:
$$
P(A \cap B) = P(A) \cdot P(B \mid A)
$$
$$P(A \cap B) = P(B) \cdot P(A \mid B)$$
donde:
- $P(A)$ es la probabilidad de que ocurra el evento $A$.
- $P(B \mid A)$ es la probabilidad de que ocurra el evento $B$ dado que ya ha ocurrido $A$.

## 2. Eventos Independientes

Si $A$ y $B$ son **independientes**, la ocurrencia de uno no afecta la del otro, por lo que:
$$P(A \cap B) = P(A) \cdot P(B)$$
En este caso se cumple que $P(B \mid A) = P(B)$.

## Ejemplos
### Ejemplo 1
Teniendo una caja de pelotas cafés, blancas y naranjas las cuales suman 14 pelotas.![[Pasted image 20250411085647.png]]
Si se sacan 2 pelotas consecutivas, al azar sin reemplazo, calcular la probabilidad de que
1. La primera sea naranja y la segunda café
2. Que las dos sean blancas

*La primera naranja y la segunda café*
$P(N\cap C)=P(C\mid N)\cdot P(N)$

$P(N)=\frac{8}{14} \rightarrow \text{Porque la primera es naranja}$ 
$P(C\mid N)=\frac{1}{13}\rightarrow \text{El denominador es 13 ya que al ser sin reemplazo, ya hemos sacado una pelota}$
$\frac{1}{13}\cdot \frac{8}{14}=0.0439\rightarrow 4.39\%$

*Que las dos sean blancas*
$P(B\cap B)=P(B\mid B)\cdot P(B)$

$P(B)=\frac{5}{14}$

$P(B\mid B)=\frac{4}{13}\rightarrow \text{Esto se debe a que ya sacamos una blanca, por eso hay una pelota menos}$

$P(B\cap B)=\frac{4}{13}\cdot \frac{5}{14}=0.1098\rightarrow 10.98\%$
---
*La primera naranja y la segunda café*
$P(N \cap C) = P(C) \cdot P(N)$

$P(N) = \frac{8}{14} \rightarrow \text{Porque la primera es naranja}$  

$P(C) = \frac{1}{14} \rightarrow \text{Como hay reemplazo, la composición de la caja no cambia}$  

$\frac{1}{14} \cdot \frac{8}{14} = 0.0408 \rightarrow 4.08\%$
 
*Que las dos sean blancas*  
$P(B \cap B) = P(B) \cdot P(B)$  
$P(B) = \frac{5}{14}$  
$P(B) = \frac{5}{14} \rightarrow \text{Al haber reemplazo, la probabilidad se mantiene}$  
$P(B \cap B) = \frac{5}{14} \cdot \frac{5}{14} = 0.1276 \rightarrow 12.76\%$

### Ejemplo 2
4 individuos han respondido a una solicitud de un banco de sangre para donaciones. Ninguno de ellos ha donado sangre antes, por lo que sus tipos de sangre son desconocidos. Suponga que solo se desea el tipo O+  solo uno de los 4 tiene ese tipo. SI los donadores potenciales se seleccionan en orden aleatorio, para determinar su tipo de sangre, ¿Cuál es la probabilidad de que por los menos tres individuos tengan que ser analizados para determinar su tipo de sangre y obtener el tipo deseado?
$$P(N\cap N)=\frac{3}{4}\cdot \frac{2}{3}=\frac{2}{4}=\frac{1}{2}\rightarrow 50\%$$
> Esta es la probabilidad de que los dos primeros no sean O+

$$P(O^{+} \cap (N\cap N))=P(O^{+}\mid N\cap N)\cdot P(N\cap N)$$
$$=\frac{1}{2}\cdot \frac{1}{2}=\frac{1}{4}\rightarrow 25\%$$
### Ejemplo 3
Una cadena de tiendas de video vende 3 marcas diferentes de reproductores de DVD. De sus ventas de reproductores DVD, 50% son de la marca 1 (la menos cara), 30% son de la marca 2 y 20% son de la marca 3. Cada fabricante ofrece un año de garantía en las partes y mano de obra. Se sabe que 25% de los reproductores de DVD de la marca 1 requieren trabajo de reparación dentro del periodo de garantía, mientras que los porcentajes correspondientes de las marcas 2 y 3 son 20% y 10%, respectivamente.

1. ¿Cuál es la probabilidad de que un comprador seleccionado al azar haya adquirido un reproductor de DVD de la marca 1 q necesita reparación mientras se encuentra dentro de garantía?
$$P(M_{1}\cap G)=P(M_{1}\mid G)\cdot P(G)$$
$$P(M_{1}\cap G)=\frac{50\%}{100\%}\cdot \frac{25\%}{100\%}$$
$$(0.5)(0.25)=0.125\rightarrow 12.5\%$$
2. ¿Cuál es la probabilidad de que un comprador seleccionado al azar haya comprado un reproductor DVD que necesitara reparación mientras se encuentra dentro de garantía?
$$P(M_{1}\cap G)=(0.5)(0.25)=0.125$$

$$P(M_{2}\cap G)=(0.3)(0.20)=0.06$$

$$P(M_{1}\cap G)=(0.2)(0.10)=0.02$$
$$\text{Sumando todos, obtenemos:}$$
$$0.205\rightarrow =20.5\%$$
3. SI un cliente regresa a la tienda con un reproductor DVD que necesita reparación dentro de garantía, ¿Cuál es la probabilidad de que sea un reproductor de la marca 1? ¿Un reproductor de la marca 2?¿Un reproductor de la marca 3?
Para la marca 1:
$$P(M_1\mid G)=\frac{0.125}{0.205}\approx 0.6098\rightarrow 61\%$$

Para la marca 2:
$$P(M_2\mid G)=\frac{0.06}{0.205}\approx 0.2927\rightarrow 29\%$$

Para la marca 3:
$$P(M_3\mid G)=\frac{0.02}{0.205}\approx 0.0976\rightarrow 10\%$$
