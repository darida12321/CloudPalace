In an experiment that is best described [[Sequential description of sample space|sequentially]], if we know the [[Conditional probability|conditional probability]] of each step, we can calculate the [[Probability law|probability]] of a sequence of events by:
$$P(\cap_{i=1}^nA_i)=P(A_1)P(A_2|A_1)P(A_3|A_1\cap A_2)\dots P(A_n|\cap_{i=1}^{n-1}A_i)$$

This logic also applies to [[Discrete random variable|discrete]] and [[Continuous random variable|continuous]] random variables:
$$p_{X_1,\dots,X_n}(x_1,\dots,x_n)=p_{X_1}(x_1)p_{X_2|X_1}(x_2|x_1)\dots p_{X_n|\cap_{i=1}^{n-1}x_i}(x_n|\cap_{i=1}^{n-1}x_i)$$
$$f_{X_1,\dots,X_n}(x_1,\dots,x_n)=f_{X_1}(x_1)f_{X_2|X_1}(x_2|x_1)\dots f_{X_n|\cap_{i=1}^{n-1}x_i}(x_n|\cap_{i=1}^{n-1}x_i)$$
 
