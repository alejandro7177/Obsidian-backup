Resolver el siguiente sistema utilizando el método de Fadeev-Leverrier. Hallar los
autovalores y los eigenvectores asociados
$$
\left\{
\begin{matrix}
(3- \lambda)x -2y -z = 0\\
x + (-2- \lambda)y + 3z = 0\\
2x + (4- \lambda)z = 0
\end{matrix}
\right.
$$
$$
A=\begin{pmatrix}
3 & -2 & -1 \\
1 & -2 & 3 \\
2 & 0 & 4
\end{pmatrix}
$$
$$B_1=A ;\ \ b_1 = 3 -2+4 =5$$
$$
B_2 = A\left(B_1-b_1*I\right)
$$
$$
B_2 = \begin{pmatrix}
3 & -2 & -1\\
1 & -2 & 3\\
2 & 0 & 4
\end{pmatrix} *
\left\{
\begin{pmatrix}
3 & -2 & -1 \\
1 & -2 & 3 \\
2 & 0 & 4
\end{pmatrix}-
\begin{pmatrix}
5 &0&0 \\
0&5&0\\
0&0&5
\end{pmatrix}
\right\} =
\begin{pmatrix}
-10 &8&-8\\
2&12&-10\\
4&-4&-6
\end{pmatrix}
$$
$$ 
b_2 = \frac{1}{2}(-10 +12-6) = -2
$$
$$
B_3 = A\left(B_2-b_2*I\right)
$$
$$
B_3 = \begin{pmatrix}
3 & -2 & -1\\
1 & -2 & 3\\
2 & 0 & 4
\end{pmatrix} * 
\left\{
\begin{pmatrix}
-10 &8&-8\\
2&12&-10\\
4&-4&-6
\end{pmatrix}-
\begin{pmatrix}
-2&0&0\\
0&-2&0\\
0&0&-2
\end{pmatrix}
\right\}
=
\begin{pmatrix}
-32&0&0\\
0&-32&0\\
0&0&-32
\end{pmatrix}
$$
$$b_3 = \frac{1}{3} trB_3 = \frac{1}{3}(-32-32-32)=-32$$

Polinomio Fadeev-Leverrierf
$$
\begin{align*}
(-1)^3 (\lambda^3-5\lambda²+2\lambda+32)=0 \\
-\lambda^3+5\lambda²-2\lambda-32=0
\end{align*}
$$
$$
\begin{align*}
-\lambda &\rightarrow +++- \rightarrow \text{1 raiz negativas}\\
+\lambda &\rightarrow -+-- \rightarrow \text{2 o 0 raices positivas} \\\\

f(-1) &= -(-1)³ + 5*(-1)+2-32 = -34\\
f(-2)&= -(-2)³+5*(-2)-2*(-2)-32 = 0 \\\\

f(1) &= -1+5-2-32= -30
\end{align*}
$$


$$
\left\{
\begin{matrix}
5x -2y -z = 0\\
x + 3z = 0\\
2x + 6z = 0
\end{matrix}
\right.
$$

$$
\begin{pmatrix}
5 & -2&-1& 0\\
1&0&3 &0\\
2&0&6 & 0
\end{pmatrix}
$$
$$
\begin{matrix}
F_2 - \frac{1}{5}F_1 \rightarrow F_2 \\
F_3 - \frac{2}{5}F_1 \rightarrow F_3
\end{matrix}
$$
$$
\begin{pmatrix}
5 & -2&-1 &|&0\\
0&0&\frac{16}{5} &|&0\\
0&0&\frac{32}{5} &|& 0
\end{pmatrix}
$$
$$
\begin{cases}
5x_1-2x_2-x_3 = 0 \\
3.2x_3 = 0\\
6.4x_3=0
\end{cases}
$$
$\boxed{x_3 =0}$

$5x_1-2x_2=0$

$\boxed{x_2 = \lambda}$

$5x_1-2\lambda = 0 \rightarrow 5x_1 = 2\lambda$

$\boxed{x_1 = \frac{2}{5}\lambda}$

$$
\text{Autovalor: -2 y su vector asociado es}\rightarrow
\begin{bmatrix}
\frac{2}{5}\lambda\\
\lambda\\
0
\end{bmatrix}
$$
