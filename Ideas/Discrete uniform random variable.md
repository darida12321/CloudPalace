A [[Discrete random variable|discrete random variable]], with an even distribution between values $a$ and $b$.
$$
f_X(x)=
\begin{cases}
1/(b-a+1)&\quad\text{if }a\leq x\leq b, \\
0&\quad\text{otherwise},
\end{cases}
$$

| [[Mean\|Mean]]    | [[Variance\|Variance]] |
| ----------------- | ---------------------- |
| $$\frac{a+b}{2}$$ | $$\frac{(b-a)^2}{12}$$ |
> [!proof]-
> We get the value 1/(b-a) by the [[Normalization property|normalization property]] of [[Discrete random variable|continuous random variables]]. Assuming the constant value is $c$, we get:
> $$1=\sum f_X(x)dx=(b-a+1)c$$
