Executes a code block after `try` while catching [[Python exception|exceptions]].
The `except` clauses pattern match on the [[Python exception|exception]], bind it to a [[Python variable|variable]] and handle it.
The `except*` clauses pattern match on groups of [[Python exception|exceptions]].
If no [[Python exception|exception]] was raised, call the `else` block.
At the end of everything, always call the `finally` block.

```python
try:
	pass
except Exception() as e:
	pass
except:
	pass
else:
	pass
finally:
	pass
```