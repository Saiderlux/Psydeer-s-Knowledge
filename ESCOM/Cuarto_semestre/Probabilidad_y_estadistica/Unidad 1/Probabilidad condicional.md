Para dos eventos cualesquiera $A$ y$B$ con $P(B)>0$, la probabilidad condicional de $A$ dada que $B$ ha ocurrido está definida por:
$$P(A \mid B)=\frac{P(A \cap B)}{P(B)}$$

La probabilidad de que **no ocurra ninguno de los dos eventos**, es decir, $A^c \cap B^c$, se expresa como:

$$
P(A^c \cap B^c) = P((A \cup B)^c) = 1 - P(A \cup B)
$$

Para calcular $P(A \cup B)$, se utiliza la fórmula de la unión de dos eventos:

$$
P(A \cup B) = P(A) + P(B) - P(A \cap B)
$$

Sustituyendo en la expresión del complemento:

$$
P(A^c \cap B^c) = 1 - \left[ P(A) + P(B) - P(A \cap B) \right]
$$

Esta expresión permite determinar la probabilidad de que no ocurra ninguno de los dos eventos a partir de las probabilidades individuales y conjuntas.

---
La probabilidad de que **no ocurra ninguno de los dos eventos**, es decir, $A^c \cap B^c$, se expresa como:

$$
P(A^c \cap B^c) = P((A \cup B)^c) = 1 - P(A \cup B)
$$

Para calcular $P(A \cup B)$, se utiliza la fórmula de la unión de dos eventos:

$$
P(A \cup B) = P(A) + P(B) - P(A \cap B)
$$

Sustituyendo en la expresión del complemento:

$$
P(A^c \cap B^c) = 1 - \left[ P(A) + P(B) - P(A \cap B) \right]
$$

---
La probabilidad de que ocurra **exactamente uno** de los eventos $A$ o $B$ corresponde a que ocurra solo uno de ellos, pero **no ambos simultáneamente**.

Este suceso se representa como:

$$
(A \cap B^c) \cup (A^c \cap B)
$$

Y su probabilidad es:

$$
P((A \cap B^c) \cup (A^c \cap B)) = P(A \cap B^c) + P(A^c \cap B)
$$

Usando las propiedades de probabilidad, esta expresión puede reescribirse en términos de $P(A)$, $P(B)$ y $P(A \cap B)$:

$$
P((A \cap B^c) \cup (A^c \cap B)) = P(A) + P(B) - 2P(A \cap B)
$$

Esto representa la probabilidad de que ocurra exactamente uno de los eventos, excluyendo el caso en que ocurren ambos simultáneamente.

---


## Ejemplos 
### Ejemplo 1
Supóngase que todos los individuos que compran cierta computadora portátil, 60% incluye una tarjeta de memoria RAM opcional en su compra, 40% incluyen un disco solido y 30% incluyen tanto memoria RAM como un disco sólido. Considérese seleccionar al azar un comprador y sea $A=\{\text{Memoria RAM adquirida}\}\text{ y }  B=\{\text{Disco solido}\}$

$$P(A)=60\%$$$$P(B)=40\%$$$$P(A\cap B)=30\%$$

**Dado que el individuo seleccionado adquirió un disco sólido, la probabilidad de que una memoria RAM también sea adquirida es:**

$$\frac{P(A\cap B)}{P(B)}=\frac{0.3}{0.4}=0.75 \rightarrow 75\% $$
**¿Cuál es la probabilidad de que un comprador no incluya ningún artículo?**
*De acuerdo con la probabilidad de que no ocurra ninguno de los dos eventos* 
$$
1-[P(A)+P(B)-P(A\cap B)]
$$
$$
1-0.6-0.4+0.3=0.3\rightarrow 30\%
$$
**¿Cuál es la probabilidad de que un comprador compre solo la memoria RAM, peo no el disco sólido?**
$$P(A)-P(A\cap B)=0.6-0.3=0.3 \rightarrow 30\%$$
**¿Cuál es la probabilidad de que un comprador compre el disco solido pero no la memoria RAM?**
$$P(B)-P(A\cap B)= 0.4-0.3=0.1\rightarrow 10\%$$
### Ejemplo 2
Una revista de noticias publica tres columnas tituladas "Arte" ($A$), "Libros" ($B$) y "Cine" (C)> Los hábitos de lectura de un lector seleccionado al azar con respecto a estas columnas son

| $A$  | $B$  | $C$  | $A\cap B$ | $A\cap C$ | $C\cap B$ | $A\cap B\cap C$ |
| ---- | ---- | ---- | --------- | --------- | --------- | --------------- |
| 0.14 | 0.23 | 0.37 | 0.08      | 0.09      | 0.13      | 0.05            |
### Ejemplo 3
Suponga que en la población general, hay 51% de hombres y 49% de mujeres, y que las proporciones de hombres y mujeres daltónicas son:


|                        | Hombres $(B)$ | Mujeres $(B^{c})$ | Total |
| ---------------------- | ------------- | ----------------- | ----- |
| Daltónico $(A)$        | 0.04          | 0.002             | 0.042 |
| No daltónico $(A^{c})$ | 0.47          | 0.488             | 0.958 |
| Total                  | 0.51          | 0.49              | 1     |
Si una persona se escoge al azar de entre esta población y se encuentra que es hombre ¿Cuál es la probabilidad de que sea daltónico?
$$P(A\mid B)=\frac{P(A \cap B)}{P(B)}=7.84\%$$
### Ejemplo 4
Hay un grupo que 40% de los integrantes tiene cabello castaño, el 25% tiene ojos azules y el 15% tiene el cabello castaño y los ojos azules. 

Para visualizar el ejemplo podemos utilizar [[Diagramas de Venn]]
![[Pasted image 20250410182357.png]]
Donde $$A=\text{Cabello castaño}=0.4$$$$B=\text{Ojos azules}=0.25$$
$$A\cap B=\text{Cabello castaño y ojos azules}=0.15$$
Si se selecciona una persona al azar y dicha persona tiene los ojos azules, ¿Cuál es la probabilidad de que tenga el cabello castaño?
$$P(A\mid B)= \frac{P(A\cap B)}{P(B)}=\frac{0.15}{0.4}=0.375$$