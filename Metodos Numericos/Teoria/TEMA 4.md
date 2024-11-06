para el rango se escalona la matriz y luego se cuenta la filas no nulas

$$r\neq r' \text{no es compatible}$$
una matriz es homogeneo si los independiente son iguales a 0

$$
\begin{align*}
2x_1 -2x_2 +5x_3 =13 \\
2x_1 +3x_2 + 4x_3 = 20 \\
3x_1 -x_2 +3_x3 =10
\end{align*}
$$
$$
\begin{align*}
2 \ 2 \ 5  |13 \\
2x_1 +3x_2 + 4x_3 = 20 \\
3x_1 -x_2 +3_x3 =10
\end{align*}

$$

| 2   | -2  | 5   | 13  |
| --- | --- | --- | --- |
| 2   | 3   | 4   | 20  |
| 3   | -1  | 3   | 10  |
$$\begin{align*}
F_2 -\frac{2}{2} F_1 \rightarrow F_2 \\
F_3-\frac{3}{2} F_1 \rightarrow F_3
\end{align*}
$$

| 2   | -2  | 5    | 13   |
| --- | --- | ---- | ---- |
| 0   | 5   | -1   | 7    |
| 0   | 2   | -4,5 | -9,5 |
$$
F_3-(\frac{10}{2})F_2 \rightarrow F_2
$$
$$
F_3 -\frac{2}{5}F_2 \rightarrow F_3
$$

| 2   | -2  | 5    | 13    |
| --- | --- | ---- | ----- |
| 0   | 5   | -1   | 7     |
| 0   | 0   | -4,1 | -12,3 |
$$
\begin{align*}
-4,1x_3 = -12,3 \rightarrow \frac{-12,3}{-4,1}=3 \\
5x_2-3=7 \rightarrow x_2 =2 \\
2x_1-2x_2+5x_3=13 \\
2x_1-2*2+5*3=13 \\
2x_1-4+15=13\\
2x_1+11=13\\
2x_1=2 \\
x_1=1
\end{align*}
$$
GAUSS-JORDAN
$$
b_{n;j-1}=\frac{a_{ij}}{}
$$
Factorizacion LU

$$
U=
\begin{bmatrix}
a_{11}& a_{12} &a_{13}\\
0&a'_{22} & a'_{23}\\
0&0&a''_{33}
\end{bmatrix}
$$
$$
L=
\begin{bmatrix}
1&0&0\\
5&1&0\\
-2&3&1
\end{bmatrix}
$$
$$L*y=b$$
$$
\begin{bmatrix}
1&0&0\\
5&1&0\\
-2&3&1
\end{bmatrix}
*
\begin{bmatrix}
y_1\\ y_2 \\ y_3
\end{bmatrix}
=
\begin{bmatrix}
11\\70\\17
\end{bmatrix}
\rightarrow
\begin{matrix}
y_1 =11\\
5y_1+y_2=70 \rightarrow y_2=15 \\
-2y_1 +3y_2+y_3=17 \rightarrow y_3=-6
\end{matrix}
$$
$$U*x=y$$
$$
\begin{bmatrix}
1&0&0\\
5&1&0\\
-2&3&1
\end{bmatrix}
*
\begin{bmatrix}
x_1\\ x_2 \\ x_3
\end{bmatrix}
=
\begin{bmatrix}
11\\15\\-6
\end{bmatrix}
\rightarrow
\left\{
\begin{matrix}
4x_1-2x_2+x_3=11\\
3x_2+7x_3=15\\
-2x_3=-6
\end{matrix}
\right.
$$

GAUSS-SEIDEL

condicion -> diagonalemente dominante

$$
\left\{
\begin{matrix}
18,72x+8,2y+8,76z =121,280 \\
6,4x+15,9y+7,18z=126,321\\
5,22x+6,4y+7,18z=118,522
\end{matrix}
\right.
$$
$$
\begin{align*}
18,72 >8,2+8,7 \\
15,9>6,4+7,18\\
14,31>5,22+6,4
\end{align*}
$$
$$x_0=y_0=z_0=1$$
$$
\begin{align*}
18,72x_1+8,2*1+8,76*1 =121,280 \\
x_1 = \frac{121,280-8,2-8,76}{18,72}\\
x_1= 5,553
\end{align*}
$$
$$
\begin{align*}
6,4*5,553 +15,9*1+7,18*1= 126,321\\
y_1= \frac{126,321-6,4*5,553-7,18}{15,9}\\
y_1=5,25
\end{align*}
$$
$$
\begin{align*}
5,22*5,553+6,4*5,25+14,3*z_1=118,522\\
z_1= 118,522-5,22*5,573-6,4*5,25\\
z_1=3,902
\end{align*}
$$
$$
\begin{align*}
x_2&=\frac{121,280-8,2*5,25-8,76*3,902}{18,72}\\
x_2&=2,353
\end{align*}
$$
$$
\begin{align*}
y_2&=\frac{126,321-6,4*2,353-7,18*3,902}{15,9}\\
y_2&=5,236
\end{align*}
$$
$$
\begin{align*}
z_2&=\frac {118,522-5,22*2,353-6,4*5,236} {14,3}\\
z_2&=5,086
\end{align*}
$$

