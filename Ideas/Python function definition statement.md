Creates a [[Python callable|callable]] function and binds it to a name.
- Can have any number of [[Python decorator|decorators]].
- Can have [[Python type parameter list statement|type parameters]] which can aid static type checkers.
- Has **parameters**, **default parameters**, a **argument list** and a **keyword argument list**.
- The **parameters** can have [[Python annotation|type annotations]].
```python
@decorator1
@decorator2(arg)
def func[T](arg1: T, arg2: T = 1, *args, **kwargs) -> None:
	pass
```