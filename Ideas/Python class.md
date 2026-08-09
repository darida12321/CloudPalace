Created using [[Python class definition statement|class definitions]]. It has a namespace `C.__dict__`.

**Attributes**
- `__name__`: The **class**'s name.
- `__qualname__`: The qualified name (`outer.inner`).
- `__module__`: The [[Python module|module]] where it's defined.
- `__dict__`: A [[Python types module mapping proxy type class|mapping proxy]] of the namespace.
- `__bases__`: A [[Python tuple|tuple]] of base classes.
- `__base__`: [[CPython]] implementation detail. Provides the memory layout.
- `__doc__`: The documentation string.
- `__annotations__`: Variable [[Python annotation|annotations]].
- `__annotate__`: The [[Python annotation|annotate]] function, as it's lazily evaluated.
- `__type_params__`: A [[Python tuple|tuple]] of [[Python type parameter list statement|type parameters]].
- `__static_attributes__`: A [[Python tuple|tuple]] of static attributes assigned like `self.X`.
- `__firstlineno__`: The line number of the first line.
- `__mro__`: The [[Python tuple|tuple]] of base classes to look at for method resolution.
**Methods**:
- `mro()`: Can be overridden to overwrite the **method resolution order**.
- `__subclasses__()`: A [[Python list|list]] of weak references to its subclasses.