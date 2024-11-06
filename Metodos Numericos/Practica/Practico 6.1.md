1. La integración proporciona un medio para calcular cuanta masa entra o sale de un reactor durante un periodo específico de tiempo, así
$$
M = \int_{t_{1}}^{t_2}Q(t)c(t)dt
$$
Donde $t_1$ y $t_2$ son los tiempos inicial y final del periodo. Use integración numérica para estimar cuanta masa sale de un reactor con base en las siguientes mediciones:

| $T, min$           | 0   | 10  | 20  | 30  | 35  | 40    | 45    | 50  |
| ------------------ | --- | --- | --- | --- | --- | ----- | ----- | --- |
| $Q \frac{m3}{min}$ | 4   | 4.8 | 5.2 | 5.0 | 4.6 | 4.3   | 4.3   | 5.0 |
| $C\frac{mg}{m3}$   | 10  | 35  | 55  | 53  | 40  | 37    | 32    | 34  |
| $Q(t)C(t)$         | 40  | 168 | 286 | 265 | 184 | 159.1 | 137.6 | 170 |
Simpson 3/8
![[Pasted image 20241022131849.png]]
$$\begin{matrix}
A_{1} = \int_{0}^{30} Q(t)c(t) = \frac{30}{8}(40+3*168+3*286+265)= 6251.25 \\
\end{matrix}$$
![[Pasted image 20241022131859.png]]
$$\begin{matrix}
A_{2} = \int_{30}^{50}Q(t)c(t) \approx \frac{h}{3}[E+2P+4I] \\\\
E = 265+170= 435 \\
I = 184+137.6=321.6\\
P = 159.1 \\\\
A_2 \approx \frac{5}{3}(435+2(159.1)+4(321.6))\\
A_2 \approx \frac{5}{3}* 2039.6\\
A_2 \approx 3399.\overline{3}\\
\end{matrix}$$

$$A = A_{1}+A_{2}= 6251.25 + 3399.\overline{3} = \boxed{9650.58\overline{3}}$$
 