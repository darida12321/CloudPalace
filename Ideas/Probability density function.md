The **probability density function** (PDF) for a [[Continuous random variable|continuous random variable]] $X$ is denoted $f_X$. The probability of $X$ being in a subset $B$ of the real line is $P(X\in B)=\int_Bf_X(x)dx$, and the probability of $X$ being in a range is $P(a\leq X\leq b)=\int_a^bf_X(x)dx$. This can be interpreted as the area under the **PDF**.

The [[Normalization property|normalization property]] for **PDFs** looks like this: 
$$\int_{-\infty}^\infty f_X(x)dx=P(-\infty<X<\infty)=1$$

For any single value, $P(X=a)=\int_a^af_X(x)dx=0$. The **PDF** doesn't define the probability of $x$, but rather, the "probability mass per unit length". This can be seen by taking a very small interval $P([x,x+\delta])=\int_x^{x+\delta}f_X(t)dt\approx f_X(x)*\delta$.






