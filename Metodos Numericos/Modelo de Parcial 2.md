1. Hallar el polinomio caracteristico del siguiente sistema de ecuaciones homogeneo con el Método Fadeev-Leverrier 
$$\begin{cases}
(4-\lambda)x_1+x_3=0\\
x_1+(1-\lambda)x_2+2x_3=0\\
x_1+(1-\lambda)x_3=0
\end{cases}$$

$$
B_1=\begin{pmatrix}
4&0&1\\
1&1&2\\
1&0&1
\end{pmatrix}
, b_1= (4+1+1)
=6$$

$$B_2 = A*(B_1-b_1I)$$

$$
B_2 = \begin{pmatrix}
4&0&1\\
1&1&2\\
1&0&1
\end{pmatrix}*
\left(
\begin{pmatrix}
4&0&1\\
1&1&2\\
1&0&1
\end{pmatrix}
-
\begin{pmatrix}
6&0&0\\
0&6&0\\
0&0&6
\end{pmatrix}
\right)
$$
$$
B_2 = 
\begin{pmatrix}
4&0&1\\
1&1&2\\
1&0&1
\end{pmatrix}*
\begin{pmatrix}
-2&0&1\\
1&-5&2\\
1&0&-5
\end{pmatrix}=
\begin{pmatrix}
-7&0&-1\\
1&-5&-7\\
-1&0&-4
\end{pmatrix}
$$

$$b_2= \frac{1}{2}(-7-5-4)=-8$$

$$
B_3 = \begin{pmatrix}
4&0&1\\
1&1&2\\
1&0&1
\end{pmatrix}*
\left(
\begin{pmatrix}
-7&0&-1\\
1&-5&-7\\
-1&0&-4
\end{pmatrix}
-
\begin{pmatrix}
-8&0&0\\
0&-8&0\\
0&0&-8
\end{pmatrix}
\right)
$$

$$
B_3 = \begin{pmatrix}
4&0&1\\
1&1&2\\
1&0&1
\end{pmatrix}*
\begin{pmatrix}
1&0&-1\\
1&3&-7\\
-1&0&4
\end{pmatrix}=
\begin{pmatrix}
3&0&0\\
0&3&0\\
0&0&3
\end{pmatrix}
$$

$$b_3= \frac{1}{3}(3+3+3) =3$$

Polinomio Caracteristico $-\lambda³+6\lambda²-8\lambda-3$

$$(\lambda-3)(-\lambda²+3\lambda+1)=0$$
$$\begin{gather}
\lambda = 3\\
\lambda = \frac{3+\sqrt{13}}{2}\\
\lambda = \frac{3-\sqrt{13}}{2}
\end{gather}$$
2. Dado la siguiente ecuacion diferencial $y' = 1+ \frac{y}{x}$ con  $y(1)=2$  , $h=0.5$

Aplicar el Método Modificado de Euler para hallar $y(2)$, corrigiendo 2 veces los resultados obtenidos. 

$$
\begin{gather}
x_0= 1 \ \ \ \ y_0 = 2 \ \ \ \ h=0.5 \ \ \ \ y_1'=3 \\
x_1=1.5\\
P(y_1)= 2 +3*0.5=3.5\\
P(y_1')= f(x_1,P(y_1))= 1+\frac{3.5}{1.5}= \frac{10}{3}\\
C(y_1)= 2+\frac{3+\frac{10}{3}}{2}*0.5=\frac{43}{12}\\
C(y_1')=f(x_1,C(y_1)) = 1+\frac{\frac{43}{12}}{1.5} = \frac{61}{18}\\
C¹(y_1)=2+\frac{3+\frac{61}{18}}{2}*0.5=\frac{259}{72}\approx 3.597222\\
C¹(y_1')=f(x_1,C¹(y_1))=1+\frac{\frac{259}{72}}{1.5}=\frac{367}{108}\approx 3.398148
\end{gather}
$$
$$
\begin{gather}
x_2= 2\\
P(y_2)=\frac{259}{72}+\frac{367}{108}*0.5=\frac{143}{27}=5.296296\\
P(y_2')= f(x_2,P(y_2))=1+\frac{5.296296}{2}=3.648148\\
C(y_2)= 3.587222+\frac{3.398148-3.648148}{2}*0.5=3.524722\\
C(y_2')= f(x_2,C(y_2))= 1+\frac{3.524722}{2}=2.762361\\
C¹(y_2)=3.587222+\frac{3.398148-2.762361}{2}*0.5=3.74616875\\
C¹(y_2')= f(x_2,C¹(y_2))= 1+\frac{3.74616875}{2}=2.873084\\
\end{gather}
$$

Runge kutta 

$$
\begin{gather}
y_1 =3.597222 \ \ \ \ x_1=1.5\\
k_1= 0.5 * \left(1+\frac{3.597222}{1.5}\right)=1.699074\\
k_2 = 0.5*\left(1+\frac{4.446757}{1.75}\right)=1.770502\\
k_3 = 0.5\left(1+\frac{4.482473}{1.75}\right)=1.780706\\
k_4 = 0.5\left(1+\frac{5.377928}{2}\right) = 1.844482\\\\

y_2 = 3.597222+ \left(\frac{1}{6}(1.699074+2(1.770502)+2(1.780706)+1.844482)\right)\\
\boxed{y_2 = 5.371550}
\end{gather}
$$
$$\begin{gather}
Y(2)= 5.386294\\
E = \frac{5.386294-5.371550}{5.386294}*100=0.00273731809*100\\
\boxed{E=0.273731\%}
\end{gather}$$
