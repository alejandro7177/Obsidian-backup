1. La integración proporciona un medio para calcular cuanta masa entra o sale de un reactor durante un periodo específico de tiempo, así
$$
M = \int_{t_{1}}^{t_2}Q(t)c(t)dt
$$
Donde $t_1$ y $t_2$ son los tiempos inicial y final del periodo. Use integración numérica para estimar cuanta masa sale de un reactor con base en las siguientes mediciones:


> [!NOTE] Formula $\frac{3}{8}$ de Simpson
> $$
> \begin{gather}
> A \approx \frac{3h}{8}[y_0+3(y_1)+3(y_2)+y_3]
> \end{gather}
> $$

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

> [!NOTE] Formula $\frac{1}{3}$ Simpson
> $$
> \begin{gather}
> h = \text{distancia entre }x's \\
> E = y_0 + y_n\\
> P = y_2 + y_4 + y_6 +... = \sum_{\substack{i = 2 \\ i \neq n \\ i \mod 2 = 0}}^N y_n\\
> I = y_1+y_3+y_5+...=  \sum_{\substack{i = 1 \\ i \neq n \\ i \mod 2 = 1}}^N y_n\\
> \\
> A \approx \frac{h}{3}(E+2P+4I)
> \end{gather}
> $$

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
 2. Un estudio de ingeniería del transporte de mercadería requiere que usted determine el número de vehículos que pasan por un punto de control en la hora pico. Usted se para al lado de la vía y cuenta el número de vehículos que pasan cada minuto a varias horas, como se muestra en la tabla a continuación

|         tiempo (h)          | 7.30 | 7.45 |  8  | 8.15 | 8.45 | 9.15 |
| :-------------------------: | :--: | :--: | :-: | :--: | :--: | :--: |
| Taza (vehiculos por minuto) | 4.5  |  6   | 6.5 |  5   | 4.5  | 2.25 |

Utilice el mejor método numérico para determinar el número total de vehículos que pasan entre las 7.30 y las 9.15. (Combinación de trapecio y Simpson) y estime el error.

Conversión de tiempo a formato decimal y multiplicamos la taza \* 60 para que tenga la misma medida de horas

|         tiempo (h)          | 7.5 | 7.75 |  8  | 8.25 | 8.75 | 9.25 |
| :-------------------------: | :-: | :--: | :-: | :--: | :--: | :--: |
| Taza (vehiculos por minuto) | 4.5 |  6   | 6.5 |  5   | 4.5  | 2.25 |
|  Taza (vehiculos por hora)  | 270 | 360  | 390 | 300  | 270  | 135  |
Simsom 3/8
![[Pasted image 20241022124714.png]]
$$\begin{matrix}
A_1 = \int_{7.5}^{8.25} f(h') \overset{\sim}{\equiv} \frac{3h}{8}\left[270+3(360)+3(390)+300\right]\\
A_1 \overset{\sim}{\equiv} \frac{0.75}{8}[270+1080+1170+300]\\
A_1 \overset{\sim}{\equiv} 0.09375 * 2820\\
A_1 \overset{\sim}{\equiv} 264.375
\end{matrix}$$
Simsom 1/3
![[Pasted image 20241022124722.png]]

$$\begin{matrix}
A_2 = \int_{8.25}^{9.25} f(h') \overset{\sim}{\equiv} \frac{h}{3}[(300+135)+2*(0)+4(270)]\\
A_2 \overset{\sim}{\equiv} \frac{0.5}{3}[435+1080]\\
A_2 \overset{\sim}{\equiv} \frac{1}{6} *1515 \\
A_2 \overset{\sim}{\equiv} 252.5
\end{matrix}$$

$$
A = A_1 + A_2 = 264.375 + 252.5 = \boxed{516.875}
$$

3. Durante un levantamiento, se le pide que calcule el área del terreno que se muestra en la Figura 1. Emplee reglas de integración numérica para determinar el área.
![[grafico_area_rio_simpsom.png]]



| x   | y    | Metodo               | x    | y    | Metodo               | x    | y    | Metodo               |
| --- | ---- | -------------------- | ---- | ---- | -------------------- | ---- | ---- | -------------------- |
| 0   | 2400 | $\frac{3}{8}$Simpson | 600  | 2600 | $\frac{3}{8}$Simpson | 1200 | 3000 | $\frac{3}{8}$Simpson |
| 200 | 2600 |                      | 800  | 2600 |                      | 1400 | 3000 |                      |
| 400 | 2400 |                      | 1000 | 2800 |                      | 1600 | 3200 |                      |
| 600 | 2600 |                      | 1200 | 3000 |                      | 1800 | 3200 |                      |

| x    | y    | Metodo               | x    | y    | Metodo               | x    | y    | Metodo               |
| ---- | ---- | -------------------- | ---- | ---- | -------------------- | ---- | ---- | -------------------- |
| 1800 | 3200 | $\frac{3}{8}$Simpson | 2400 | 2600 | $\frac{3}{8}$Simpson | 3000 | 1800 | $\frac{3}{8}$Simpson |
| 2000 | 3200 |                      | 2600 | 2200 |                      | 3200 | 1600 |                      |
| 2200 | 3000 |                      | 2800 | 2000 |                      | 3400 | 1200 |                      |
| 2400 | 2600 |                      | 3000 | 1800 |                      | 3600 | 1000 |                      |

| x    | y    | Metodo               |
| ---- | ---- | -------------------- |
| 3600 | 1000 | $\frac{3}{8}$Simpson |
| 3800 | 800  |                      |
| 4000 | 600  |                      |
| 4200 | 200  |                      |
$$
\begin{gather}
A_1 = \int_0^{600} f(x)dx \approx \frac{600}{8}[2400+3(2600)+3(2400)+2600]\\
A_1 \approx 75(20000)\\
A_1 \approx 1500000
\end{gather}
$$
$$
\begin{gather}
A_2 = \int_{600}^{1200} f(x)dx\approx \frac{600}{8}[2600+3(2600)+3(2800)+3000]\\
A_2 \approx 75(21800)\\
A_2 \approx 1635000
\end{gather}
$$
$$\begin{gather}
A_3 = \int_{1200}^{1800} f(x)dx \approx \frac{600}{8}[3000+3(3000)+3(3200)+3200]\\
A_3 \approx 75(24800)\\
A_3 \approx 1860000
\end{gather}$$
$$\begin{gather}
A_4 = \int_{1800}^{2400}f(x)dx \approx \frac{600}{8}[3200+3(3200)+3(3000)+2600]\\
A_4 \approx 75(24400)\\
A_4 \approx 1830000
\end{gather}$$
$$\begin{gather}
A_5 = \int_{2400}^{3000}f(x)dx \approx \frac{600}{8}[2600+3(2200)+3(2000)+1800]\\
A_5 \approx 75(17000)
A_5 \approx 1275000
\end{gather}$$
$$\begin{gather}
A_6 = \int_{3000}^{3600}f(x)dx\approx \frac{600}{8}[1800+3(1600)+3(1200)+1000]\\
A_6 \approx 75(11200)\\
A_6 \approx 840000
\end{gather}$$
$$
\begin{gather}
A_7 = \int_{3600}^{4200}f(x)dx\approx \frac{600}{8}[1000+3(800)+3(600)+200]\\
A_7 \approx 75(5400)\\
A_7 \approx 405000
\end{gather}
$$
$$
\begin{gather}
A = \sum_{i=1}^{7} A_i\\
A = 1500000+1635000+1860000+1830000+1275000+840000+405000\\
A = 9345000\\
A = 9.345 *10^6
\end{gather}
$$

Respuesta:
El area aproxima de terreno es igual a 9.435.000 pies²