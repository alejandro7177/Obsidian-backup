Se tiene un conjunto de puntos, que se han obtenido en forma experimental midiendo diferentes densidades del sodio a diferentes temperaturas:

| Temperatura | 102      | 245      | 327      | 423      | 565      |
| ----------- | -------- | -------- | -------- | -------- | -------- |
| Densidad    | 0.564642 | 0.644218 | 0.717356 | 0.783327 | 0.853329 |
1. Aplique la fórmula de Lagrange para la temperatura igual a 275°
2. Aplique la fórmula de Interpolación parabólica progresiva para la temperatura igual a 275° y estime el error cometido

1.
$$
\begin{gather}
\frac{P(x)}{(275-102)(275-245)(275-327)(275-423)(275-565)}=\\
\frac{0.564642}{(275-102)(102-245)(102-327)(102-423)(102-565)}+\\
\frac{0.644218}{(275-245)(245-102)(245-327)(245-423)(245-565)}+\\
\frac{0.717356}{(275-327)(327-102)(327-245)(327-423)(327-565)}+\\
\frac{0.783327}{(275-423)(423-102)(423-245)(423-327)(423-565)}+\\
\frac{0.853329}{(275-565)(565-102)(565-245)(565-327)(565-423)}
\end{gather}
$$

$$\begin{gather}
\frac{P(x)}{(275-102)(275-245)(275-327)(275-423)(275-565)}=\\
\frac{282321}{4.13638E17}-\frac{322109}{1.00187E16}-\frac{322109}{1.00187E16}+\frac{7057}{1.03854E15}-\frac{853329}{1.45209E18}=\\
P(x) =(\frac{282321}{4.13638E17}-\frac{322109}{1.00187E16}-\frac{322109}{1.00187E16}+\frac{7057}{1.03854E15}-\frac{853329}{1.45209E18})*(-11583249600)
\end{gather}$$

2. 
