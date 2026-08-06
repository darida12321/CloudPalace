When no [[Python exception|exception]] is present, `raise` the one currently being handled, or a `RuntimeError`.
When an [[Python exception|exception]] is specified, `raise` that one with its `__traceback__` set to this line.
When raising an [[Python exception|exception]] `from` an old exception, set the `__cause__` of the old one.
When raising an [[Python exception|exception]] `from None`, supress the exception chaining. 
```python
raise
raise Exception()
raise Exception() from prev_exception
raise Exception() from None
```
