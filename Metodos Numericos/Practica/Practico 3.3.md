Un silo para granos está formado por una sección principal cilíndrica y un techo semiesférico. Si el volumen total del silo incluyendo la parte dentro de la sección del techo es de 15000 pies³ y la parte cilíndrica es de 30 pies de altura, ¿cuál es el radio del silo?
1. Modelice la situación problemática.
2. Aproximar el radio del silo, aplicando el Método de Interpolación Lineal considerando el intervalo inicial \[10; 15]
3. Aproximar el radio del silo, aplicando el Método de Newton Raphson considerando el intervalo inicial \[10; 15].
4. Comparando la aplicación de ambos métodos, elaborar conclusiones respecto a la velocidad de convergencia.

$$
\begin{align}
\pi r²h+ \frac{2\pi r^3}{3}=15000 \\
\frac{3\pi r²h}{3}+\frac{2\pi r^3}{3}=15000\\
\frac{3\pi r²h+2\pi r^3}{3} = 15000 \\
3\pi r²h+2\pi r^3 =45000\\
2\pi r^3+90\pi r² -45000 = 0 \\
\end{align}
$$
$$
\begin{align}
\pi r²h+ \frac{2}{3}\pi r^3=15000 \\
\pi r²(30+ \frac{2}{3}r)=15000
\end{align}
$$
$$
\begin{align}
x_1 = 10 \\
x_2 = 15 \\
y_1 = −10442,480 \\
y_2 = 39823,001 \\\\

x_3 = \frac{x_1y_2-x_2y_1}{y_2-y_1}= 11,0387 \\
y_3 = −2095,4074\\\\

x_4 = \frac{x_2y_3-x_3y_2}{y_3-y_2} =11,2370\\ 
y_4 = −382,7524\\\\

x_5 = \frac{x_3y_4-x_4y_3}{y_4-y_3}=11,2813\\
y_5 = 5,1574\\\\

x_6 = \frac{x_4y_5-x_5y_4}{y_5-y_4}=11,280711016\\
y_6 = −0,01268\\\\

x_7 = \frac{x_5y_6-x_6y_5}{y_6-y_5}= 11,280712461\\
y_7 = 0,000003045
\end{align}

$$

2. Newton Rapson
$$
\begin{align*}
x_1 = 10\\
x_2 = 15\\
f(x)= 2\pi r^3+90\pi r² -45000\\
f'(x)=6\pi r²+90\pi r \\
f''(x)=12\pi r +90\pi \\\\
f(x_1)+f(x_2)=\\
f'(x_1)= 6\pi(10)²+90\pi(10) = 600\pi + 900\pi = 4712,3889 \neq 0\\
f''(x_1)=
\end{align*}
$$




Crear entorno virtual
```bash
python3 -m venv env
```

Si no tiene venv
```bash
python3 -m pip install virtualenv
```

activar env
```bash
source env/bin/activate
```

Instalar dependecias
```bash
pip install -r requirements.txt
```

Ingresar a la carpeta pract_3
```bash
cd pract_3/
```

ejecutar la app
```bash
streamlit run app.py
```

Listo !!!
