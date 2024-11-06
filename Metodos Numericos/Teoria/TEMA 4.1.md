#### Ecuaciones homogeneas

$$ \text {Conj } \rightarrow \text {TRIVIALES}$$$$ r < n \rightarrow \text {NO TRIVIALES}$$Generalidades
notación matricial:
$$(A - \lambda I)X=0$$
X: vector característico o autovector
$$D =[A-\lambda I]$$  $$\lambda^n+p\lambda+...+p_{n-1}=0$$
Polinomio Característico
$$\text {Resolver polinomio y obtener } \lambda \text{ que hacen } D = 0$$
n: autovalores o valores característicos

#### Pasos
1- Resolver polinomio característico
2- Reemplazar en el sist de ecuaciones los lambda 
3- Resolver sistema de ecuaciones

### Método FADEEV-LEVERRIER
  $$\text {Para encontrar }\lambda \text{ y } x;\text{asociados a }\lambda$$
  $$(-1)^n \lambda^n+p\lambda+...+p_{n-1}=0$$
  $$\text {1- Calcular matriz de forma sucesiva hallando } b_k$$

$$B_1=A;b_1=trB_1$$
$$B_2=A(B_1-b_1I);b_2=1/2 trB_2$$
$$..........................$$
$$B_n=A(B_n-b_{n-1}I);b_n=1/n \text { }trB_n$$

### Método de las POTENCIAS
$$\text {Casos donde solo se desea conocer el autovalor más pequeño o grande}$$
$$(A-\lambda I)X=0$$
$$AX-\lambda IX=AX-\lambda X=0$$
$$AX=\lambda X$$

##### Pasos
1- Se usa AX = lambdaX con X arbitraria y se hace un proceso iterativo
$$AX_0=\lambda X_1$$
2- 
$$AX_1=\lambda X_2$$
3- Hasta que se llegue a un error estimado
4- Se llega a una sucesión
$$AX0;A^2X_0$$

Mínimo
$$X=A^{-1}\lambda X$$
$$A²X=1/\lambda X$$

Ejemplo:

