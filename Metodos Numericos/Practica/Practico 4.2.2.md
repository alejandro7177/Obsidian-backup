En el estudio de las vibraciones de un sistema consistente en 3 masas insertadas en una
varilla, la ecuación del movimiento tiene que ver con la formulación de valores propios:

$$\begin{pmatrix}
2-\lambda & -0,5 & 0\\
-0,5 & 1-  \lambda & -0,5 \\
0 & -0,5 & \frac{2}{3} - \lambda
\end{pmatrix}
$$

$$
\begin{align*}
2k-2mw²=0 \\
2k = 2mw²\\
k = mw² \\
1 = \frac{mw²}{k}= \lambda \\
1- \lambda = 0
\end{align*}
$$
$$
\begin{align*}
2k-3mw²=0 \\
2k=3mw² \\
k=\frac{3}{2} mw²\\
0=\frac{\frac{3}{2}{mw²}} {k}\\
\frac{1}{3/2}=\frac{mw²}{k}\\
\frac{1}{3/2}=\lambda \\
\frac{1}{3/2} - \lambda=0 \\
\frac{2}{3} - \lambda=0 \\
\end{align*}
$$

$$
B_1 = \begin{pmatrix}
2 & -0,5& 0\\
-0,5 & 1 & -0,5\\
0 & 0,5 & \frac{2}{3}
\end{pmatrix}
$$
$$ b_1=2+1+\frac{2}{3} = \boxed{\frac{11}{3}}$$
$$
B_2 = \begin{pmatrix}
2 & -0,5& 0\\
-0,5 & 1 & -0,5\\
0 & 0,5 & \frac{2}{3}
\end{pmatrix}*
\left(\begin{pmatrix}
2 & -0,5& 0\\
-0,5 & 1 & -0,5\\
0 & 0,5 & \frac{2}{3}
\end{pmatrix}
-\begin{pmatrix}
\frac{11}{3}&0&0\\
0&\frac{11}{3}&0\\
0&0&\frac{11}{3}
\end{pmatrix}
\right)
$$
$$
B_2 = \begin{pmatrix}
2 & -0,5& 0\\
-0,5 & 1 & -0,5\\
0 & 0,5 & \frac{2}{3}
\end{pmatrix}*
\begin{pmatrix}
-\frac{5}{3} & -0,5& 0\\
-0,5 & -\frac{8}{3} & -0,5\\
0 & 0,5 & -3
\end{pmatrix}
=
\boxed{\begin{pmatrix}
-\frac{37}{12}&\frac{1}{3}&\frac{1}{4}\\
\frac{1}{3}&-\frac{8}{3}&1\\
-\frac{1}{4}&-1&-\frac{9}{4}\end{pmatrix}}
$$
$$
b_2 = \frac{1}{2} trB_2 = \frac{1}{2} (-8)=\boxed{-4}
$$
$$
B_3 = \begin{pmatrix}
2 & -0,5& 0\\
-0,5 & 1 & -0,5\\
0 & 0,5 & \frac{2}{3}
\end{pmatrix}*
\left(\begin{pmatrix}
-\frac{37}{12}&\frac{1}{3}&\frac{1}{4}\\
\frac{1}{3}&-\frac{8}{3}&1\\
-\frac{1}{4}&-1&-\frac{9}{4}
\end{pmatrix}-
\begin{pmatrix}
-4&0&0\\
0&-4&0\\
0&0&-4
\end{pmatrix}\right)
$$
$$
B_3 = \begin{pmatrix}
2 & -0,5& 0\\
-0,5 & 1 & -0,5\\
0 & 0,5 & \frac{2}{3}
\end{pmatrix}*
\begin{pmatrix}
\frac{11}{12}&\frac{1}{3}&\frac{1}{4}\\
\frac{1}{3}&\frac{4}{3}&1\\
-\frac{1}{4}&-1&\frac{7}{4}
\end{pmatrix} =
\boxed{\begin{pmatrix}
\frac{5}{3}&0&0\\ 
0&\frac{5}{3}&0\\ 
0&0&\frac{5}{3}
\end{pmatrix}}
$$
$$
b_3  = \frac{1}{3}trB_3 = \frac{1}{3}*\left(\frac{5}{3}+\frac{5}{3}+\frac{5}{3}\right)=\frac{1}{3}*5 = \boxed{\frac{5}{3}}
$$
Polinomio caracteristico
$$
(-1)^3*\left(\lambda³ -\frac{11}{3}\lambda²+4\lambda-\frac{5}{3}\right)=0
$$
$$
-\lambda³ +\frac{11}{3}\lambda²-4\lambda+\frac{5}{3}=0
$$
$$
\boxed{-3\lambda³ +11\lambda²-12\lambda+5=0}
$$
Descartes
$\text{x positivo :} -+-+ \rightarrow \text{3 raices positivas reales o 1 real y 2 complejas }$
$\text{x negativo :} ++++ \rightarrow \text{0 raices negativas}$

Tanteo
$$
\begin{matrix}
x_{0} = 0 \rightarrow f(x_{0})=5 \\
x_{1}=1 \rightarrow f(x_{1})=1 \\
\boxed{x_{2}=2 \rightarrow f(x_{2})=1} \\
\boxed{x_{3}=3 \rightarrow f(x_{3})= −13}

\end{matrix}
$$
Newton Rapson para obtener la raiz
$f(x)'=-9\lambda^{2}+22 \lambda -12$
$f(x)''=-18\lambda +22$
$1*f(1)'' = 1*4=4$
$-13*f(-13)''= 256$

Ambos cumple la condicion

$$
\begin{matrix}
x_{0}= 2 \\
x_{1}= 2-\left( -\frac{1}{4} \right) =2.25 \\
x_{2}= 2.25- \frac{0,484375}{8,0625} =2,189922481 \\
x_{3}= 2,189922481 - \frac{−0,03273559}{−6,983549673} =2,185234952 \\
x_{4}= 2,185234952 - \frac{0,000191058}{6,902097215} = 2,1898948 \\
x_{5}= 2,1898948 - \frac{0,032542285}{6,983067516} =2,18523463\\
x_{6}=2,18523463 - \frac{0,000188836}{6,902091633}=2,185207271 \\ \\


|x_{3}-x_{4}| = 2,18523463 - 2,185207271 = 0.000027359 < 0.0001
\end{matrix}
$$

$\lambda \approx 2.185207271$

$$\begin{pmatrix}
-0.1852 & -0.5 & 0\\
-0.5 & 1.1852 & -0.5 \\
0 & -0.5 & −1.5185
\end{pmatrix}
$$
$F_2 - 2.699784017F_1 \rightarrow F_2$  
$$\begin{pmatrix}
-0.1852 & -0.5 & 0\\
0 & 1,164692008 & -0.5 \\
0 & -0.5 & −1.5185
\end{pmatrix}
$$
$F_3+0.429298043F_2 \rightarrow F_3$
$$\begin{pmatrix}
-0.1852 & -0.5 & 0\\
0 & 1.164692008 & -0.5 \\
0 & 0 & −1.733149022
\end{pmatrix}
$$
$$
\begin{cases}
-0.1852x_1 -0.5x_2 = 0\\
1.164692008x_2 -0.5x_3=0
\end{cases}
$$
$$
\text{Autovalor: 2.185207271 y su vector asociado}\rightarrow
\begin{bmatrix}
0\\
0\\
0
\end{bmatrix}
$$

c) Aplique el método de las potencias para obtener el máximo autovalor y su vector propio correspondiente. Realice 04 iteraciones partiendo de (1,1,-0.5)T y muestre el error de λ y x, comparado con los exactos obtenidos en b).

$$\begin{bmatrix}
2 & -0,5& 0\\
-0,5 & 1 & -0,5\\
0 & 0,5 & \frac{2}{3}
\end{bmatrix} *
\begin{Bmatrix}
1\\
1\\
-0.5
\end{Bmatrix}
=
\begin{Bmatrix}\frac{3}{2}\\ \frac{3}{4}\\ \frac{1}{6}\end{Bmatrix} = 
\begin{pmatrix}\frac{18}{12}\\ \frac{9}{12}\\ \frac{2}{12}\end{pmatrix}=

\frac{9}{12} \begin{Bmatrix}2\\1\\\frac{2}{9}\end{Bmatrix}
$$
$$
\begin{pmatrix}
2& -0.5&0\\
-0.5&1&-0.5\\
0&0.5&2/3
\end{pmatrix}*
$$







