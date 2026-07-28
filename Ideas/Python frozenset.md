Represents an immutable [[Set|set]] of hashable (defines `__hash__()`) items. The operators expect sets on both sides, but the functions can be used with any [[Python sequence|iterable]].

**Constructor**:
- `frozenset()`, `frozenset(iterable)`
**Functions**:
- `set.issubset(iterable)`: Check if set is [[Subset|subset]] of other. (`<` and `<=`)
- `set.issuperset(iterable)`: Check if set is [[Subset|superset]] of other. (`>` and `>=`)
- `set.union(iterable)`: Get the [[Union of sets|union]] of two sets (`|`)
- `set.intersection(iterable)`: Get the [[Intersection of sets|intersection]] of two sets (`&`)
- `set.difference(iterable)`: Get the [[Difference of sets|difference]] of two sets (`-`)
- `set.symmetric_difference(iterable)`: Get the [[Symmetric difference of sets|symmetric difference]] of two sets (`^`)
- `set.isdisjoint(iterable)` Check if the sets are [[Disjoint sets|disjoint]].
- `set.copy()`: Create a copy
**Operations**:
- `len(set)`: Returns the size
- `x in set`: Whether x is contained in the set.
- `for x in set`: Iterate through the elements








