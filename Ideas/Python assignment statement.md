Assign a value to a variable
```python
my_var = 1
a, (b, c), [d, e], obj.val, f[i, j, k], *g = ...
```

Variables can be [[Python annotation|type annotated]].
The assignment rules are:
- `a`: Assign a variable
- `(b, c)`: Assign elements of a [[Python tuple|tuple]].
- `[d, e]`: Assign elements of a [[Python list|list]].
- `obj.val`: Assign to an object's value.,
- `f[i, j, k]`: Assign to a [[Python mutable sequences|slice]].
- `*g`: Assign all other elements as a list.

**Augmented assignment** performs an operation on the base variable.
(`+=`, `-=`, `*=`, `@=`, `/=`, `//=`, `%=`, `**=`, `>>=`, `<<=`, `&=`, `^=`, `|=`)



