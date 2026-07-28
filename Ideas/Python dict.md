Represents a mutable mapping from hashable (has `__hash__()` objects to arbitrary objects. Insertion order is preserved. Some of its functions return [[Python dictionary view|dictionary view]] objects.

**Constructor**:
- `{}`, `{1: 'a', 'b': True}`
- `{x: x+1 for x in range(10)}`
- `dict([(1, 'abc'), ('def', True)])`
**Class methods**:
- `dict.fromkeys(iterable, value=None)`: Create a new dictionary with `iterable` as keys, and `value` as value everywhere.
**Functions**:
- `d.copy()`: Make shallow copy
- `d.get(key, default=None)`: Get value for `key` or `default`.
- `d.update(mapping/iterable)`: Update with key/value pairs.
- `d.setdefault(key, default=None)`: If `key` exists, return its value. If not, set `key`'s value to `default` and return it.

- `d.popitem()`: Remove and return first item `(key, value)` pair.
- `d.pop(key, default)`: Remove and return `key`'s value, or `default` if provided
- `d.clear()`: Remove all items

- `d.keys()`: Get [[Python dictionary view|view]] of keys
- `d.values()`: Get [[Python dictionary view|view]] of values.
- `d.items()`: Get [[Python dictionary view|view]] of `(key, value)` item pairs.

**Operations**:
- `list(d)`: Return list of keys
- `len(d)`: Return number of items
- `reversed(d)`: Get a reversed iterator of keys.
- `d[key]`: Get element mapped to key, or call `__missing__()`, or throw error.
- `d[key] = value`: Set a key to a value
- `del d[key]`: Remove key and its value
- `key in d`: Check if key is in the keys
- `key not in d`: Check if key not in d
- `iter(d)`: Get iterator over keys
- `d | other`: Create dict with merged keys and values of `d` and `other`
- `d |= other`: Update d with keys and values of `other`.


