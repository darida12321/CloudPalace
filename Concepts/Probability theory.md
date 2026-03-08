Probability theory is the mathematical field describing [[Random event|random events]]. Each [[Random event|event]] has a set of possible outcomes, called a [[Sample space|sample space]]. A [[Probability law|probability law]] assigns a value to each outcome, following [[Kolmogorov’s axiomatization]]. For an [[Random event|event]] $A$, this is denoted by $P(A)$. This is a [[Probability model|probability model]]

# Random variables
When the outcomes of the [[Sample space|sample space]] are numerical in nature, or when it's helpful to map them to a number, we can define a [[Random variable|random variable]]. It is a function that maps every element of the [[Sample space|sample space]] to a number. When there are finite or [[Countable infinity|countably infinite]] possible outcomes, the [[Random variable|random variable]] is [[Discrete random variable|discrete]]. Otherwise, it's [[Continuous random variable|continuous]]. 

[[Discrete random variable|Discrete random variables]] are described by a [[Probability mass function|probability mass function (PMF)]]. It denotes the probability of the outcome getting mapped to that number: $P(X=x)=p_X(x)$. On the other hand, [[Continuous random variable|continuous random variables]] are described by a [[Probability density function|probability density function (PDF)]]. It denotes the probability that the random variable falls into a specific interval $P([a,b])=\int_a^bf_X(t)dt$. Note, that $f_X$ does not equal the probability of any event. Rather, it describes a probability per unit distance. This means that it can take values greater than 1.

We can see that [[Probability mass function|PMFs]] and [[Probability density function|PDFs]] are different in nature, but they can be united by the [[Cumulative distribution function|cumulative distribution function (CDF)]]. It merges these concepts by accumulating the probabilities "up to" $x$.  $P(X<x)=F_X(x)$. In the [[Continuous random variable|continuous]] case, it's a continuous function, while in the [[Discrete random variable|discrete]] case, it has discrete jumps.

For both [[Probability mass function|PMFs]], [[Probability density function|PDFs]] and [[Cumulative distribution function|CDFs]], we can define **joint** probabilities: the probability that two [[Random variable|random variables]] have the specified value. From a joint probability, we can also determine **marginal** probabilities by summing the values up along an axis.

For solving problems, the [[Normalization property|normalization property]] is often useful. It's one of the [[Kolmogorov’s axiomatization|axioms]], which states that the sum of all probabilities is 1.

|                                                                                                                                                          | [[Probability mass function\|PMF]]                           | [[Probability density function\|PDF]]                                                                     | [[Cumulative distribution function\|CDF]]                                                           |
| :------------------------------------------------------------------------------------------------------------------------------------------------------- | :----------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------- |
| Definition [[Probability mass function\|PMF]], [[Probability density function\|PDF]], [[Cumulative distribution function\|CDF]]                          | $$p_X(x)\!=\!P(X\!\!=\!x)$$                                  | $$f_X(x)\!=\!\frac{P([x,x\!+\!\delta])}{\delta}$$                                                         | $$F_X(x)\!=\!P(X\!\!\leq\!x)\;$$                                                                    |
| Joint [[Joint probability mass function\|PMF]], [[Joint probability density function\|PDF]], [[Joint cumulative distribution function\|CDF]]             | $$\begin{align}&p_{X,Y}(x,y)=\\P(&X=x,Y=y)\end{align}$$      | $$\begin{align}&\qquad f_{X,Y}(x,y)=\\&\frac{P([x,x\!+\!\delta],[y,y\!+\!\delta])}{\delta^2}\end{align}$$ | $$\begin{align}&F_{X,Y}(x,y)=\\P(&X\leq x,Y\leq y)\end{align}$$                                     |
| Marginal [[Marginal probability mass function\|PMF]], [[Marginal probability density function\|PDF]], [[Marginal cumulative distribution function\|CDF]] | $$\begin{align}&p_X(x)= \\\sum_y&p_{X,Y}(x,y)\\\end{align}$$ | $$\begin{align}& f_X(x)=\\\int &f_{X,Y}(x,y)\;dy\end{align}$$                                             | $$\begin{align}&F_X(x)=\\\lim_{y\rightarrow\infty}&F_{X,Y}(x,y)\end{align}$$                        |
| [[Normalization property]]                                                                                                                               | $$\sum_xp_X(x)=1$$                                           | $$\int_{-\infty}^\infty f_X(x)\;dx=1$$                                                                    | $$\begin{align}\lim_{x\rightarrow -\infty}F_X(x)=0\\\lim_{x\rightarrow \infty}F_X(x)=1\end{align}$$ |
# Conditional probability
What is the probability of an [[Random event|event]], given that another event has happened (i.e. we have some prior knowledge)? This question comes up a lot in probability theory. We use [[Conditional probability|conditional probability]] as another [[Probability law|probability law]], since it follows [[Kolmogorov’s axiomatization]].

[[Conditional probability]] captures the information that an event provides about another event. However, there is a special case, where 2 events do not provide any information about each other. These are called [[Independent events|independent events]]. Three or more [[Independent events|independent events]] does not imply that any two of those are also [[Independent events|independent]]

Two [[Random event|events]] can also be [[Conditionally independent events|conditionally independent]]. It's worth noting that this does not imply regular [[Independent events|independence]], and vice versa.

|                                                                                                                                                                         | [[Probability law\|Probability]]                                                | [[Discrete random variable\|Discrete variable]]                          | [[Continuous random variable\|Continuous variable]]                      |
| :---------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| [[Conditional probability]]:<br>([[Conditional probability mass function\|PMF]], [[Conditional probability density function\|PDF]])                                     | $$P(A\vert B)=\frac{P(A\cap B)}{P(B)}$$                                         | $$p_{X\vert Y}(x\vert y)$$                                               | $$f_{X\vert Y}(x\vert y)$$                                               |
| [[Independent events]]:<br>([[Independent discrete random variable\|PMF]], [[Independent continuous random variable\|PDF]])                                             | $$\begin{align}P(A\cap B)&=P(A)P(B)\\&\text{or}\\P(A\vert B)&=P(A)\end{align}$$ | $$\begin{align}p_{X,Y}(x,y)=\\p_X(x)p_Y(y)\end{align}$$                  | $$\begin{align}f_{X,Y}(x,y)=\\f_X(x)f_Y(y)\end{align}$$                  |
| [[Conditionally independent events]]:<br>([[Conditionally independent discrete random variables\|PMF]], [[Conditionally independent continuous random variables\|PDF]]) | $$P(A\vert B\cap C)=P(A\vert C)$$                                               | $$\begin{align}&p_{X\vert Y,A}(x\vert y)\\&=p_{X\vert A}(x)\end{align}$$ | $$\begin{align}&f_{X\vert Y,A}(x\vert y)\\&=f_{X\vert A}(x)\end{align}$$ |
# Mean, variance and beyond
The distributions of a [[Random variable|random variable]] can be quite complex. However, we often don't care about the fine details, and just want to know the general "shape" of the distribution.

For that, the first and most useful attribute is the [[Mean|mean]]. This is the same as the [[Expectation|expected value]] of the [[rand. Then, if we centralize the distribution (set their [[Mean|mean]] to 0), we can calculate their [[Variance|variance]]. This measures how "spread out" the distribution is.

If we set the [[Mean|mean]] to 0 and the [[Variance|variance]] to 1, we get a **standardized** distribution. In this case, we can still get more information about its shape by using [[Standardized moment|standardized moments]] or [[Cumulant|cumulants]]. These two agree on the definition of the [[Skew|skew]] (leaning). However, [[Kurtosis|kurtosis]] (pointiness) is rarely used, and these two approaches define it differently.

To aid with the calculation of expectations, we can use the [[Total expectation theorem|total expectation theorem]], which is the equivalent of the [[Total probability theorem|total probability theorem]]. $E[X]=\sum_{i=1}^nP(A_i)E[gX|A_i]$

| Name         | Description                                         | Definition                                                            |
| :----------- | --------------------------------------------------- | --------------------------------------------------------------------- |
| [[Mean]]     | First [[Moment\|moment]]                            | $$\mu=E[X]$$                                                          |
| [[Variance]] | Second [[Central moment\|central moment]]           | $$\begin{align}\sigma^2&=E[(X-E[X])^2\\&=E[X^2]-(E[X])^2\end{align}$$ |
| [[Skew]]     | Third [[Standardized moment\|standardized moment]]  | $$\frac{\mu_3}{\sigma^3}=\frac{E[(X-\mu)^3]}{(E[(X-\mu)^2])^{3/2}}$$  |
| [[Kurtosis]] | Fourth [[Standardized moment\|standardized moment]] | $$\frac{\mu_4}{\sigma^4}=\frac{E[(X-\mu)^4]}{(E[(X-\mu)^2])^{4/2}}$$  |

# Probability theorems
Given these definitions, we can start developing some theorems that help us solve probability problems. We will explain them using regular [[Probability law|probabilities]], however, they also apply to [[Random variable|random variables]].

The [[Sample space|sample space]] is often built up of multiple random phenomena. This can make it difficult to count up all the ways an [[Random event|event]] could happen. There are two approaches to handling this:
- [[Total probability theorem|Divide and conquer]]: First, [[Partition of a set|partition]] the [[Sample space|sample space]] into simpler subspaces. Check the probability of the [[Random event|event]] in each [[Subset|subset]], then add them together.
- [[Multiplication rule|Sequentially]]: If events happen in a sequential manner, enumerate all the possible paths via which you can get to the [[Random event|event]], evaluate their probabilities, and add them together.

A famous result, [[Bayes' rule]], comes from the combination of the [[Multiplication rule|multiplication rule]] and the definition of [[Conditional probability|conditional probability]].  It describes how the probability of an event changes given some evidence.
$$P(A|B)=\frac{P(B|A)P(A)}{P(B)}$$

|                               |                        [[Probability law\|Probability]]                        |                             [[Discrete random variable\|Discrete variable]]                              |                           [[Continuous random variable\|Continuous variable]]                            |
| :---------------------------- | :----------------------------------------------------------------------------: | :------------------------------------------------------------------------------------------------------: | :------------------------------------------------------------------------------------------------------: |
| [[Total probability theorem]] |         $$\begin{align}&P(B)=\\\sum_{i=1}^n&P(A_i\cap B)\end{align}$$          |                $$\begin{align}&p_X(x)=\\\sum_{i=1}^n&P(A_i)p_{X\vert A_i}(x)\end{align}$$                |                $$\begin{align}&f_X(x)=\\\sum_{i=1}^n&P(A_i)f_{X\vert A_i}(x)\end{align}$$                |
| [[Multiplication rule]]       |    $$\begin{align}&\;\;P(A_1\cap A_2)=\\&P(A_1)P(A_2\vert A_1)\end{align}$$    |     $$\begin{align}&p_{X_1,X_2}(x_1,x_2)=\\p_{X_1}&(x_1)p_{X_2\vert X_1}(x_2\vert x_1)\end{align}$$      |    $$\begin{align}&f_{X_1,X_2}(x_1,x_2)=\\f_{X_1}&(x_1)f_{X_2\vert X_1}(x_2\vert x_1\!)\end{align}$$     |
| [[Bayes' rule]]               | $$\begin{align}&\quad P(A\vert B)=\\&\frac{P(B\vert A)P(A)}{P(B)}\end{align}$$ | $$\begin{align}&\quad p_{X\vert Y}(x\vert y)=\\&\frac{p_X(x)p_{Y\vert X}(y\vert x)}{p_Y(y)}\end{align}$$ | $$\begin{align}&\quad f_{X\vert Y}(x\vert y)=\\&\frac{f_X(x)f_{Y\vert X}(y\vert x)}{f_Y(y)}\end{align}$$ |
# Functions on random variables
[[Functions|Functions]] on [[Random variable|random variables]] $Y=g(X)$ produce other [[Random variable|random variables]]. There is no general formula for this, they are defined as $p_Y(y)=\sum_{\{x|g(x)=y\}}p_X(x)$. For [[Continuous random variable|continuous random variables]], there is a [[Functions on a continuous random variable|method]] to get an analytical solution.

A [[Functions|function]] acting on an [[Expectation|expectation]] is also easy to define: $E[g(X)]=\sum_x g(x)p_X(x)$ 
A special case is when a [[Functions|function]] is [[Linear transformation|linear]], $Y=aX+b$.
- [[Expectation]]: $E[Y]=aE[X]+b$
- [[Variance]]: $\text{var}(Y)=a^2\text{var}(X)$

Given two [[Random variable|random variables]], that are [[Independent events|independent]], we also have $E[XY]=E[X]E[Y]$.

# Notable random variables
Some [[Random variable|random variables]] tend to come up a lot in practice. They have been named, and their [[Mean|mean]] and [[Variance|variance]] are well known.

##### Discrete random variables
[[Discrete uniform random variable]]: A uniformly distributed variable. #TODO 
[[Bernoulli random variable]]: Toss a coin, which comes up heads with probability $p$.
[[Binomial random variable]]: Toss $n$ coins, and count how many came up heads.
[[Geometric random variable]]: Toss coins until a heads comes up. How many tosses did it take?
[[Poisson random variable]]: ??? #TODO 

##### Continuous random variables
[[Continuous uniform random variable]]: A uniformly distributed variable
[[Exponential random variable]]: Distance between randomly occurring events.
[[Normal random variable]]: Occurs a lot due to the [[Central limit theorem|central limit theorem]]. #TODO
[[Laplace distribution]] #TODO 
[[Cauchy distribution]] #TODO



---
sources:
- Interpretations of Probability: [Stanford Encyclopedia of Philosophy](https://plato.stanford.edu/entries/probability-interpret/)
- Math: [Bertsekas Tsitsiklis Introduction to probability](https://www.vfu.bg/en/e-Learning/Math--Bertsekas_Tsitsiklis_Introduction_to_probability.pdf)

