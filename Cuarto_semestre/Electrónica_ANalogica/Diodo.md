![[Pasted image 20250424153900.png]]La imagen muestra la curva característica corriente-tensión (I-V) de un diodo semiconductor. Esta gráfica ilustra cómo se comporta un diodo en diferentes condiciones de voltaje.

En el eje horizontal se representa el voltaje (VF) aplicado al diodo, mientras que en el eje vertical se muestra la corriente (IF) que circula a través del dispositivo.

La gráfica está dividida en varias regiones importantes:

1. **Región Directa**: Aparece en el primer cuadrante (parte superior derecha). Cuando el diodo está polarizado en directa (voltaje positivo), permite el paso de corriente con facilidad después de superar cierto umbral de voltaje.
2. **Codo**: Punto donde la curva cambia rápidamente de pendiente, marcando el inicio de la conducción significativa. Este punto corresponde aproximadamente al voltaje umbral del diodo (típicamente **0.7V** para diodos de silicio).
3. **Región Inversa**: En el tercer cuadrante (parte inferior izquierda), cuando el diodo está polarizado en inversa (voltaje negativo), solo circula una pequeña "Corriente de Fuga" hasta cierto punto.
4. **Región de Ruptura**: Si el voltaje inverso aumenta demasiado, se alcanza un punto de "Ruptura" donde el diodo comienza a conducir súbitamente en sentido inverso, lo que podría dañar el componente si no está diseñado para operar en esta región.

## Ecuación del diodo
$$I=I_{s}(e^{\frac{V_{D}}{nV_{T}}}-1)$$
Donde:
- $I$ corriente que atraviesa el diodo
- $V_{D}$ diferencia de tensión entre sus extremos
- $I_{S}$ corriente de saturación en inversa (aprox. $1×10^{4}$)
- $n$ es el coeficiente de emisión. $n=1$ para el Ge y $n=2$ para el Si
- El voltaje térmico $V_{T}$ es aprox. $25.85 \text{ mV}$

## Diferencias entre los distintos niveles de resistencia
![[Pasted image 20250425130524.png]]
## Rectificador de media onda
![[Pasted image 20250425132848.png]]

Debido a la naturaleza del diodo, estos son utilizados como rectificadores de corriente. Esto quiere decir que convierten una señal CA en CD.
![[Pasted image 20250425131924.png]]
![[Pasted image 20250425131949.png]]

![[Pasted image 20250425131932.png]]
![[Pasted image 20250425132016.png]]

**Valor promedio de la salida de media onda**
$$V_{prom}=\frac{V_{p}}{\pi}$$
El valor promedio es el valor que se leería en un multímetro de CD.
**Demostración**
$$v = V_p sen \theta$$
$$V_{PROM} = \frac{área}{2\pi}$$
$$= \frac{1}{2\pi} \int_0^\pi V_p sen \theta d\theta$$
$$= \frac{V_p}{2\pi} (-cos \theta)\bigg|_0^\pi$$
$$= \frac{V_p}{2\pi} [-cos \pi -(-cos \, 0)]$$
$$= \frac{V_p}{2\pi} [-(-1)-(-1)]$$
$$= \frac{V_p}{2\pi} (2)$$

$$V_{PROM} = \frac{V_p}{\pi}$$
## Rectificador de onda completa
![[Pasted image 20250425132918.png]]

![[Pasted image 20250425133046.png]]

En virtud de que el númer de ciclos positivos que constituyen el voltaje rectificado de onda completa es el doble que el voltaje de media onda, entonces el valor promedio (CD) de un rectificador de onda completa es el doble del de media onda y se puede calcular por
$$V_{prom}=V_{CD}=\frac{2V_{p}}{\pi}=0.636V_{p}$$
si se considera $V_{T}$ o $V_{B}$
$$V_{prom}=V_{CD}=0.636(V_{p}-2V_{B})$$
## Rectificador de onda completa tipo puente
![[Pasted image 20250427161505.png]]

- **V₂**: es la **tensión pico** secundaria del transformador (entre extremos, sin considerar caída de diodos).
    
- **V_B**: representa la **caída de tensión** en **cada** diodo en conducción (aprox. 0.7 V si es silicio).
    
- **2 V_B**: aparece porque, en cada semiciclo, la corriente atraviesa **dos** diodos en serie.
    
- Por tanto, **el pico de salida** (medido sobre la carga) será
    
    $$V_{s,\text{pico}} = V_2 - 2\,V_B$$
En un rectificador de onda completa, el **valor medio** de una senoidal rectificada vale
$$V_{\text{PROM}}=\frac{2}{\pi}\cdot (V_{2}-2V_{B})$$

**NOTA:**
La frecuencia angular es:
$$\omega = 2\pi f$$

o bien

$$f = \frac{\omega}{2\pi}$$

El periodo (T) es:

$$T = \frac{1}{f}$$

o bien

$$T = \frac{2\pi}{\omega}$$
## Filtros para Rectificadores

El objetivo de un filtro en la fuente de alimentación es reducir en gran medida las fluctuaciones del voltaje de salida de un rectificador de media onda o de onda completa y producir un nivel casi constante de voltaje de CD.
![[Pasted image 20250427162700.png]]
Un **condensador o capacitor** en un circuito **almacena energía en forma de campo eléctrico**. Su comportamiento ante señales variables es la base del filtrado.

La idea clave es:

🔵 **El capacitor "resiste" cambios lentos de voltaje (corriente continua), pero "permite pasar" cambios rápidos (corriente alterna de alta frecuencia).**
![[Pasted image 20250427163918.png]]
### Valor de rizo
 **¿Qué mide el factor de rizo $r$?**

Es un **indicador adimensional** de la “planitud” de la tensión continua tras el filtrado.

- **Valor pequeño de $r$** → muy poca ondulación residual → salida bien suavizada.
    
- **Valor grande de $r$** → mucho rizado → la salida sigue siendo muy pulsante.
-
**Ecuación**
$$r=\frac{V_{r}}{V_{cd}}$$
- **$V_{r}$​ (Voltaje de rizo)**
    - Se suele tomar como la **diferencia pico-a-pico** de la componente alterna que queda superpuesta a la componente continua.
        
    - En la figura se dibuja como la distancia entre el punto más alto y el más bajo de la pequeña “onda” que queda sobre la recta de $V_{\mathrm{cd}}$.
    - $$V_{r}\approx \frac{I_{carga}}{fC} $$
- **$V_{\mathrm{cd}}$​ (Valor medio o DC)**
    - Es el **promedio** de la tensión de salida tras el filtro, es decir, la componente continua real que alimentará la carga.
        
    - Gráficamente, es el nivel sobre el cual “flota” el rizo.

Para un rectificador de ondaa completa, con un filtro con capacitor a la entrada suficientemente alto, si $V_{\text{dc}}$ se halla muy cerca del valor del voltaje de pico rectificado de entrada, las expresiones para $V_{\text{dc}}$ y $V_{\text{r}}$ serán entonces como sigue

$$V_{\text{dc}}=\left( 1- \frac{0.00417}{R_{L}C} \right) V_{\text{p(ent)}}$$
$$V_{\text{r}}=\frac{0.0024}{R_{L}C}(V_{\text{p(ent)}})$$
Donde: $V_{\text{p(ent)}}$ es el voltaje pico rectificado aplicado al filtro

#### Anexos
Cuando el capacitor del filtro se descara el voltaje en el capacitor es:
$v_{C}=V_{\text{p(ent)}}e^\frac{-t}{RC}$
![[Pasted image 20250427200711.png]]
$$v_{\text{C(min)}}=V_{\text{p(ent)}}\left( 1-\frac{T}{RC} \right)$$
- El Voltaje de rizo pico a pico es
  $$V_{r(p-p)}=\frac{V_{\text{P(ent)}}T}{RC} $$
donde $$T=\frac{1}{f}$$
- EL valor del voltaje promedio, $V_{cd}$ es:
  $$V_{\text{cd}}\left( 1- \frac{0.00417}{R_{L}C} \right)V_{\text{p(ent)}}$$
- El voltaje de rizo pico es:$$V_{\text{r(p)}}=\frac{0.00833V_{\text{p(ent)}}}{2R_{L}C(\sqrt{3 })}$$
- Concluyendo
$$V_{\text{r(eficaz)}}=\frac{0.0024V_{\text{p(ent)}}}{R_{L}C}$$