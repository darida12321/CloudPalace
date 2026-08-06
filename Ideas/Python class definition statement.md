A class definition is an [[Python callable|executable]] statement. It can inherit from a list of **base classes**. If no parents are set, then it will inherit from [[Python object|object]] by default.
- Can have any number of [[Python decorator|decorators]].
- Can have [[Python type parameter list statement|type parameters]] which can aid static type checkers.
```python
@decorator1
@decorator2(arg)
class name[T](parent1, parent2):
	pass
```