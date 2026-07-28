Represents a mutable [[Set|set]] of hashable (defines `__hash__()`) items. The operators expect sets on both sides, but the functions can be used with any [[Python sequence|iterable]].

These have a few extra functions when compared to [[Python frozenset|frozenset]], since these are mutable.

**Constructor**:
- `{a}`, `{a, b, c}`
- `{x for x in iterable if condition}`
- `set()`, `set(iterable)`
**Functions**:
- `set.issubset(iterable)`: Check if set is [[Subset|subset]] of other. (`<` and `<=`)
- `set.issuperset(iterable)`: Check if set is [[Subset|superset]] of other. (`>` and `>=`)

- `set.union(iterable)`: Get the [[Union of sets|union]] of two sets (`|`)
- `set.intersection(iterable)`: Get the [[Intersection of sets|intersection]] of two sets (`&`)
- `set.difference(iterable)`: Get the [[Difference of sets|difference]] of two sets (`-`)
- `set.symmetric_difference(iterable)`: Get the [[Symmetric difference of sets|symmetric difference]] of two sets (`^`)

- `set.update(iterable)`:  Add other elements to the set (`|=`)
- `set.intersection_update(iterable)`: Keep only elements that appear in the list (`&=`)
- `set.difference_update(iterable)`: Remove elements from set (`-=`)
- `set.symmetric_difference_update(iterable)`: Keep elements found in only one (`^=`) 

- `set.add(elem)`: Add elem to set.
- `set.remove(elem)`: Remove elem from set. error if not present
- `set.discard(elem)`: Remove elem if present
- `set.pop()`: Remove an arbitrary element and return it.
- `sset.clear()`: Remove all elements.

- `set.isdisjoint(iterable)` Check if the sets are [[Disjoint sets|disjoint]].
- `set.copy()`: Create a copy
**Operations**:
- `len(set)`: Returns the size
- `x in set`: Whether x is contained in the set.
- `for x in set`: Iterate through the elements




