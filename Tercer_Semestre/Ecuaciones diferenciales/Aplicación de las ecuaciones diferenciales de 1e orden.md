Problema del enfriamiento. Ley de Newton del enfriamiento
La taza de cambio en el tiempo de la temperatura de un cuerpo es proporcional a la diferencia de temperatura entre el cuerpo y el medio ambiente.
Si $T$ = temperatura del cuerpo
$T_{m}$ = temperatura del medio ambiente
$$\frac{dT}{dt}=-k(T-T_{m})$$ $k=$ constante de proporcionalidad, $k>0$ 

Signo $\theta$  porque el cuerpo se va enfriando
$T-T_{m}>0$ 

###### Problemas resueltos
Schaum, cap. 9.

9.1. Una barra metálica a una temperatura de $100$ grados Farenheit, se pone en un cuarto a una temperatura constante de $0$ grados Farenheit.
Después de 20 minutos, la temperatura de la barra es $50$ grados Farenheit, hallar:
	a)El tiempo que gastará la barra para llegar a una temperatura de $25$ grados Farenheit.
	b)La temperatura de la barra después de $10$ minutos
a)
$$T_{m}=0\degree F$$
$$\frac{dT}{dt}=-k(T-T_{m})$$ $$\frac{dT}{dt}=-kT$$
$$\frac{dT}{dt}+kT=0$$
Ecuación diferencial lineal de primer orden
$$T'+kT=0$$
$$I=e^{\int p(t)\,dt}=e^{\int k\,dt}=e^{k\int\,dt}=e^{kt}$$
$$e^{kt}(T'+kT)=e^{kt}\cdot{0}$$
$$\frac{d(Te^{kt})}{dt}=0$$
$$\int d(Te^{kt})\ = \int 0 \cdot dt \ $$
$$Te^{kt}=0+c$$
$$T=\frac {c}{e^{kt}}=ce^{-kt}$$
$$T(t)=ce^{kt}$$
Condiciones iniciales
En $t=0$ minutos, $T=100\degree F$ (barra).
$100\degree F= ce^{-k0s}$
$100\degree F=ce^0=c$ 

$$\rightarrow T=ce^{-kt}=(100\degree F)e^{kt}$$
Condición inicial
En $t=20$ min
$T=50\degree F$
$50\degree F=100\degree F e^{k(20min)}$ 

$\frac{50\degree F}{100\degree F}=e^{k(20min)}$ 

$\frac{1\degree F} {2\degree F}=e^{k(20min)}$ 

$\ln{\frac{1}{2}}=\ln{e^{-(20min)k}}$ 

$\ln{1}-\ln{2}=-(20min)k$ 

$\frac{\ln{2}}{20min}=k$ 
$k=0.035 \frac {1}{min}$ 

$\rightarrow$ la T es

$T=100 \degree F e^{-0.035 \frac {1}{min}t}$ 

a) $t=?,    T=25\degree F$ 

$25\degree F=100\degree F e^{-0.035\frac{1}{min}t}$ 
$\frac{25}{100}=e^{-0.035\frac{1}{min}t}$
$\frac{1}{4}=e^{-0.035\frac{1}{min}t}$

$\ln{t}=\ln{e^{-0.035\frac{1}{min}t}}$
$\ln{1}-\ln{4}=0.035\frac{1}{min}t$ 
$\frac{\ln{4}}{0.035}min=t$
$40min=39.6=t$ 

b) $t=10min, T=?$
$T=100\degree F e^{-0.035\frac{1}{min}(10min)}$ 
$=100\degree F e^{-0.35}$
$=70.5\degree F$



###### Caída de los cuerpos con resistencia del air
Considere un cuerpo de masa m cayendo verticalmente bajo la influencia de la aceleración gravitacional y una resistencia del aire proporcional a su velocidad
 $m=cte$
$g=cte$

1ra ley de Newton:
$$F=\frac{dp}{dt}=\frac{dmv}{dt}=m\frac{dv}{dt}=ma$$
La fuerza neta que actúa sobre un cuerpo es igual al cambio en su cantidad de movimiento
$F_{N}=$ Fuerza neta o total

![[Pasted image 20241021131921.png]]
