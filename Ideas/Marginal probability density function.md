From a [[Joint probability density function|joint PDF]], you can calculate the **marginal PMF** by:
$$f_X(x)=\int_{-\infty}^\infty f_{X,Y}(x,y)\;dy=\int_{-\infty}^\infty f_Y(y)f_{X|Y}(x|y)\;dy$$
This is generalizable for higher dimensions:
$$f_{X,Y}(x,y)=\int_{-\infty}^\infty f_{X,Y,Z}(x,y,z)\;dz$$
$$f_Y(y)=\int_{-\infty}^\infty \int_{-\infty}^\infty p_{X,Y,Z}(x,y,z)\;dx\;dz$$

This has the [[Normalization property|normalization property]]:
$$\int_{-\infty}^\infty \int_{-\infty}^\infty f_{X,Y}(x,y)\;dx\;dy=1$$







