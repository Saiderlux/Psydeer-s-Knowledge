Considere un circuito eléctrico RL. Contiene una resistencia y una inductancia (bobina)
![[Pasted image 20241023130526.png]]
\
R=resistencia=ohmios
L=inductancia=henrios
E=fem= fuerza electromotriz=volts
I=corriente=amperios

El voltaje del circuito es
$$E=V_{L}+V_{R}$$
$$L\frac{dI}{dt}+RI=E$$
$$\frac{dI}{dt}+\frac{R}{L}I=\frac{E}{L}$$
circuito RL

Para un circuito RC. tiene una resistencia y un capacitor.
![[Pasted image 20241023130941.png]]
c=capacitancia=faradios

La ecuacion del voltaje es:
$$V_{R}+V_{C}=V_{E}$$
$$RI+\frac{Q}{C}=E$$
$$R\frac{dQ}{dt}+\frac{Q}{C}=E$$
$$\frac{dQ}{dt}+\frac{1}{RC}Q=\frac{E}{R}$$
Nos da la carga. 

##### Ejemplo
Un circuito RC tiene una fem de 50 volts, R=5ohms, L= henry y no tiene corriente inicial. Halle la corriente del circuito en un momento $t$.
$$\frac{dI}{dt}+\frac{R}{L}I=\frac{E}{L}$$
$$\frac{dI}{dt}+\frac{50\Omega}{1H}I=\frac{5V}{1H}$$
$$I=e^{\int p(t)dt}=e^{\int \frac{50\Omega}{H} dt}=e^{\frac{50\Omega}{H} t}$$
$$e^{\frac{50\Omega}{H}t}[\frac{dI}{dt}+\frac{50\Omega}{H}I]=\frac{5V}{H}e^{\frac{5\Omega}{H}t}$$