# What is probability?
**Probability theory** is about the mathematical description of uncertain situations. For every uncertain experiment, we must define a [[Sample spaces|sample space]]: its possible outcomes, and a [[Probability law|probability law]]: the probability of each of those outcomes. This probability law must obey [[Kolmogorov’s axiomatization]].

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

Describe probability, conditional, Bayes' theorem
Describe random vars, multiple, conditionals
Describe independence
Sequential vs divide and conquer

# Notable random variables
Explain expectation and variance (second central moment)


[[Probabilistic models]]. We start with [[Kolmogorov’s axiomatization]], where we get $P(A)$.
[[Random variable]]
[[Functions on a random variable]]


RANDOM EVENTS
[[Random event]]: $A$
[[Probability law]]: $P(A)$ 
[[Conditional probability]]: $P(A|B)=P(A\cap B)/P(B)$
[[Bayes' theorem]]: $P(A|B)=P(B|A)P(A)/P(B)$

Sequential approach vs divide and conquer approach
[[Multiplication rule]]: $P(A_1\cap A_2)=P(A_1)P(A_2|A_1)$
[[Total probability theorem]]: $P(B)=\sum_iP(A_i)P(B|A_i)$

Independence
[[Independent events]]: 
$P(A\cap B)=P(A)*P(B)$
$P(A|B)=P(A)$ 
[[Conditionally independent events]]: 
$P(A\cap B|C)=P(A|C)P(B|C)$
$P(A|B\cap C)=P(A|C)$

DISCRETE RANDOM VARIABLES:
[[Discrete random variable]]: $X$
[[Probability mass function]]: $p_X(x)$
[[Joint probability mass function]]: $p_{X,Y}(x,y)=P(X=x,Y=y)$
[[Conditional probability mass function]]: $p_{X|Y}(x|y)=p_{X,Y}(x,y)/p_Y(y)$

Sequential approach vs divide and conquer approach
[[Multiplication rule]]: $p_{X,Y}(x,y)=p_Y(y)p_{X|Y}(x|y)$
[[Total probability theorem]]: $p_X(x)=\sum_yp_Y(y)p_{X|Y}(x|y)$

Independence
[[Independent random variable]]: 
$p_{X,Y}(x,y)=p_X(x)p_Y(y)$
$p_{X|Y}(x|y)=p_X(x)$
[[Conditionally independent random variables]]: 
$P_{X,Y|A}(x,y)=p_{X|A}(x)p_{Y|A}(y)$
$p_{X|Y,A}(x|y)=p_{X|A}(x)$


EXPECTATION AND VARIANCE
[[Expectation]]: $E[X]=\sum_xxp_X(x)$
[[Conditional expectation]]: $E[X|Y=y]=\sum_xxp_{X|Y}(x|y)$
[[Total expectation theorem]]: $E[X]=\sum_yp_Y(y)E[X|Y=y]$
[[Variance]]: $\text{var}(X)=E[(X-E[X])^2]$

SPECIFIC RANDOM VARIABLES
[[Bernoulli random variable]]
[[Binomial random variable]]
[[Geometric random variable]]
[[Poisson random variable]]







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

