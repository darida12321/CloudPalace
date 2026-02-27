The **conditional probability density function** takes a regular [[Probability density function|PDF]], and conditions it on a [[Random event|random event]], or another [[Random variable|random variable]].

Conditioning on an [[Random event|event]]:  
$$P(X\in B|A)=\int_Bf_{X|A}(x)dx$$
Now we must figure out what $f_{X|A}$ is. Consider the [[Random event|event]] that $X$ belongs to a [[Subset|subset]] $A$ of the real line:
$$P(X\in B|X\in A)=\frac{P(X\in B\land X\in A)}{P(X\in A)}=\frac{\int_{A\cap B}f_X(x)dx}{P(X\in A)}$$
These two definitions must match, so we get:
$$
f_{X|A}(x|A)=
\begin{cases}
\frac{f_X(x)}{P(X\in A)}&\qquad\text{if }x\in A, \\
0&\qquad\text{otherwise},
\end{cases}
$$

Conditioning on a [[Random variable|random variable]]: 
$$f_{X|Y}(x|y)=\frac{f_{X,Y}(x,y)}{f_Y(y)}$$



