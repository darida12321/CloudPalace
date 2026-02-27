A [[Continuous random variable|continuous random variable]], with an even distribution between values $a$ and $b$. It is analogous to the [[Discrete uniform random variable|discrete uniform random variable]].
$$
f_X(x)=
\begin{cases}
1/(b-a)&\quad\text{if }a\leq x\leq b, \\
0&\quad\text{otherwise},
\end{cases}
$$

| [[Expectation\|Mean]] | [[Variance\|Variance]] |
| --------------------- | ---------------------- |
| $$\frac{a+b}{2}$$     | $$\frac{(b-a)^2}{12}$$ |
> [!proof]-
> We get the value 1/(b-a) by the **normalization property** of [[Continuous random variable|continuous random variables]]. Assuming the constant value is $c$, we get:
> $$1=\int_{-\infty}^\infty f_X(x)dx=\int_a^bc\;dx=c\int_a^b1dx=c(b-a)$$
