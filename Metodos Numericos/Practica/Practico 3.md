1. Supóngase que se ha diseñado un tanque esférico en un pequeño pueblo. El volumen del líquido que puede contener se calcula como
   $$V  =\pi h²\left(\frac{3r-h}{3}\right)$$
   donde V es el volumen en m³, h es la profundidad del agua en el tanque en metros y R el radio del tanque también en metros. Considerando R=3 m y V=30m³
- [x]  Evalúe cuántas y qué tipo de raíces puede tener esta ecuación.
- [x] Separe todas las raíces aplicando el **Método de tanteos**.
- [ ] Aproxime a qué profundidad debe llenarse el tanque de modo que contenga 30 m³ utilizando el Método de intervalo medio con E<0,001
- [ ] Ídem anterior, utilizando el **Método de interpolación lineal**.
- [ ] Obtenga conclusiones de la aplicación de ambos métodos de aproximación.

$$30 = \pi h²\left(\frac{3r-h}{3}\right)$$
$$30 = \frac{3r\pi h²}{3}-\frac{\pi h^3}{3}$$
$$30 = \frac{\cancel{3}r\pi h²}{\cancel{3}}-\frac{\pi h^3}{3}$$
$$30 = r\pi h²-\frac{\pi h^3}{3}$$
$$30 = \frac{3r\pi h²-\pi h³}{3}$$
$$90 = 3r\pi h^2-\pi h³$$
$$-\pi h³ + 9\pi h²-90 = 0$$
$$Descartes$$
$$\text{x negativo + + }-\rightarrow \text{1 raiz negativa} $$
$$\text{x positivo  } - +- \rightarrow \text{2 o 0 raices}$$
$$\text{Metodo de tanteo}$$
- Negativo
  $$
x_0 = 0 \rightarrow f(0)= -90
$$
$$x_1 = -1 \rightarrow f(-1) = −58,584$$
$$x_2 = -2 \rightarrow f(-2) = 48,2300$$
- Positivo
$$x_0 = 0 \rightarrow f(0)= -90$$
$$x_1 = 1 \rightarrow f(1)= −64,867$$
$$x_2 = 2 \rightarrow f(2)= −2,0354$$
$$x_3 = 3 \rightarrow f(3)= 79,6460$$
$$x_4 = 4 \rightarrow f(4)= 161,327$$
$$x_5 = 5 \rightarrow f(5)= 224,159$$
$$x_6 = 6 \rightarrow f(6)= 249,292$$
$$x_7 = 7 \rightarrow f(7)= 217,876$$
$$x_8 = 8 \rightarrow f(8)= 111,0619$$
$$x_9 = 9 \rightarrow f(9)= −90$$
#### Calculo de la cantidad de iteraciones para el metodo de tanteo

$$
n \geq \frac{log(b-a)- log(E)}{log(2)}
$$
$$
n \geq \frac{log(48,23-(-58,584))- log(0,001)}{log(2)}
$$
$$
n \geq \frac{log(106,814)- log(0,001)}{log(2)}
$$
$$
n \geq \frac{2,028628179-(-3)}{0,301029996}
$$
$$
n\geq \frac{5,028628179}{0,301029996}
$$
$$n \geq 16,704741208$$
$$n \geq 17$$
Metodo de tanteo para la raiz negativa
$$\frac{-2+(-1)}{2} =-1,5 \rightarrow f(−1,5)=−15,779873559 $$

$$\frac{-2+(-1,5)}{2} =−1,75 \rightarrow f(−1,75)=13,427120642 $$
$$\frac{-1,75+(-1,5)}{2} =−1,625 \rightarrow f(−1,625)=−1,857463928 $$
$$\frac{-1,75+(−1,625)}{2} =−1,6875 \rightarrow f(−1,6875)=5,612255519 $$
$$\frac{-1,6875+(−1,625)}{2} =−1,65625 \rightarrow f(−1,65625)=1,834540207 $$
$$\frac{−1,65625+(−1,625)}{2} =−1,640625 \rightarrow f(−1,640625)=−0,022139805 $$
$$\frac{−1,65625+(−1,640625)}{2} =−1,6484375 \rightarrow f(−1,6484375)=0,903526221 $$
$$\frac{−1,65625+(−1,6484375)}{2} =−1,65234375 \rightarrow f(−1,65234375)=1,368364157$$
$$\frac{−1,65625+(−1,6484375)}{2} =−1,65234375 \rightarrow f(−1,65234375)=1,368364157$$
$$\frac{−1,65234375+(−1,6484375)}{2} =−1,650390625 \rightarrow f(−1,650390625)=1,135777995$$
$$\frac{−1,650390625+(−1,6484375)}{2} =−1,649414063 \rightarrow f(−1,649414063)=1,019610378$$
$$\frac{−1,649414063+(−1,6484375)}{2} =−1,648925782 \rightarrow f(−1,648925782)=0,961557912$$
$$\frac{−1,648925782+(−1,6484375)}{2} =−1,648681641 \rightarrow f(−1,648681641)=0,932539455$$
$$\frac{−1,648681641+(−1,6484375)}{2} =−1,648559571 \rightarrow f(−1,648559571)=0,918032245$$
$$\frac{−1,648559571+(−1,6484375)}{2} =−1,648498535 \rightarrow f(−1,648498535)=0,91077901$$
$$\frac{−1,648498535+(−1,6484375)}{2} =−1,648468018 \rightarrow f(−1,648468018)=0,907152634$$
$$\frac{−1,648468018+(−1,6484375)}{2} =−1,648452759 \rightarrow f(−1,648452759)=0,905339417$$
$$\frac{−1,648452759+(−1,6484375)}{2} =−1,64844513 \rightarrow f(−1,64844513)=0,904432876$$
### Interpolación
$$x_3 = \frac{y_2 -y_1}{-y_1 x_2 -x_1(-y_1)}+x_1$$
$$
\begin{align*}
x_1 &= -58,584 \\
x_2 &= 48,23 \\
x_3 &=  
\end{align*}
$$

2. Un analista de mercado, que trabaja para un fabricante de dispositivos informáticos,
encuentra que, si la compañía produce y vende x impresoras al mes, su utilidad total (en
pesos) es:
$$
P(x)= 8x+0,3x²-0,0013x³-372
$$
¿Cuántas impresoras debe producir la compañía para alcanzar el punto de equilibrio (no
pierde ni gana)? Existen dos puntos.
1. Analice las condiciones de convergencia del Método de Newton Raphson en los
intervalos iniciales [24 ; 26] y [250 ; 252]

$$\begin{align*}
P'(x)&= -0,0039x²+0,6x +8 \\
P''(x)&= -0,0078x+0,6
\end{align*}
$$
$$\begin{align*}
P(x_2)&=8(26)+0,3(26)²-0,0013(26)³-372=15,9512< \\
P'(x_2)&= -0,0039(26)²+0,6(26) +8=20,9636 \neq 0 \\
P''(x_2)&= -0,0078(26)+0,6=0,3972\\
P(x_2)*P''(x_2)&= 15,9512 *0,3972 =6,33581664 > 0 
\end{align*}
$$
$$\begin{align*}
P(x_1)&=8(24)+0,3(24)²-0,0013(24)³-372=−25,1712 \\
P'(x_1)&= -0,0039(24)²+0,6(24) +8=20,1536 \neq 0 \\
P''(x_1)&= -0,0078(24)+0,6=0,4128\\
P(x_1)*P''(x_1)&= −25,1712*0,4128 =−10,39067136 > 0 
\end{align*}
$$
$$x_2\text{ cumple las condiciones de newton raphson }x_1 \text{ no}$$
$$\begin{align*}
P(x_3)&=8(250)+0,3(250)²-0,0013(250)³-372=65,5 \\
P'(x_3)&= -0,0039(250)²+0,6(250) +8=−85,75 \neq 0 [250,252] \epsilon \\
P''(x_3)&= -0,0078(250)+0,6=−1,35\\
P(x_3)*P''(x_3)&= 65,5 *−1,35 =−88,425 > 0
\end{align*}
$$
$$\begin{align*}
P(x_4)&=8(252)+0,3(252)²-0,0013(252)³-372=−108,7104 \\
P'(x_4)&= -0,0039(252)²+0,6(252) +8=−88,4656 \neq 0 [250,252] \epsilon \\
P''(x_4)&= -0,0078(252)+0,6=−1,3656\\
P(x_4)*P''(x_4)&= −108,7104 *−1,3656 =148,45492224 > 0 
\end{align*}
$$
$$x_4\text{ cumple las condiciones de newton raphson }x_3 \text{ no}$$
2. Newton Rawson
$$x_{n+1} =x_n - \frac{f(x_n)}{f'(x_n)}$$
$$x_{2.1} =26- \frac{15,9512}{20,9636} = 25,239100155 $$
$$E_1= |x_{2.1}-x_2|=|26-25,239100155|=0,760899845> 10^{-3}$$
$$x_{2.2}= 25,239100155 -$$





