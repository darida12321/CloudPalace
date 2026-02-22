The **total expectation theorem** is similar to the [[Total probability theorem|total probability theorem]], but it applies to [[Expectation|expectations]].
$$E[X]=\sum_yp_Y(y)E[X|Y=y]$$

It can be verified by using the [[Total probability theorem|total probability theorem]]:
$$
\begin{align}
E[X] &= \sum_xxp_X(x) \\
&= \sum_xx\sum_yp_Y(y)p_{X|Y}(x|y) \\
&= \sum_yp_Y(y)\sum_xxp_{X|Y}(x|y) \\
&= \sum_yp_Y(y)E[X|Y=y]
\end{align}
$$
