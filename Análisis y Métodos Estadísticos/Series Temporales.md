# Definición

Una **serie temporal** (o simplemente una **serie**) es una secuencia de $N$ observaciones (datos) ordenadas y equidistantes cronológicamente sobre una característica (serie **univariante** o **escalar**) o sobre varias características (serie **multivariante** o **vectorial**) de una unidad observable en diferentes momentos.

## Representaciones matemáticas frecuentes de series temporales univariantes:

$y_1, y_2, ..., y_n$; $(y_t)^{N}_{t=1}$; $(y_t : t =1, ..., N)$, donde $y_t$ es la observación número $t$ $(1 \le t \le N)$ de la serie y $N$ es el número de observaciones de que consta la serie completa (el **tamaño** o la **longitud** de la serie). Las $N$ observaciones $y_1, y_2, ..., y_N$ pueden recogerse en un vector columna $\mathbf{y} \equiv [y_1,y_2,...,y_N]'$ de orden $N \times 1$.

## Representaciones matemáticas frecuentes de series temporales multivariantes

$y_1, y_2, ..., y_N$; $(y_t)^{N}_{t=1}$; $(y_t; t=1,...,N)$, donde $y_t \equiv [y_{t1}, y_{t2}, ..., y_{tM}]'$ $(M \ge 2)$ es la observación número $t$ $(1 \le t \le N)$ de la serie y $N$ es el número de observaciones de que consta la serie completa. Las $N$ observaciones $y_1, y_2, ..., y_N$ pueden recogerse en una matriz $\mathbf{Y}$ de orden $N \times M$.

$$\mathbf{Y} \equiv \begin{bmatrix} y_1'\\ y_ \end{bmatrix}$$