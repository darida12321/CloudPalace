Represents a dynamic **view** of a [[Python dict|dict]]. The `keys` and `items` are set-like, so [[Python set|set]] operations can be used.

**Constructor**:
- `d.keys()`, `d.values()`, `d.items()`.
**Fields**:
- `dictview.mapping`: Return a [[Python types module mapping proxy type class|types.MappingProxyType]] that wraps the dictionary.
**Functions**:
- `reversed(dictview)`: return reversed iterator.
**Operations**:
- `len(dictview)`: get number of entries
- `iter(dictview)`: return iterator over it.
- `x in dictview`: check if `x` is in the keys/values/items
