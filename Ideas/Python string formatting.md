Python specifies a [[Python string|string]] **format specification**, which is used by [[Python f-string|f-strings]], [[Python t-string|t-strings]] and various `format()` functions. Generally it looks like this:

`[[fill]align][sign] [z][#] [0][width][grouping] .[precision][grouping] [type]`


##### Examples
```python
# Align
format(-1, '_A^4')) # 'A-1A' Set fill

format(-1, '_=4'))  # '-  1' Padding between (default when fill is "0")
format(-1, '_<4'))  # '-1  ' Left aligned (default)
format(-1, '_>4'))  # '  -1' Right alined (default for numbers)
format(-1, '_^4'))  # ' -1 ' Center aligned

# Sign
format(12, '-') # No leading sign for positive numbers (default)
format(12, '+') # Add leading sign for positive numbers
format(12, ' ') # Add leading space for positive numbers

# Flags
format(-0.0, 'z') # Turn -0 into 0
format(12, '#')   # Add '0x' to hex, decimal point to floats.

# Width
format(1, '5')  # '    1' Set width
format(1, '05') # '-0001' Sign-aware zero padding
format(1234567, '_') # '1_234_567' Insert "_" every 3rd digit
format(1234567, ',') # '1_234_567' Insert "," every 3rd digit

# Precision
format(1.2345, '.2f')   # '1.23' Digits after decimal in f, F, g, G types
format('abcd', '.2s')   # 'ab'   Size of string for string types
format(0.1234567, '_f') # '0.123,456,7' Insert "_" every 3rd digit
format(0.1234567, ',f') # '0.123_456_7' Insert "," every 3rd digit

# Types
format('hi', 's') # 'hi' String (default)

# Integer types
format(12, 'b') # '1100' Binary
format(97, 'c') # 'a'    Character
format(12, 'd') # '12'   Decimal
format(12, 'o') # '14'   Octal
format(12, 'x') # 'c'    Hexadecimal
format(12, 'X') # 'C'    Hexadecimal uppercase
format(12, 'n') # '12'   Uses locale to insert digit separators

# Float types
format(12, '.2e') # '1.20e+01' Scientific notation
format(12, '.2E') # '1.20E+01' Scientific notation uppercase
format(12, '.2f') # '12.00'    Fixed-point notation
format(12, '.2F') # '12.00'    Fixed-point notation uppercase
format(12, 'g')   # '12'       General format           (e or f)
format(12, 'G')   # '12'       General format uppercase (E or F)
format(12, 'n')   # '12'       Uses locale to insert digit seperators
format(12, '.2%') # '1200%'    Percentage