![[Pasted image 20250428165633.png]]
Un diodo Zener mantiene un voltaje casi constante en sus terminales dentro del rango especificado de valores de corriente inversa
![[Pasted image 20250428170222.png]]
## Características del diodo Zener
- Dispositivo de unión P-N
- Se polariza en región inversa
- Actúa como un regulador de voltaje

## NOTA
![[Pasted image 20250428205542.png]]
Definiciones de la nomenclatura son:
- $I_{ZK}=$ Valor mínimo de corriente inversa
- $I_{ZM}=$ Corriente máxima en inversa
- $V_{ZT}=$ Voltaje nominal Zener
- $I_{ZT}=$ Corriente de prueba del Zener en inversa
- $r_{Z}=R_{Z}=\left( \frac{\Delta V_{Z}}{\Delta I_{Z}} \right)=$ Resistencia Zener que normalmente se especifica a $I_{ZT}$
![[Pasted image 20250428210548.png]]

--- 
Existen tres maneras de polarizar un circuito regulador con diodo Zener
1. Mantener fijos los valores : $V_{i}$ (voltaje de entrada) y $R_{L}$ (resistencia de carga)
2. Mantener Fija la $R_{L}$ y variable la $V_{i}$
3. Mantener fija la $V_{i}$ y variable la $R_{L}$
![[Pasted image 20250504155920.png]]
---
1.  Mantener fijos los valores : $V_{i}$ (voltaje de entrada) y $R_{L}$ (resistencia de carga).
**Análisis en dos etapas**
1.- Determinar el estado del diodo Zener mediante su eliminación de la res y por medio del cálculo de voltaje a través del circuito abierto resultante
![[Pasted image 20250504160220.png]]Por la regla del divisor de voltaje
$$V=V_{L}=\frac{R_{L}V_{i}}{R+R_{L}}$$
Si $V>V_{Z}$ el diodo Zener está encendido.
Si $V<V_{Z}$ el diodo Zener está apagado.

2.- 
**A) Caso del Zener apagado**
El Zener es un circuito abierto
$$V_{\text{out}}=V_{L}^{\text{(abierto)}},\text{ } I_{Z}\approx_{0}$$
La única corriente que circula es la de la carga. El Zener prácticamente no conduce

**B) Caso del Zener encendido**
Es decir, que ha llegado a su voltaje de avalancha
1. Voltaje de salida fijo
$$V_{L}=V_{Z}$$
	- El Zener actúa como una válvula que mantiene siempre ese nivel de tensión.
2. Corriente que llega por $R$
$$I_{R}=\frac{V_{i}-V_{Z}}{R}$$
	- Es la corriente total que sale de la fuente y atraviesa la resistencia.
3. Corriente que va a la carga
$$I_{L}=\frac{V_{Z}}{R_{L}}$$
4. Corriente que absorbe el Zener
$$I_{Z}=I_{R}-I_{L}$$
	- Es la diferencia entre lo que entra ($I_{R}$) y lo que sale hacia la carga ($I_{L}$)
5. Verificaciones finales
	- Rango de operaciones para asegurar regulación estable y no exceder corriente máxima
	$$I_{ZK}\leq I_{Z}\leq I_{ZM}$$
	- Potencia que disipa el Zener debe ser menor que la potencia nominal del diodo
$$P_{Z}=V_{Z}\cdot I_{Z}$$
---
2. Mantener fija $R_{L}$ y variable la $V_{i}$
Para $R_{L}$ fija en la figura, el valor de $V_{i}$ debe ser tal que encienda el diodo Zener.
![[Pasted image 20250505103445.png]]
- El $V_{i \text{ min}}$ se determina por
$$V_{L}=V_{Z}=\frac{R_{L}V_{i}}{R_{L}+R}$$
y
$$V_{i \text{ min}}=\frac{(R_{L}+R)V_{Z}}{R_{L}}$$
- El valor máximo de $V_{i}$ estáa limitado por la corriente Zener máxima $I_{ZM}$. Dado que $I_{ZM}=I_{R}-I_{L}$ se tiene
$$I_{R \text{ max}}=I_{ZM}+I_{L}$$
Dado que $I_{L}$ está fija en $\frac{V_{Z}}{R_{L}}$ e $I_{ZM}$ es el valor máximo de $I_{Z}$, la $V_{i}$ máxima se define por
$$V_{i \text{ max}}=V_{R \text{ max}}+V_{Z}$$
$$V_{i \text{ max}}=I_{R \text{ max}}R+V_{Z}$$
