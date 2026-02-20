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

# Probability

[[Probabilistic models]]. We start with [[Kolmogorov’s axiomatization]], where we get $P(A)$.

[[Conditional probability]] $P(A|B)$
$$P(A|B)=\frac{P(A\cup B)}{P(B)}$$



#TODO

---
sources:
- Interpretations of Probability: [Stanford Encyclopedia of Philosophy](https://plato.stanford.edu/entries/probability-interpret/)
- Math: [Bertsekas Tsitsiklis Introduction to probability](https://www.vfu.bg/en/e-Learning/Math--Bertsekas_Tsitsiklis_Introduction_to_probability.pdf)

