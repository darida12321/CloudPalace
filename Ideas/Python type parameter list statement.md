[[Python function definition statement|Functions]], [[Python class definition statement|classes]] and [[Python type statement|type]] statements can have a **parameter list**. These are stored in the `__type_params__` attribute.

Type parameters come from the [[Python typing module|typing module]] in three kinds:
- `typing.TypeVar`: A plain name. Named like `T`.
- `typing.TypeVarTuple`: A tuple of any number of type. Named like `*Ts`.
- `typing.ParamSpec`: The parameters of a callable. Named like `**P`.

```python
def overly_generic[
   SimpleTypeVar,
   TypeVarWithDefault = int,
   TypeVarWithBound: int,
   TypeVarWithConstraints: (str, bytes),
   *SimpleTypeVarTuple = (int, float),
   **SimpleParamSpec = (str, bytearray),
](
   a: SimpleTypeVar,
   b: TypeVarWithDefault,
   c: TypeVarWithBound,
   d: Callable[SimpleParamSpec, TypeVarWithConstraints],
   *e: SimpleTypeVarTuple,
): ...
```