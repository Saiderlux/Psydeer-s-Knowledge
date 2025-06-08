Considérese un tanque que contiene inicialmente $V_{0}$ galones de solución salina que contiene a lb de sal. Otra solución salina que contiene b lb. de sal por galón, se vierte en el tanque a la tasa      e $\frac {gal}{min}$ . Al mismo tiempo la solución mezclada sale del tanque a la tasa de f $\frac{gal}{min}$ . Hallar la cantidad de sal que hay en el tanque en el tiempo $t$ .
![[Pasted image 20241023122719.png]]
Sea Q=cantidad de sal en libras lb. en un momento

$$\rightarrow \frac{dQ}{dt}=\frac{dQ_{entra}}{dt}-\frac{dQ_{sale}}{dt}$$
$$\frac{dQ}{dt}=b\cdot e-\frac{dQ_{sale}}{dt}$$
Para hallar $\frac{dQ_{sale}}{dt}$  debemos calcular el volumen de solución salina que hayan en el tanque en un momento $t$, el cual es igual al volumen $V_{0}$, más el volumen agregado $e\cdot t$, menos el volumen de la solución que sale $f \cdot t$ 

$$V_{t}=V_{inicial}+V_{entra}-V_{sale}$$
$$=v_{0}+e\cdot t-f \cdot t$$
La concentración en cualquier tiempo t es: 
$$c=\frac{Q}{V_{t}}=\frac{Q}{V_{0}+e\cdot t-f\cdot t}$$
$\rightarrow$ La tasa a la cual sale la sal del tanque es:
$$\frac{dQ}{dt}=f\cdot c=f \cdot \frac{Q}{V_{0}+e\cdot t-f\cdot t}$$
$\rightarrow$Sustituyendo
$$\frac{dQ}{dt}=b\cdot e-f \cdot \frac{Q}{V_{0}+e\cdot t-f\cdot t}$$
$$\frac{dQ}{dt}+f \cdot \frac{Q}{V_{0}+e\cdot t-f\cdot t}=b\cdot e$$
##### Ejemplo 9.11
Un tanque contiene inicialmente 100 galones de $ma$ solución salina que contiene 20 lb de sal. Para $t=0$, se vierte agua dulce en el tanque de la tasa de  5 $\frac{gal}{min}$ mientras que sale del tanque una solución bien mezclada a la misma tasa. Halle la cantidad de sal en el instante $t$ 

$V_{0}=100 gal$ 
$a=20lb$
$t=0$ 
$e=5 \frac{gal}{min}$
$f=5 \frac{gal}{min}$
$Q=?$

$$\frac{dQ}{dt}+f \cdot \frac{Q}{V_{0}+e\cdot t-f\cdot t}=b\cdot e$$
$$\frac{dQ}{dt}+ \frac{5\frac{gal}{min}}{100gal+5\frac{gal}{min}\cdot t-5\frac{gal}{min}\cdot t}Q=0\cdot 5\frac{gal}{min}$$
$$\frac{dQ}{dt}+\frac{1}{20min}Q=0$$
$$I=e^{\int p(t)dt}=e^{\int\frac{1}{20min}dt}=e^{\frac{1}{20min}t}$$
$$e^{\frac{1}{20min}t}[\frac{dQ}{dt}+\frac{1}{20min}Q]=e^{\frac{1}{20min}t}\cdot0$$
$$\frac{d}{dt}(e^{\frac{1}{20min}t})=0$$
$$\int{d(e^{\frac{1}{20min}t})}=\int 0dt$$
$$e^{\frac{1}{20min}t}Q=c$$
$$Q=ce^{-\frac{1}{20min}t}$$
Condiciones iniciales
$$t=0,Q=a=20lb
$$$$20lb=ce^{-\frac{1}{20min}0}$$
$$20lb=ce^0=c$$
$$Q=20lb\cdot e^{-\frac{1}{20min}t}$$