The **cumulative distribution function** (CDF) unites the [[Probability mass function|probability mass function]] and the [[Probability density function|probability density function]]. Essentially, it "accumulates" the probability "up to" $x$. It is defined as $F_X(x)=P(X\leq x)$.

| [[Discrete random variable\|Discrete]]                          | [[Continuous random variable\|Continuous]] |
| :-------------------------------------------------------------- | ------------------------------------------ |
| $$F_X(x)=\sum_{k\leq x}p_X(k)$$                                 | $$F_X(x)=\int_{-\infty}^xf_X(t)dt$$        |
| $$p_X(k)=F_X(k)-F_X(k-1)$$(When $X$ only takes integer values.) | $$f_X(x)=\frac{dF_X}{dx}x$$                |
The [[Normalization property|normalization property]] can be transformed into conditions on the [[Limit|limits]] of the function:
$$\lim_{x\rightarrow -\infty}F_X(x)=0\qquad\lim_{x\rightarrow\infty}F_X(x)=1$$

