### FÓRMULA FUNDAMENTAL DEL CÁLCULO DE ERRORES

1. Hallar los errores absolutos y relativos que se cometerán al calcular el peso de una
esfera, trabajando con aritmética por truncamiento a 3 dígitos y sabiendo que 
$$
\begin{align*}
P_c &= 11.3g/cm³ \qquad P=P_c * V \\
r &= 4,37cm  \qquad V = \frac{4}{3}*\pi*r³ \\
\pi &=3,14159 
\end{align*}
$$
$$\text{Cota de errores absolutos por truncamiento }10^{-K}$$
$$
P = P_c*\frac{4}{3}*\pi *r³
$$ 
$$
P = 11,3 * 4/3*3,14159*4,37³ = 3950,1264
$$
$$
\Delta P(\tilde{P_c},\tilde{\pi},\tilde{r}) =
\left|\frac{\partial f}{\partial P_c} \right| \Delta P_c +
\left|\frac{\partial f}{\partial \pi} \right| \Delta \pi +
\left|\frac{\partial f}{\partial r} \right| \Delta r
$$
$$
\left|\frac{\partial (P_c*\frac{4}{3}*\pi *r³)}{\partial P_c} \right| \Delta P_c +
\left|\frac{\partial (P_c*\frac{4}{3}*\pi *r³)}{\partial \pi} \right| \Delta \pi +
\left|\frac{\partial (P_c*\frac{4}{3}*\pi *r³)}{\partial r} \right| \Delta r =
$$
$$
\left|\frac{4\pi r^3}{3}\right|\Delta P_c + |4P_c\pi r²| \Delta \pi +
\left|\frac{4P_c r³}{3} \right|\Delta r =
$$
$$\text{No se si distribui el error}$$
$$
343,568 *0,001 + 2712,016 *0,001 + 1257,365 *0,001 = 4,312949
$$
$$\text{Error Absoluto } \Delta P = 4,312949 $$
$$\text{Error Relativo: }\frac{\Delta P}{P} = \frac{4.312949}{3950.1264} \approx 0,00109185 \approx 1,09185\%$$

$$
\begin{align*}
&3950,1264 \pm 4,312949& \\
&Y_{min}=3945,813451& \\
&Y_{max}=3954,439349&
\end{align*}
$$

2. ¿Con qué precisión deberán ser tratadas la masa de un objeto que cae al vacío y la
fuerza que actúa sobre el mismo para que la aceleración a pueda obtenerse con un error
relativo menor que una milésima? Considerar los valores truncados en la tercera cifra
decimal.
$$
\begin{align*}
M =0.755 kg \\
F =7.595Kg*m/s²\\
\text{Formula a utilizar: } a =F/M
\end{align*}
$$
$$
\Delta a \geq \left|\frac{\partial a}{\partial F} \right|\Delta F+ \left|\frac{\partial a}{\partial M}\right|\Delta M 
$$
$$
\frac{\Delta a}{\frac{F}{M}} \geq \frac{\left|\frac{\partial a}{\partial F}\right|\Delta F }{\frac{F}{M}}+ \frac{\left|\frac{\partial a}{\partial M}\right|\Delta M}{\frac{F}{M}} 
$$
$$
\frac{\Delta a}{\frac{F}{M}} \geq \frac{\left|\frac{\partial (F/M)}{\partial F}\right|\Delta F }{\frac{F}{M}}+ \frac{\left|\frac{\partial (F/M)}{\partial M}\right|\Delta M}{\frac{F}{M}} 
$$
$$
\frac{\Delta a}{\frac{F}{M}} \geq 
\frac{
\frac{\partial (F/M)}{\partial F}\Delta F }{\frac{F}{M}}+ 
\frac{
\frac{\partial (F/M)}{\partial M}\Delta M}{\frac{F}{M}} 
$$
$$
\frac{\Delta a}{\frac{F}{M}} \geq 
\frac{
\frac{1}{M}\Delta F }{\frac{F}{M}}+ 
\frac{
-\frac{F}{M²}\Delta M}{\frac{F}{M}} 
$$
$$
\frac{\Delta a}{\frac{F}{M}} \geq 
\frac{
\Delta F}{F}-
\frac{MF}{M²F}\Delta M 
$$
$$
\frac{\Delta a}{\frac{F}{M}} \geq 
\frac{
\Delta F}{F}-
\frac{\Delta M}{M} 
$$
$$\text{Distribuir el error de 0,001}$$
$$
\begin{align*}
\frac{0,001}{2} &\geq \frac{\Delta F}{F}\\
\frac{0,001}{2} &\geq \frac{\Delta M}{M}
\end{align*}
$$
$$
\begin{align*}
0,0005*F &\geq \Delta F\\
0,0005*M &\geq \Delta M 
\end{align*}
$$
$$\text{resultados}$$
$$
\begin{align*}
3,7975*10^{-3} &\geq \Delta F\\
3,775*10^{-4} &\geq \Delta M 
\end{align*}
$$



