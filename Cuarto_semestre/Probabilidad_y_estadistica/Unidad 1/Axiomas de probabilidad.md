Sea $S$ un espacio muestral asociado a un experimento y $A$ un evento cualquiera de $S$, *la probabilidad del evento* $A$ es una función que asigna a $A$ un número real $P(A)$ con las siguientes propiedades
i) $0\leq P(A) \leq{1}$
ii) $P(S)=1$
iii) Si $A_{1},A_{2},\dots, A_{n}$ son eventos mutuamente excluyentes en $S$ entonces:
$$P\left( \bigcup_{i=1}^{n} A_i \right) = \sum_{i=1}^{n} P(A_i)$$
iv) Si $A_{1},A_{2},\dots, A_{n}$ es una secuencia numerable de eventos mutuamente excluyentes en S, entonces:
$$P\left( \bigcup_{i=1}^{\infty} A_i \right) = \sum_{i=1}^{\infty} P(A_i)$$
---
# Teoremas 
Sean ($A$, $B$) y ($C$) tres eventos cualesquiera de un espacio muestral ($S$) asociado a un experimento, entonces:

1. $$ P(\emptyset) = 0 $$  
2. $$ P(A') = 1 - P(A) $$  
3. $$ P(A \cup B) = P(A) + P(B) - P(A\cap B) $$  
4.  
   $$ P(A \cup B \cup C) = P(A) + P(B) + P(C) - P(A\cap B) - P(A\cap C) - P(B\cap C) + P(A\cap B\cap C) $$  
5.  
   $$  
   P\left( \bigcup_{i=1}^{k} A_i \right) = \sum_{i=1}^{k} P(A_i) - \sum_{i<j=2}^{k} P(A_i A_j)  + \sum_{i<j<r=3}^{k} P(A_i A_j A_r) + \dots + (-1)^{k-1} P\left( \bigcap_{i=1}^{k} A_i \right)  
   $$    
6. Si \( $A \subseteq B$ \) entonces $$ P(A) \leq P(B) $$  

---
