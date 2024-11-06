Una compañía electrónica produce transistores, resistores y chips de computadoras. Cada transistor requiere 4,3 unidades de cobre, una de zinc y dos de vidrio. Cada resistor requiere tres, tres y una unidad de dichos materiales, respectivamente, y cada chip de computadora requiere dos, una y tres unidades de los materiales, respectivamente. En forma de tabla, esta información queda así:


| Componente            | Cobre | Zing | Vidrio |
| --------------------- | ----- | ---- | ------ |
| Transistores          | 4,3   | 1    | 2      |
| Resistores            | 3     | 3    | 1      |
| Chips de Computadoras | 2     | 1    | 3      |
Los suministros de estos materiales varían de una semana a la otra, de modo que la compañía necesita determinar una corrida de producción diferente cada semana. Por ejemplo, cierta semana las cantidades disponibles de los materiales son 960 unidades de cobre, 510 unidades
de zinc y 610 unidades de vidrio

1. Plantea el sistema de ecuaciones lineales que modela la situación
   $$
\begin{align*}
Cobre &= x\\
Zing &= y\\
Vidrio &= z\\\\
\left\{
\begin{matrix}
4,3t+ 3r + 2c = x \\
t+3r+c=y \\
2t+r+3c=z
\end{matrix}
\right.
\end{align*}
$$
2. Aplica los diferentes métodos de resolución de sistemas de ecuaciones lineales y analice los resultados obtenidos
$$
\begin{align*}
\begin{pmatrix}
4.3&3&2&960\\
1&3&1&510\\
2&1&3&610
\end{pmatrix}
=
&\begin{bmatrix}
1&0&0\\
\frac{10}{43}&1&0\\
\frac{20}{43}&-\frac{17}{43}&1
\end{bmatrix}
*
\begin{bmatrix}
4.3&3&2\\
0&\frac{60}{43}&\frac{99}{43}\\
0&0&\frac{2341}{860}
\end{bmatrix}\\\\
\\
&\begin{bmatrix}
4.3&3&2\\
1&3&1\\
2&1&3
\end{bmatrix}
\\
&F_2-\frac{10}{43}F_1 \rightarrow F_2 \\
&F_3 - \frac{20}{43}F_1 \rightarrow F_3\\
&\begin{bmatrix}
4.3&3&2\\
0&\frac{60}{43}&\frac{99}{43}\\
0&-\frac{17}{43}&\frac{89}{43}
\end{bmatrix}\\
&F_3-\left(-\frac{17}{60}\right)F_2 \rightarrow F_3\\
&\begin{bmatrix}
4.3&3&2\\
0&\frac{60}{43}&\frac{99}{43}\\
0&0&\frac{2341}{860}
\end{bmatrix}
\end{align*}
$$

L \* y=b

$$
\begin{bmatrix}
1&0&0\\
\frac{10}{43}&1&0\\
\frac{20}{43}&-\frac{17}{43}&1
\end{bmatrix}*
\begin{bmatrix*}y_1\\y_2\\y_3\end{bmatrix*}
=
\begin{bmatrix*}960\\510\\610\end{bmatrix*}
\rightarrow
\left\{
\begin{matrix}
y_1 = 960\\
\frac{10}{43}y_1+y_2 =510 \rightarrow y_2 = \frac{12330}{43} \approx 286.744\\
\frac{20}{43}y_1-\frac{17}{43}y_2+y_3 = 610 \rightarrow y_3 =610-\frac{1920}{43}+\frac{209610}{1849}\\
y_3 = \frac{1254940}{1849} \approx 678.7128
\end{matrix}
\right.
$$
U \* x = y
$$
\begin{bmatrix}
4.3&3&2\\
0&\frac{60}{43}&\frac{99}{43}\\
0&0&\frac{2341}{860}
\end{bmatrix}*
\begin{bmatrix}
x_1\\x_2\\x_3
\end{bmatrix}=
\begin{bmatrix}960\\\frac{12330}{43}\\\frac{1254940}{1849}\end{bmatrix}
\rightarrow
\left\{
\begin{matrix}
4.3x_1 +3x_2+2x_3 = 960\\
\frac{60}{43}x_2+\frac{99}{43}x_3=\frac{12330}{43}\\
\frac{2341}{860}x_3=\frac{1254940}{1849}\rightarrow x_3 =\frac{\frac{1254940}{1849}}{\frac{2341}{860}}\\
x_3=\frac{25098800}{100663}\approx 249.3349
\end{matrix}
\right.
$$
$$
\begin{align*}
\frac{60}{43}x_2+\frac{99}{43}*\frac{25098800}{100663}=\frac{12330}{43}\\
\frac{60}{43}x_2 = \frac{12330}{43}-\frac{2484781200}{4328509}\\
\frac{60}{43}x_2=-\frac{1243606410}{4328509} \\
x_2 = \frac{-\frac{1243606410}{4328509}}{\frac{60}{43}}\\
x_2 = -\frac{41453547}{201326} \approx −205,9026
\end{align*}$$
$$
\begin{matrix}
4.3x_1 +3*\left(-\frac{41453547}{201326}\right)+2*\frac{25098800}{100663} = 960\\
4.3x_1 = 960 + \frac{23965441}{201326}\\
x_1 = \frac{\frac{217238401}{201326}}{4.3} \\
x_1 = \frac{217238401}{865701.8}\approx 250.9390
\end{matrix}
$$


