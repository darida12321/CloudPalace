A **formatted string literal** is created similarly to regular [[Python string|strings]], but with an `f` or `F` at the beginning (`f'string'`, `f"string"`, `f'''string'''`, `f"""string"""`).

It allows for expressions to be evaluated within curly brackets.
- **Debug specifier**: An `=` at the end will print the expression, then its value.
- **Conversion specifier**: `!s`, `!r` or `!a` will format it with `str()`, `repr()` or `ascii()`.
- **Format specifier**: Putting `:` at the end will format it using [[Python string formatting|string formatting]].

```python
myvar = 1/2
f'The variable is {myvar}' # 'The variable is 0.5'

# Debug specifier
f'{myvar=}' # 'myvar=0.5'

# Conversion specifier
f'{myvar!s}' # Format using str()
f'{myvar!r}' # Format using repr()
f'{myvar!a}' # Format using ascii()

# Formatting specifier
f'{myvar:.2f}' # Apply formatting, 0.5000

# Everything together
f'{myvar=!s:_^7}' # myvar=__0.5__
```

