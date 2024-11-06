Dado el siguiente sistema de ecuaciones:
$$
\left\{
\begin{matrix}
2x_1+3x_2+4x_3=6\\
4x_1+5x_2+10x_3=16\\
4x_1+8x_2+2x_3=2
\end{matrix}
\right.
$$
1. Encuentre la factorización LU de la matriz de coeficientes.
$$
\begin{bmatrix}
2 & 3 & 4\\
4&5&10\\
4&8&2
\end{bmatrix}=
\overset{L}{
\begin{pmatrix}
1 & 0 & 0\\
 2& 1 & 0\\
 2& -2& 1
\end{pmatrix}}*
\overset{\text{U}}{
\begin{pmatrix}
2&3&4\\
0&-1&2\\
0&0&-2
\end{pmatrix}}
$$$$
\begin{bmatrix}
2 & 3 & 4\\
4&5&10\\
4&8&2
\end{bmatrix}
\overset{F_2-2F_1\rightarrow F_2}{
\approx}
\begin{bmatrix}
2&3 & 4\\
0&1&2\\
4&8&2
\end{bmatrix}
\overset{F_3-2F_1\rightarrow F_3}{
\approx}
\begin{bmatrix}
2&3 & 4\\
0&-1&2\\
0&2&-6
\end{bmatrix}
\overset{F_3+2F_2\rightarrow F_3}{
\approx}
\begin{bmatrix}
2&3 & 4\\
0&-1&2\\
0&0&-2
\end{bmatrix}
$$

2. Resuelva el sistema de ecuaciones utilizando la descomposición anterior.

$$L*y=b$$
$$
\begin{bmatrix}
1 & 0 & 0\\
 2& 1 & 0\\
 2& -2& 1
\end{bmatrix}
*
\begin{bmatrix}
y_1\\ y_2 \\ y_3
\end{bmatrix}
=
\begin{bmatrix}
6\\16\\2
\end{bmatrix}
\rightarrow
\begin{matrix}
y_1 = 6\\
2y_1 +y_2 = 16 \rightarrow y_2=4\\
2y_1-2y_2+y_3=2 \rightarrow 4+y_3 = 2 \rightarrow y_3=-2
\end{matrix}
$$
$$U*x=y$$
$$\begin{bmatrix}
2&3&4\\
0&-1&2\\
0&0&-2
\end{bmatrix}
*
\begin{bmatrix}
x_1\\ x_2 \\ x_3
\end{bmatrix}
=
\begin{bmatrix}
6\\4\\-2
\end{bmatrix}
\rightarrow
\left\{
\begin{matrix}
2x_1&+3x_2&+4x_3&=6\\
&-x_2&+2x_3 &=4\\
&&-2x_3&=-2

\end{matrix}
\right.
$$
$$
\begin{matrix}
\boxed{x_3= 1}\\
-x_2 +2 = 4 \rightarrow \boxed{x_2=-2}\\
2x_1-6+4=6 \rightarrow 2x_1= 8  \rightarrow \boxed{x_1 = 4}\\
\end{matrix}
$$
