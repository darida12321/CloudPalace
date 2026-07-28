Inherits from **[[Python numbers module integral class|numbers module integral class]]**. Represents an [[Signed integer representation|signed int]], with arbitrary size.

**Constructor**:
- `1`
- `int(1.2)`
- `int('1')`
- `int('1f', 16)`
**Class methods**:
- `int.from_bytes()`: Convert [[Python bytes|bytes]] to integer
**Functions**:
- `x.bit_length()`: Return number of bits it takes up. (minus sign and leading zeros)
- `x.bit_count()`: Return number of ones in the binary representation.
- `x.to_bytes()`: Return array of bytes representing the integer.
- `x.as_integer_ratio()`: Return the int itself and 0. Exists to match [[Python float|floats]].
- `x.is_integer()`: Return True. Exists to match [[Python float|floats]].
**Operations**:
- `complex()`: Conversion to complex
- `bool()`: Conversion to bool
- `+`, `-`, `*`, `/`, `**`
- `abs()`: Absolute value

