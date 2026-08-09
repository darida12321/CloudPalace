This module implements a lot of math functions.

**Number theory**:
- `comb(n, k)`: [[Combinations]] of choosing $k$ out of $n$ items.
- `perm(n, k)`: [[Permutations]] of choosing $k$ out of $n$ items.
- `factorial(n)`: Factorial $n!$
- `gcd(*ints)`: Greatest common divisor.
- `lcm(*ints)`: Least common multiple.
- `isqrt(n)`: Integer square root.

**Floating point arithmetic**:
- `ceil(x)`, `floor(x)`, `trunc(x)`: Rounding
- `fabs(x)`: Absolute value
- `fma(x, y, z)`: Fused multiply and add `(x*y)+z`.
- `fmod(x, y)`: Remainder of `x/y`.
- `modf(x)`: Fractional and integer parts
- `remainder(x, y)`: Remainder of `x` with respect to `y`.

- `copysign(x, y)`: Absolute of `x` with the sign of `y`.
- `frexp(x)`: Mantissa and exponent of `x`.
- `ldexp(x, i)`: Reverse of `frexp(x)`. Calculated by `x * (2**i)`.
- `isclose(a, b, rel_tol, abs_tol)`: Check if `a` and `b` are close with tolerance.
- `isfinite(x)`, `isinf(x)`, `isnan(x)`: Check for unique [[Floating-point representation|floating point]] values.
- `nextafter(x, y, steps)`: A float `steps` steps after `x` towards `y`.
- `ulp(x)`: Least significant bit.

**Powers and logs**:
- `sqrt(x)`: Square root $\sqrt{x}$.
- `cbrt(x)`: Cube root $\sqrt[3]{x}$.
- `pow(x, y)`: Power $x^y$.
- `exp(x)`: Exponential $e^x$.
- `exp2(x)`: Exponential base 2 $2^x$.
- `expm1(x)`: Exp x-1. $e^{x-1}$.
- `log(x, base)`: Log base `base`. $\log_\text{base}{x}$.
- `log1p(x)`: Natural log of x+1. $log{x+1}$.
- `log2(x)`: Log base 2 $\log_2{x}$.
- `log10(x)`: Log base 10 $\log_{10}{x}$.

**Summation and product**:
- `dist(p, q)`: Euclidean distance.
- `fsum(iterable)`: Sum of values in `iterable`.
- `hypot(*coords)`: Euclidean norm of coordinates.
- `prod(iterable, start)`: Product of elements with a `start` value.
- `sumprod(p, q)`: Sum of products from two iterables.

**Trigonometry**:
- `degrees(x)`, `radians(x)`: Angle conversion
- `acos(x)`, `asin(x)`, `atan(x)`, `atan2(y, x)`, `cos(x)`, `sin(x)`, `tan(x)`: Trig functions
- `acosh(x)`, `asinh(x)`, `atanh(x)`, `cosh(x)`, `sinh(x)`, `tanh(x)`: Hyperbolic functions

**Special functions**:
- `erf(x)`: The error function
- `erfc(x)`: The complementary error function.
- `gamma(x)`: The gamma function.
- `lgamma(x)`: Natural logarithm of the absolute of the gamma function.

**Constants**:
- `pi`: $\pi$.
- `e`: Euler's number.
- `tau`: $2*\pi$.
- `inf`: Positive infinity.
- `nan`: Not a number.