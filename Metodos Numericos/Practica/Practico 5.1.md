Interpolación en intervalos regularmente espaciados. Dada la siguiente tabla de valores:

|  x  |    15    | 25       | 35       | 45       | 55       | 65       |
| :-: | :------: | -------- | -------- | -------- | -------- | -------- |
|  y  | 0.965926 | 0.906308 | 0.819152 | 0.707107 | 0.573576 | 0.422618 |
1. Utilice la fórmula de Newton-Gregory Ascendente para hallar el valor de $x = 17$
2. Aplique la fórmula de Newton-Gregory Descendente y hallar el valor de $x = 60$
3. Determine el valor de x que corresponde a $y = 0.90728517$ usando Interpolación Inversa - Lineal y Cuadrática

1.

|  x  |    y     | $\Delta y$ | $\Delta²y$ | $\Delta³ y$ | $\Delta⁴ y$ | $\Delta⁵ y$ |
| :-: | :------: | ---------- | ---------- | ----------- | ----------- | ----------- |
| 15  | 0.965926 | -0.059618  | -0.027538  | 0.002649    | 0.267816    | -0.801284   |
| 25  | 0.906308 | -0.087156  | -0.024889  | 0.270465    | -0.533468   |             |
| 35  | 0.819152 | -0.112045  | 0.245576   | -0.263003   |             |             |
| 45  | 0.707107 | -0.133531  | -0.017427  |             |             |             |
| 55  | 0.573576 | -0.150958  |            |             |             |             |
| 65  | 0.422618 |            |            |             |             |             |
$$
P_n(x) = y_0 + \Delta y_0u + \frac{\Delta² y_0u}{2!}u(u-1)+\frac{\Delta³ y_0u}{3!}u(u-1)(u-2)+\frac{\Delta⁴ y_0u}{4!}u(u-1)(u-2)(u-3)
$$
$$u = \frac{17 - 15}{10} = -\frac{1}{5}$$
$$\begin{gather}
P(17)= 0.965926 + -0.059618u + \frac{-0.027538u}{2!}u(u-1)\\+\frac{0.002649u}{3!}u(u-1)(u-2)+\frac{0.267816u}{4!}u(u-1)(u-2)(u-3) \approx 0.95093\\
P(17) \approx \boxed{0.95093}
\end{gather}$$

2.
$$
P_n(x) = y_n + \Delta y_nu + \frac{\Delta² y_nu}{2!}u(u-1)+\frac{\Delta³ y_nu}{3!}u(u-1)(u-2)+\frac{\Delta⁴ y_nu}{4!}u(u-1)(u-2)(u-3)
$$
$$u = \frac{60-65}{10}=-\frac{5}{10}= -\frac{1}{2}$$

$$
\begin{gather}
P(60)=0.422618+(-0.150958u)+\left(-\frac{0.017427u}{2!}\right)u(u+1)+\left(-\frac{0.263003u}{3!}\right)u(u+1)(u+2)\\
+\left(-\frac{0.533468u}{4!}\right)u(u+1)(u+2)(u+3) \approx \boxed{0.48878}
\end{gather}
$$
3.

$$
P(x) = y_0 + \frac{\Delta y_0}{h}*(x-x_0)
$$
$$\begin{gather}
P(x)=0.965926-\frac{0.059618}{10}*(x-15)\\
0.90728517 = 0.965926 -\frac{0.059618}{10}*(x-15)\\
0.90728517 = 0.965926 - 0.0059618 *(x-15)\\
0.90728517-0.965926 = - 0.0059618 *(x-15)\\
-0.05864083 =- 0.0059618 *(x-15)\\
\frac{0.05864083}{0.0059618} =x-15 \\
9.83609480358 = x-15\\
9.83609480358 +15=x\\
\boxed{x=24.83609480358}
\end{gather} $$