The **variance** of a [[Random variable|random variable]] $X$ is defined as $\text{var}(X)=E[(X-E[X])^2]$. Its square root is the [[Standard deviation|standard deviation]]. An easier formula for calculating this uses [[Moment|moments]]: $\text{var}(X)=E[X^2]-(E[X])^2$. 

Given a linear [[Functions|function]] $Y=aX+b$, we have $\text{var}(Y)=a^2\text{var}(X)$.

If two [[Random variable|random variables]] are [[Independent discrete random variable|independent]], then $\text{var}(X+Y)=\text{var}(X)+\text{var}(Y)$

>[!proof]-
> Proof of the alternative **variance** formula:
>$$
\begin{align}
\text{var}(X)&=E[(X-E[X])^2] \\
&= \sum_x(x-E[X])^2p_X(x) \\
&= \sum_x(x^2-2xE[X]+(E[X])^2)p_X(x) \\
&= \sum_xx^2p_X(x)-2E[X]\sum_xxp_X(x)+(E[X])^2\sum_xp_X(x) \\
&= E[X^2]-2(E[X^2])^2+(E[X])^2 \\
&= E[X^2]-(E[X]^2)
\end{align}
$$
