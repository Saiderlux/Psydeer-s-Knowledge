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