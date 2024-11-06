Acotación de raíces

negativo positivo -> corta un numero impar de veces
positivo positivo -> corta un numero par de veces o ninguna

Método de tanteos (para separar la raíz "cantidad de veces que corta con el eje de las x")


$$
|f(x_i)|
$$
Practica

$$
f(x)= 2 x⁴ -6x² +7x-2
$$
para x positivo:  + - + -

- 3 cambios de signo -> 3 o 1 raíces positivas (porque puede tener 2 raíces complejas)

para x negativo + - - -

-  1 cambio de signo -> 1 raíz real negativa

$$
\Delta x = -0,5
$$
$$
	x_0 = 0 -> f(x_0) = 2 *0⁴ -6 * 0^2 + 7*0 -2 = -2
$$
$$
	x_1 = -0,5 -> f(x_1) = 2 *(-0,5)⁴ -6 * (-0,5)^2 + 7*(-0,5) -2 = -6,875
$$
$$
	x_2 = -1 -> f(x_1) = 2 *(-1)⁴ -6 * (-1)^2 + 7*(-1) -2 = -6,875
$$
$$
	x_3 = -1,5 -> f(x_3) = -18,875
$$
Formula
$$
n \geq \frac{log(b-a)- log(E)}{log(2)}
$$
$$
f(x)) 2 x⁴ -6x² +7x-2 en (-2.5,-2)  \epsilon 10^{-3}
$$
$$
n \geq \frac{log(-2 -(-2,5))-log(10^{-3})}{log(2)}
$$
$$
n \ge \frac{log(0.5)- log(0.001)}{log(2)}
$$

$$
n \ge \frac{log(0.5) - (-3)}{log(2)} \approx 8,96578428
$$

Raíz 
$$
f(x) =2 x⁴ -6x² +7x-2
$$
$$
	x_1 =\frac{-2.5 +(-2)}{2} = -2.25 \rightarrow f(-2.25) = 3,13328
$$
$$
x_2 = \frac{-2.25 +(-2)}{2} = -2,125 \rightarrow f(-2,125)  = -3.18
$$
$$
x_3 = \frac{-2.125 +(-2,25)}{2} = -2,1875 \rightarrow f(-0.0875)  = -2,6583
$$

Otro ejercicio
$$
V = \pi h²\left(\frac{3R-h}{3}\right)
$$
$$
30 = -\frac{\pi h³}{3} + \pi h² r
$$
$$
30 = -\frac{\pi h³}{3}+\frac{9\pi h²}{3}
$$
$$
90 = -\pi  h³ + 9\pi h²
$$
$$
-\pi h³ + 9\pi h²-90 = 0
$$
$$Descartes$$
$$\text{x negativo + + }-\rightarrow \text{1 raiz negativa} $$
$$\text{x positivo  } - +- \rightarrow \text{2 o 0 raices}$$

Método de tanteos
$$
x_0 = 0 \rightarrow f(0)= -90
$$
$$x_1 = -1 \rightarrow f(-1) = −58,584$$
$$x_2 = -2 \rightarrow f(-2) = 48,2300$$
Positivo

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
### Metodo de interpolacion
![[Pasted image 20240828202144.png]]
se crea una paralela entre [a,b] y se regula el intervalo en donde corta la recta siempre verificando que los signos sean distintos
La ecuacion de la recta que pasa por los puntos P1 ; P2 es:
$$y - y_1 = \frac{y_2 -y_1}{x_2-x_1}(x-x_1)$$
$$- y_1 = \frac{y_2 -y_1}{x_2-x_1}(x_3-x_1)$$
Despeje
$$\frac{- y_1}{x_3-x_1} = \frac{y_2 -y_1}{x_2-x_1}$$
$$x_3-x_1 = \frac{y_2 -y_1}{x_2-x_1}*\frac{1}{-y_1}$$
$$x_3 = \frac{y_2 -y_1}{x_2-x_1}*\frac{1}{-y_1}+x_1$$
$$x_3 = \frac{y_2 -y_1}{-y_1 x_2 -x_1(-y_1)}+x_1$$

$$
\text{correcto: }x_3 = \frac{x_1y_2 -x_2y_1}{y_2-y1}
$$


Metodo de newton-rawson

Si x es una primera aproximacion al valor de una raiz, la que puede ser directamente

$$
\tan\alpha = f'(x_n) = \frac{f(x_n)}{x_n - x_{n+1}}
$$
$$
x_{n+1} =x_n - \frac{f(x_n)}{f'(x_n)}
$$
observaciones de fourier
$$I) f(a)+f(b)<0$$
$$II)f'(x) \text{ distinta de 0 para todo x comprendida en (a;b)}$$
$$III) f(x_0)*f''(x_0) >0$$

sirve para q la tangete no este fuera del intevalo ab

### Practica

 $$
f(x)= 2 x⁴ -6x² +7x-2
$$
$$
x_{i+1}= \frac{x_{i_1}*f(x_1)-x_1 *f(x_{i-1})}{f(x_i)-f(x_{i-1})}
$$

$$
x_{n+1}= x_n -\frac{f(x_n)}{f'(x_n)}
$$
$$x_n = -2,5$$
$$x_m = -2$$
$$f'(x_m)= 8x³-12x+7=8(-2)³-12(-2)+7= -64+24+7=-33$$
$$f'(x_n)=8x³-12x+7=8(-2,5)³-12(-2,5)+7= -125+30+7=-88$$
$$f''(x)= 24x²+12$$
$$f''(x_n)= 24(-2,5)²+12=138$$
$$f''(x_m)= 24(-2)²+12=84$$
$$f(x_m)=-8$$

$$
x_{n+1}= x_n -\frac{f(x_n)}{f'(x_n)}
$$
$$
x_{n+1}= -2 -\frac{-8}{-33}= -1,75
$$
$$f(x_4)=f(-1,75)= 2 (-1,75)⁴ -6(-1,75)² +7(-1,75)-2=−13,8671875$$
$$
[-2.5,-1.75]
$$
$$\text{Error: }|-2-(-1,75)|=0,25> E$$
$$f'(x_4)=8(-1,75)³-12(-1,75)+7=-42.875+21=−21,875$$
$$f''(x_4)=12(-1,75)^2+24=36,75+24=60,75$$

$$x_{n+1}=-1,75-\frac{-13,8671}{-21,875}$$
$$x_5= -2,3839245$$
$$f(x_5)=f(-2,3839245)= 2 (-2,3839245)⁴ -6(-2,3839245)² +7(-2,3839245)-2=11,809113154$$

$$[-2,3839245,-1,75]$$
$$\text{Error: }-2,3839245-(-1,75)= −0,6339245> E$$
$$f'(x_5)=f(-2,3839245)=8(-2,3839245)³-12(-2,3839245)+7=−72,777480736$$

$$f''(x_5)=12(-2,3839245)^2+24=92,19715226$$
## Metodo de iteración
$$f(x)= e^x-x²-5$$
$$f_1(x)=e^x$$
$$f_2(x)=x²+5$$
$$|f_1''(x_0)|> |f_2''(x_0)|$$
$$
x_0=2,5 \rightarrow f_2(x_0) = f_1(x_1) \text{ se despeja }x_1
$$
$$2,5²+5=e^{x_1}$$
Aiden
$$
r \approx x_{x+1}-\frac{(x_{x-1}-x_n)²}{x_{n+1}-2x_n+x_{n-1}}
$$


