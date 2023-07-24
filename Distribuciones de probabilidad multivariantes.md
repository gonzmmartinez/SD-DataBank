## Introducción

Suponga que $Y_1,Y_2,...,Y_n$ denota los resultados de $n$ intentos sucesivos de un experimento. Por ejemplo, esta secuencia podría representar los pesos de $n$ personas o las medidas de $n$ características físicas para una sola persona. Un conjunto específico de resultados o mediciones muestrales puede ser expresado en términos de la intersección de los $n$ eventos $(Y_1 = y_1), (Y_2 = y_2), ..., (Y_n = y_n)$, que denotaremos como $(Y_1 = y_1, Y_2 = y_2, ..., Y_n = y_n)$ o bien, de un modo más compacto como $(y_1, y_2, ..., y_n)$. El cálculo de la probabilidad de esta intersección es esencial para hacer inferencias acerca de la población de la cual se tomó la muestra y es una razón importante para estudiar distribuciones de probabilidad multivariantes.

---

## Distribuciones de probabilidad bivariantes y multivariantes

Se pueden definir muchas variables aleatorias sobre el mismo espacio muestral. Por ejemplo, considere el experimento de lanzar un par de dados. El espacio muestral contiene 36 puntos muestrales, correspondientes a las $mn = (6)(6) = 36$ formas en las que pueden aparecer números en las caras de los dados. Cualquiera de las siguientes variables aleatorias podría estar definida sobre el espacio muestral y podría ser de interés para el experimentador:

- $Y_1$: el número de puntos que aparecen en el dado 1.
- $Y_2$: el número de puntos que aparecen en el dado 2.
- $Y_3$: la suma del número de puntos en los dados.
- $Y_4$: el producto del número de puntos que aparecen en los dados.

Los 36 puntos muestrales asociados con el experimento tienen la misma probabilidad y corresponden a los 36 eventos numéricos $(y_1, y_2)$. Así, lanzar un par de números 1 es el evento sencillo $(1,1)$. Lanzar un 2 en el dado 1 y un 3 en el dado 2 es el evento sencillo $(2,3)$. Como todos los pares $(y_1, y_2)$ ocurren con la misma frecuencia relativa, asignamos una probabilidad $\frac{1}{36}$ a cada punto muestral. Para este ejemplo sencillo la intersección $(y_1, y_2)$ contiene a lo sumo un punto muestral. En consecuencia, la función de probabilidad bivariante es:

$$\begin{gather*}
	p(y_1, y_2) = P(Y_1 = y_1, Y_2 = y_2) = \frac{1}{36}, \quad y_1 = 1, 2, ..., 6, \quad y_2 = 1, 2, ..., 6
\end{gather*}$$

En la figura \ref{fig:51} se muestra una gráfica de la función de probabilidad bivariante para el experimento de lanzar dados. Observe que una probabilidad diferente de cero se asigna a un punto $(y_1, y_2)$ del plano si y solo si $y_1 = 1, 2, ..., 6$ y $y_2 = 1, 2, ..., 6$. Entonces, a los 36 puntos del plano se les asignan exactamente probabilidades diferentes de cero. Además, las probabilidades se asignan en tal forma que la suma de las probabilidades diferentes de cero es igual a 1. En la figura \ref{fig:51} los planos a los que se asignan probabilidades diferentes de cero están representados en el plano $(y_1, y_2)$, mientras que las probabilidades asociadas con esos puntos están dadas por las longitudes de las rectas que aparecen arriba de ellos. La figura \ref{fig:51} puede verse como un histograma teórico de frecuencias relativa en tres dimensiones para los pares de observaciones $(y_1, y_2)$. Al igual que en el caso discreto de una sola variable, el histograma teórico da un modelo para el histograma muestral que se obtendría si el experimento de lanzar dados se repitiera un gran número de veces.

\begin{figure}[h!]
	\centering
	\caption{}
	\label{fig:51}
	\includegraphics[width=0.6\linewidth]{Anexo/screenshot001}
\end{figure}

\begin{tcolorbox}\begin{defn}
	Sean $Y_2$ y $Y_2$ variables aleatorias discretas. La \textit{función de probabilidad conjunta} (o bivariante) para $Y_1$ e $Y_2$ está dada por:
	\begin{equation}
		p(y_1, y_2) = P(Y_1 = y_1, Y_2 = y_2), \quad -\infty < y_1 < \infty, -\infty < y_2 < \infty
	\end{equation}
\end{defn}\end{tcolorbox}

En el caso de la variable única la función de probabilidad para una variable aleatoria discreta $Y$ asigna probabilidades diferentes de cero a un número finito o contable de valores distintos de $Y$, en forma tal que la suma de las probabilidades es igual a 1. Del mismo modo, en el caso bivariante la función de probabilidad conjunta $p(y_1, y_2)$ asigna probabilidades diferentes de cero a sólo un número finito o contable de pares de valores $(y_1, y_2)$. Además, las probabilidades diferentes de cero deben sumar 1.

\begin{thm}\label{thm:51}
	Si $Y_1$ y $Y_2$ son variables aleatorias discretas con función de probabilidad conjunta $p(y_1, y_2)$, entonces:
	\begin{enumerate}[1.]
		\item $p(y_1, y_2) \ge 0$ para toda $y_1$, $y_2$
		
		\item $\sum_{y_1, y_2} p(y_1, y_2) = 1$, donde la suma es para todos los valores $(y_1, y_2)$ a los que se asignan probabilidades diferentes de cero.
	\end{enumerate}
\end{thm}

Al igual que en el caso discreto univariante, la función de probabilidad conjunta para variables aleatorias discretas a veces se denomina \textbf{función de masa de probabilidad conjunta} porque especifica la probabilidad (masa) asociada con cada uno de los posibles pares de valores para las variables aleatorias. Una vez que la función de probabilidad conjunta se haya determinado para variables aleatorias discretas $Y_1$ y $Y_2$, calcular las probabilidades conjuntas en donde aparecen $Y_1$ y $Y_2$ es fácil. Para el experimento de lanzar dados, $P(2 \le Y_1 \le 3, 1 \le Y_2 \le 2)$ es:
\begin{flalign*}
	P(2 \le Y_1 \le 3, 1 \le Y_2 \le 2) &= p(2,1) + p(2,2) + p(3,1) + p(3,2)\\
	&= \frac{4}{36} = \frac{1}{9}
\end{flalign*}

\begin{ex}\label{ex:51}
	Un supermercado local tiene tres cajas. Dos clientes llegan a las cajas en momentos diferentes cuando las cajas no atienden a otros clientes. Cada cliente escoge una caja de manera aleatoria, independientemente del otro. Denote con $Y_1$ el número de clientes que escogen la caja 1 y con $Y_2$ el número que selecciona la caja 2. Encuentre la función de probabilidad conjunta de $Y_1$ y $Y_2$.
\end{ex}

Podríamos proceder en muchas formas. La más directa es considerar el espacio muestral asociado con el experimento. Denotemos con el par $[i,j]$ el evento sencillo de que el primer cliente escogió la caja $i$ y el segundo cliente escogió la caja $j$, donde $i,j=1,2$ y $3$. Usando la regla $mn$, el espacio muestral está formado por $3 \times 3 = 9$ puntos muestrales. De acuerdo con las suposiciones dadas antes, cada punto muestral es igualmente probable y tiene probabilidad $\nicefrac{1}{9}$. El espacio muestral asociado con el experimento es:
\begin{gather*}
	S = [\set{1,1},\set{1,2},\set{1,3},\set{2,1},\set{2,2},\set{2,3},\set{3,1},\set{3,2},\set{3,3}]
\end{gather*}

Observe que el punto muestral $\set{1,1}$ es el único correspondiente a $(Y_1=2, Y_2=0)$ y por tanto $P(Y_1=2,Y_2=0)=\frac{1}{9}$. Del mismo modo, $P(Y_1=1,Y_2=1)=P(\text{$\set{1,2}$ o $\set{2,1}$})=\frac{2}{9}$. La siguiente tabla contiene las probabilidades asociadas con cada posible par de valores para $Y_1$ y $Y_2$, es decir, la función de probabilidad conjunta para $Y_1$ y $Y_2$. Como siempre, los resultados del teorema \ref{thm:51} se cumplen para este ejemplo.

\begin{table}[h!]
	\centering
	\caption{}
	\label{tab:51}
	\def\arraystretch{1.25}
	\begin{tabular}[h!]{cccc}
		\hline
		& \multicolumn{3}{c}{$y_1$}\\ \cline{2-4}
		$y_2$ & $0$ & $1$ & $2$\\
		\hline
		$0$ & $\nicefrac{1}{9}$ & $\nicefrac{2}{9}$ & $\nicefrac{1}{9}$\\
		$1$ & $\nicefrac{2}{9}$ & $\nicefrac{2}{9}$ & $0$\\
		$2$ & $\nicefrac{1}{9}$ & $0$ & $0$\\
		\hline 
	\end{tabular}
\end{table}

Al igual que en el caso de variables aleatorias univariantes, la distinción entre variables aleatorias continuas conjuntas y discretas conjuntas puede ser caracterizado en términos de sus funciones de distribución (conjuntas).

\begin{tcolorbox}\begin{defn}
	Para cualesquiera variables aleatorias $Y_1$ y $Y_2$, la función de distribución (bivariante) conjunta $F(y_1, y_2)$ es:
	\begin{equation}
		F(y_1, y_2) = P(Y_1 \le y_1, Y_2 \le y_2), \quad -\infty < y_1 < \infty, -\infty < y_2 < \infty
	\end{equation}
\end{defn}\end{tcolorbox}

Para dos variables discretas $Y_1$ y $Y_2$, $F(y_1, y_2)$ está dada por:
\begin{equation}
	F(y_1, y_2) = \sum_{t_1 \le y_1} \sum_{t_2 \le y_2} p(t_1, t_2)
\end{equation}

Para el experimento de lanzar un dado,
\begin{flalign*}
	F(2,3) &= P(Y_1 \le 2, Y_2 \le 3)\\
	&= p(1,1) + p(1,2) + p(1,3) + p(2,1) + p(2,2) + p(2,3)
\end{flalign*}

Como $p(y_1, y_2) = \frac{1}{36}$ para todos los pares de valores de $y_1$ y $y_2$ en consideración, $F(2,3) = \frac{6}{36} = \frac{1}{6}$.

\begin{ex}\label{ex:52}
	Considere las variables aleatorias $Y_1$ y $Y_2$ del ejemplo \ref{ex:51}. Encuentre $F(-1,2)$, $F(1.5,2)$ y $F(5,7)$
\end{ex}

Usando los resultados de la tabla anterior vemos que:
\begin{gather*}
	F(-1,2) = P(Y_1 \le -1, Y_2 \le 2) = P(\emptyset) = 0
\end{gather*}

Además,
\begin{flalign*}
	F(1.5, 2) &= P(Y_1 \le 1.5, Y_2 \le 2)\\
	&= p(0,0) + p(0,1) + p(0,2) + p(1,0) + p(1,1) + p(1,2) = \frac{8}{9}
\end{flalign*}

De manera similar,
\begin{gather*}
	F(5,7) = P(Y_1 \le 5, Y_2 \le 7) = 1
\end{gather*}

Observe que $F(y_1, y_2) = 1$ para toda $(y_1,y_2)$ tal que $min\set{y_1, y_2} \ge 2$. También, $F(y_1,y_2) = 0$ si $min\set{y_1,y_2} < 0$

Se dice que dos variables aleatorias son continuas conjuntas si su función de distribución conjunta $F(y_1, y_2)$ es continua en ambos argumentos.

\begin{tcolorbox}\begin{defn}
	Sean $Y_1$ y $Y_2$ variables aleatorias continuas con función de distribución conjunta $F(y_1, y_2)$. Si existe una función no negativa $f(y_1, y_2)$, tal que:
	\begin{equation}
		F(y_1, y_2) = \int_{-\infty}^{y_1} \int_{-\infty}^{y_2} f(t_1,t_2) dt_2 dt_1
	\end{equation}
	
	Para toda $-\infty < y_1 < \infty$, $-\infty < y_2 < \infty$, entonces se dice que $Y_1$ y $Y_2$ son \textbf{variables aleatorias continuas conjuntas}. La función $f(y_1, y_2)$ recibe el nombre de \textbf{función de densidad de probabilidad conjunta}.
\end{defn}\end{tcolorbox}

Las funciones de distribución acumulativa bivariante satisfacen un conjunto de propiedades similares a las especificadas para funciones de distribución acumulativa univariante.

\begin{thm}
	Si $Y_1$ y $Y_2$ son variables aleatorias con función de distribución conjunta $F(y_1, y_2)$, entonces:
	\begin{enumerate}[1.]
		\item $F(-\infty, \infty) = F(-\infty, y_2) = F(y_1, -\infty) = 0$
		
		\item $F(\infty, \infty) = 1$
		
		\item Si $y_1^* \ge y_1$ y $y_2^* \ge y_2$, entonces:
		\begin{equation*}
			F(y_1^*, y_2^*) - F(y_1^*, y_2) - F(y_1, y_2^*) + F(y_1, y_2) \ge 0
		\end{equation*}
	\end{enumerate}
\end{thm}

La parte 3 resulta de que:
\begin{gather*}
	F(y_1^*, y_2^*) - F(y_1^*, y_2) - F(y_1,y_2^*) + F(y_1, y_2)\\
	= P(y_1 < Y_1 \le y_1^*, y_2 < Y_2 \le y_2^*) \ge 0
\end{gather*}

Observe que $F(\infty, \infty) \equiv \lim_{y_1 \rightarrow \infty} \lim_{y_2 \rightarrow \infty} F(y_1, y_2) = 1$ implica que la función de densidad conjunta $f(y_1,y_2)$ debe ser tal que la integral de $f(y_1,y_2)$ para todos los valores de $(y_1,y_2)$ es 1.

\begin{thm}
	Si $Y_1$ y $Y_2$ son variables aleatorias continuas conjuntas con una función de densidad conjunta dada por $f(y_1,y_2)$, entonces:
	\begin{enumerate}[1.]
		\item $f(y_1,y_2) \ge 0$ para toda $(y_1,y_2)$
		
		\item $\int_{-\infty}^{\infty} \int_{-\infty}^{\infty} f(y_1,y_2) dy_1 dy_2 = 1$
	\end{enumerate}
\end{thm}
\break
Al igual que en el caso continuo univariante, la función de densidad conjunta puede ser interpretada de manera intuitiva como un modelo para el histograma de frecuencia relativa conjunta para $Y_1$ y $Y_2$.

Para el caso continuo univariante, las áreas bajo la densidad de probabilidad para un intervalo corresponden a probabilidades. De igual manera, la función de densidad de probabilidad bivariante $f(y_1,y_2)$ traza una superficie de densidad de probabilidad sobre el plano $(y_1,y_2)$. (figura \ref{fig:52})

\begin{figure}[h!]
	\centering
	\caption{}
	\label{fig:52}
	\includegraphics[width=0.5\linewidth]{Anexo/screenshot003}
\end{figure}

Los volúmenes bajo esta superficie representan probabilidades. Así, $P(a_1 \le Y_1 \le a_2, b_1 \le Y_2 \le b_2)$ es el volumen sombreado que se ve en la figura \ref{fig:52} y es igual a:
\begin{gather}
	\int_{b_1}^{b_2} \int_{a_1}^{a_2} f(y_1,y_2) dy_1 dy_2
\end{gather}

\begin{ex}
	Suponga que una partícula radiactiva se localiza aleatoriamente en un cuadrado con lados de longitud unitaria. Esto es, si se consideran dos regiones de igual área y dentro del cuadrado unitario es igualmente probable que se la partícula se encuentre en cualquiera de las dos. Denote con $Y_1$ y $Y_2$ las coordenadas de la ubicación de la partícula. Un modelo razonable para el histograma de frecuencia relativa para $Y_1$ y $Y_2$ es la análoga bivariante de la función de densidad uniforme univariante:
	\begin{equation*}
		f(y_1, y_2) = \begin{cases}
			1 & 0 \le y_1 \le 1, 0 \le y_2 \le 1\\
			0 & \text{en cualquier otro caso}
		\end{cases}
	\end{equation*}
\end{ex}

\begin{enumerate}[a.]
	\item Trace la superficie de densidad de probabilidad.
	
	El trazo se muestra en la figura \ref{fig:53}
	
	\item Encuentre $F(0.2, 0.4)$
	\begin{flalign*}
		F(0.2, 0.4) &= \int_{-\infty}^{0.4} \int_{-\infty}^{0.2} f(y_1,y_2) dy_1 dy_2\\
		&= \int_{0}^{0.4} \int_{0}^{0.2} (1) dy_1 dy_2\\
		&= \int_{0}^{0.4} \left( y_1\bigg|_{0}^{0.2} \right) dy_2 = \int_{0}^{0.4} 0.2 dy_2 = 0.08
	\end{flalign*}
	
	La probabilidad $F(0.2, 0.4)$ corresponde al volumen bajo $f(y_1,y_2)=1$ que está sombreado en la figura \ref{fig:53}. Como lo indican las consideraciones geométricas, la probabilidad deseada (volumen) es igual a 0,08, que obtuvimos mediante integración al principio.
	
	\begin{figure}[h!]
		\centering
		\caption{}
		\label{fig:53}
		\includegraphics[width=0.5\linewidth]{Anexo/screenshot004}
	\end{figure}
	
	\break
	
	\item Encuentre $P(0.1 \le Y_1 \le 0.3, 0 \le Y_2 \le 0.5)$
	\begin{flalign*}
		P(0.1 \le Y_1 \le 0.3, 0 \le Y_2 \le 0.5) &= \int_{0}^{0.5} \int_{0.1}^{0.3} f(y_1,y_2) dy_1 dy_2\\
		&= \int_{0}^{0.5} \int_{0.1}^{0.3} 1 dy_1 dy_2 = 0.1
	\end{flalign*}
	
	Esta probabilidad corresponde al volumen bajo la función de densidad $f(y_1,y_2) = 1$ que está arriba de la región $0.1 \le y_1 \le 0.3, 0 \le y_2 \le 0.5$. Al igual que la solución del inciso $\text{b.}$, la solución actual se puede obtener con el uso de conceptos de geometría elemental. La densidad o altura de la superficie es igual a 1 y por tanto la probabilidad deseada (volumen) es:
	\begin{equation*}
		P(0.1 \le Y_1 \le 0.3, 0 \le Y_2 \le 0.5) = (0.2)(0.5)(1)= 0.1
	\end{equation*}
\end{enumerate}

\begin{ex}\label{ex:54}
	Se ha de almacenar gasolina en un enorme tanque una vez  principio de cada semana y luego se vende a clientes individuales. Denote con $Y_1$ el nivel de gasolina (proporción) que alcanza el tanque después de surtirlo. Debido a suministros limitados $Y_1$ varía de una semana a otra. Denote con $Y_2$ la proporción de la capacidad del tanque que se vende durante la semana. Como $Y_1$ y $Y_2$ son proporciones, estas dos variables toman valores entre 0 y 1. Además, la cantidad de gasolina vendida, $y_2$, no puede ser mayor que la cantidad disponible, $y_1$. Suponga que la función de densidad conjunta para $Y_1$ y $Y_2$ está dada por:
	\begin{equation*}
		f(y_1, y_2) = \begin{cases}
			3y_1 & 0 \le y_2 \le y_1 \le 1\\
			0 & \text{en cualquier otro punto}
		\end{cases}
	\end{equation*}
	
	En la figura \ref{fig:54} se muestra una gráfica de esta función.
	
	Encuentre la probabilidad de que menos de la mitad del tanque tenga gasolina y más de un cuarto del tanque se venda.
\end{ex}

Buscamos $P(0 \le Y_1 \le 0.5, Y_2 > 0.25)$. Para cualquier variable aleatoria continua, la probabilidad de observar un valor en una región es el volumen bajo la función de densidad por arriba de la región de interés. La función de densidad $f(y_1, y_2)$ es positiva solo en la región triangular grande del plano que se ve en el segundo gráfico de la figura \ref{fig:54}. Estamos interesados sólo en valores de $y_1$ y $y_2$ tales que $0 \le y_1 \le 0.5$ y $y_2 > 0.25$. La intersección de esta región y la región donde la función de densidad es positiva está dada por el pequeño triángulo (sombreado) del segundo gráfico de la figura \ref{fig:54}. En consecuencia, la probabilidad que deseamos es el volumen bajo la función de densidad del primer gráfico de la figura \ref{fig:54} arriba de la región del plano $(y_1,y_2)$ que se ve en el segundo gráfico.
\begin{figure}[h!]
	\centering
	\caption{}
	\label{fig:54}
	\includegraphics[width=0.8\linewidth]{Anexo/screenshot005}
\end{figure}

\break

Entonces, tenemos:
\begin{flalign*}
	P(0 \le Y_1 \le 0.5, 0.25 \le Y_2) &= \int_{\frac{1}{4}}^{\frac{1}{2}} \int_{\frac{1}{4}}^{y_1} 3y_1 dy_2 dy_1\\
	&= \int_{\frac{1}{4}}^{\frac{1}{2}} 3y_1 \left( y_2 \bigg|_{\frac{1}{4}}^{y_1} \right) dy_1\\
	&= \int_{\frac{1}{4}}^{\frac{1}{2}} 3y_1 \left(y_1 - \frac{1}{4} \right) dy_1\\
	&= \left[ y_1^3 - \left( \frac{3}{8} \right) y_1^2 \right]_{\frac{1}{4}}^{\frac{1}{2}}\\
	&= \left[ \left(\frac{1}{8}\right) - \left(\frac{3}{8}\right) \left(\frac{1}{4}\right) \right] - \left[ \left(\frac{1}{64}\right) - \left( \frac{3}{8} \right) \left( \frac{1}{16} \right) \right]\\
	&= \frac{5}{128}
\end{flalign*}

El cálculo de la probabilidad especificada en el ejemplo \ref{ex:54} comprendió integrar la función de densidad conjunta para $Y_1$ y $Y_2$ sobre la región apropiada. La especificación de los límites de integración se hizo más fácil al trazar la región de integración en la segunda figura \ref{fig:54}. Este método, trazando la región apropiada de integración, con frecuencia facilita establecer la integral apropiada.

Los métodos estudiados en esta sección se pueden usar para calcular la probabilidad de la intersección de dos eventos $(Y_1 = y_1, Y_2 = y_2)$. De igual modo podemos definir una función de probabilidad (o función de densidad de probabilidad) para la intersección de $n$ eventos $(Y_1 = y_1, Y_2 = y_2, ..., Y_n = y_n)$. La función de probabilidad conjunta correspondiente al caso discreto está dada por:
\begin{equation}
	p(y_1, y_2, ..., y_n) = P(Y_1 = y_1, Y_2 = y_2, ..., Y_n = y_n)
\end{equation}

La función de densidad conjunta de $Y_1, Y_2, ..., Y_n$ está dada por $f(y_1, y_2, ..., y_n)$. Al igual que en el caso bivariante, estas funciones dan modelos para las distribuciones de frecuencia relativa conjunta de las poblaciones de observaciones conjuntas $(y_1, y_2, ..., y_n)$ para el caso discreto y el caso continuo, respectivamente. El caso continuo,
\begin{equation}
	\begin{aligned}
		P(Y_1 \le y_1, Y_2 \le y_2, ..., Y_n \le y_n) &= F(y_1, y_2, ..., y_n)\\
		&= \int_{-\infty}^{y_1} \int_{-\infty}^{y_2} ... \int_{-\infty}^{y_n} f(t_1, t_2, ..., t_n) dt_n ... dt_1
	\end{aligned}
\end{equation}

Para todo conjunto de números reales $(y_1, y_2, ..., y_n)$. Las funciones de distribución multivariantes definidas por esta igualdad satisfacen propiedades semejantes a las especificadas para el caso bivariante.

\subsection{Distribuciones de probabilidad marginal y condicional}\label{sec:53}

Recuerde que los valores distintos tomados por una variable aleatoria discreta representan eventos mutuamente excluyentes. De manera análoga, para todos los distintos pares de valores $(y_1, y_2)$, los eventos bivariantes $(Y_1 = y_1, Y_2 = y_2)$, representados por $(y_1, y_2)$, son eventos mutuamente excluyentes. Se deduce que el evento univariante $(y_1, y_2)$ es la unión de eventos bivariantes del tipo $(Y_1 = y_1, Y_2 = y_2)$, con la unión tomada para todos los posibles valores de $y_1$.

Por ejemplo, reconsidere el experimento de tirar un dado de la sección anterior, donde:
\begin{gather*}
	Y_1 = \text{número de puntos de la cara superior del dado 1}\\
	Y_2 = \text{número de puntos de la cara superior del dado 2}
\end{gather*}

Entonces:
\begin{flalign*}
	P(Y_1 = 1) &= p(1,1) + p(1,2) + p(1,3) + ... + p(1,6)\\
	&= \frac{1}{36} + \frac{1}{36} + \frac{1}{36} + ... + \frac{1}{36} = \frac{6}{36} = \frac{1}{6}\\
	P(Y_1 = 2) &= p(2,1) + p(2,2) + p(2,3) + ... + p(2,6) = \frac{1}{6}\\
	&\cdot\\ &\cdot\\ &\cdot\\
	P(Y_1 = 6) &= p(6,1) + p(6,2) + p(6,3) + ... + p(6,6) = \frac{1}{6}
\end{flalign*}

Expresadas en notación de sumatoria, las probabilidades acerca de la variable $Y_1$ sola son:
\begin{equation*}
	P(Y_1 = y_1) = p_1(y_1) = \sum_{y_2 = 1}^{6} p(y_1, y_2)
\end{equation*}

Del mismo modo, las probabilidades correspondientes a valores de la variable $Y_2$ sola están dadas por:
\begin{equation*}
	P(Y_2 = y_2) = p_2(y_2) = \sum_{y_1 = 1}^{6} p(y_1, y_2)
\end{equation*}

La sumatoria en el caso discreto corresponde a la integración en el caso continuo, que nos lleva a la siguiente definición:

\begin{tcolorbox}\begin{defn}\label{def:54}
	$\text{}$
	\begin{enumerate}[a.]
		\item Sean $Y_1$ y $Y_2$ variables aleatorias discretas conjuntas con función de probabilidad $p(y_1, y_2)$. Entonces las funciones de probabilidad marginal de $Y_1$ y $Y_2$, respectivamente, están dadas por:
		\begin{equation}
			p_1(y_1) = \sum_{\text{todos } y_2} p(y_1, y_2) \quad \text{y} \quad p_2(y_2) = \sum_{\text{todos } y_1} p(y_1, y_2)
		\end{equation}
		
		\item Sean $Y_1$ y $Y_2$ variables aleatorias continuas conjuntas con función de densidad conjunta $f(y_1, y_2)$. Entonces las funciones de densidad marginal de $Y_1$ y $Y_2$, respectivamente, están dadas por:
		\begin{equation}
			f_1(y_1) = \int_{-\infty}^{\infty} f(y_1, y_2) dy_2 \quad \text{y} \quad f_2(y_2) = \int_{-\infty}^{\infty} f(y_1, y_2) dy_1
		\end{equation}
	\end{enumerate}
\end{defn}\end{tcolorbox}

El término \textbf{marginal}, como se aplica a las funciones de probabilidad univariante de $Y_1$ y $Y_2$, tiene significado intuitivo. Para hallar $p_1(y_1)$ sumamos $p(y_1, y_2)$ para todos los valores de $y_2$ y por tanto acumulamos las probabilidades en el eje $y_1$ (o margen). Los casos discretos y continuos se ilustran en los siguientes dos ejemplos:

\begin{ex}\label{ex:55}
	De un grupo de tres republicanos, dos demócratas y uno independiente se ha de seleccionar aleatoriamente un comité de dos personas. Denote con $Y_1$ el número de republicanos y con $Y_2$ el número de demócratas del comité. Encuentre la función de probabilidad conjunta de $Y_1$ y $Y_2$ y luego encuentre la función de probabilidad marginal de $Y_1$.
\end{ex}

Las probabilidades buscadas aquí son semejantes a las probabilidades hipergeométricas. Por ejemplo:
\begin{equation*}
	P(Y_1 = 1, Y_2 =1) = p(1,1) = \frac{\binom{3}{1}\binom{2}{1}\binom{1}{0}}{\binom{6}{2}} = \frac{3 (2)}{15} = \frac{6}{15}
\end{equation*}

Debido a que hay 15 puntos muestrales igualmente probables; para el evento en cuestión debemos seleccionar un republicano de entre los tres, un demócrata de entre los dos y cero independientes. Cálculos semejantes llevan a las otras probabilidades que se ven en la tabla \ref{tab:52}.

Para hallar $p_1(y_1)$ debemos sumar los valores de $Y_2$, como indica la definición \ref{def:54}. Por tanto, estas probabilidades están dadas por los totales de columna de la tabla \ref{tab:52}. Esto es,
\begin{equation*}
	p_1(0) = p(0,0) + p(0,1) + p(0,2) = 0 + \frac{2}{15} + \frac{1}{15} = \frac{3}{15}
\end{equation*}

Del mismo modo,
\begin{equation*}
	p_1(1) = \frac{9}{15} \quad \text{y} \quad p_1(2) = \frac{3}{15}
\end{equation*}

En forma análoga, la función de probabilidad marginal de $Y_2$ está dada por los totales de fila.
\begin{table}[h!]
	\centering
	\caption{}
	\label{tab:52}
	\def\arraystretch{1.25}
	\begin{tabular}[h!]{ccccc}
		\hline
		& \multicolumn{3}{c}{$y_1$} &\\
		\cline{2-4}
		$y_2$ & $0$ & $1$ & $2$ & \textit{Total}\\ \hline
		$0$ & $0$ & $\nicefrac{3}{15}$ & $\nicefrac{3}{15}$ & $\nicefrac{6}{15}$\\
		$1$ & $\nicefrac{2}{15}$ & $\nicefrac{6}{15}$ & $0$ & $\nicefrac{8}{15}$\\
		$2$ & $\nicefrac{1}{15}$ & $0$ & $0$ & $\nicefrac{1}{15}$\\ \hline
		\textit{Total} & $\nicefrac{3}{15}$ & $\nicefrac{9}{15}$ & $\nicefrac{3}{15}$ & $1$\\
	\end{tabular}
\end{table}

\begin{ex}\label{ex:56}
	Sea:
	\begin{equation*}
		f(y_1,y_2) = \begin{cases}
			2y_1 & 0 \le y_1 \le 1, 0 \le y_2 \le 1\\
			0 & \text{en cualquier otro punto}
		\end{cases}
	\end{equation*}
	
	Grafique $f(y_1, y_2)$ y encuentre las funciones de densidad marginal para $Y_1$ y $Y_2$.
\end{ex}

Geométricamente, $f(y_1, y_2)$ describe una superficie en forma de cuña, como se ve en la figura \ref{fig:56}.

Antes de aplicar la definición \ref{def:54} para hallar $f_1(y_1)$ y $f_2(y_2)$, usaremos la figura \ref{fig:56} para visualizar el resultado. Si la probabilidad representada por la cuña estuviera acumulada en el eje $y_1$ (acumulando probabilidad a lo largo de líneas paralelas al eje $y_2$), el resultado sería una densidad de probabilidad triangular que se vería como el lado de la cuña de la figura \ref{fig:56}. Si la probabilidad estuviera acumulada a lo largo del eje $y_2$ (acumulándose a lo largo de líneas paralelas al eje $y_1$), la densidad resultante sería uniforme. Confirmaremos estas soluciones visuales mediante la aplicación de la definición \ref{def:54}.

\begin{figure}[h!]
	\centering
	\caption{}
	\label{fig:56}
	\includegraphics[width=0.5\linewidth]{Anexo/screenshot007}
\end{figure}

Entonces, si $0 \le y_1 \le 1$,
\begin{equation*}
	f_1(y_1) = \int_{-\infty}^{\infty} f(y_1, y_2) dy_2 = \int_{0}^{1} 2y_1 dy_2 = 2y_1 \left( y_2\bigg|_{0}^{1} \right)
\end{equation*}

y  si $y_1 < 0$ o $y_1 > 1$,
\begin{equation*}
	f_1(y_1) = \int_{-\infty}^{\infty} f(y_1, y_2) dy_2 = \int_{0}^{1} 0 dy_2 = 0
\end{equation*}

Entonces,
\begin{equation*}
	f_1(y_1) = \begin{cases}
		2y_1 & 0 \le y_1 \le 1\\
		0 & \text{en cualquier otro punto}
	\end{cases}
\end{equation*}

Del mismo modo, si $0 \le y_2 \le 1$,
\begin{equation*}
	f_2(y_2) = \int_{-\infty}^{\infty} f(y_1, y_2) dy_1 = \int_{0}^{1} 0 dy_1 = 0
\end{equation*}

Resumiendo,
\begin{equation*}
	f_2(y_2) = \begin{cases}
		1 & 0 \le y_2 \le 1\\
		0 & \text{en cualquier otro punto}
	\end{cases}
\end{equation*}

Las gráficas de $f_1(y_1)$ y $f_2(y_2)$ trazan densidades de probabilidad triangulares y uniformes, respectivamente, como es de esperarse.

Llevemos ahora nuestra atención a distribuciones condicionales, viendo primero al caso discreto.

La ley multiplicativa da la probabilidad de la intersección $A \cap B$ como
\begin{equation}
	P(A\cap B) = P(A) \cdot P(B|A)
\end{equation}

Donde $P(A)$ es la probabilidad incondicional de $A$ y $P(B|A)$ es la probabilidad de B dado que A ha ocurrido. Ahora considere la intersección de los dos eventos numéricos, $(Y_1 = y_1)$ y $(Y_2 = y_2)$, representada por el evento bivariante $(y_1, y_2)$. Se deduce directamente de la ley multiplicativa de probabilidad que la probabilidad bivariante para la intersección $(y_1, y_2)$ es
\begin{equation}
	\begin{aligned}
		p(y_1, y_2) &= p_1 (y_1) \cdot p(y_2 | y_1)\\
		&= p_2 (y_2) \cdot p(y_1 | y_2)
	\end{aligned}
\end{equation}

Las probabilidades $p_1(y_1)$ y $p_2(y_2)$ están asociadas con las distribuciones de probabilidad univariantes para $Y_1$ y $Y_2$ individualmente. Usando la interpretación de probabilidad condicional, $p(y_1|y_2)$ es la probabilidad de que la variable aleatoria $Y_1$ sea igual a $y_1$, dado que $Y_2$ toma el valor $y_2$.

\begin{tcolorbox}\begin{defn}\label{def:55}
	Si $Y_1$ y $Y_2$ son variables aleatorias discretas conjuntas con función de probabilidad conjunta $p(y_1,y_2)$ y funciones de probabilidad marginal $p_1(y_1)$ y $p_2(y_2)$, respectivamente, entonces la \textbf{función de probabilidad discreta condicional} de $Y_1$ dada $Y_2$ es:
	\begin{equation}
		p(y_1|y_2) = P(Y_1 = y_1|Y_2 = y_2) = \frac{P(Y_1=y_1, Y_2 = y_2)}{P(Y_2 = y_2)} = \frac{p(y_1, y_2)}{p_2(y_2)}
	\end{equation}
	
	Siempre que $p_2(y_2) > 0$
\end{defn}\end{tcolorbox}

Entonces, $P(Y_1 = 2 | Y_2 = 3)$ es la probabilidad condicional de que $Y_1 = 2$ dado que $Y_2 = 3$. Una interpretación similar se puede unir a la probabilidad condicional $p(y_2 | y_1)$. Observe que $p(y_1 | y_2)$ es \textit{indefinida} si $p_2(y_2)=0$

\begin{ex}\label{ex:57}
	Consulte el ejemplo \ref{ex:55} y encuentre la distribución condicional de $Y_1$ dado que $Y_2 = 1$. Esto es, dado que una de las dos personas del comité es demócrata, encuentre la distribución condicional para el número de republicanos seleccionados por el comité.
\end{ex}

Las probabilidades conjuntas están dadas en la tabla \ref{tab:52}. Para hallar $p(y_1|Y_2=1)$, nos concentramos en la fila correspondiente a $Y_2=1$. Entonces:
\begin{gather*}
	P(Y_1 = 0|Y_2 = 1) = \frac{p(0,1)}{p_2(1)} = \frac{\frac{2}{15}}{\frac{8}{15}} = \frac{1}{4}\\
	P(Y_1 = 1|Y_2 = 1) = \frac{p(1,1)}{p_2(1)} = \frac{\frac{6}{15}}{\frac{8}{15}} = \frac{3}{4}
\end{gather*}

y
\begin{gather*}
	P(Y_1\ge 2|Y_2 = 1) = \frac{p(2,1)}{p_2(1)} = \frac{0}{\frac{8}{15}} = 0
\end{gather*}

En el comité seleccionado aleatoriamente, si una persona es demócrata (o, lo que es lo mismo, si $Y_2=1$), hay una alta probabilidad de que el otro sea republicano (o sea $Y_1=1$)

En el caso continuo podemos obtener una analogía apropiada de la función de probabilidad condicional $p(y_1|y_2)$, pero no se obtiene en una forma tan sencilla. Si $Y_1$ y $Y_2$ son continuas, $P(Y_1=y_1|Y_2=y_2)$ no se puede definir como en el caso discreto porque $(Y_1=y_1)$ y $(Y_2=y_2)$ son eventos con probabilidad cero. Las siguientes consideraciones, sin embargo, llevan a una definición útil y consistente para una función de densidad condicional.

Suponiendo que $Y_1$ y $Y_2$ son continuas conjuntas con función de densidad $f(y_1,y_2)$, podríamos estar interesados en una probabilidad de la forma:
\begin{equation*}
	P(Y_1 \le y_1|Y_2 = y_2) = F(y_1|y_2)
\end{equation*}

Que, como función de $y_1$ para una $y_2$ fija, se denomina \textit{función de distribución condicional} de $Y_1$, dado que $Y_1=y_2$

\begin{tcolorbox}\begin{defn}
	Si $Y_1$ y $Y_2$ son variables aleatorias continuas conjuntas con función de densidad conjunta $f(y_1,y_2)$, entonces la \textbf{función de distribución condicional} de $Y_1$ dado que $Y_2=y_2$ es:
	\begin{equation}
		F(y_1|y_2) = P(Y_1 \le y_1|Y_2 = y_2)
	\end{equation}
\end{defn}\end{tcolorbox}

Observe que $F(y_1|y_2)$ es una función de $y_1$ para un valor fijo de $y_2$.

Si pudiéramos tomar $F(y_1|y_2)$, multiplicarlo por $P(Y_2=y_2)$ para cada posible valor de $Y_2$ y sumar todas las probabilidades restantes, podríamos obtener $F(y_1)$. Esto no es posible porque el número de valores para $y_2$ es incontable y todas las probabilidades $P(Y_2=y_2)$ son cero. Pero podemos hacer algo análogo al multiplicarlo por $f_2(y_2)$ y luego integrar para obtener:
\begin{equation*}
	F(y_1) = \int_{-\infty}^{\infty} F(y_1|y_2) f_2(y_2) dy_2
\end{equation*}

La cantidad $f_2(y_2)dy_2$ se puede considerar como la probabilidad aproximada de que $Y_2$ tome un valor en un pequeño intervalo alrededor de $y_2$, y la integral es una suma generalizada.

Ahora, de consideraciones previas, sabemos que
\begin{equation*}
	\begin{aligned}
		F(y_1) &= \int_{-\infty}^{y_1} f_1(t_1) dt_1 = \int_{-\infty}^{y_1} \left[ \int_{-\infty}^{\infty} f(t_1,y_2) dy_2 \right] dt_1\\
		&= \int_{-\infty}^{\infty} \int_{-\infty}^{y_1} f(t_1, y_2) dt_1 dy_2
	\end{aligned}
\end{equation*}

De estas dos expresiones para $F(y_1)$ debemos tener
\begin{equation*}
	F(y_1|y_2)f_2(y_2) = \int_{-\infty}^{y_1} f(t_1,y_2) dt_1
\end{equation*}

O bien,
\begin{equation*}
	F(y_1|y_2) = \int_{-\infty}^{y_1} \frac{f(t_1,y_2)}{f_2(y_2)} dt_1
\end{equation*}

Al integrando de esta expresión lo llamaremos \textit{función de densidad condicional} de $Y_1$ dado que $Y_2=y_2$, y lo denotaremos por $f(y_1,y_2)$.

\begin{tcolorbox}\begin{defn}\label{def:57}
	Sean $Y_1$ Y $Y_2$ variables aleatorias continuas conjuntas con densidad conjunta $f(y_1, y_2)$ y densidades marginales $f_1(y_1)$ y $f_2(y_2)$, respectivamente. Para cualquier $y_2$ tal que $f_2(y_2) > 0$, la densidad condicional de $Y_1$ dada $Y_2=y_2$ está dada por:
	\begin{equation}
		f(y_1|y_2) = \frac{f(y_1,y_2)}{f_2(y_2)}
	\end{equation}
	
	Y, para cualquier $y_1$ tal que $f_1(y_1) > 0$, la densidad condicional de $Y_2$ dada $Y_1=y_1$ está dada por:
	\begin{equation}
		f(y_2|y_1) = \frac{f(y_1,y_2)}{f_1(y_1)}
	\end{equation}
\end{defn}\end{tcolorbox}

Observe que la densidad condicional $f(y_1|y_2)$ es indefinida para toda $y_2$ tal que $f_2(y_2)=0$. Del mismo modo, $f(y_2|y_1)$ es indefinida si $y_1$ es tal que $f_1(y_1)=0$

\begin{ex}\label{ex:58}
	Una máquina automática expendedora de bebidas tiene una cantidad aleatoria $Y_2$ de bebida en existencia al principio de una día determinado y dosifica una cantidad aleatoria $Y_1$ durante el día (con cantidades expresadas en galones). La máquina no se reabastece durante el día y, en consecuencia, $Y_1 \le Y_2$. Se ha observado que $Y_1$ y $Y_2$ tienen una densidad conjunta dada por:
	\begin{equation*}
		f(y_1,y_2) = \begin{cases}
			\displaystyle\frac{1}{2} & 0 \le y_1 \le y_2 \le 2\\
			0 & \text{en cualquier otro punto}
		\end{cases}
	\end{equation*}
	
	Esto es, los puntos $(y_1,y_2)$ están uniformemente distribuidos en el triángulo con las fronteras dadas. Encuentre la densidad condicional de $Y_1$ dada $Y_2=y_2$. Evalúa la probabilidad de que se venda menos de $\frac{1}{2}$ galón, dado que la máquina contiene 1,5 galones al empezar el día.
\end{ex}

La densidad marginal de $Y_2$ está dada por:
\begin{equation*}
	f_2(y_2) = \int_{-\infty}^{\infty} f(y_1,y_2) dy_1
\end{equation*}

Entonces,
\begin{equation*}
	f_2(y_2) = \begin{cases}
		\displaystyle \int_{0}^{y_2}  \left(\frac{1}{2}\right) dy_1 = \left(\frac{1}{2}\right) y_2 & 0 \le y_2 \le 2\\
		\displaystyle \int_{-\infty}^{\infty} 0 dy_1 = 0 & \text{en cualquier otro punto}
	\end{cases}
\end{equation*}

Observe que $f_2(y_2) > 0$ si y sólo si $0 < y_2 \le 2$. Entonces, para cualquier $0 < y_2 \le 2$, usando la definición \ref{def:57}
\begin{equation*}
	f(y_1|y_2) = \frac{f(y_1,y_2)}{f_2(y_2)} = \frac{\frac{1}{2}}{\left(\frac{1}{2}\right) (y_2)} = \frac{1}{y_2}, \qquad 0 \le y_1 \le y_2
\end{equation*}

También, $f(y_1|y_2)$ es indefinida si $y_2 \le 0$ o $y_2 > 2$. La probabilidad de interés es:
\begin{equation*}
	P\left(Y_1 \le \frac{1}{2}|Y_2 = 1.5\right) = \int_{-\infty}^{\frac{1}{2}} f(y_1|y_2 = 1.5) dy_1 = \int_{0}^{\frac{1}{2}} \frac{1}{1.5} dy_1 = \frac{\frac{1}{2}}{1.5} = \frac{1}{3}
\end{equation*}

Si la máquina contiene 2 galones al empezar el día, entonces
\begin{equation*}
	P\left(Y_1 \le \frac{1}{2}| Y_2 = 2\right) = \int_{0}^{\frac{1}{2}} \frac{1}{2} dy_1 = \frac{1}{4}
\end{equation*}

Por tanto, la probabilidad condicional de que $Y_1 \le \frac{1}{2}$ dado que $Y_2 = y_2$ cambia de manera apreciable dependiendo de la selección particular de $y_2$.

\subsection{Variables aleatorias independientes}

Dos eventos $A$ y $B$ son independientes si $P(A \cap B) = P(A) \times P(B)$. Cuando estudiemos variables aleatorias, si $a < b$ y $c < d$ es frecuente que nos interesemos en eventos del tipo $(a < Y_1 \le b) \cap (c < Y_2 \le d)$. Por consistencia con la definición anterior de eventos independientes, si $Y_1$ y $Y_2$ son independientes, nos gustaría tener:
\begin{equation*}
	P(a < Y_1 \le b, c < Y_2 \le d) = P(a < Y_1 \le b) \times P(c < Y_2 \le d)
\end{equation*}

Para cualquier elección de números reales $a < b$ y $c < d$. Esto es, si $Y_1$ y $Y_2$ son independientes, la probabilidad conjunta se puede escribir como el producto de las probabilidades marginales. Esta propiedad se satisface si $Y_1$ y $Y_2$ son independientes en el sentido detallado en la siguiente definición.

\begin{tcolorbox}\begin{defn}\label{def:58}
	Sea $Y_1$ que tiene una función de distribución $F_1(y_1)$ y sea $Y_2$ que tiene una función de distribución $F_2(y_2)$, y $F(y_1,y_2)$ es la función de distribución conjunta de $Y_1$ y $Y_2$. Entonces se dice que $Y_1$ y $Y_2$ son \textbf{independientes} si y solo si:
	\begin{equation}
		F(y_1,y_2) = F_1(y_1) \cdot F_2(y_2)
	\end{equation}
	
	Para todo par de números reales $(y_1,y_2)$
	
	Si $Y_1$ y $Y_2$ no son independientes, se dice que son \textbf{dependientes}.
\end{defn}\end{tcolorbox}

Por lo general, es cómodo establecer la presencia o ausencia de independencia, por medio del resultado del siguiente teorema. Se omite la demostración.

\begin{thm}
	Si $Y_1$ y $Y_2$ son variables aleatorias discretas con función de probabilidad conjunta $p(y_1,y_2)$ y funciones de probabilidad marginal $p_1(y_1)$ y $p_2(y_2)$, respectivamente, entonces $Y_1$ y $Y_2$ son independientes si y sólo si
	\begin{equation}
		p(y_1,y_2) = p_1(y_1) \cdot p_2(y_2)
	\end{equation}
	
	Para todos los pares de números reales $(y_1,y_2)$
	
	Si $Y_1$ y $Y_2$ son variables aleatorias continuas con función de densidad conjunta $f_1(y_1,y_2)$ y funciones de densidad marginal $f_1(y_1)$ y $f_2(y_2)$, respectivamente, entonces $Y_1$ y $Y_2$ son independientes si y solo si
	\begin{equation}
		f(y_1,y_2) = f_1(y_1) \cdot f_2(y_2)
	\end{equation}
	
	Para todos los pares de números reales $(y_1, y_2)$.
\end{thm}

A continuación ilustramos el concepto de independencia con algunos ejemplos.

\begin{ex}\label{ex:59}
	Para el problema de tirar un dado, demuestre que $Y_1$ y $Y_2$ son independientes.
\end{ex}

En este problema a cada uno de los 36 puntos muestrales se le dio probabilidad $\frac{1}{36}$. Considere, por ejemplo, el punto $(1,2)$. Sabemos que $p(1,2) = \frac{1}{36}$. También, $p_1(1) = P(Y_1 = 1) = \frac{1}{6}$ y $p_2(2) = P(Y_2 = 2) = \frac{1}{6}$. Por tanto,
\begin{equation*}
	p(1,2) = p_1(1) \cdot p_2(2)
\end{equation*}

Lo mismo es cierto para todos los demás valores de $y_1$ y $y_2$, de lo cual se deduce que $Y_1$ y $Y_2$ son independientes.

\begin{ex}\label{ex:510}
	Consulte el ejemplo \ref{ex:55}, ¿El número de republicanos en la muestra es independiente del número de demócratas? (¿Es $Y_1$ independiente de $Y_2$?)
\end{ex}

La independencia de variables aleatorias discretas requiere que $p(y_1, y_2) = p_1(y_1) \cdot p_2(y_2)$ para toda selección $(y_1, y_2)$. Entonces, si esta igualdad es violada para cualquier par de valores $(y_1, y_2)$, las variables aleatorias son dependientes. Al observar la esquina superior izquierda de la tabla \ref{tab:52}, veremos que:
\begin{equation*}
	P(0,0) = 0
\end{equation*}

Pero $p_1(0) = \frac{3}{15}$ y $p_2(0) = \frac{6}{15}$. En consecuencia,
\begin{equation*}
	p(0,0) \ne p_1(0) \cdot p_2(0)
\end{equation*}

De modo que $Y_1$ y $Y_2$ son dependientes.

\begin{ex}\label{ex:511}
	Sea:
	\begin{equation*}
		f(y_1,y_2) = \begin{cases}
			6y_1 y_2^2 & 0 \le y_1 \le 1, 0 \le y_2 \le 2\\
			0 & \text{en cualquier otro punto}
		\end{cases}
	\end{equation*}
	
	Demuestre que $Y_1$ y $Y_2$ son independientes
\end{ex}

Tenemos:
\begin{equation*}
	f_1(y_1) = \begin{cases}
		\displaystyle \int_{-\infty}^{\infty} f(y_1, y_2) dy_2 = \int_{0}^{1} 6y_1 y_2^2 dy_2 = 6y_1 \left(\frac{y_2^3}{3}\bigg|_0^1\right) = 2y_1 & 0 \le y_1 \le 1\\
		\displaystyle \int_{-\infty}^{\infty} f(y_1,y_2) dy_2 = \int_{-\infty}^{\infty} 0 dy_1 = 0 & \text{en cualquier otro punto}
	\end{cases}
\end{equation*}

Del mismo modo,
\begin{equation*}
	f_2(y_2) = \begin{cases}
		\displaystyle \int_{-\infty}^{\infty} f(y_1,y_2) dy_1 = \int_{0}^{1} 6y_1 y_2^2 dy_1 = 3y_2^2 & 0 \le y_2 \le 1\\
		\displaystyle \int_{-\infty}^{\infty} f(y_1,y_2) dy_1 = \int_{-\infty}^{\infty} 0 dy_1 = 0 & \text{en cualquier otro punto}
	\end{cases}
\end{equation*}

En consecuencia,
\begin{equation*}
	f(y_1, y_2) = f_1(y_1) \cdot f_2(y_2)
\end{equation*}

Para todos los números reales $(y_1,y_2)$ y, por tanto, $Y_1$ y $Y_2$ son independientes.

\begin{ex}\label{ex:512}
	Sea
	\begin{equation*}
		f(y_1,y_2) = \begin{cases}
			2 & 0 \le y_2 \le y_1 \le 1\\
			0 & \text{en cualquier otro punto}
		\end{cases}
	\end{equation*}
	
	Demuestre que $Y_1$ y $Y_2$ son dependientes.
\end{ex}

Vemos que $f(y_1,y_2) = 2$ sobre la región sombreada que se ve en la figura \ref{fig:57}. Por tanto,
\begin{equation*}
	f_1(y_1) = \begin{cases}
		\displaystyle \int_{0}^{y_1} 2dy_2 = 2y_1 \bigg|_0^{y_1} = 2y_1 & 0 \le y_1 \le 1\\
		0 & \text{en cualquier otro punto}
	\end{cases}
\end{equation*}
\begin{figure}[h!]
	\centering
	\caption{}
	\label{fig:57}
	\includegraphics[width=0.5\linewidth]{Anexo/screenshot008}
\end{figure}

\break

Del mismo modo,
\begin{equation*}
	f_2(y_2) = \begin{cases}
		\displaystyle \int_{y_2}^{1} 2dy_1 = 2y_1\bigg|_{y_2}^1 = 2(1-y_2) & 0 \le y_2 \le 1\\
		0 & \text{en cualquier otro punto}
	\end{cases}
\end{equation*}

Por tanto,
\begin{equation*}
	f(y_1,y_2) \ne f_1(y_1) \cdot f_2(y_2)
\end{equation*}

Para algún par de números reales $(y_1,y_2)$ y, por tanto, $Y_1$ y $Y_2$ son dependientes.

Observará una diferencia distinta en los límites de integración empleados para hallar las funciones de densidad marginal obtenidas en los ejemplos \ref{ex:511} y \ref{ex:512}. Los límites de integración para $y_2$, comprendidos en hallar la densidad marginal de $Y_1$ en el ejemplo \ref{ex:512}, dependían de $y_1$. En contraste, los límites de integración fueron constantes cuando determinamos las funciones de densidad marginal en el ejemplo \ref{ex:511}. Si los límites de integración son constantes, el siguiente teorema proporciona una forma fácil de demostrar la independencia de dos variables aleatorias.

\begin{thm}\label{thm:55}
	Sean $Y_1$ y $Y_2$ que tienen una densidad conjunta $f(y_1,y_2)$ que es positiva si y sólo si $a \le y_1 \le b$ y $c \le y_2 \le d$, para constantes $a$, $b$, $c$ y $d$; y $f(y_1,y_2) = 0$ en otro caso. Entonces $Y_1$ y $Y_2$ son variables aleatorias independientes si y solo si
	\begin{equation}
		f(y_1,y_2) = g(y_1) \cdot h(y_2)
	\end{equation}
	
	Donde $g(y_1)$ es una función no negativa de $y_1$ solamente y $h(y_2)$ es una función no negativa de $y_2$ solamente.
\end{thm}

La demostración de este teorema se omite. El beneficio clave del resultado dado en el teorema \ref{thm:55} es que en realidad no necesitamos obtener las densidades marginales. De hecho, las funciones $g(y_1)$ y $h(y_2)$ no necesitan ser funciones de densidad (aún cuando sean múltiplos constantes de las densidades marginales, deberíamos tomarnos la molestia de determinar éstas).

\begin{ex}\label{ex:513}
	Sean $Y_1$ y $Y_2$ que tienen una densidad conjunta dada por:
	\begin{equation*}
		f(y_1, y_2) = \begin{cases}
			2y_1 & 0 \le y_1 \le 1, 0 \le y_2 \le 1\\
			0 & \text{en cualquier otro punto}
		\end{cases}
	\end{equation*}
	
	¿$Y_1$ y $Y_2$ son variables independientes?
\end{ex}

Observe que $f(y_1,y_2)$ es positiva si y sólo si $0 \le y_1 \le 1$ y $0 \le y_2 \le 1$. Además, $f(y_1,y_2) = g(y_1) \cdot h(y_2)$, donde:
\begin{equation*}
	g(y_1) = \begin{cases}
		y_1 & 0 \le y_1 \le 1\\
		0 & \text{en cualquier otro punto}
	\end{cases} \quad y \quad h(y_2) = \begin{cases}
		2 & 0 \le y_2 \le 1\\
		0 & \text{en cualquier otro punto}
	\end{cases}
\end{equation*}

Por tanto $Y_1$ y $Y_2$ son variables aleatorias independientes. Observe que $g(y_1)$ y $h(y_2)$, como aquí se definen, \textit{no son} funciones de densidad, aún cuando $2g(y_1)$ y $\frac{h(y_2)}{2}$ sean densidades.

\begin{ex}\label{ex:514}
	Consulte el ejemplo \ref{ex:54}, ¿$Y_1$, la cantidad en existencia, es independiente de $Y_2$, la cantidad vendida?
\end{ex}

Como la función de densidad es positiva si y sólo si $0 \le y_2 \le y_1 \le 1$, no existen constantes $a$, $b$, $c$ y $d$ tales que la densidad sea positiva en la región $a \le y_1 \le b, c \le y_2 \le d$. Entonces, el teorema \ref{thm:55} no se puede aplicar. No obstante, se puede demostrar que $Y_1$ y $Y_2$ son variables aleatorias dependientes porque la densidad conjunta no es el producto de las densidades marginales.

Las definiciones \ref{def:58} fácilmente se pueden generalizar a $n$ dimensiones. Suponga que tenemos $n$ variables aleatorias, $Y_1$, $Y_2$, ..., $Y_n$, donde $Y_i$ tiene función de distribución $F_i(y_i)$, para $i = 1, 2, ..., n$; donde $Y_1$, $Y_2$, ..., $Y_n$ tienen función de distribución conjunta $F(y_,1 y_2, ..., y_n)$. Entonces $Y_1$, $Y_2$, ..., $Y_n$ son independientes si y sólo si:
\begin{equation}
	F(y_1, y_2, ..., y_n) = F_1(y_1) \cdot ... \cdot F_n(y_n)
\end{equation}

Para todos los números reales $y_1$, $y_2$, ..., $y_n$, con las formas equivalentes obvias para los casos discretos y continuos.

\subsection{El valor esperado de una función de variables aleatorias}

Para unificar la siguiente definición sólo se necesita construir el equivalente multivariante del caso univariante.

\begin{tcolorbox}\begin{defn}\label{def:59}
		Sea $g(Y_1, Y_2, ..., Y_n)$ una función de las variables aleatorias discretas, $Y_1$, $Y_2$, ..., $Y_k$, que tienen función de probabilidad $p(y_1, y_2, ..., y_k)$. Entonces el \textbf{valor esperado} de $g(Y_1, Y_2, ..., Y_k)$ es:
		\begin{equation}
			E[g(Y_1, Y_2, ..., Y_k)] = \sum_{\text{toda } y_k} \cdots \sum_{\text{toda } y_2} \sum_{\text{toda } y_1} g(y_1, y_2, ..., y_k) \cdot p(y_1, y_2, ..., y_k)
		\end{equation}
	
		Si $Y_1$, $Y_2$, ..., $Y_k$ son variables aleatorias continuas con función de densidad conjunta $f(y_1, y_2, ..., y_k)$, entonces:
		\begin{equation}
			E[g(Y_1, Y_2, ..., Y_k)] = \int_{-\infty}^{\infty} \cdots \int_{-\infty}^{\infty} \int_{-\infty}^{\infty} g(y_1, y_2, ..., y_k) \cdot f(y_1, y_2, ..., y_k) dy_1 dy_2 \cdot\cdot\cdot dy_k
		\end{equation}
\end{defn}\end{tcolorbox}

\begin{ex}\label{ex:515}
	Considere que $Y_1$ y $Y_2$ tienen una densidad conjunta dada por:
	\begin{equation*}
		f(y_1, y_2) = \begin{cases}
			2y_1 & 0 \le y_1 \le 1, 0 \le y_2 \le 1\\
			0 & c.o.c.
		\end{cases}
	\end{equation*}

	Encuentre $E(Y_1 Y_2)$
\end{ex}

De la definición \ref{def:59} obtenemos:
\begin{flalign*}
	E(Y_1 Y_2) &= \int_{-\infty}^{\infty} y_1 y_2 f(y_1,y_2) dy_1 dy_2 = \int_{0}^{1} \int_{0}^{1} y_1 y_2 (2y_1) dy_1 dy_1\\
	&= \int_{0}^{1} y_2 \left( \frac{2 y_1^2}{3} \bigg|_0^1 \right) dy_2 = \int_{0}^{1} \left( \frac{2}{3} \right) y_2 dy_2 = \frac{2}{3} \frac{y_2^2}{2} \bigg|_0^1 = \frac{1}{3}
\end{flalign*}

Demostraremos que la definición \ref{def:59} es consistente con la definición del valor esperado de una variable aleatoria univariante. Considere dos variables aleatorias $Y_1$ y $Y_2$ con función de densidad $f(y_1, y_2)$. Deseamos hallar el valor esperado de $g(Y_1, Y_2) = Y_1$.

De la definición \ref{def:59} tenemos:
\begin{flalign*}
	E(Y_1) &= \int_{-\infty}^{\infty} \int_{-\infty}^{\infty} y_1 f(y_1,y_2) dy_2 dy_1\\
	&= \int_{-\infty}^{\infty} y_1 \left[ \int_{-\infty}^{\infty} f(y_1,y_2) dy_2 \right] dy_1
\end{flalign*}

La cantidad dentro de los paréntesis rectangulares, por definición, es la función de densidad marginal para $Y_1$. Por tanto, obtenemos:
\begin{equation}
	E(Y_1) = \int_{-\infty}^{\infty} y_1 f_1(y_1) dy_1
\end{equation}

Que es la definición del valor esperado de una variable aleatoria univariante.

\begin{ex}\label{ex:516}
	Considere que $Y_1$ y $Y_2$ tienen una densidad conjunta dada por:
	\begin{equation*}
		f(y_1,y_2) = \begin{cases}
			2y_1 & 0 \le y_1 \le 1, 0 \le y_2 \le 1\\
			0 & c.o.c.
		\end{cases}
	\end{equation*}

	Encuentre el valor esperado de $Y_1$
\end{ex}

Solución:
\begin{flalign*}
	E(Y_1) &= \int_{0}^{1} \int_{0}^{1} y_1 (2y_1) dy_1 dy_2\\
	&= \int_{0}^{1} \left( \frac{2 y_1^2}{3} \bigg|_0^1 \right) dy_2 = \int_{0}^{1} \frac{2}{3} dy_2 = \frac{2}{3} y_2 \bigg|_0^1 = \frac{2}{3}
\end{flalign*}

Al consultar la figura \ref{fig:56} y calcular el valor esperado de $Y_1$ vemos que el valor $E(Y_1) = \frac{2}{3}$ parece ser bastante razonable.

\begin{ex}\label{ex:517}
	En la figura \ref{fig:56} el valor medio de $Y_2$ parece ser igual a $0.5$. Confirmemos este cálculo visual. Encuentre $E(Y_2)$
\end{ex}

Solución:
\begin{flalign*}
	E(Y_2) &= \int_{0}^{1} \int_{0}^{1} y_2 (2 y_1) dy_1 dy_2 = \int_{0}^{1} y_2 \left( \frac{2  y_1^2}{2} \bigg|_0^1 \right) dy_2\\
	&= \int_{0}^{1} y_2 dy_2 = \frac{y_2^2}{2} \bigg|_0^1 = \frac{1}{2}
\end{flalign*}

\begin{ex}\label{ex:518}
	Sean $Y_1$ y $Y_2$ variables aleatorias con función de densidad:
	\begin{equation*}
		f(y_1,y_2) = \begin{cases}
			2y_1 & 0 \le y_1 \le 1, 0 \le y_2 \le 1\\
			0 & c.o.c.
		\end{cases}
	\end{equation*}

	Encuentre $V(Y_1)$
\end{ex}

La densidad marginal para $Y_1$ obtenida en el ejemplo \ref{ex:56} es:
\begin{equation*}
	f_1(y_1) = \begin{cases}
		2y_1 & 0 \le y_1 \le 1\\
		0 & c.o.c.
	\end{cases}
\end{equation*}

Entonces $V(Y_1) = E(Y_1^2) - [E(Y_1)]^2$, y
\begin{equation*}
	E(Y_1^k) = \int_{-\infty}^{\infty} y_1^k f_1(y_1) dy_1 = \int_{0}^{1} y_1^k (2y_1) dy_1 = \frac{2y_1^{k+2}}{k+2} \bigg|_0^1 = \frac{2}{k+2}
\end{equation*}

Si hacemos $k=1$ y $k=2$, se deduce que $E(Y_1)$ y $E(Y_1^2)$ son $\frac{2}{3}$ y $\frac{1}{2}$, respectivamente. Entonces $V(Y_1) = E(Y_1^2) - [E(Y_1)]^2 = \frac{1}{2} - (\frac{2}{3})^2 = \frac{1}{18}$

\begin{ex}\label{ex:519}
	Del proceso para producir una sustancia química industrial se obtiene un producto que contiene dos tipos de impurezas. Para una muestra específica proveniente de este proceso, denotemos con $Y_1$ la proporción de impurezas en la muestra y con $Y_2$ la proporción de impurezas tipo I entre todas las impurezas halladas. Suponga que la distribución conjunta de $Y_1$ y $Y_2$ puede ser modelada con la siguiente función de densidad de probabilidad:
	\begin{equation*}
		f(y_1,y_2) = \begin{cases}
			2(1-y_1) & 0 \le y_1 \le 1, 0 \le y_2 \le 1\\
			0 & c.o.c.
		\end{cases}
	\end{equation*}

	Encuentre el valor esperado de la proporción de impurezas tipo I de la muestra.
\end{ex}

Como $Y_1$ es la proporción de impurezas en la muestra y $Y_2$ es la proporción de impurezas tipo I entre las impurezas muestrales, se deduce que $Y_1 Y_2$ es la proporción de impurezas tipo I en toda la muestra. Entonces, buscamos hallar $E(Y_1 Y_2)$:
\begin{flalign*}
	E(Y_1 Y_2) &= \int_{0}^{1} \int_{0}^{1} 2y_1 y_2 (1 - y_1) dy_2 dy_1 = 2 \int_{0}^{1} y_1 (1 - y_1) \left( \frac{1}{2} \right) dy_1\\
	&= \int_{0}^{1} (y_1 - y_1^2) dy_1 = \left( \frac{y_1^2}{2} - \frac{y_1^3}{3} \right) \bigg|_0^1 = \frac{1}{2} - \frac{1}{3} = \frac{1}{6}
\end{flalign*}

Por tanto, esperaríamos que $\frac{1}{6}$ de la muestra estuviera formado por impurezas tipo I.

\subsection{Teoremas especiales}

Los teoremas que facilitan el cálculo del valor esperado de una constante, el valor esperado de una constante por una función de variables aleatorias y el valor esperado de la suma de funciones de variables aleatorias son semejantes a los del caso univariante.

\begin{thm}\label{thm:56}
	Sea $c$ una constante. Entonces:
	\begin{equation}
		E(c) = c
	\end{equation}
\end{thm}

\begin{thm}\label{thm:57}
	Sea $g(Y_1, Y_2)$ una función de las variables aleatorias $Y_1$ y $Y_2$ y sea $c$ una constante. Entonces:
	\begin{equation}
		E[cg(Y_1,Y_2)] = cE[g(Y_1,Y_2)]
	\end{equation}
\end{thm}

\begin{thm}\label{thm:58}
	Sean $Y_1$ y $Y_2$ variables aleatorias y $g_1(Y_1, Y_2)$, $g_2(Y_1, Y_2)$, ..., $g_k(Y_1, Y_2)$ funciones de $Y_1$ y $Y_2$. Entonces:
	\begin{equation}
		E[g_1(Y_1, Y_2) + g_2(Y_1,Y_2) + ... + g_k(Y_1, Y_2)] = E[g_1(Y_1, Y_2)] + E[g_2(Y_1, Y_2)] + ... + E[g_k(Y_1, Y_2)]
	\end{equation}
\end{thm}

\begin{ex}\label{ex:520}
	Consulte el ejemplo \ref{ex:54}. La variable aleatoria $Y_1 - Y_2$ denota la cantidad proporcional de gasolina remanente al fin de la semana. Encuentre $E(Y_1 - Y_2)$
\end{ex}

Empleando el teorema \ref{thm:58} con $g_1(Y_1, Y_2) = Y_1$ y $g_2(Y_1, Y_2) = -Y_2$ vemos que:
\begin{equation*}
	E(Y_1 - Y_2) = E(Y_1) + E(-Y_2)
\end{equation*}

Se aplica el teorema \ref{thm:57}, dando $E(-Y_2) = -E(Y_2)$, por tanto,
\begin{equation*}
	E(Y_1 - Y_2) = E(Y_1) - E(Y_2)
\end{equation*}

También,
\begin{flalign*}
	E(Y_1) &= \int_{0}^{1} \int_{0}^{y_1} y_1 (3y_1) dy_2 dy_1 = \int_{0}^{1} 3y_1^3 dy_1 = \frac{3}{4} \bigg|_0^1 = \frac{3}{4}\\
	E(Y_2) &= \int_{0}^{1} \int_{0}^{y_1} y_2 (3y_1) dy_2 dy_1 = \int_{0}^{1} 3y_1 \left( \frac{y_2^2}{2} \bigg|_0^1 \right) dy_1 = \int_{0}^{1} \frac{3}{2} y_1^3 dy_1\\
	&= \frac{3}{8} y_1^4 \bigg|_0^1 = \frac{3}{8}
\end{flalign*}

Entonces,
\begin{equation*}
	E(Y_1 - Y_2) = \frac{3}{4} - \frac{3}{8} = \frac{3}{8}
\end{equation*}

De modo que esperaríamos que $\frac{3}{8}$ del tanque esté lleno al final de las ventas de la semana.

Si las variables aleatorias motivo de estudio son independientes, en ocasiones podemos simplificar el trabajo necesario para hallar valores esperados. El siguiente teorema es muy útil en ese sentido.

\begin{thm}\label{thm:59}
	Sean $Y_1$ y $Y_2$ variables aleatorias independientes y sean $g(Y_1)$ y $h(Y_2)$ funciones sólo de $Y_1$ y $Y_2$ respectivamente. Entonces:
	\begin{equation}
		E[g(Y_1) \cdot h(Y_2)] = E[g(Y_1)] \cdot E[h(Y_2)]
	\end{equation}

	Siempre que existan los valores esperados.
\end{thm}

Daremos la demostración del resultado para el caso continuo. Denotemos con $f(y_1,y_2)$ la densidad conjunta de $Y_1$ y $Y_2$. El producto $g(Y_1) \cdot h(Y_2)$ es una función de $Y_1$ y $Y_2$. Entonces, por la definición \ref{def:59} y la suposición de que $Y_1$ y $Y_2$ son independientes,
\begin{flalign*}
	E[g(Y_1) \cdot h(Y_2)] &= \int_{-\infty}^{\infty} g(y_1) h(y_2) f(y_1,y_2) dy_2 dy_1\\
	&= \int_{-\infty}^{\infty} g(y_1) h(y_2) f_1(y_1) f_2(y_2) dy_2 dy_1\\
	&= \int_{-\infty}^{\infty} g(y_1) f_1(y_1) \left[ \int_{-\infty}^{\infty} h(y_2) f_2(y_2) dy_2 \right] dy_1\\
	&= \int_{-\infty}^{\infty} g(y_1) f_1(y_1) E[h(Y_2)] dy_1\\
	&= E[h(Y_2)] \int_{-\infty}^{\infty} g(y_1) f_1(y_1) dy_1 = E[g(Y_1)] \cdot E[h(Y_2)]
\end{flalign*}

La demostración para el caso discreto sigue un modo análogo.

\begin{ex}\label{ex:521}
	Consulte el ejemplo \ref{ex:519}. En el ejemplo encontramos $E(Y_1 Y_2)$ directamente. Al investigar la forma de la función de densidad conjunta dada ahí, podemos ver que $Y_1$ y $Y_2$ son independientes. Encuentre $E(Y_1 Y_2)$ con el uso del resultado de que $E(Y_1 Y_2) = E(Y_1) \cdot E(Y_2)$ si $Y_1$ y $Y_2$ son independientes.
\end{ex}

La función de densidad conjunta está dada por
\begin{equation*}
	f(y_1,y_2) = \begin{cases}
		2(1-y_1) & 0 \le y_1 \le 1, 0 \le y_2 \le 1\\
		0 & c.o.c.
	\end{cases}
\end{equation*}

Entonces,
\begin{equation*}
	f_1(y_1) = \begin{cases}
		\displaystyle \int_{0}^{1} 2(1-y_1) dy_2 = 2(1-y_1) & 0 \le y_1 \le 1\\
		\displaystyle 0 & \text{en cualquier otro punto}
	\end{cases}
\end{equation*}

y,
\begin{equation*}
	f_2(y_2) = \begin{cases}
		\displaystyle \int_{0}^{1} 2(1-y_1) dy_1 = -(1-y_1)^2 \bigg|_0^1 = 1 & 0 \le y_2 \le 1\\
		\displaystyle 0 & \text{en cualquier otro punto}
	\end{cases}
\end{equation*}

Tenemos entonces,
\begin{flalign*}
	E(Y_1) &= \int_{0}^{1} y_1 [2(1-y_1)] dy_1 = 2 \left( \frac{y_1^2}{2} - \frac{y_1^3}{3} \right) \bigg|_0^1 = \frac{1}{3}\\
	E(Y_2) &= \frac{1}{2}
\end{flalign*}

Porque $Y_2$ está uniformemente distribuida en $(0,1)$.

Se deduce que 
\begin{equation*}
	E(Y_1 Y_2) = E(Y_1) \cdot E(Y_2) = \left( \frac{1}{3} \right) \cdot \left( \frac{1}{2} \right) = \frac{1}{6}
\end{equation*}

Lo que concuerda con la respuesta del ejemplo \ref{ex:519}

\subsection{Covarianza de dos variables aleatorias}\label{sec:57}

Intuitivamente consideramos la dependencia de dos variables aleatorias $Y_1$ y $Y_2$ como un proceso en el que una de las variables, por ejemplo $Y_1$, aumenta o disminuye cuando $Y_2$ cambia. Concentraremos nuestra atención en dos medidas de dependencia: la \textbf{covarianza} entre dos variables aleatorias y su \textbf{coeficiente de correlación}. En la figura \ref{fig:58}$\text{(a)}$ y $\text{(b)}$ se muestran las gráficas de los valores observados de dos variables, $Y_1$ y $Y_2$, para muestras de $n=10$ unidades experimentales tomadas de cada una de las dos poblaciones. Si todos los puntos caen a lo largo de una recta, como indica la figura \ref{fig:58}$\text{(a)}$, $Y_1$ y $Y_2$ son obviamente dependientes. En contraste, la figura \ref{fig:58}$\text{(b)}$ indica poca o ninguna dependencia entre $Y_1$ y $Y_2$.

Suponga que conocemos los valores de $E(Y_1) = \mu_1$ y $E(Y_2) = \mu_2$ y localizamos este punto en la gráfica de la figura \ref{fig:58}. Ahora localizamos un punto graficado, $(y_1, y_2)$, en la figura \ref{fig:58}$\text{(a)}$ y medimos las desviaciones $(y_1 - \mu_1)$ y $(y_2 - \mu_2)$. Ambas desviaciones toman el mismo signo algebraico para cualquier punto, $(y_1, y_2)$, y su producto $(y_1 - \mu_1)\cdot(y_2 - \mu_2)$ es positivo. Los puntos a la derecha de $\mu_1$ generan pares de desviaciones positivas; los puntos a la izquierda producen pares de desviaciones negativas; y el promedio del producto de las desviaciones $(y_1 - \mu_1) \cdot (y_2 - \mu_2)$ es grande y positivo. Si la relación lineal indicada en la figura \ref{fig:58}$\text{(a)}$ se hubiera inclinado hacia abajo a la derecha, todos los pares de desviaciones correspondientes hubieran sido de signo contrario y el valor promedio de $(y_1 - \mu_1) \cdot (y_2 - \mu_2)$ hubiera sido un número negativo grande.
\begin{figure}[h!]
	\centering
	\caption{}
	\label{fig:58}
	\includegraphics[width=0.45\linewidth]{Anexo/screenshot009}
\end{figure}

\break

La situación que acabamos de describir no ocurre para la figura \ref{fig:58}$\text{(b)}$, donde existe poca dependencia entre $Y_1$ y $Y_2$. Sus desviaciones correspondientes $(y_1 - \mu_1)$ y $(y_2 - \mu_2)$ tomarán el mismo signo algebraico para algunos puntos y signos opuestos para otros. Entonces, el producto $(y_1 - \mu_1) \cdot (y_2 - \mu_2)$ será positivo par algunos puntos, negativo para otros y promediará algún valor cercano a cero.

Es evidente que el valor promedio de $(Y_1 - \mu_1) \cdot (Y_2 - \mu_2)$ proporciona una medida de la dependencia lineal entre $Y_1$ y $Y_2$. Esta cantidad, $E[(Y_1 - \mu_1) \cdot (Y_2 - \mu_2)]$, se denomina \textbf{covarianza} de $Y_1$ y $Y_2$.

\begin{tcolorbox}\begin{defn}\label{def:510}
		Si $Y_1$ y $Y_2$ son variables aleatorias con medias $\mu_1$ y $\mu_2$, respectivamente, la \textbf{covarianza} de $Y_1$ y $Y_2$ es:
		\begin{equation}
			\Cov(Y_1, Y_2) = E[(Y_1 - \mu_1) \cdot (Y_2 - \mu_2)]
		\end{equation}
\end{defn}\end{tcolorbox}

Cuanto mayor sea el valor absoluto de la covarianza de $Y_1$ y $Y_2$, mayor será la dependencia lineal entre $Y_1$ y $Y_2$. Los valores positivos indican que $Y_1$ aumenta cuando $Y_2$ aumenta; los valores negativos indican que $Y_1$ disminuye cuando $Y_2$ aumenta. Un valor cero de la covarianza indica que las variables son \textit{no correlacionadas} y que no hay dependencia lineal entre $Y_1$ y $Y_2$.

Desafortunadamente, es difícil utilizar la covarianza como medida absoluta de dependencia porque su valor depende de la escala de medición. En consecuencia, es difícil determinar a primera vista si una covarianza particular es grande o pequeña. Este problema se puede eliminar al estandarizar su valor y usar el \textit{coeficiente de correlación}, $\rho$, una cantidad relacionada con la varianza y que se define como:
\begin{equation}
	\rho = \frac{\Cov(Y_1 ,Y_2)}{\sigma_1 \sigma_2}
\end{equation}

Donde $\sigma_1$ y $\sigma_2$ son desviaciones estándar de $Y_1$ y $Y_2$ respectivamente.

El signo del coeficiente de correlación es igual al signo de la covarianza. Entonces, $\rho > 0$ indica que $Y_2$ aumenta a medida que $Y_1$ aumenta, y $\rho = +1$ implica correlación perfecta, con todos los puntos cayendo en una recta con pendiente positiva. Un valor de $\rho = 0$ implica cero covarianza y que no hay correlación. Un coeficiente negativo de correlación implica una disminución en $Y_2$ cuando $Y_1$ aumenta, y $\rho = -1$ implica correlación perfecta, con todos los puntos cayendo en una recta con pendiente negativa. Una fórmula computacional conveniente para la covarianza se explica en el siguiente teorema:

\begin{thm}\label{thm:510}
	Si $Y_1$ y $Y_2$ son variables aleatorias con medias $\mu_1$ y $\mu_2$, respectivamente, entonces:
	\begin{equation}
		\begin{aligned}
			\Cov(Y_1, Y_2) &= E[(Y_1 - \mu_1)(Y_2 - \mu_2)] = E(Y_1Y_2) - E(Y_1)E(Y_2)\\
			&= E[(Y_1 - \mu_1)(Y_2 - \mu_2)] = E(Y_1Y_2 - \mu_1Y_2 - \mu_2Y_1 + \mu_1\mu_2)
		\end{aligned}
	\end{equation}

	Del teorema \ref{thm:58}, el valor esperado de una suma es igual a la suma de los valores esperados; y del teorema \ref{def:57}, el valor esperado de una constante multiplicado por una fracción de valores aleatorias es la constante por el valor esperado. Entonces,
	\begin{equation}
		\Cov(Y_1,  Y_2) = E(Y_1, Y_2) - \mu_1 E(Y_2) - \mu_2 E(Y_1) + \mu_1 \mu_2
	\end{equation}

	Como $E(Y_1) = \mu_1$ y $E(Y_2) = \mu_2$, se deduce que:
	\begin{equation}
		\Cov(Y_1, Y_2) = E(Y_1Y_2) - E(Y_1) E(Y_2) = E(Y_1 Y_2) - \mu_1 \mu_2
	\end{equation} 
\end{thm}

\begin{ex}\label{ex:522}
	Consulte el ejemplo \ref{ex:54}. Encuentre la covarianza entre la cantidad en existencia $Y_1$ y la cantidad de ventas $Y_2$.
\end{ex}

Recuerde que $Y_1$ y $Y_2$ tienen función de densidad conjunta dada por:
\begin{equation*}
	f(y_1, y_2) = \begin{cases}
		3y_1 & 0 \le y_2 \le y_1 \le 1\\
		0 & \text{en cualquier otro punto}
	\end{cases}
\end{equation*}

Entonces,
\begin{flalign*}
	E(Y_1 Y_2) &= \int_{0}^{1} \int_{0}^{y_1} y_1 y_2 (3y_1) dy_2 dy_1 = \int_{0}^{1} 3y_1^2 \left( \frac{y_2^2}{2} \bigg|_0^{y_1} \right) dy_1\\
	&= \int_{0}^{1} \frac{3}{2} y_1^4 dy_1 = \frac{3}{2} \left( \frac{y_1^5}{5} \bigg|_0^1 \right) = \frac{3}{10}
\end{flalign*}

Del ejemplo \ref{ex:520} sabemos que $E(Y_1) = \frac{3}{4}$ y $E(Y_2) = \frac{3}{8}$. Entonces, usando el teorema \ref{thm:510}, obtenemos:
\begin{equation*}
	\Cov(Y_1, Y_2) = E(Y_1 Y_2) - E(Y_1) E(Y_2) = \frac{3}{10} - \frac{3}{4} \cdot \frac{3}{8} = 0.30 - 0.28 = 0.02
\end{equation*}

En este ejemplo, los valores grandes de $Y_2$ pueden presentarse sólo con valores grandes de $Y_1$ y la densidad, $f(y_1, y_2)$, es más grande para valores más grandes de $Y_1$. Entonces, intuimos que la covarianza entre $Y_1$ y $Y_2$ debe ser positiva.

\begin{ex}\label{ex:523}
	Tengan $Y_1$ y $Y_2$ densidad conjunta dada por:
	\begin{equation*}
		f(y_1,y_2) = \begin{cases}
			2y_1 & 0 \le y_1 \le 1, 0 \le y_2 \le 1\\
			0 & \text{en cualquier otro punto}
		\end{cases}
	\end{equation*}

	Encuentre la covarianza de $Y_1$ y $Y_2$
\end{ex}

Del ejemplo \ref{ex:515}, $E(Y_1 Y_2) = \frac{1}{3}$. También, de los ejemplos \ref{ex:516} y \ref{ex:517}, $\mu_1 = E(Y_1) = \frac{2}{3}$ y $\mu_2 = E(Y_2) = \frac{1}{2}$, y
\begin{equation*}
	\Cov(Y_1, Y_2) = E(Y_1 Y_2) - \mu_1 \mu_2 = \frac{1}{3} - \frac{2}{3} \cdot \frac{1}{2} = 0
\end{equation*}

El ejemplo \ref{ex:523} proporciona un caso específico del resultado general dado en el teorema \ref{thm:511}.

\begin{thm}\label{thm:511}
	Si $Y_1$ y $Y_2$ son variables aleatorias independientes, entonces
	\begin{equation}
		\Cov(Y_1, Y_2) = 0
	\end{equation}

	Así, las variables aleatorias independientes deben ser no correlacionadas.
	
	El teorema \ref{thm:510} establece que
	\begin{equation}
		\Cov(Y_1, Y_2) = E(Y_1 Y_2) - \mu_1 \mu_2
	\end{equation}

	Como $Y_1$ y $Y_2$ son independientes, el teorema \ref{thm:59} implica que:
	\begin{equation}
		E(Y_1 Y_2) = E(Y_1) E(Y_2) = \mu_1 \mu_2
	\end{equation}

	Y el resultado deseado se deduce de inmediato.
\end{thm}

Observe que las variables aleatorias $Y_1$ y $Y_2$ del ejemplo \ref{ex:523} son independientes; en consecuencia, por el teorema \ref{thm:511}, su covarianza debe ser cero. El recíproco del teorema \ref{thm:511} no es verdadero, como se ilustra en el ejemplo siguiente:

\begin{ex}\label{ex:524}
	Sean $Y_1$ y $Y_2$ variables aleatorias discretas con distribución de probabilidad conjunta como se ve en la tabla \ref{tab:53}. Demuestre que $Y_1$ y $Y_2$ son dependientes pero tienen covarianza cero.
\end{ex}

El cálculo de probabilidades marginales da $p_1(-1) = p_1(1) = \frac{5}{16} = p_2(-1) = p_2(1)$ y $p(0) = \frac{6}{16} = p_2(0)$. El valor $p(0,0) = 0$ en la celda del centro se destaca. Obviamente,
\begin{equation*}
	p(0,0) \ne p_1(0) \cdot p_2(0)
\end{equation*}

Y esto es suficiente para demostrar que $Y_1$ y $Y_2$ son dependientes.
\begin{table}[h!]
	\centering
	\caption{}
	\label{tab:53}
	\def\arraystretch{1.25}
	\begin{tabular}[h!]{cccc}
		\hline
		& \multicolumn{3}{c}{$y_1$}\\
		\cline{2-4}
		$y_2$ & $-1$ & $0$ & $+1$\\
		\hline
		$-1$ & $\nicefrac{1}{16}$ & $\nicefrac{3}{16}$ & $\nicefrac{1}{16}$\\
		$0$ & $\nicefrac{3}{16}$ & $0$ & $\nicefrac{3}{16}$\\
		$+1$ & $\nicefrac{1}{16}$ & $\nicefrac{3}{16}$ & $\nicefrac{1}{16}$\\
		\hline
	\end{tabular}
\end{table}

Observando de nuevo las probabilidades marginales, vemos que $E(Y_1) = E(Y_2) = 0$.  También,
\begin{flalign*}
	E(Y_1 Y_2) &= \sum_{\text{toda } y_1} \sum_{\text{toda } y_2} y_1 y_2 p(y_1,y_2)\\
	&= (-1) (-1) \left( \frac{1}{16} \right) + (0) (0) (0) + (0) (1) \left( \frac{3}{16} \right) + (1) (-1) \left( \frac{1}{16} \right) + (1) (0) \left( \frac{3}{16} \right) + (1) (1) \left( \frac{1}{16} \right)\\
	&= \frac{1}{16} - \frac{1}{16} - \frac{1}{16} + \frac{1}{16} = 0
\end{flalign*}

Entonces,
\begin{equation*}
	\Cov(Y_1, Y_2) = E(Y_1 Y_2) - E(Y_1) E(Y_2) = 0 - 0 (0) = 0
\end{equation*}

Este ejemplo demuestra que el recíproco del teorema \ref{thm:511} no es verdadero. Si la covarianza de dos variables aleatorias es cero, las variables \textit{no necesitan} ser independientes.

\subsection{Valor esperado y varianza de funciones de lineales de variables aleatorias}

Más adelante en el curso, frecuentemente encontraremos estimadores que son funciones lineales de las mediciones de una muestra, $Y_1$, $Y_2$, ..., $Y_n$. Si $a_1$, $a_2$, ..., $a_n$ son constantes, será necesario calcular el valor esperado y varianza de una función lineal de las variables aleatorias $Y_1$, $Y_2$, ..., $Y_n$.
\begin{equation}
	U_1 = a_1Y_1 + a_2Y_2 + a_3Y_3 + ... + a_nY_n = \sum_{u=1}^{n} a_iY_i
\end{equation}

También podemos estar interesados en la covarianza entre dos de estas combinaciones lineales. Los resultados que simplifican el cálculo de estas cantidades se resumen en el teorema siguiente:

\begin{thm}\label{thm:512}
	Sean $Y_1$, $Y_2$, ..., $Y_n$ y $X_1$, $X_2$, ..., $X_m$ variables aleatorias con $E(Y_i) = \mu_i$ y $E(X_j) = \xi_j$. Defina
	\begin{equation}
		U_1 = \sum_{i=1}^{n} a_i Y_i \qquad \text{y} \qquad U_2 = \sum_{j=1}^{m} b_j X_j
	\end{equation}

	Para las constantes $a_1$, $a_2$, ..., $a_n$ y $b_1$, $b_2$, ..., $b_m$. Entonces se cumple lo siguiente:
	\begin{enumerate}[a.]
		\item $E(U_1) = \sum_{i=1}^{n} a_i \mu_i$
		
		\item $V(U_1) = \sum_{i=1}^{n} a_i^2 V(Y_i) + 2\sum \sum_{1 \le i < j \le n} a_i a_j \Cov(Y_i, Y_j)$, donde la doble suma es para todos los pares $(i,j)$ con $i < j$.
		
		\item $\Cov(U_1, U_2) = \sum_{i=1}^{n} \sum_{j=1}^{m} a_i b_j \Cov(Y_i, X_j)$.
	\end{enumerate}
\end{thm}

Antes de continuar con la demostración del teorema \ref{thm:512}, ejemplificaremos su uso.

\begin{ex}\label{ex:525}
	Sean $Y_1$, $Y_2$, y $Y_3$ variables aleatorias, donde $E(Y_1) = 1$, $E(Y_2) = 2$, $E(Y_3) = -1$, $V(Y_1) = 1$, $V(Y_2) = 3$, $V(Y_3) = 5$, $\Cov(Y_1, Y_2) = -0.4$, $\Cov(Y_1, Y_3) = \frac{1}{2}$ y $\Cov(Y_2, Y_3) = 2$. Encuentre el valor esperado y la varianza de $U = Y_1 - 2Y_2 + Y_3$. Si $W=3Y_1 + Y_2$, encuentre $\Cov(U, W)$.
\end{ex}

$U = a_1 Y_1 + a_2 Y_2 + a_3 Y_3$, donde $a_1 = 1$, $a_2 = -2$ y $a_3 = 1$. Entonces, por el teorema \ref{thm:512},
\begin{equation*}
	E(U) = a_1 E(Y_1) + a_2 E(Y_2) + a_3 E(Y_3) = (1) (1) + (-2) (2) + (1) (-1) = -4
\end{equation*}

De manera similar,
\begin{flalign*}
	V(U) &= a_1^2 V(Y_1) + a_2^2 V(Y_2) + a_3^2 V(Y_3) + 2a_1 a_2 \Cov(Y_1, Y_2) + 2a_1 a_3 \Cov(Y_1, Y_3) + 2a_2 a_3 \Cov(Y_2, Y_3)\\
	&= (1)^2 (1) + (-2)^2 (3) + (1)^2 (5) + (2) (1) (-2) (-0.4) + (2) (1) (1) \left( \frac{1}{2} \right) + (2) (-2) (1) (2)\\
	&= 12.6
\end{flalign*}

Observe que $W = b_1 Y_1 + b_2 Y_2$, donde $b_1 = 3$ y $b_2 = 1$. Entonces,
\begin{flalign*}
	\Cov(U, W) &= a_1 b_1 \Cov(Y_1, Y_1) + a_1 b_2 \Cov(Y_1, Y_2) + a_2 b_1 \Cov(Y_2, Y_1) + a_2 b_2 \Cov(Y_2, Y_2) + a_3 b_1 \Cov(Y_3, Y_1) + a_3 b_2 \Cov(Y_3, Y_2)
\end{flalign*}

Observe que $\Cov(Y_i, Y_j) = \Cov(Y_j, Y_i)$ y $\Cov(Y_i, Y_i) = V(Y_i)$. Por lo tanto,
\begin{flalign*}
	\Cov(U, W) &= (1) (3) (1) + (1) (1) (-0.4) + (-2) (3) (-0.4) + (-2) (1) (3) + (1) (3) \left( \frac{1}{2} \right) + (1) (1) (2)\\
	&= 2.5
\end{flalign*}

Como $\Cov(U, W) \ne 0$, se deduce que $U$ y $W$ son \textbf{dependientes}.

Ahora continuamos con la demostración del teorema \ref{thm:512}.

El teorema consta de tres partes, de las cuales $\text{(a)}$ viene directamente de los teoremas \ref{thm:57} y \ref{thm:58}. Para demostrar $\text{(b)}$ recurrimos a la definición de varianza y escribimos:
\begin{flalign*}
	V(U_1) &= E[U_1 - E(U_1)]^2 = E\left[ \sum_{i=1}^{n} a_i Y_i - \sum_{i=1}^{n}  a_i \mu_i \right]^2\\
	&= E\left[ \sum_{i=1}^{n}  a_i(Y_i - \mu_i) \right]^2\\
	&= E\left[ \sum_{i=1}^{n}  a_i^2 (Y_1 - \mu_i)^2 + 2\sum_{i=1}^{n} \sum_{j=1}^{n} a_i a_j (Y_i - \mu_i)(Y_j - \mu_j) \right]\\
	&= \sum_{i=1}^{n} a_i^2 E(Y_1 - \mu_i)^2 + 2 \underset{i \ne j}{\sum_{i=1}^{n} \sum_{i=1}^{n}} a_i a_j E\bigl[(Y_i - \mu_i) (Y_j - \mu_j)\bigr]
\end{flalign*}

Por las definiciones de varianza y covarianza tenemos:
\begin{equation*}
	V(U_1) = \sum_{i=1}^{n} a_i^2 V(Y_i) + 2 \underset{i \ne j}{\sum_{i=1}^{n} \sum_{i=1}^{n}} a_i a_j \Cov(Y_i, Y_j)
\end{equation*}

Como $\Cov(Y_i, Y_j) = \Cov(Y_j, Y_i)$, podemos escribir:
\begin{equation*}
	V(U_1) = \sum_{i=1}^{n} a_i^2 V(Y_i) + 2 \underset{1 \le i < j \le n}{\sum \sum} a_i a_j \Cov(Y_i, Y_j)
\end{equation*}

Se pueden usar pasos similares para obtener $\text{(c)}$. Tenemos:
\begin{flalign*}
	\Cov(U_1, U_2) &= E\set{[U_1 - E(U_1)][U_2 - E(U_2)]}\\
	&= E\Bigg[ \Bigg( \sum_{i=1}^{n} a_i Y_i - \sum_{i=1}^{n} a_i\mu_i \Bigg) \Bigg( \sum_{j=1}^{m} b_j X_j - \sum_{j=1}^{m} b_j \xi_j \Bigg) \Bigg]\\
	&= E \Bigg\{ \Bigg[ \sum_{i=1}^{n} a_i (Y_i - \mu_i) \Bigg] \Bigg[ \sum_{j=1}^{m} b_j (X_j - \xi_j) \Bigg] \Bigg\}\\
	&= E \Bigg[ \sum_{i=1}^{n} \sum_{j=1}^{m} a_i b_j (Y_i - \mu_i) (X_j - \xi_j) \Bigg]\\
	&= \sum_{i=1}^{n} \sum_{j=1}^{m} a_i b_j E\big[(Y_i - \mu_i)(X_j - \xi_j)\big]\\
	&= \sum_{i=1}^{n} \sum_{j=1}^{m} a_i b_j \Cov(Y_i, X_j)
\end{flalign*}

Al observar que $\Cov(Y_i, Y_i) = V(Y_i)$, podemos ver que $\text{(b)}$ es un caso especial de $\text{(c)}$.

\begin{ex}\label{ex:526}
	Consulte los ejemplos \ref{ex:54} y \ref{ex:520}. En el segundo estuvimos interesados en $Y_1 - Y_2$, la cantidad proporcional de gasolina restante al final de una semana. Encuentre la varianza de $Y_1 - Y_2$.
\end{ex}

Usando el teorema \ref{thm:512}, tenemos:
\begin{equation*}
	V(Y_1 - Y_2) = V(Y_1) + V(Y_2) - 2\Cov(Y_1,Y_2)
\end{equation*}

Como,
\begin{equation*}
	f_1(y_1) = \begin{cases}
		3y_1^2 & 0 \le y_1 \le 1\\
		0 & \text{en cualquier otro punto}
	\end{cases}
\end{equation*}

Y,
\begin{equation*}
	f_2(y_2) = \begin{cases}
		\big( \frac{3}{2} \big) (1-y_2^2) & 0 \le y_2 \le 1\\
		0 & \text{en cualquier otro punto}
	\end{cases}
\end{equation*}

Se deduce que,
\begin{flalign*}
	E(Y_1^2) &= \int_{0}^{1} 3y_1^4 dy_1 = \frac{3}{5}\\
	E(Y_2^2) &= \int_{0}^{1} \frac{3}{2} y_2^2 (1-y_2^2) dy_2 = \frac{3}{2} \bigg[ \frac{1}{3} - \frac{1}{5} \bigg] = \frac{1}{5}
\end{flalign*}

Del ejemplo \ref{ex:520} tenemos que $E(Y_1) = \frac{3}{4}$ y $E(Y_2) = \frac{3}{8}$. Entonces,
\begin{equation*}
	V(Y_1) = \bigg( \frac{3}{5} \bigg) - \bigg( \frac{3}{4} \bigg)^2 = 0.04 \quad \text{y} \quad V(Y_2) = \bigg( \frac{1}{5} \bigg) - \bigg( \frac{3}{8} \bigg)^2 = 0.06
\end{equation*}

En el ejemplo \ref{ex:522} determinamos que $\Cov(Y_1, Y_2) = 0.02$. Por tanto,
\begin{flalign*}
	V(Y_1 - Y_2) &= V(Y_1) - V(Y_2) - 2\Cov(Y_1,Y_2)\\
	&= 0.04 + 0.06 - 2(0.02) = 0.06
\end{flalign*}

La desviación estándar de $Y_1 - Y_2$ es entonces $\sqrt{0.06} = 0.245$

\begin{ex}\label{ex:527}
	Sean $Y_1$ y $Y_2$, ..., $Y_n$, variables aleatorias independientes con $E(Y_i) = \mu$ y $V(Y_i) = \sigma^2$. (Estas variables pueden denotar los resultados de $n$ intentos independientes de un experimento.). Defina,
	\begin{equation*}
		\overline{Y} = \frac{1}{n} \sum_{i=1}^{n} Y_i
	\end{equation*}

	Y demuestre que $E(\overline{Y}) = \mu$ y $V(\overline{Y}) = \frac{\sigma^2}{n}$
\end{ex}

Observe que $\overline{Y}$ es una función lineal de $Y_1$, $Y_2$, ..., $Y_n$ con todas las constantes $a_i$ iguales a $\frac{1}{n}$. Esto es,
\begin{equation*}
	\overline{Y} = \bigg( \frac{1}{n} \bigg) Y_1 + ... + \bigg( \frac{1}{n} \bigg) Y_n
\end{equation*}

Por el teorema \ref{thm:512}$\text{(a)}$,
\begin{equation*}
	E(\overline{Y}) = \sum_{i=1}^{n} a_i \mu_i = \sum_{i=1}^{n} a_i \mu = \mu \sum_{i=1}^{n} a_i = \mu \sum_{i=1}^{n} \frac{1}{n} = \frac{n \mu}{n} = \mu
\end{equation*}

Por el teorema \ref{thm:512}$\text{(b)}$,
\begin{equation*}
	V(\overline{Y}) = \sum_{i=1}^{n} a_i^2 V(Y_i) + 2 \sum_{i=1}^{n} \sum_{i=1}^{n} a_i a_j \Cov(Y_i, Y_j)
\end{equation*}

Los términos de la covarianza son todos iguales a cero porque las variables aleatorias son independientes, entonces,
\begin{equation*}
	V(\overline{Y}) = \sum_{i=1}^{n} \bigg( \frac{1}{n} \bigg)^2 \sigma_i^2 = \sum_{i=1}^{n} \bigg( \frac{1}{n} \bigg)^2 \sigma^2 = \frac{1}{n^2} \sum_{i=1}^{n} \sigma^2 = \frac{n \sigma^2}{n^2} = \frac{\sigma^2}{n}
\end{equation*}

\begin{ex}\label{ex:528}
	El número de artículos defectuosos $Y$ en una muestra de $n = 10$ artículos seleccionados del proceso de fabricación tiene una distribución de probabilidad binomial. Un estimador de la fracción defectuosa del lote es la variable $\hat{p} = \frac{Y}{n}$. Encuentre el valor esperado y la varianza de $\hat{p}$.
\end{ex}

El término $\hat{p}$ es una función lineal de una sola variable $Y$, donde $\hat{p} = a_1 Y$ y $a_1 = \frac{1}{n}$. Entonces, por el teorema \ref{thm:512},
\begin{equation*}
	E(\hat{p}) = a_1 E(Y) = \frac{1}{n} E(Y)
\end{equation*}

El valor esperado y la varianza de una variable aleatoria binomial son $np$ y $npq$, respectivamente. Sustituyendo por $E(Y)$, obtenemos,
\begin{equation*}
	E(\hat{p}) = \frac{1}{n} (np) = p
\end{equation*}

Entonces, el valor esperado del número de artículos defectuosos $Y$, dividido entre el tamaño muestral, es $p$. Del mismo modo,
\begin{equation*}
	V(\hat{p}) = a_1^2 V(Y) = \bigg( \frac{1}{n} \bigg)^2 np1 = \frac{pq}{n}
\end{equation*}

\begin{ex}\label{ex:529}
	Suponga que una urna contiene $r$ bolas rojas y $(N-r)$ bolas negras. Una muestra aleatoria de $n$ bolas se saca sin restitución y se observa $Y$, el número de bolas rojas de la muestra. Sabemos que $Y$ tiene una distribución de probabilidad \textbf{hipergeométrica}. Encuentre la media y la varianza de $Y$.
\end{ex}

Primero observamos algunas características de muestrear sin restitución. Suponga que el muestreo se realiza en forma secuencial y observamos resultados para $X_1$, $X_2$, ..., $X_n$, donde:
\begin{equation*}
	X_i = \begin{cases}
		1 & \text{si el i-ésimo resultado es una bola roja}\\
		0 & \text{en caso contrario}
	\end{cases}
\end{equation*}

Incuestionablemente, $P(X_1 = 1) = \frac{r}{N}$. Pero también es cierto que $P(X_2 = 1) = \frac{r}{N}$ porque,
\begin{flalign*}
	P(X_2 = 1) &= P(X_1 = 1, X_2 = 1) + P(X_1 = 0, X_2 = 1)\\
	&= P(X_1 = 1) P(X_2 = 1 | X_1 = 1) + P(X_1 = 0) P(X_2 = 1 | X_1 = 0)\\
	&= \bigg( \frac{r}{N} \bigg) \bigg( \frac{r-1}{N-1} \bigg) + \bigg( \frac{N-r}{N} \bigg) \bigg( \frac{r}{N-1} \bigg) = \frac{r(N-1)}{N(N-1)} = \frac{r}{N}
\end{flalign*}

Lo mismo es cierto para $X_k$, esto es,
\begin{equation*}
	P(X_k = 1) = \frac{r}{N}, \qquad k = 1, 2, ..., n
\end{equation*}

Entonces, la probabilidad (incondicional) de sacar una bola roja en cualquier ensayo es $\frac{r}{N}$.

Del mismo modo, se puede demostrar que,
\begin{equation*}
	P(X_j = 1, X_k = 1) = \frac{r(r-1)}{N(N-1)}, \qquad j \ne k
\end{equation*}

Ahora, observe que $Y = \sum_{i=1}^{n} X_i$ y por lo tanto,
\begin{equation*}
	E(Y) = \sum_{i=1}^{n} E(X_i) = \sum_{i=1}^{n} \bigg( \frac{r}{N} \bigg) = n \bigg( \frac{r}{N} \bigg)
\end{equation*}

Para hallar $V(Y)$ necesitamos $V(X_i)$ y $\Cov(X_i, X_j)$. Como $X_i$ es 1 con probabilidad $\frac{r}{N}$ y 0 con probabilidad $1-(\frac{r}{N})$, se deduce que,
\begin{equation*}
	V(X_i) = \frac{r}{N} \bigg( 1 - \frac{r}{N} \bigg)
\end{equation*}

También,
\begin{flalign*}
	\Cov(X_i, X_j) &= E(X_i X_j) - E(X_i) E(X_j) = \frac{r(r-1)}{N(N-1)} - \bigg( \frac{r}{N} \bigg)^2\\
	&= - \frac{r}{N} \bigg( 1- \frac{r}{N} \bigg) \bigg( \frac{1}{N-1} \bigg)
\end{flalign*}

Porque $X_i X_j = 1$ si y sólo si $X_i = 1$ y $X_j = 1$ y $X_i X_j = 0$ en caso contrario. Del teorema \ref{thm:512}, sabemos que,
\begin{flalign*}
	V(Y) &= \sum_{i=1}^{n} V(X_i) + 2 \underset{i < j}{\sum \sum} \Cov(X_i, X_j)\\
	&= \sum_{i=1}^{n} \bigg( \frac{r}{N} \bigg) \bigg( 1 - \frac{r}{N} \bigg) + 2 \underset{i < j}{\sum \sum} \Bigg[ - \frac{r}{N} \bigg( 1 - \frac{r}{N} \bigg) \bigg( \frac{1}{N-1} \bigg) \Bigg]\\
	&= n  \bigg( 1 - \frac{r}{N} \bigg) \bigg( 1 - \frac{r}{N} \bigg) - n (n-1) \bigg( \frac{r}{N} \bigg) \bigg( 1 - \frac{r}{N} \bigg) \bigg( \frac{1}{N-1} \bigg)
\end{flalign*}

Porque la doble sumatoria contiene $\frac{n(n-1)}{2}$ términos iguales. Un poco de álgebra dará como resultado,
\begin{equation*}
	V(Y) = n \bigg( \frac{r}{N} \bigg) \bigg( 1 - \frac{r}{N} \bigg) \bigg( \frac{N - n}{N - 1} \bigg)
\end{equation*}

\subsection{Distribución de probabilidad multinomial}

Supongamos una variable aleatoria binomial que resulta de un experimento que consiste en $n$ intentos con dos posibles resultados por intento. Con frecuencia encontramos situaciones similares en las que el número de posibles resultados por intento es más que dos. Por ejemplo, experimentos que comprenden tipos de sangre por lo general tienen al menos cuatro posibles resultados por intento. Experimentos que comprenden el muestreo de artículos defectuosos pueden clasificar el tipo de defectos observados en más de dos clases.

Un experimento multinomial es una generalización del experimento binomial.

\begin{tcolorbox}\begin{defn}\label{def:511}
		Un \textbf{experimento multinomial} posee las siguientes propiedades:
		\begin{enumerate}[1.]
			\item El experimento consta de $n$ intentos idénticos.
			
			\item El resultado de cada intento cae en una de las $k$ clases o celdas.
			
			\item La probabilidad de que el resultado de un solo intento caiga en la celda $i$ es $p_i$, $i=1, 2, ..., k$, y sigue siendo el mismo de un intento a otro. Observe que $p_1 + p_2 + p_3 + ... + p_k = 1$.
			
			\item Los intentos son dependientes.
			
			\item Las variables aleatorias de interés son $Y_1$, $Y_2$, ..., $Y_k$, donde $Y_i$ es igual al número de intentos para los cuales el resultado cae en la celda $i$. Observe que $Y_1 + Y_2 + Y_3 + ... + Y_k = n$.
		\end{enumerate}
\end{defn}\end{tcolorbox}

La función de probabilidad conjunta para $Y_1$, $Y_2$, ..., $Y_k$ está dada por,
\begin{equation*}
	p(y_1, y_2, ..., y_k) = \frac{n!}{y_1! y_2! \cdots y_k!} p_1^{y_1} p_2^{y_2} \cdots p_k^{y_k}
\end{equation*}

Donde,
\begin{equation*}
	\sum_{i=1}^{k} p_i = 1 \quad \text{y} \quad \sum_{i=1}^{k} y_i = n
\end{equation*}

\begin{tcolorbox}\begin{defn}\label{def:512}
		Suponga que $p_1$, $p_2$, ..., $p_k$ son tales que $\sum_{i=1}^{k} p_i = 1$, y $p_i > 0$ para $i = 1, 2, ..., k$. Se dice que las variables aleatorias $Y_1$, $Y_2$, ..., $Y_k$ tienen una \textbf{distribución multinomial} con parámetros $n$ y $p_1$, $p_2$, ..., $p_k$ si la función de probabilidad conjunta de $Y_1$, $Y_2$, ..., $Y_k$ está dada por,
		\begin{equation}
			p(y_1, y_2, ..., y_k) = \frac{n!}{y_1! y_2! \cdots y_k!} p_1^{y_1} p_2^{y_2} \cdots p_k^{y_k}
		\end{equation}
	
		Donde, para cada $i$, $y_i = 0, 1, 2, ..., n$ y $\sum_{i=1}^{k} y_i = n$
\end{defn}\end{tcolorbox}

Muchos experimentos en los que aparece una clasificación son multinomiales. Por ejemplo, clasificar personas en cinco grupos resulta en una enumeración o cantidad correspondiente a cada una de cinco clases de ingreso. O bien, podríamos estar interesados en estudiar la reacción de ratones a un estímulo particular en un experimento psicológico. Si los ratones pueden reaccionar en una de tres formas cuando se aplica el estímulo, el experimento da el número de ratones que caigan en cada clase de reacción. Del mismo modo, un estudio de tránsito podría requerir un conteo y clasificación de los tipos de vehículos de motor que usan una sección de carretera. Un proceso industrial podría manufacturar artículos que caigan en una de tres clases de calidad: aceptables, de segunda y rechazos. Un estudiante de arte podría clasificar pinturas en una de $k$ categorías de acuerdo con el estilo y periodo, o podríamos clasificar ideas filosóficas de los autores en un estudio de literatura. El resultado de una campaña publicitaria podría dar datos que indiquen una clasificación de reacciones del consumidor. Muchas observaciones de ciencias físicas no son sensibles a mediciones en una escala continua y, por tanto, resultan en datos enumerativos que corresponden a los números de observaciones que caen en varias clases.

Observe que el experimento binomial es un caso especial del experimento multinomial cuando hay $k = 2$ clases. 

\begin{ex}\label{ex:530}
	De acuerdo con cifras de un censo reciente, las proporciones de adultos (personas de más de 18 años de edad) en Estados Unidos, asociados con cinco categorías de edades se dan en la siguiente tabla.
	\begin{table}[h!]
		\centering
		\caption{}
		\label{tab:x}
		\includegraphics[width=0.2\linewidth]{Anexo/screenshot011}
	\end{table}

	Si estas cifras son precisas y cinco adultos se muestrean aleatoriamente, encuentre la probabilidad de que la muestra contenga una persona entre las edades de 18 y 24 años, dos entre 25 y 34, y dos entre 45 y 64.
\end{ex}

Vamos a numerar las cinco clases de edad 1, 2, 3, 4 y 5 de arriba abajo y supondremos que las proporciones son las probabilidades asociadas con cada una de las clases. Entonces deseamos hallar,
\begin{equation*}
	p(y_1, y_2, y_3, y_4, y_5) = \frac{n!}{y_1! y_2! y_3! y_4! y_5!} p_1^{y_1} p_2^{y_2} p_3^{3} p_4^{4} p_5^{5}
\end{equation*}

Para $n = 5$ y $y_1 = 1$, $y_2 = 2$, $y_3 = 0$, $y_4 = 2$ y $y_5 = 0$. Sustituyendo estos valores en la fórmula para la función de probabilidad conjunta, obtenemos
\begin{flalign*}
	p(1,2,0,2,0) &= \frac{5!}{1! 2! 0! 2! 0!} (0.18)^1 (0.23)^2 (0.16)^0 (0.27)^2 (0.16)^0\\
	&= 30 (0.18) (0.23)^2 (0.27)^2 = 0.208
\end{flalign*}

\begin{thm}\label{thm:513}
	Si $Y_1$, $Y_2$, ..., $Y_k$ tienen una distribución binomial con parámetros $y$, y $p_1$, $p_2$, ..., $p_k$, entonces
	\begin{enumerate}[1.]
		\item $E(Y_i) = n p_i$, $V(Y_i) = n p_i q_i$
		
		\item $\Cov(Y_s, Y_t) = -n p_s p_t$, si $s \ne t$
	\end{enumerate}
\end{thm}

La distribución marginal de $Y_i$ se puede usar para obtener la media y varianza. Recuerde que $Y_i$ puede ser interpretada como el número de intenso que caen en la celda $i$. Imagine todas las celdas, excluyendo la $i$, combinadas en una sola celda grande. Entonces cada intento resultará en la celda $i$ o en una celda que no sea la $i$, con probabilidades $p_i$ y $1 - p_i$, respectivamente. Entonces, $Y_i$ posee una distribución de probabilidad marginal binomial. En consecuencia,
\begin{equation*}
	E(Y_i) = n p_i \qquad \text{y} \qquad V(Y_i) = n p_i q_i, \qquad \text{donde} \quad q_i = 1 - p_i
\end{equation*}

Los mismos resultados se pueden obtener al establecer los valores esperados y evaluar. Por ejemplo,
\begin{equation*}
	E(Y_1) = \sum_{y_1} \sum_{y_2} \cdots \sum_{y_k} y_1 \frac{n!}{y_1! y_2! \cdots y_k!} p_1^{y_1} p_2^{y_2} \cdots p_k^{y_k}
\end{equation*}

La demostración de la parte 2 usa el teorema \ref{thm:512}. Considere el experimento multinomial como una sucesión de $n$ intentos independientes y defina, para $s \ne t$,
\begin{equation*}
	U_i = \begin{cases}
		1 & \text{si el intento $i$ resulta en clase $s$}\\
		0 & \text{de otro modo}
	\end{cases}
\end{equation*}

Y,
\begin{equation*}
	W_i = \begin{cases}
		1 & \text{si el intento $i$ resulta en clase $t$}\\
		0 & \text{de otro modo}
	\end{cases}
\end{equation*}

Entonces,
\begin{equation*}
	Y_s = \sum_{i=1}^{n} U_i \quad \text{y} \quad Y_t = \sum_{j=1}^{n} W_j
\end{equation*}

(Como $U_i = 1$ o $0$ dependiendo de si el $i$-ésimo intento resultó en clase $s$, $Y_s$ es simplemente la suma de una serie de números 0 y 1. Ocurre un 1 en la suma cada vez que observemos un artículo de la clase $s$ y un 0 cada vez que observemos cualquier otra clase. Entonces, $Y_s$ es simplemente el número de veces que se observe la clase $s$. Una interpretación similar se aplica a $Y_t$).

Observe que $U_i$ y $W_i$ no pueden ser iguales a 1 (el $i$-ésimo artículo no puede estar simultáneamente en las clases $s$ y $t$). Entonces, el producto $U_i W_i$ siempre es igual a cero y $E(U_i W_i) = 0$. Los siguientes resultados nos permiten evaluar $\Cov(Y_s, Y_t)$:
\begin{flalign*}
	E(U_i) &= p_s\\
	E(W_j) &= p_t\\
	\Cov(U_i, W_j) &= 0, \qquad \text{si $i \ne j$ porque los intentos son independientes}\\
	\Cov(U_i, W_i) &= E(U_i W_i) - E(U_i) E(W_i) = 0 - p_s p_t
\end{flalign*}

Del teorema \ref{thm:512} tenemos entonces,
\begin{flalign*}
	\Cov(Y_s, Y_t) &= \sum_{i=1}^{n} \sum_{j=1}^{n} \Cov(U_i, W_j)\\
	&= \sum_{i=1}^{n} \Cov(U_i, W_i) + \underset{i \ne j}{\sum \sum} \Cov(U_i, W_j)\\
	&= \sum_{i=1}^{n} (-p_s p_t) + \underset{i \ne j}{\sum \sum} 0 = -n p_s p_t
\end{flalign*}

La covarianza es negativa, lo que ya se esperaba, porque un gran número de resultados en la celda $s$ forzaría al número de la celda $t$ a ser pequeño.

\subsection{Valores esperados condicionales}

La sección \ref{sec:53} contiene un examen de funciones de probabilidad condicional y funciones de densidad condicional que ahora relacionaremos con valores esperados condicionales. Éstos se definen en la misma forma que los valores esperados univariantes, excepto que las densidades condicionales y las funciones de probabilidad se usan en lugar de sus similares marginales.

\begin{tcolorbox}\begin{defn}\label{def:513}
		Si $Y_1$ y $Y_2$ son dos variables aleatorias cualesquiera, el \textbf{valor esperado condicional} de $g(Y_1)$ dado que $Y_2 = y_2$, se define que es:
		\begin{equation}
			E(g(Y_1)|Y_2 = y_2) = \int_{-\infty}^{\infty} g(y_1) f(y_1|y_2) dy_2
		\end{equation}
	
		Si $Y_2$ y $Y_2$ son continuas conjuntamente, y
		\begin{equation}
			E(g(Y_1)|Y_2 = y_2) = \sum_{\text{toda $y_1$}} g(y_1) p(y_1|y_2)
		\end{equation}
	
		Si $Y_1$ y $Y_2$ son discretas conjuntamente.
\end{defn}\end{tcolorbox}

\begin{ex}\label{ex:531}
	Consulte las variables aleatorias $Y_1$ y $Y_2$ del ejemplo \ref{ex:58}, donde la función de densidad conjunta está dada por
	\begin{equation*}
		f(y_1, y_2) = \begin{cases}
			\frac{1}{2} & 0 \le y_1 \le y_2 \le 2\\
			0 & \text{en cualquier otro punto}
		\end{cases}
	\end{equation*}

	Encuentre el valor esperado condicional de la cantidad de ventas, $Y_1$, dado que $Y_2 = 1.5$.
\end{ex}

En el ejemplo \ref{ex:58} determinamos que si $0 < y_2 \le 2$,
\begin{equation*}
	f(y_1 | y_2) = \begin{cases}
		\frac{1}{y_2} & 0 < y_2 \le y_2\\
		0 & \text{en cualquier otro punto}
	\end{cases}
\end{equation*}

Así, de acuerdo con la definición \ref{def:513}, para cualquier valor de $y_2$ tal que $0 < y_2 \le 2$,
\begin{flalign*}
	E(Y_1 | Y_2 = 2_2) &= \int_{-\infty}^{\infty} y_1 f(y_1 | y_2) dy_1\\
	&= \int_{0}^{y_2} y_1 \bigg( \frac{1}{y_2} \bigg) dy_1 = \frac{1}{y_2} \bigg( \frac{y_1^2}{2} \bigg|_0^{y_2} \bigg) = \frac{y_2}{2}
\end{flalign*}

En vista de que estamos interesados en el valor $y_2 = 1.5$, se deduce que $E(Y_1 | Y_2 = 1.5) = \frac{1.5}{2} = 0.75$. Esto es, si la máquina automática expendedora de bebidas contiene $1.5$ galones al principio del día, la cantidad esperada para venderse ese día es $0.75$ galones.

En general, el valor esperado condicional de $Y_1$ dada $Y_2 = y_2$ es una función de $y_2$. Si ahora hacemos variar $Y_2$ en todos sus posibles valores, podemos considerar el valor esperado condicional $E(Y_1 | Y_2)$ como una función de la variable aleatoria $Y_2$. En el ejemplo \ref{ex:531} obtuvimos $E(Y_1 | Y_2 = y_2) = \frac{y_2}{2}$. Se deduce que $E(Y_1 | Y_2) = \frac{Y_2}{2}$. Como $E(Y_1 | Y_2)$ es una función de la variable aleatoria $Y_2$, también es una variable aleatoria; y como tal, tiene media y varianza. Consideramos la media de esta variable aleatoria en el teorema \ref{thm:514} y la varianza en el teorema \ref{thm:515}.

\begin{thm}\label{thm:514}
	Si $Y_1$ y $Y_2$ son dos variables aleatorias, entonces
	\begin{equation}
		E(Y_1) = E[E(Y_1 | Y_2)]
	\end{equation}

	Donde en el lado derecho de la ecuación el valor esperado interior es con respecto a la distribución condicional de $Y_1$ dada $Y_2$ y el valor esperado exterior es con respecto a la distribución de $Y_2$
\end{thm}

Suponga que $Y_1$ y $Y_2$ son continuas conjuntamente con función de densidad conjunta $f(y_1, y_2)$ y densidades marginales $f_1 (y_1)$ y $f_2 (y_2)$, respectivamente, entonces
\begin{flalign*}
	E(Y_1) &= \int_{-\infty}^{\infty} y_1 f(y_1, y_2) dy_1 dy_2\\
	&= \int_{-\infty}^{\infty} \int_{-\infty}^{\infty} y_1 f(y_1 | y_2) f_2(y_2) dy_1 dy_2\\
	&= \int_{-\infty}^{\infty} \Bigg\{ \int_{-\infty}^{\infty} y_1 f(y_1 | y_2) dy_1 \Bigg\} f_2(y_2) dy_2\\
	&= \int_{-\infty}^{\infty} E(Y_1 | Y_2 = y_2) f_2(y_2) dy_2 = E[E(Y_1 | Y_2)]
\end{flalign*}

La demostración es semejante para el caso discreto.

\begin{ex}\label{ex:532}
	Un programa de control de calidad para una línea de ensamble comprende el muestreo de $n = 10$ artículos terminados por día y contar el número de artículos defectuosos, $Y$. Si $p$ denota la probabilidad de observar uno defectuoso, entonces $Y$ tiene una distribución binomial, suponiendo que un número de artículos son producidos por la línea. Pero $p$ varía diariamente y se supone que tiene una distribución uniforme en el intervalo de $0$ a $\frac{1}{4}$. Encuentre el valor esperado de $Y$.
\end{ex}

Del teorema \ref{thm:514} sabemos que $E(Y) = E[E(Y | p)]$. Para una $p$ dada, $Y$ tiene una distribución binomial, de ahí que $E(Y | p) = np$. Por tanto,
\begin{equation*}
	E(Y) = E[E(Y | p)] = E(np) = nE(p) = n \bigg( \frac{\frac{1}{4} - 0}{2} \bigg) = \frac{n}{8}
\end{equation*}

Y para $n = 10$
\begin{equation*}
	E(Y) = \frac{10}{8} = 1.25
\end{equation*}

A la larga, esta política de inspección va a promediar $1.25$ artículos defectuosos por día.

La varianza condicional de $Y_1$ dada $Y_2 = y_2$ está definida por analogía con una varianza ordinaria, de nuevo utilizando la densidad condicional o función de probabilidad de $Y_1$ dada $Y_2 = y_2$ en lugar de la densidad ordinaria o función de probabilidad de $Y_1$. Esto es, 
\begin{equation*}
	V(Y_1 | Y_2 = y_2) = E(Y_1^2 | Y_2 = y_2) - [E(Y_1 | Y_2 = y_2)]^2
\end{equation*}

Como en el caso de la media condicional, la varianza condicional es una función de $y_2$. Si dejamos que $Y_2$ tome todos los valores posibles, podemos definir $V(Y_1 | Y_2)$ como una variable aleatoria que es una función de $Y_2$. Específicamente, si $g(y_2) = V(Y_1 | Y_2 = y_2)$ es una función particular del valor observado $y_2$, entonces $g(Y_2 = V(Y_1 | Y_2)$ es la \textit{misma función} de la variable aleatoria, $Y_2$. El valor esperado de $V(Y_1 | Y_2)$ es útil para calcular la varianza de $Y_1$, como se detalla en el teorema \ref{thm:515}

\begin{thm}\label{thm:515}
	Si $Y_1$ y $Y_2$ representan variables aleatorias, entonces
	\begin{equation}
		V(Y_1) = E\big[V(Y_1 | Y_2)\big] + V\big[E(Y_1 | Y_2)\big]
	\end{equation}
\end{thm}

Como se indicó antes, $V(Y_1 | Y_2)$ está dada por
\begin{equation*}
	V(Y_1 | Y_2) = E(Y_1^2 | Y_2) - \big[E(Y_1 | Y_2)\big]^2
\end{equation*}

Y,
\begin{equation*}
	E\big[V(Y_1 | Y_2)\big] = E\big[E(Y_1^2 | Y_2)\big] - E\big\{\big[E(Y_1 | Y_2)\big]^2\big\}
\end{equation*}

Por definición,
\begin{equation*}
	V\big[E(Y_1 | Y_2)\big] = E \big\{ \big[E(Y_1 | Y_2)\big]^2 \big\} - \big\{ E\big[E(Y_1 | Y_2)\big] \big\}^2
\end{equation*}

La varianza de $Y_1$ es,
\begin{flalign*}
	V(Y_1) &= E \big[ Y_1^2 \big] - \big[ E(Y_1) \big]^2\\
	&= E \big\{ E \big[ Y_1^2 | Y_2 \big] \big\} - \big\{ E \big[ E(Y_1 | Y_2) \big] \big\}^2\\
	&= E \big\{ E \big[ Y_1^2 | Y_2 \big] \big\} - E \big\{ \big[ E(Y_1 | Y_2) \big]^2 \big\} + E \big\{ \big[ E(Y_1 | Y_2) \big]^2 \big\} - \big\{ E \big[ E(Y_1 | Y_2) \big] \big\}^2\\
	&= E \big[ V(Y_1 | Y_2) \big] + V \big[ E(Y_1 | Y_2) \big]
\end{flalign*}

\begin{ex}\label{ex:533}
	Consulte el ejemplo \ref{ex:532}. Encuentre la varianza de $Y$.
\end{ex}

Del teorema \ref{thm:515} sabemos que,
\begin{equation*}
	V(Y_1) = E \big[ V(Y_1 | Y_2) \big] + V \big[ E(Y_1 | Y_2) \big]
\end{equation*}

Para una $p$ dada, $Y$ tiene una distribución binomial, y en consecuencia $E(Y | p) = np$ y $V(Y | p) = npq$. Por tanto,
\begin{flalign*}
	V(Y) &= E \big[ V(Y | p) \big] + V \big[ E(Y | p) \big]\\
	&= E(npq) + V(np) = nE \big[ p (1-p) \big] + n^2 V(p)
\end{flalign*}

Como $p$ está uniformemente distribuida en el intervalo $(0, \frac{1}{4})$, y $E(p^2) = V(p) + [E(p)]^2$, se deduce que,
\begin{equation*}
	E(p) = \frac{1}{8}, \qquad V(p) = \frac{(\frac{1}{4} - 0)^2}{12} = \frac{1}{192}, \qquad E(p^2) = \frac{1}{192} + \frac{1}{64} = \frac{1}{48}
\end{equation*}

Así que,
\begin{flalign*}
	V(Y) &= nE \big[ p (1-p) \big] + n^2 V(p) = n \big[ E(p) - E(p^2) \big] + n^2 V(p)\\
	&= n \bigg( \frac{1}{8} - \frac{1}{48} \bigg) + n^2 \bigg( \frac{1}{192} \bigg) = \frac{5n}{48} + \frac{n^2}{192}
\end{flalign*}

Y para $n=10$,
\begin{equation*}
	V(Y) = \frac{50}{48} + \frac{100}{192} = 1.5625
\end{equation*}

Por tanto, la desviación estándar de $Y$ es $\sigma = \sqrt{1.5625} = 1.25$

La media y la varianza de $Y$ calculada en los ejemplos \ref{ex:532} y \ref{ex:533} podrían comprobarse determinando la función de probabilidad incondicional de $Y$ y calcular $E(Y)$ y $V(Y)$ directamente. Para hacerlo, necesitaríamos hallar la distribución conjunta de $Y$ y $p$. De esta distribución conjunta se puede obtener la función de probabilidad marginal de $Y$ y determinar $E(Y)$ al evaluar $\sum_{y} y p(y)$. La varianza se puede determinar en la forma usual, de nuevo usando la función de probabilidad marginal de $Y$. En los ejemplos \ref{ex:532} y \ref{ex:533} evitamos trabajar directamente con las distribuciones conjunta y marginal. Los teoremas \ref{thm:514} y \ref{thm:515} nos permitieron un cálculo mucho más rápido de la media y la varianzas deseadas. Como siempre, la media y la varianza de una variable aleatoria pueden combinarse con el teorema de \textbf{Tchebysheff} para obtener límites para probabilidades, cuando la distribución de la variable sea desconocida o difícil de deducir.

En los ejemplos \ref{ex:532} y \ref{ex:533} encontramos una situación en la que la distribución de una variable aleatoria ($Y = \text{el número de artículos defectuosos}$) se dio \textit{condicionalmente} para posibles valores de una cantidad $p$ que podría variar de un día a otro. El hecho de que $p$ variara se tomó en cuenta al asignar una distribución de probabilidad a esta variable. Éste es un ejemplo de un modelo \textit{jerárquico}. En estos modelos la distribución de una variable de interés, por ejemplo, $Y$, está \textit{condicionada} al valor de un “parámetro” $\theta$. La incertidumbre alrededor del valor real de $\theta$ se modela al asignarle una distribución de probabilidad. Una vez que especificamos la distribución condicional de $Y$ dada $\theta$ y la distribución marginal de $\theta$, la distribución conjunta de $Y$ y $\theta$ se obtiene al multiplicar la condicional por la marginal. La distribución marginal de $Y$ se obtiene entonces de la distribución conjunta mediante una integración o suma que incluya los posibles valores de $\theta$. Los resultados de esta sección se pueden usar para encontrar $E(Y)$ y $V(Y)$ \textit{sin que sea necesario} determinar esta distribución marginal.