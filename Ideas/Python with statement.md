```python
with A() as a, B() as b:
	pass
```

Specifying multiple items is equivalent to nesting multiple `with` statements.

The items are **context managers** defining two [[Python callable|functions]]:
- `__enter__(self)`: Enter the runtime context.
- `__exit__(self, exc_type, exc_value, traceback)` Exit the runtime context.

For a single item (`A() as a`), the execution is as follows:
1. The **context manager** (`A()`) is created.
2. The target `a` is set to the **context manager**'s `__enter__()` function.
3. The code block is executed.
4. The **context manager**'s `__exit__()` function is called, with an [[Python exception|exception]] if it occurred.
