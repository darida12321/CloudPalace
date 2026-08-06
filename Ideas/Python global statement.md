Causes the listed [[Python variable|variables]] to be **global** (defined in the [[Python module|module's]] namespace).
You cannot use a **global** variable before declaring it as global.
```python
def func():
	global x, y, z
	x, y, z = (1, 2, 3)

print(x, y, z) # NameError
func()
print(x, y, z) # 1, 2, 3
```