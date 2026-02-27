The **total expectation theorem** is similar to the [[Total probability theorem|total probability theorem]], but it applies to [[Expectation|expectations]].
$$E[X]=\sum_{i=1}^nP(A_i)E[gX|A_i]$$
And again, the logic can be applied to [[Random variable|random variables]], both [[Discrete random variable|discrete]] and [[Continuous random variable|continuous]].
$$E[X]=\sum_yp_Y(y)E[X|Y=y]$$
$$E[X]=\int f_Y(y)E[X|Y=y]\;dy$$

> [!proof]-
> The [[Discrete random variable|discrete]] case can be proven using the [[Total probability theorem|total probability theorem]]:
> $$
> \begin{align}
> E[X] &= \sum_xxp_X(x) \\
> &= \sum_xx\sum_yp_Y(y)p_{X|Y}(x|y) \\
> &= \sum_yp_Y(y)\sum_xxp_{X|Y}(x|y) \\
> &= \sum_yp_Y(y)E[X|Y=y]
> \end{align}
> $$
> The [[Continuous random variable|continuous]] case is proven by:
> $$
> \begin{align}
> \int E[X|Y=y]f_Y(y)\;dy&=\int\left[\int xf_{X|Y}(x|y)\;dx\right]f_Y(y)\;dy \\
> &=\iint xf_{X|Y}(x|y)f_Y(y)\;dx\;dy \\
> &=\iint xf_{X,Y}(x,y)\;dx\;dy \\
> &=\int x\left[\int f_{X,Y}(x,y)\;dy\right]\;dx \\
> &=\int xf_X(x)\;dx \\
> &= E[X]
> \end{align}
> $$
