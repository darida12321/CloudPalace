[[Functions|Functions]] on a [[Continuous random variable|continuous random variable]] produce another [[Continuous random variable|random variable]]. This can often be analytically solved using by using this 2-step approach. First, calculate the [[Cumulative distribution function|CDF]] of the new variable. Then derivate it to arrive at the [[Probability density function|PDF]].
$$F_Y(y)=P(g(X)\leq y)=\int_{\{x|g(x)\leq y\}}f_X(x)\;dx$$
$$f_Y(y)=\frac{dF_Y}{dy}(y)$$
For a [[Linear transformation|linear]] [[Functions|function]] $Y=aX+b$, we have:
$$f_Y(y)=\frac{1}{|a|}f_X\left(\frac{y-b}{a}\right)$$
There is a special case when $f$ is [[Monotonity|monotonically increasing or decreasing]], and $h$ is its [[Inverse function|inverse function]]. then:
$$f_Y(y)=f_X(h(y))\left|\frac{dh}{dy}(y)\right|$$

