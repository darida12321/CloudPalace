The most common way of representing [[Fractional representation|fractional numbers]]. It essentially uses scientific notation in binary $M*2^E$. A float is comprised of three parts: 
- **Sign bit**: Single bit denoting the sign.
- **Mantissa**: Number between $1$ and $10_2$.
- **Exponent**: The power to raise the mantissa to.

The **mantissa** always has one number before the decimal point. In [[Number base|base 10]] that gives 9 options (1-9), but in [[Number base|base 2]], its value can only be 1 so it's not written out explicitly. As such, the bits correlate to the 1/2, 1/4, 1/8, ... positions.

The **exponent** is represented in [[Excess-K|excess-K]] notation. However, the lowest (all 0) and highest (all 1) values represent special values.
- **Exponent** is 0s: If the **mantissa** is 0, the value is 0. Else it's subnormal (close to 0)
- **Exponent** is 1s: If the **mantissa** is 0, the value is +/- infinity. Else, it's Nan (not a number) 

The specs are specified in the **IEEE** (Institute of Electrical and Electronics Engineers) standard. It has multiple floating point formats. Two of the most common ones are:
- **Single precision**: 32 bit (1 sign bit, 8 **exponent** bits in [[Excess-K|excess-127]], 23 **mantissa** bits)
- **Double precision**: 64 bit. (1 sign bit, 11 **exponent** bits in [[Excess-K|excess-1023]], 52 **mantissa** bits)



