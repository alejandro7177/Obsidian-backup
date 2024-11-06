## Árboles de decisión 

- [ ] Poda - que el árbol no llegue a un overfiting 
- [ ] Hojas - Indice Gini
$$
\text{Impurez Gini} = 1 -(\text{Probabilidad de Si})²-(\text{Probabilidad de No})²
$$
- [ ] Indice Gini = 0 para nodos puros
### Métricas de Evaluación 
matriz de confusión

|          | Positivo           | Negativo           |
| -------- | ------------------ | ------------------ |
| Positivo | True Positivo(TP)  | Falso Negativo(FN) |
| Negativo | Falso Positivo(FP) | True Negativo(TN)  |


$$Accuracy = \frac{(TP+TN)}{(TP+TN+FP+FN)}$$
$$Presicion= \frac{TP}{(TP+FP)}$$
$$Recall= \frac{TP}{TP+FN}$$
$$Especificidad = \frac{TN}{algoXd}$$
$$\text{F1 Score}=2*\frac{precision*recall}{precision+recall}$$
$$MSE =\frac{1}{N} \sum_{i=1}^{N} (y_1 - \tilde{y_1})²$$
$$\text{Poda: } C_\alpha = Error +\alpha T$$
### Random Forest
Es un modelo que contiene varios arboles
un arbol 

# Maquina de soporte vectorial

10.40.1.254 port 3128

