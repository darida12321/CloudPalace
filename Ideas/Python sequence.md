**Iterable containers** must implement an `__iter__()` function, which returns an **iterator**.
**Iterators** also have an `__iter__()` function returning itself, and a `__next__()` function for getting the next element. This is used in `for` loops 

- [[Python immutable sequence|Immutable sequences]]: Hashable.
	- [[Python range|Range]]: Numbers between a start and stop.
	- [[Python tuple|Tuple]]: Assortment of objects.
	- [[Python string|String]]: Sequence of values that represent [[Unicode|unicode]] code points. 
	- [[Python bytes|Bytes]]: Sequence of 8-bit bytes represented by integers.
- [[Python mutable sequences|Mutable sequences]]: Define a few extra functions for modifying itself.
	- [[Python list|List]]: Assortment of objects.
	- [[Python bytearray|Byte Array]]: Same as [[Python bytes|bytes]], but mutable.


**Operations**:
- `x in s`, `x not in s`: Membership checks
	- For [[Python string|string]], [[Python bytes|bytes]] and [[Python bytearray|byte array]], it tests subsequences too. `'gg' in 'eggs'`
- `s + t`: Concatenate two sequences
- `s * n`: Concatenate `s` n times
- `s[i]`: Get `i`th item
- `s[i:j]` Slice from `i` to `j`
- `s[i:j:k]`: Slice from `i` to `j` with step `k`. 
	- `i` and `j` are truncated from `-len(s)` to `len(s)`
	
**Methods**:
- `s.count()`: Return number of occurrences of a value.
- `s.index()`: Return index of first occurrence of a value.













