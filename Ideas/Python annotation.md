[[Python callable|Function]] parameters, return values, and [[Python variable|variables]] can have **annotations**.
It doesn't have to be a [[Python types module|type]], it can be any value, since the interpreter ignores it. However, it can be useful for static type checkers.

Intended use:
```python
x: int = 3

def func(a: int, b: int) -> int:
	return a+b
```

Also possible:
```python
x: int = 'Hello'

def func(a: 6, b: True) -> 'Hello':
	return a+b
```

Annotations are lazily evaluated, and constrained to **annotation scopes**. These are created by **annotations**, [[Python type parameter list statement|type parameter lists]] and [[Python type statement|type]] statements.