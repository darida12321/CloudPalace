A generic type alias for classes (e.g. `list[int]`) that define a `__class_getitem__()` function. It can specify the content type of a container, or the return type of a function.

**Constructor**:
- `T[X, Y, ...]`.
**Fields**:
- `__origin__`: the non-parameterized generic class
- `__args__`: Tuple of types passed into it.
- `__parameters__`: Type variables found in arguments ([[Python typing module|typing module]])
- `__unpacked__`: [[Python bool|Bool]] for whether it's unpacked using the `*` operator ([[Python typing module|typing module]])






