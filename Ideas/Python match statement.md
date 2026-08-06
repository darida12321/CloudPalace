Used for pattern matching.
```python
match (1+2, 3):
    case (1, 3): pass # Literal pattern
    case my_var: pass # Capture pattern
    case _:      pass # Wildcard pattern
    case foo.x:  pass # Value pattern
	case (a):    pass # Group pattern (for grouping)
	case [1, 2]: pass # Sequence pattern
	case {a: 1}: pass # Mapping pattern
	case Foo(x, y=2)  # Class pattern (bind x, filter on y)
	
	case (1, 3) | (2, 3): pass # OR pattern
	case (1, 3) as name:  pass # AS pattern
	
	case (1, 3): pass             # Case
	case (3, 3) if (1 == 2): pass # Case with guard
```