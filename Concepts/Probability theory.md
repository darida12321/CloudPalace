# What is probability?
**Probability theory** is about the mathematical description of uncertain situations. For every uncertain experiment, we must define a [[Sample space|sample space]]: its possible outcomes, and a [[Probability law|probability law]]: the probability of each of those outcomes. This probability law must obey [[Kolmogorov’s axiomatization]].

##### But what *is* probability?
[[Kolmogorov’s axiomatization|Kolmogorov's axioms]] are clearly useful, but what *is* it that they actually describe? We use "probabilities" in many different contexts:
1. **Objective knowledge**: "Based on seismic data, an earthquake will probably hit Japan."
2. **An agent's confidence**: "I will probably get an A on this exam."
3. **A physical concept**: "This radium atom will probably decay in 10,000 years."

There is heated debate about which of these are real phenomena, and whether any of these are mere illusions created by the other two. However, most interpretations attempt to describe one of these three concepts.

A good interpretation must be:
- **Admissible**: An interpretation transforms all probability axioms into true statements.
- **Ascertainable**: There is a method for finding out what the probability of something is.
- **Applicable**: Probabilities are used everywhere. The interpretation should cover all cases.

Here are some of the leading interpretations:
- [[The classical interpretation of probability|Classical]]:  Reduce an event to equally likely possible outcomes, and count them.
- [[The logical interpretation of probability|Logical]]: Create a formal logical model describing each experiment.
- [[The evidential interpretation of probability|Evidential]]: Probability is not logical. It describes how some evidence helps a hypothesis.
- [[The subjective interpretation of probability|Subjective]]: Probability is an agent's belief. This one is the most widely accepted.
- [[The frequency interpretation of probability|Frequency]]: Probability is obtained by counting the results of experiments.
- [[The propensity interpretation of probability|Propensity]]: A physical property of a system, describing its tendency for certain results.
- [[The best-system interpretation of probability|Best-system]]: Probability is a human-made theory that systematizes observations.

Now with this philosophical tangent out of the way, let us get into the math.

# Probability concepts
Every [[Random event|random event]] has a set of possible outcomes, called a [[Sample space|sample space]]. Then, a [[Probability law|probability law]] assigns a value to each outcome, following [[Kolmogorov’s axiomatization]]. For an [[Random event|event]] $A$, this is denoted by $P(A)$. This is a [[Probability model|probability model]]

##### Random variables
When the outcomes are numerical in nature, or when it's helpful to map them to a number, we can define a [[Random variable|random variable]]. It is a function that maps every element of the [[Sample space|sample space]] to a number. When there are finite or [[Countable infinity|countably infinite]] possible outcomes, the [[Random variable|random variable]] is [[Discrete random variable|discrete]]. Otherwise, it's [[Continuous random variable|continuous]]. 

##### PMF, PDF and CDF
[[Discrete random variable|Discrete random variables]] are described by a [[Probability mass function|probability mass function (PMF)]]. It describes the probability of the outcome getting mapped to that number: $P(X=x)=p_X(x)$. On the other hand, [[Continuous random variable|continuous random variables]] are described by a [[Probability density function|probability density function (PDF)]]. The probability of the value falls into a specific interval is $P([a,b])=\int_a^bf_X(t)dt$. Note, that $f_X$ does not denote the probability of any event, as it can be greater than 1.

We can see that [[Probability mass function|PMFs]] and [[Probability density function|PDFs]] are different in nature, but they can be united by the [[Cumulative distribution function|cumulative distribution function (CDF)]]. It merges these concepts by accumulating the probabilities "up to" $x$.  $P(X<x)=F_X(x)$. In the [[Continuous random variable|continuous]] case, it's a continuous function, while in the [[Discrete random variable|discrete]] case, it has discrete jumps.

|                                                                                                                                                          | [[Probability mass function\|PMF]]                           | [[Probability density function\|PDF]]                        | [[Cumulative distribution function\|CDF]]                                    |
| :------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ---------------------------------------------------------------------------- |
| Definition [[Probability mass function\|PMF]], [[Probability density function\|PDF]], [[Cumulative distribution function\|CDF]]                          | $$p_X(x)=P(X\!=\!x)$$                                        | $$f_X(x)=\frac{P([x,x\!+\!\delta])}{\delta}$$                | $$F_X(x)=P(X\!\leq\!x)\;$$                                                   |
| Joint [[Joint probability mass function\|PMF]], [[Joint probability density function\|PDF]], [[Joint cumulative distribution function\|CDF]]             | $$p_{X,Y}(x,y)$$                                             | $$f_{X,Y}(x,y)$$                                             | $$F_{X,Y}(x,y)$$                                                             |
| Marginal [[Marginal probability mass function\|PMF]], [[Marginal probability density function\|PDF]], [[Marginal cumulative distribution function\|CDF]] | $$\begin{align}&p_X(x)= \\\sum_y&p_{X,Y}(x,y)\\\end{align}$$ | $$\begin{align}&f_X(x)=\\\int &f_{X,Y}(x,y)\;dy\end{align}$$ | $$\begin{align}&F_X(x)=\\\lim_{y\rightarrow\infty}&F_{X,Y}(x,y)\end{align}$$ |
##### Conditional probability
Conditional, independent, conditionally independent random vars

|                                                                                                                                                                         | [[Probability law\|Probability]]                                                | [[Discrete random variable\|Discrete variable]]                          | [[Continuous random variable\|Continuous variable]]                      |
| :---------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| [[Conditional probability]]:<br>([[Conditional probability mass function\|PMF]], [[Conditional probability density function\|PDF]])                                     | $$P(A\vert B)=\frac{P(A\cap B)}{P(B)}$$                                         | $$p_{X\vert Y}(x\vert y)$$                                               | $$f_{X\vert Y}(x\vert y)$$                                               |
| [[Independent events]]:<br>([[Independent discrete random variable\|PMF]], [[Independent continuous random variable\|PDF]])                                             | $$\begin{align}P(A\cap B)&=P(A)P(B)\\&\text{or}\\P(A\vert B)&=P(A)\end{align}$$ | $$\begin{align}p_{X,Y}(x,y)=\\p_X(x)p_Y(y)\end{align}$$                  | $$\begin{align}f_{X,Y}(x,y)=\\f_X(x)f_Y(y)\end{align}$$                  |
| [[Conditionally independent events]]:<br>([[Conditionally independent discrete random variables\|PMF]], [[Conditionally independent continuous random variables\|PDF]]) | $$P(A\vert B\cap C)=P(A\vert C)$$                                               | $$\begin{align}&p_{X\vert Y,A}(x\vert y)\\&=p_{X\vert A}(x)\end{align}$$ | $$\begin{align}&f_{X\vert Y,A}(x\vert y)\\&=f_{X\vert A}(x)\end{align}$$ |


# Probability theorems
Given our definitions, we can start defining some general probability concepts. We will explain them for the case of a [[Probability model|probability model]], however, they apply equally to [[Random variable|random variables]].



normalization property (p, disc, cont) SINGLE
multiplication rule (p, disc, cont) SINGLE
total probability theorem (p, disc, cont) SINGLE
bayes' rule (p, disc, cont) SINGLE

|                            | [[Probability law\|Probability]] | [[Discrete random variable\|Discrete variable]] | [[Continuous random variable\|Continuous variable]] |
| :------------------------- | -------------------------------- | ----------------------------------------------- | --------------------------------------------------- |
| [[Normalization property]] |                                  |                                                 |                                                     |









# Notable random variables
Explain expectation and variance (second central moment)





# NOTES

[[Functions on a random variable]]


RANDOM EVENTS
[[Bayes' rule]]: $P(A|B)=P(B|A)P(A)/P(B)$
[[Discrete Bayes' rule]]:
[[Continuous Bayes' rule]]: $f_{X|Y}(x|y)=f_X(x)f_{Y|X}(y|x)/f_Y(y)$ 


Sequential approach vs divide and conquer approach
[[Multiplication rule]]: $P(A_1\cap A_2)=P(A_1)P(A_2|A_1)$
[[Total probability theorem]]: $P(B)=\sum_iP(A_i)P(B|A_i)$


[[Normalization property]]: #TODO just add some shit to pdf-s and pmf-s. property of the axioms





Functions on a continuous random variable: #TODO 
$$F_Y(y)=P(g(X)\leq y)=\int_{\{x|g(x)\leq y\}}f_X(x)\;dx$$
$$f_Y(y)=\frac{dF_Y}{dy}(y)$$
if $Y=aX+b$, then:
$$f_Y(y)=\frac{1}{|a|}f_X\left(\frac{y-b}{a}\right)$$
if $f$ is [[Monotonity|monotonically increasing or decreasing]], and $h$ is its [[Inverse function|inverse]], then:
$$f_Y(y)=f_X(h(y))\left|\frac{dh}{dy}(y)\right|$$


Functions of multiple random variables: #TODO 






EXPECTATION AND VARIANCE
[[Expectation]]: $E[X]=\sum_xxp_X(x)$
[[Conditional expectation]]: $E[X|Y=y]=\sum_xxp_{X|Y}(x|y)$
[[Total expectation theorem]]: $E[X]=\sum_yp_Y(y)E[X|Y=y]$
[[Variance]]: $\text{var}(X)=E[(X-E[X])^2]$

SPECIFIC RANDOM VARIABLES
[[Discrete uniform random variable]]
[[Bernoulli random variable]]
[[Binomial random variable]]
[[Geometric random variable]]
[[Poisson random variable]]

[[Continuous uniform random variable]]
[[Exponential random variable]]
[[Normal random variable]]
[[Laplace distribution]]




counting:
[[The counting principle]]
[[Permutations]]
[[K-permutations]]
[[Combinations]]
[[Number of partitions]]




#TODO  kurtosis (after skew), and a p5js example depicting it graphically

---
sources:
- Interpretations of Probability: [Stanford Encyclopedia of Philosophy](https://plato.stanford.edu/entries/probability-interpret/)
- Math: [Bertsekas Tsitsiklis Introduction to probability](https://www.vfu.bg/en/e-Learning/Math--Bertsekas_Tsitsiklis_Introduction_to_probability.pdf)

