Can be used for nested [[Python callable|functions]]/[[Python class|classes]]. Causes the [[Python variable|variables]] to refer to pre-existing variables found in the nearest scope.
```python
def outer():
  x, y, z = (1, 2, 3)
  def inner():
    nonlocal x, y, z
    print(x, y, z)
  inner() # 1, 2, 3
  x = 5
  inner() # 5, 2, 3
```