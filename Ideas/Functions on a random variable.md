Any [[Functions|function]] acting on a [[Random variable|random variable]] $X$ produces another [[Random variable|random variable]] $Y=g(X)$. The [[Probability mass function|PMF]] for $Y$ is defined as $p_Y(y)=\sum_{\{x|g(x)=y\}}p_X(x)$

The [[Expectation|expectation]] is: $E[g(X)]=\sum_x g(x)p_X(x)$ 
This also applies to [[Joint probability mass function|Joint PMFs]]: $E[g(X,Y)]=\sum_{x,y}g(x,y)p_{X,Y}(x,y)$

Given a linear function of the form $Y=aX+b$, we can easily calculate $Y$'s:
- [[Expectation]]: $E[Y]=aE[X]+b$
- [[Variance]]: $\text{var}(Y)=a^2\text{var}(X)$

