# Derivacion  númerica

formula avanzada
$$\begin{matrix}
f(x) f(x+h) \\
f(x-h) f(x) \\
f(x-h) f(x) f(x+h)\\
\end{matrix}
$$


| $$h$$       | $$f(x+h)$$ | $$f(x+h)-f(x)$$ | $$f(x)$$ | $$error$$ |
| ----------- | ---------- | --------------- | -------- | --------- |
| 1e-01       | 3,004166   |                 |          |           |
| 1e-02       |            |                 |          |           |
| 1e-03       |            |                 |          |           |
| 1e-04       |            |                 |          |           |
| 1e-05       |            |                 |          |           |
| 1e-06       |            |                 |          |           |
| 1e-07       |            |                 |          |           |
| _**1e-08**_ |            |                 |          |           |
| 1e-09       |            |                 |          |           |

Analisis del error

serie de taylor 

$$f(x+h) = $$

# Derivacion mediante Formula de Intepolacion

$$hf(x)= f(x_0 + hu)= f(x_0)+ \Delta f(x_0)u +\Delta² f(x_0) \frac{u(u-1)}{2!}+ \Delta³f(x_0)\frac{u(u-1)(u-2)}{3!}+... $$
$$
hf'(x_0+hu) = \Delta f(x_0)+ \frac{\Delta² f(x_0)}{2!} * (2u-1)+\frac{\Delta³ f(x_0)}{3!}*(3u²-6u+2)+\frac{\Delta³ f(x_0)}{4!}*(4u³-18u²+22u-6)$$
Segunda derivada
$$h²f(x_0+hu) = \Delta²f(x_0)+\Delta³f(x_0)(u-1)+\frac{\Delta⁴f(x_0)}{4!}(12u²-36u-22)+...$$
$$hf(x)= f(x_0 + hu)= f(x_0)+ \nabla f(x_0)u +\nabla² f(x_0) \frac{u(u-1)}{2!}+ \nabla³f(x_0)\frac{u(u-1)(u-2)}{3!}+... $$

# Practico

| x   | $$y$$       | $$\Delta y$$ | $$\Delta^2 y$$ | $$\Delta³ y$$ | $$\Delta⁴ y$$ | $$\Delta⁵ y$$ |
| --- | ----------- | ------------ | -------------- | ------------- | ------------- | ------------- |
| 12  | 0,96262<br> | −0,01544     | −0,00066       | 0,00789       | −0,01665      | 0,02704       |
| 13  | 0,94718     | −0,0161      | 0,00723        | −0,00876      | 0,01039       |               |
| 14  | 0,93108     | -0,00887     | −0,00153       | 0,00163       |               |               |
| 15  | 0,92221     | −0,0104      | 0,0001         |               |               |               |
| 16  | 0,91181     | −0,0103      |                |               |               |               |
| 17  | 0,90151     |              |                |               |               |               |

$$\begin{matrix}
f'(12)= \Delta f(12) -\frac{1}{2}\Delta²f(12)+\frac{1}{3}\Delta³f(12)-\frac{1}{4}\Delta⁴f(12)+K  \\
f'(12)= -0,01544 -\frac{1}{2}(-0,00066)+\frac{1}{3}(0,00789)-\frac{1}{4}(−0,01665)\\
f'(12)= -\frac{3327}{4} = -831,75
\end{matrix}
$$
$$\begin{matrix}
f'(12,4)= \\
u = \frac{x-x_0}{h} = \frac{12,4-12}{1}= 0,4
\end{matrix}
$$
# Integracion numerica
simson impar
trapecio 2
3/8 simpon 
$$E = x_0 +x_n$$
$$I = \text{suma de las ordenadas (x) que tengan subindices inpares}$$
$$P = \text{suma de las ordenadas (x) que tengan subindices pares} $$

