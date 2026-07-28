Represents a read-only dynamic vied of a [[Python dict|dict]].

**Constructor**:
- `types.MappingProxyType(mapping)`
**Class methods**:
- `int.from_bytes()`: Convert [[Python bytes|bytes]] to integer
**Functions**:
- `proxy.copy()`: Return shallow copy of mapping.
- `get(key, default)`: Return value for `key` if it exists, `default` otherwise.
- `items()`: Return a [[Python dictionary view|view]] of the underlying mapping's items.
- `keys()`: Return a [[Python dictionary view|view]] of the underlying mapping's keys.
- `values()`: Return a [[Python dictionary view|view]] of the underlying mapping's values.
**Operations**:
- `key in proxy`: Membership check.
- `proxy[key]`: Return the item for the `key`.
- `iter(proxy)`: Return iterator over keys.
- `reversed(proxy)`: Return reversed iterator.
- `len(proxy)`: Return number of items.
- `hash(proxy)`: Return hash of mapping.


