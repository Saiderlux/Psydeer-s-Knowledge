Imagina que una empresa de entregas analiza el tiempo que tarda un paquete en llegar a su destino
Media: tiempo de entrega
Varianza  ¿Los tiempos son consistentes o muy variables?
Asimetría: ¿Las entregas tardan más de lo esperado en algunos casos?
Curtosis ¿Existen muchos casos de entregas extremadamente lentas o rápidas?

Sea $X$ la suma de los valores obtenidos al lanzar dos dados. SU espacio muestral es:
$$X=\{2,3,4,5,6,7,8,9,10,11,12\}$$
$$M_{X}(t)=E[e^{tX}]=\sum\limits^{12}_{x=1}e^{tx}P(X=x)$$
$$M_{X}(t)=\frac{1}{36}e^{2t}+\frac{2}{36}e^{3t}+\frac{3}{36}e^{4t}+\frac{4}{36}e^{5t}+\frac{5}{36}e^{6t}+\frac{6}{36}e^{7t}+\frac{5}{36}e^{8t}+\frac{4}{36}e^{9t}+\frac{3}{36}e^{10t}+\frac{2}{36}e^{11t}+\frac{1}{36}e^{12t}$$
$$M'_{X}(t)=\frac{1}{18}e^{2t}+\frac{1}{6}e^{3t}+\frac{1}{3}e^{4t}+\frac{5}{9}e^{5t}+\frac{5}{6}e^{6t}+\frac{7}{6}e^{7t}+\frac{10}{9}e^{8t}+e^{9t}+\frac{5}{6}e^{10t}+\frac{11}{18}e^{11t}+\frac{1}{3}e^{12t}$$
$$M''_{X}(t)=\frac{1}{18}e^{2t}+\frac{1}{6}e^{3t}+\frac{1}{3}e^{4t}+\frac{5}{9}e^{5t}+\frac{5}{6}e^{6t}+\frac{7}{6}e^{7t}+\frac{10}{9}e^{8t}+e^{9t}+\frac{5}{6}e^{10t}+\frac{11}{18}e^{11t}+\frac{1}{3}e^{12t}$$

### Ejercicio 1
Sea $X_{1},X_{2},X_{3}$ una muestra aleatoria de distribución aleatoria con la función de probabilidad:

$$p(x)=\begin{cases}
\frac{1}{3}, & \text{si } x = 0, \\
\frac{2}{3}, & \text{si } x = 1.\\
0, & \text{otro caso}
\end{cases}$$
| $X_{1}$ | $X_{2}$ | $X_{3}$ |     |
| ------- | ------- | ------- | --- |
| 0       | 0       | 0       | 0   |
| 0       | 0       | 1       | 0   |
| 0       | 1       | 0       | 0   |
| 0       | 1       | 1       | 0   |
| 1       | 0       | 0       | 0   |
| 1       | 0       | 1       | 0   |
| 1       | 1       | 0       | 0   |
| 1       | 1       | 1       | 1   |
$$P(Y=y)$$
$$\left(\frac{2}{3}\right)\left(\frac{2}{3}\right)\left(\frac{2}{3}\right)=\frac{8}{27}$$
$$1-\frac{8}{7}=\frac{19}{27}$$
$$y=1 \rightarrow \frac{8}{27}$$
$$y=0 \rightarrow \frac{19}{27}$$
$$M_{y}(t)=\frac{19}{27} e^{t(0)}+ \frac{8}{27}e^{t(1)}=\frac{19}{27} + \frac{8}{27}e^{t}$$
### Ejercicio 2
Dos pelotas son lanzadas de tal manera que tiene la misma probabilidad caer en cualquiera de las cuatro canastas, las dos pelotas pueden caer en la misma canasta. Sea $X$ el número de canastas desocupadas al final del experimento, ¿Cuál es la función generativa de momentos de $X$?