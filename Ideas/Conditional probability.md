**Conditional probability** calculates the probability of an [[Random event|event]] $A$, given that $B$ happened (so $P(B)>0$). We denote this with $P(A|B)$. 
$$P(A|B)=\frac{P(A\cap B)}{P(B)}$$

This specifies a new [[Probability law|probability law]] where the [[Sample space|sample space]] is $B$. It follows [[Kolmogorov’s axiomatization]]:
- **Nonnegativity**: $\forall A.P(A|B)\geq 0$
- **Normalization**: $P(\Omega|B)=P(\Omega\cap B)/P(B)=P(B)/P(B)=1$
- **Additivity**: 
$$
\begin{align}

P(A_1\cup A_2|B)&=\frac{P((A_1\cup A_2)\cap B)}{P(B)} \\
&=\frac{P((A_1\cap B)\cup(A_2\cap B))}{P(B)} \\
&=\frac{P(A_1\cap B)+P(A_2\cap B)}{P(B)} \\
&=P(A_1|B)+P(A_2|B)

\end{align}
$$

#TODO format as proof


