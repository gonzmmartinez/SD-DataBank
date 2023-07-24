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
$$P(Y_1 = 1, Y_2 = 1) = p(1,1) = \frac{\binom31\binom21\binom10}{\binom62} = \frac{3(2)}{15} = \frac{6}{15}$$
Debido a que hay 15 puntos muestrales igualmente probables; para el evento en cuestión debemos seleccionar un republicano de entre los tres, un demócrata de entre los dos y cero independientes.

Para hallar $p_1(y_1)$ debemos sumar los valores de $Y_2$, como indica la [definición de probabilidad marginal](#Definición%20de%20probabilidad%20marginal). Por tanto, estas probabilidades están dadas por los totales de columna de la tabla. Esto es, $$p_1(0) = p(0,0) + p(0,1) + p(0,2) = 0 + \frac{2}{15} + \frac{1}{15} = \frac{3}{15}$$
Y del mismo modo, $$p_1(1) = \frac{9}{15} \qquad \text{y} \qquad p_1(2) = \frac{3}{15}$$
En forma análoga, la función de probabilidad marginal de $Y_2$ está dada por los totales de fila.
![center|300](Pasted%20image%2020230724155524.png)

---

### Ejemplo

Sea $$f(y_1,y_2) = \begin{cases} 2y_1 & 0 \le y_1 \le 1, 0 \le y_2 \le 1\\ 0 & \text{en cualquier otro caso} \end{cases}$$
Grafique $f(y_1,y_2)$ y encuentre las funciones de densidad marginal para $Y_1$ y $Y_2$.

Geométricamente, $f(y_1,y_2)$ describe una superficie en forma de cuña. Antes de aplicar la [definición de probabilidad marginal](#Definición%20de%20probabilidad%20marginal) para hallar $f_1(y_1)$ y $f_2(y_2)$, usaremos la forma para visualizar el resultado. Si la probabilidad representada por la cuña estuviera en el eje $y_1$ (acumulando probabilidad a lo largo de líneas paralelas al eje $y_2$), el resultado sería una densidad de probabilidad triangular que se vería como el lado de la cuña de la figura. SI la probabilidad estuviera acumulada a lo largo del eje $y_2$ (acumulándose a lo largo de líneas paralelas al eje $y_1$), la densidad resultante sería uniforme. Confirmaremos estas soluciones visuales mediante la aplicación de la definición.

![center](Pasted%20image%2020230724160650.png)
Entonces, si $0 \le y_1 \le 1$, $$f_1(y_1) = \int_{-\infty}^{\infty} f(y_1,y_2) dy_2 = \int_{0}^{1} 2y_1 dy_2 = 2y_1 (y_1 |_0^1)$$ y si $y_1 < 0$ o $y_1 > 1$, $$f_1(y_1) = \int_{-\infty}^{\infty} f(y_1,y_2) dy_2 = \int_{0}^{1} 0 dy_2 = 0$$
Entonces, $$f_1(y_1) = \begin{cases} 2y_1 & 0 \le y_1 \le 1\\ 0 & \text{en cualquier otro punto} \end{cases}$$
Del mismo modo, si $0 \le y_2 \le 1$, $$f_2(y_2) = \int_{-\infty}^{\infty} f(y_1,y_2) dy_1 = \int_{0}^{1} 0 dy_1 = 0$$
Resumiendo, $$f_2(y_2) = \begin{cases} 1 & 0 \le y_2 \le 1\\ 0 & \text{en cualquier otro punto} \end{cases}$$
Las gráficas de $f_1(y_1)$ y $f_2(y_2)$ trazan densidades de probabilidad triangulares y uniformes, respectivamente, como es de esperarse.