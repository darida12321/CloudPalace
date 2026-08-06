**Decorators** are usually used before [[Python callable|functions]] and class methods.
They are a [[Python callable|callable]] which is invoked with the function as the only argument.

A code like this:
```python
@f1(arg)
@f2
def func(): pass
```

Translates to this:
```python
def func(): pass
func = f1(arg)(f2(func))
```
