The **expected value** (also called **expectation** or [[Mean|mean]]) of a [[Random variable|random variable]] $X$ is the weighted average of all outcomes. This is the first [[Moment|moment]] of the variable.

|                     | [[Discrete random variable\|Discrete]] | [[Continuous random variable\|Continuous]]   |
| :------------------ | -------------------------------------- | -------------------------------------------- |
| Expectation         | $E[X]=\sum_xxp_X(x)$                   | $E[X]=\int_{-\infty}^\infty xf_X(x)dx$       |
| Expected value rule | $E[f(X)]=\sum_xf(x)p_X(x)$             | $E[f(X)]=\int_{-\infty}^\infty f(x)f_X(x)dx$ |

##### Applying functions
The [[Expectation|expectation]] is: $E[g(X)]=\sum_x g(x)p_X(x)$ 
This also applies to [[Joint probability mass function|Joint PMFs]]: $E[g(X,Y)]=\sum_{x,y}g(x,y)p_{X,Y}(x,y)$
Given a [[Linear transformation|linear]] [[Functions|function]] $Y=aX+b$,  $Y$'s expectation is: $E[Y]=aE[X]+b$

If two [[Random variable|random variables]] are [[Independent discrete random variable|independent]], then $E[XY]=E[X]E[Y]$. In fact, for any two  [[Functions|functions]] $f$ and $g$, we get $E[f(X)g(Y)]=E[f(X)]E[g(Y)]$



