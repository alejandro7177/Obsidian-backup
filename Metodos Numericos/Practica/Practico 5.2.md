Cada 10 años se levanta un censo de población en Estados Unidos. En la siguiente tabla se incluyen datos de la población, en miles de habitantes, de 1940 a 1990.

| Año                              | 1940   | 1950   | 1960   | 1970   | 1980   | 1990   |
| -------------------------------- | ------ | ------ | ------ | ------ | ------ | ------ |
| Población en miles de habitantes | 132165 | 151326 | 179323 | 203302 | 226542 | 249633 |
1. Use la interpolación de Lagrange para aproximar la población en el año 1965
2. La población de 1965 fue aproximadamente de 189.703.000 habitantes. ¿Qué exactitud, a su juicio, tienen sus cifras correspondientes al año 1965

$$
\begin{gather}
\frac{P(x)}{(1965-1940)(1965-1950)(1965-1960)(1965-1970)(1965-1980)(1965-1990)}=\\
\frac{123165}{(x-1940)(1940-1950)(1940-1960)(1940-1970)(1940-1980)(1940-1990)}\\
+ \frac{151326}{(x-1950)(1950-1940)(1950-1960)(1950-1970)(1950-1980)(1950-1990)}\\
+ \frac{179323}{(x-1960)(1960-1940)(1960-1950)(1960-1970)(1960-1980)(1960-1990)}\\
+ \frac{203302}{(x-1970)(1970-1940)(1970-1950)(1970-1960)(1970-1980)(1970-1990)}\\
+ \frac{226542}{(x-1980)(1980-1940)(1980-1950)(1980-1960)(1980-1970)(1980-1990)}\\
+ \frac{249633}{(x-1990)(1990-1940)(1990-1950)(1990-1960)(1990-1970)(1990-1980)}
\end{gather}
$$

$$\begin{gather}
\frac{P(x)}{(1965-1940)(1965-1950)(1965-1960)(1965-1970)(1965-1980)(1965-1990)}=\\
-0.00041055+0.0042035-0.02988716667-0.03388366667+0.00629283333+-0.00083211
\end{gather}$$
$$\begin{gather}
-\frac{P(x)}{3515625} = -0.05451716001 \\
P(x) = -0.05451716001*(-3515625)\\
P(x)=191661.89066015626
\end{gather}$$

Error: $\frac{|189703-191661.89066015626|}{189703}=\frac{1958.89}{189703}=0.01032608868$
Error Relativo 1.03%


