By combining the definition of [[Conditional probability|conditional probability]], and the [[Multiplication rule|multiplication rule]], we get:
$$P(A|B)=\frac{P(B|A)P(A)}{P(B)}$$
The **discrete** equivalent, applying to [[Discrete random variable|discrete random variables]]:
$$p_{X|Y}(x|y)=\frac{p_X(x)p_{Y|X}(y|x)}{p_Y(y)}=\frac{p_X(x)p_{Y|X}(y|x)}{\sum p_X(t)p_{Y|X}(y|t)\;dt}$$

The **continuous** equivalent, applying to [[Continuous random variable|continuous random variables]]:
$$f_{X|Y}(x|y)=\frac{f_X(x)f_{Y|X}(y|x)}{f_Y(y)}=\frac{f_X(x)f_{Y|X}(y|x)}{\int f_X(t)f_{Y|X}(y|t)\;dt}$$
