Para todos los distintos pares de valores $(y_1,y_2)$, los eventos bivariantes $(Y_1 = y_1, Y_2 = y_2)$, representados por $(y_1,y_2)$, son eventos mutuamente excluyentes. Se deduce que el evento univariante $(y_1,y_2)$ es la unión de eventos bivariantes del tipo $(Y_1 = y_1, Y_2 = y_2)$, con la unión tomada para todos los posibles valores de $y_1$.

Por ejemplo, reconsiderando el experimento de tirar un dado, donde $$\begin{gather*} Y_1 = \text{número de puntos de la cara superior del dado 1}\\ Y_2 = \text{número de puntos de la cara superior del dado 2} \end{gather*}$$
Entonces, $$\begin{flalign*} P(Y_1 = 1) &= p(1,1) + p(1,2) + p(1,3) + ... + p(1,6)\\ &= \frac{1}{36} + \frac{1}{36} + \frac{1}{36} + ... + \frac{1}{36} + \frac{1}{36} + = \frac{6}{36} = \frac{1}{6}\\ P(Y_1 = 2) &= p(2,1) + p(2,2) + p(2,3) + ... + p(2,6) = \frac{1}{6}\\ &\vdots\\ P(Y_1 = 6) &= p(6,1) + p(6,2) + p(6,3) + ... + p(6,6) = \frac{1}{6} \end{flalign*}$$
Expresadas en notación de sumatoria, las probabilidades acerca de la variable $Y_1$ sola son: $$P(Y_1 = y_1) = p_1 (y_1) = \sum_{y_2 = 1}^6 p(y_1,y_2)$$
Y del mismo modo, las probabilidades correspondientes a valores de la variable $Y_2$ sola están dadas por: $$P(Y_2 = 2) = p_2(y_2) = \sum_{y_1 = 1}^6 p(y_1,y_2)$$

---

## Definición de probabilidad marginal

Sean $Y_1$ y $Y_2$ variables aleatorias discretas conjuntas con función de probabilidad $p(y_1,y_2)$. Entonces las funciones de probabilidad marginal de $Y_1$ y $Y_2$, respectivamente, están dadas por:
$$p_1(y_1) = \sum_{\text{todos $y_2$}} p(y_1,y_2) \quad \text{y} \quad p_2(y_2) = \sum_{\text{todos $y_1$}} p(y_1,y_2)$$
Sean $Y_1$ y $Y_2$ variables aleatorias continuas conjuntas con función de densidad conjunta $f(y_1,y_2)$. Entonces las funciones de densidad marginal de $Y_1$ y $Y_2$, respectivamente, están dadas por:
$$f_1(y_1) = \int_{-\infty}^{\infty} f(y_1,y_2) dy_2 \quad \text{y} \quad f_2(y_2) = \int_{-\infty}^{\infty} f(y_1,y_2) dy_1$$
El término **marginal**, como se aplica a las funciones de probabilidad univariante de $Y_1$ y $Y_2$, tiene significado intuitivo. Para hallar $p_1(y_1)$ sumamos $p(y_1,y_2)$ para todos los valores de $y_2$ y por tanto acumulamos las probabilidades en el eje $y_1$ (o margen).

---

### Ejemplo

De un grupo de tres republicanos, dos demócratas y uno independiente se ha de seleccionar aleatoriamente un comité de dos personas. Denote con $Y_1$ el número de republicanos y con $y_2$ el número de demócratas del comité. Encuentre la función de probabilidad conjunta de $Y_1$ y $Y_2$, luego encuentre la función de probabilidad marginal de $Y_1$.

Las probabilidades buscadas aquí son semejantes a las probabilidades hipergeométricas. Por ejemplo:
$$P(Y_1 = 1, Y_2 = 1) = p(1,1) = \frac{\binom31\binom21\binom10}{\binom6}$$