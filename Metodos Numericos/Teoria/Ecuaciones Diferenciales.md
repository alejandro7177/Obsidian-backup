ecuacion diferencial de 2do orden $y''+y=0$ 
$F(x,y,y',y'',\dots,y^n)=0$

Metodo Euler
$y'=f(x;y)$

$y'=f(x;y) =f[x;y(x)]=F(x)$

$y'_{0} = f(x_{0},y_{0})$

$\int_{x_{0}}^{x_{1}}y'dx \approx A_{1}$

$C(y_{1})= y_{0}+\frac{y_{0}'+P(y_{1'})}{2} h$

$y_{0}=16$

$$\begin{matrix}
y'= \frac{6x²}{y} \\
y_{0}=16 \\
x_{0}=5 \\
h=0.1 \\
y'=\frac{6*4²}{16}=6 \\
x_{1}=0.4+0.1=0.5 \\
y_{1}=y_{0}+y_{0}'*h = 16+6*0.1= 16.6 \\
y_{1}'=F(x_{1},y_{1})= \frac{6*4.1²}{16,6}=6.0759 \\
x_{2}= 4.1+0.1=4.2 \\
y_{2}=16.6+6.0759 =17.20759 \\
y_{2}'=\frac{6+4.2²}{17.20759}=6.150774 \\
x_{3}=4.2+0.1=4.3 \\ \\
y_{3}=17.20759+6.150774*0.1=17,82266\\
y_{3}'= \frac{6+4.3²}{17,82266}= \frac{24.49}{17,82266} =1,374093429
\end{matrix}$$

| i   | $x_{i}$ | $y_{i}$  | $y_{i}'$ |
| --- | ------- | -------- | -------- |
| 0   | 4       | 16       | 6        |
| 1   | 4.1     | 16.6     | 6.0759   |
| 2   | 4.2     | 17.20759 | 6.150774 |
| 3   | 4.3     | 17.82266 | 6.2246   |
| 4   | 4.4     | 18.4451  |          |
