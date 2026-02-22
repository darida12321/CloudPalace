A [[Discrete random variable|discrete random variable]] which is *essentially* a [[Binomial random variable|binomial random variable]] with very small $p$, and very large $n$. The $\lambda$ represents $n*p$ (the sizes cancel out).
$$p_X(k)=e^{-k}\frac{\lambda^k}{k!},\qquad k=0,1,\dots$$
The [[Expectation|mean]] is $\lambda$.
The [[Variance|variance]] is $p(1-p)$.

Calculation for the mean of the **Poisson random variable**. 
$$
\begin{align}
E[X] &= \sum_{k=0}^\infty ke^{-\lambda}\frac{\lambda^k}{k!} \\
&= \sum_{k=1}^\infty ke^{-\lambda}\frac{\lambda^k}{k!}\qquad\text{the }k=0\text{ term is zero} \\
&= \lambda\sum_{k=1}^\infty e^{-\lambda}\frac{\lambda^{k-1}}{(k-1)!} \\
&= \lambda\sum_{m=0}^\infty e^{-\lambda}\frac{\lambda^{m}}{m!}\qquad\text{let }m=k-1 \\
&= \lambda
\end{align}
$$


