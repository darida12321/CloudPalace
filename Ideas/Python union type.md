This annotates a union of types (e.g. `int | list[int]`). Under the hood, it maps to the `typing.Union[int, list[int]]` type from the [[Python typing module|typing module]].

**Constructor**:
- `X | Y`: Makes a `typing.Union[X, Y]`
- `X | None`: Makes a `typing.Optional[X]`
**Operations**:
- `|`: Create further `typing.Union`-s.
- `==`: Order, redundancy and parentheses are ignored.


