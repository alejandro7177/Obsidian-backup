Dada la ecuación:

$$
e^x +x_2-7 =0
$$

1. Separar una raiz negativa con el metodo de tanteo
2. Aproxima la raíz separada con el metodo de interpolación lineal, iterando 3 veces al metodo (trabajar con 4 decimales)
3. Calcular el error cometido en la determinación de la raíz aproximada

$$
\begin{align}
f(x)=e^x +x_2-7\\
f(0)= 1 +0 -7 = -6\\
f(-1)=e^{-1}+1-7-5,6321\\
f(-2)=e^{-2}+4-7 = -2,8646\\
f(-3)=e^{-3}+9-7=2,0497
\end{align}
$$
$$
\begin{align}
x_1 = -2\\
x_2 = -3\\
y_1 = -2,8646\\
y_2 = 2,0497\\\\

x_3 = \frac{x_1y_2-x_2y_1}{y_2-y_1}\approx -2,5829\\
y_3 = -0,2530\\
Er_1 = \frac{|x_3-x_2|}{|x_3|} = \frac{0,4171}{2,5829}=0,1614\\
Ea_1=|x_3-x_2| = 0,4171 \\\\

x_4=\frac{x_2y_3-x_3y_2}{y_3-y_2}\approx-2,6287\\
y_4 = -0,0177\\
Er_2 = \frac{|x_4-x_3|}{|x_4|} = \frac{0,0458}{2,6287}=0,0174\\
Ea_2=|x_3-x_2| = 0,0458 \\\\

x_5=\frac{x_3y_4-x_4y_3}{y_4-y_3}\approx-2,6321\\ 
y_5=-0,0001\\

Er_2 = \frac{|x_5-x_4|}{|x_5|} = \frac{0,0034}{2,6321}=0,0012\\
Ea_2=|x_4-x_5| = 0,0034 \\\\

\end{align}
$$
En un laboratorio se producen 42 mil unidades de insulina, con las cuales se abastece
a 3 ciudades A, B, C. La última semana del mes, la ciudad A solicitó tantas unidades
como la B y la C juntas. Además, la B pidió la suma de la mitad de lo pedido por la A,
más la tercera parte de lo pedido por la C. ¿Qué cantidad solicitó cada una?

$$
\left\{
\begin{matrix}
A + B + C = 42\\
-A+B + C =0 \\
\frac{1}{2}A  -B+\frac{1}{3}C = 0
\end{matrix}
\right.
$$

$$
\begin{pmatrix}
1&1&1\\
-1&1&1\\
1/2&-1&1/3
\end{pmatrix}
$$

$$
\begin{align}
F_2+F1\rightarrow F_2\\
F_3-\frac{1}{2}F_1 \rightarrow F_3
\end{align}
$$

$$
\begin{pmatrix}
1&1&1\\
0&2&2\\
0&-3/2&-1/6
\end{pmatrix}
$$

$$
F_3 +\frac{3}{4}F_2$$

$$\begin{pmatrix}
1&1&1\\
0&2&2\\
0&0&4/3
\end{pmatrix}$$

$$
\begin{pmatrix}
1&1&1\\
-1&1&1\\
1/2&-1&1/3
\end{pmatrix}=
\begin{pmatrix}
1&0&0\\
-1&1&0\\
1/2&-3/4&1
\end{pmatrix}*\begin{pmatrix}
1&1&1\\
0&2&2\\
0&0&4/3
\end{pmatrix}
$$

$$L*y = b$$

$$
\begin{bmatrix}
1&0&0\\
-1&1&0\\
1/2&-3/4&1
\end{bmatrix}*
\begin{bmatrix}y_1\\y_2\\y_3\end{bmatrix}=
\begin{bmatrix}42\\0\\0\end{bmatrix} \rightarrow
\left\{
\begin{matrix}
y_1=42\\
-y_1 +y_2 = 0 \rightarrow y_2 = 42\\
\frac{1}{2}y_1-\frac{3}{4}y_2+y_3= 0 \rightarrow y_3 =-10.5
\end{matrix}
\right.
$$

$$
U*x=y
$$

$$
\begin{bmatrix}
1&1&1\\
0&2&2\\
0&0&4/3
\end{bmatrix}*
\begin{bmatrix}x_1\\x_2\\x_3\end{bmatrix}=
\begin{bmatrix}42\\42\\10,5\end{bmatrix} \rightarrow

\left\{
\begin{matrix}
x_1+x_2+x_3=42 \rightarrow \boxed{x_1=21}\\
2x_2+2x_3= 42 \rightarrow \boxed{x_2=13.125}\\
x_3 = \boxed{7.875}
\end{matrix}
\right.

$$



