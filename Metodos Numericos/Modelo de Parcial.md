1. Dado el siguiente sistema de equaciones homogéneos:
   $$
   \begin{cases}
   (3-\lambda)x_1+5x_2+x_3 = 0\\
   5x_1+(2-\lambda)x_2 = 0\\
   x_1+(1+\lambda)x_3 = 0
   \end{cases}
   $$
$$\begin{pmatrix}
3&5&1\\
5&2&0\\
1&0&1
\end{pmatrix}*
\begin{Bmatrix}1\\1\\1\end{Bmatrix} =
\begin{Bmatrix}9\\7\\2\end{Bmatrix}=
9\begin{Bmatrix}1\\\frac{7}{9}\\\frac{2}{9}\end{Bmatrix}
$$
$$\begin{pmatrix}
3&5&1\\
5&2&0\\
1&0&1
\end{pmatrix}*
\begin{pmatrix}1\\\frac{7}{9}\\\frac{2}{9}\end{pmatrix}=
\begin{Bmatrix}
\frac{64}{9}\\\frac{59}{9}\\\frac{11}{9}
\end{Bmatrix}=
\frac{64}{9}\begin{Bmatrix}
1\\\frac{59}{64}\\\frac{11}{64}
\end{Bmatrix}
$$
$$
\begin{pmatrix}
3&5&1\\
5&2&0\\
1&0&1
\end{pmatrix}*
\begin{pmatrix}1\\\frac{59}{64}\\\frac{11}{64}\end{pmatrix}=
\begin{Bmatrix}\frac{249}{32}\\\frac{219}{32}\\\frac{75}{64}\end{Bmatrix}=
\frac{249}{32}\begin{Bmatrix}1\\ \frac{219}{249} \\ \frac{25}{166}\end{Bmatrix}
$$
Autovalor
$$
\begin{Bmatrix}1\\\frac{219}{249}\\\frac{25}{166}\end{Bmatrix}
$$
$$
E = \left|\frac{7.78125- 7.11111}{7.78125}\right|*100= 8.612\%
$$

 2. Dado la ecuación diferencial $y'=\frac{x}{y+1}$ con $y(0)=0$ ,  $h=0.25$ 
   2.1. Aplicar el Método Modificado de Euler para obtener los valores necesarios para le item b) corrigiendo una vez los resultados obtenidos
 $$
 \begin{gather}
 x_0=0\ \ \ \ y_0=0\ \ \ \ h=0.25\ \ \ \ y_0'=0\\
 x_1=0+0.25=0.25\\
 P(y_1)=0+0*0.25 = 0\\
 P(y_1')=f(x_1, P(y_1))= \frac{0.25}{0+1}=0.25\\
 C(y_1)= 0+\left(\frac{0+0.25}{2}\right)=0.125\\
 C(y_1')=f(x_1,C(y_1))= \frac{0.25}{0.125+1}=\frac{2}{9}
 \end{gather}
 $$
 $$
 \begin{gather}
  x_2 = 0.5\\
 P(y_2) = 0+ \frac{2}{9}*0.25= \frac{1}{18}\\
 P(y_2')=f(x_2, P(y_2))=\frac{0.5}{\frac{19}{18}}=\frac{9}{19}\\
 C(y_2)=0.125+\left[\frac{\frac{2}{9}+\frac{9}{19}}{2}\right]=0.17763\\
 C(y_2')=f(x_2,C(y_2))=\frac{0.5}{0.17763+1}=0.244581
 \end{gather}
 $$
 $$
 \begin{gather}
 x_3 = 0.75\\
 P(y_3)= 0.17763+0.244581*0.75 = 0.361065\\
 P(y_3')= f(x_3, P(y_3))= \frac{0.75}{0.3610165+1}=0.5510587\\
 C(y_3)= 0.17763+\frac{0.244581+0.5510587}{2}=0.5754498\\
 C(y_3')=f(x_3,C(y_3))= \frac{0.75}{0.5754498+1}=0.476054498
 \end{gather}
 $$

   2.2. Con el Método de Milne, haya y(1) corrigiendo 2 veces el resultados
   $$
   \begin{gather}
   P(y(1)) = 0+ \frac{4}{12}\left(2(0.476054)-0.244581+2(0.222222)\right)=0.3839903\\
   C(y(1))=0.17763+\frac{1}{12}(0.244581+4(0.476054)+0.3839903)=0.388695\\
  \boxed{C¹(y(1))= 0.17763+\frac{1}{12}(0.244581+4(0.476054)+0.388695) =0.389087}
   \end{gather}
   $$
   2.3. Calcula el error % cometido en b) sabiendo exacta está dada por: $y = \sqrt{x²+1}-1$  

$$
E = \frac{0.414213-0.389087}{0.414213}*100 = 0.056314*100=5.6314\% 
$$
2. Los siguiente datos definen la concentración de oxígeno disuelto a nivel del mar para agua dulce como función de la temperatura

|  T, C°  |   0    |   8    |    16     |  24   |  32   |  40   |
| :-----: | :----: | :----: | :-------: | :---: | :---: | :---: |
| O, mg/L | 14.621 | 11.843 | 9.8664736 | 8.418 | 7.305 | 6.413 |
3.1. Intepolar para x=16, utilizando la formula mas conveniente
Langrange
$$
\begin{gather}
\frac{P(x)}{(16)(16-8)(16-24)(16-32)(16-40)} = \frac{14.621}{(16-0)(0-8)(0-24)(0-32)(0-40)}+\\\frac{11.843}{(16-8)(8)(8-24)(8-32)(8-40)}+\frac{8.418}{(16-24)(24)(24-8)(24-32)(24-40)}+\\
\frac{7.305}{(16-32)(32)(32-8)(32-24)(32-40)}+\frac{6.413}{(16-40)(40)(40-8)(40-24)(40-32)}
\\\\
\frac{P(x)}{-393216}=\frac{14.621}{3932160} -\frac{11.843}{786432}-\frac{8.418}{393216}+\frac{7.305}{786432}-\frac{6.413}{3932160}\\\\\\

\frac{P(x)}{-393216}= 0.0000037183-0.0000150591-0.000021408+0.0000092-0.000001630\\\\
P(x)= -0.0000250917*(-393216)\\
\boxed{P(x)=9.866473636}
\end{gather}
$$
3.2
$$
\begin{gather}
P(x)= y_0+\frac{\Delta y_0}{h}(x-x_0)\\
13 = 14.621-\frac{2.778}{8}(x-0)\\
13 = 14.621 - 0.34725x\\
13-14.621 = -0.34725x\\
-1.621 = -0.34725x\\
\frac{1.621}{0.34725}=x\\
\boxed{4.66810 = x}
\end{gather}
$$
3.3
$$
\begin{gather}
A_1 = 3(14.621+3*11.843+3*9.8664736+8.418)\approx 264.50226\\
A_2 = \frac{8}{3}((8.418-6.413)+4(7.305))\approx 83.266666\\
A = A_1+A_2 = 264.50226+83.266666 = \boxed{347.768926}
\end{gather}
$$
