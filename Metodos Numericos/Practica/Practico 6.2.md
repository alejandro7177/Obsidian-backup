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

