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