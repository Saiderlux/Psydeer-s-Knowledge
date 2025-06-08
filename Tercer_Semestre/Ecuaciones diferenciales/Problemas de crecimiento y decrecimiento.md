Llámese $N(t)$ a la cantidad de sustancia (o población) que está creciendo o decreciendo. SI suponemos como $\frac{dN}{dt}$ el cambio en esta sustancia, que sea proporcional a la sustancia presente en el tiempo $t$, entonces 
$$\frac{dN}{dt}=k \cdot N$$
$$k= \text {constante de proporcionalidad}$$
Funciona para distribuciones continuas, no discretas x

#### 9.4
Se sabe que cierto material radiactivo. se desintegra a una tasa proporcional a la cantidad presente.
Si inicialmente hay 50 mg de material radiactivo presente y después de dos horas se observa que ha perdido el 10% de su masa original, hallar:
	a) Una expresión para la masa restante en un momento $t$
	b) La masa del material después de cuatro horas
	c) El tiempo en el cual se ha desintegrado en la mitad de la masa inicial

##### a) 
$$\frac{dN}{dt}=kN$$
$$\frac{dN}{dt}-kN=0$$
$$I=e^{\int p(t)dt}=e^{-\int k dt}=e^{\int -kt}$$
$$e^{-kt}[N-KN]=0$$
$$\frac{d}{dt}[e^{-kt}N]=0$$
$$\int d(e^{-kt}N)=\int 0dt$$
$$e^{-kt}N=0+c$$
$$N(t)=ce^{kt}$$
Condiciones iniciales
$$Ent=0, N=50mg$$
$$50mg=c^{k(0)}=ce^{0}=c$$
$$N=50mg\cdot e^{kt}$$
En $t=2h$ , $$N = 50mg-50mg\%  $$
$$=50mg-5mg$$
$$=45mg$$
$$\rightarrow 45mg=50mg\cdot e^{k(2h)}$$
$$\frac{45}{50}=e^{k(2h)}$$
$$\frac{9\cdot5}{5\cdot 10}=e^{k(2h)}=\ln{\frac{9}{10}}=\ln {e^{k(2h)}}$$
$$\ln{\frac{9}{10}}=k(2h)$$
$$k=\frac{\ln{\frac{9}{10}}}{2h}=-0.053\frac{1}{h}$$
$$\rightarrow N=50mg \cdot e^{-0.053\cdot \frac{t}{h} }$$
##### b)
$t=4$
$$\rightarrow N=50mg \cdot e^{-0.053\cdot \frac{4h}{h}}$$
$$N=40.5mg$$
##### c)
$$t=?$$
$$N=\frac{N_{0}}{2}=\frac{50mg}{2}=25mg$$
$$25mg=50mg\cdot e^{-0.053\cdot \frac{1}{h}t}$$
$$\frac{25mg}{50mg}=e^{-0.053\cdot \frac{1}{h}t}$$
$$\frac{1}{2}=e^{-0.053\cdot \frac{1}{h}t}$$
$$\ln{\frac{1}{2}}=\ln{e^{-0.053\cdot \frac{1}{h}t}}$$
$$\ln{1}-\ln{2}=-0.053\cdot \frac{1}{h}t$$
$$-\ln{2}=-0.053\cdot \frac{1}{h}t$$
$$\frac{\ln{2}}{0.053\cdot \frac{1}{h}}=t$$
$$\frac{\ln{2}}{0.053}h=t$$
$$t=13h$$
Vida media es el tiempo t necesario para que se reduzca a la mitad