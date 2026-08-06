Using `yield` in a function turns it into a [[Python callable|generator function]].
It can be used to `yield` all values `from` an iterable.
```python
def f(arg): 
	yield 1+2, ('a', True)
	yield from ['iterable', 2]
```
