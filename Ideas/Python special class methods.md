[[Python operations|Operations]] in python such as `x[i]` roughly translate to `type(x).__getitem__(x, i)`. There are a large number of special method names that define how an [[Python operations|operation]] works on a custom [[Python class|class]].

**Basic class customization**:
- `__new__`: Used to create a [[Python class instance|class instance]].
- `__init__`: Used on the [[Python class instance|class instance]] during `__new__` to initialize it.
- `__del__`: Called when the [[Python class instance|class instance]] is deleted.
- `__init_subclass__`: Called when another [[Python class|class]] subclasses this one.
- `__set_name__`: When a [[Python class|class]] gets assigned to a name (`x = C()`)
- `__mro_entries__`: Non-type bases can define base types (**method resolution order**) 
- `__class_getitem__`: Return a specialization of a generic by some [[Python type parameter list statement|type parameters]].

- `__annotations__`: Variable and function [[Python annotation|annotations]].
- `__annotate__`: An [[Python annotation|annotation]] function, because it has lazy evaluation.

**Attributes**:
- `__getattribute__`: Implements attribute access.
- `__getattr__`: Called when the default attribute access fails.
- `__setattr__`: Called when attribute assignment is attempted.
- `__delattr__`: Called when attribute deletion is attempted.
- `__get__`: Get the attribute of a [[Python class instance|class instance]].
- `__set__`: Set the attribute of a [[Python class instance|class instance]].
- `__delete__`: Delete an attribute of a [[Python class instance|class instance]].
- `__objclass__`: Specifies the [[Python class|class]] where an [[Python object|object]] was defined. 
- `__slots__`: Explicitly declare properties, and deny `__dict__` and `__weakref__`.

**Representations**:
- `__repr__`: Compute the official [[Python string|string]] representation of an object.
- `__str__`: Called by `str(object)`, the informal [[Python string|string]] representation of an object.
- `__bytes__`: The [[Python bytes|bytes]] representation of an object.
- `__bool__`: The truth value of the object.

**Built-in functions**:
- `__format__`: Called by the `format()` [[Python built-in functions|built-in function]].
- `__hash__`: Called by the `hash()` [[Python built-in functions|built-in function]].
- `__dir__`: Called by the `dir()` [[Python built-in functions|built-in function]].
- `__instancecheck__`: Called by the `isinstance()` [[Python built-in functions|built-in function]].
- `__subclasscheck__`: Called by the `issubclass()` [[Python built-in functions|built-in function]].
- `__len__`: Called by the `len()` [[Python built-in functions|built-in function]].
- `__length_hint__`: Return an estimated length for the object. Good for optimizations.
- `__reversed__`: Called by the `reversed()` [[Python built-in functions|built-in function]].

- `__complex__`: Called by the `complex()` [[Python built-in functions|built-in function]].
- `__int__`: Called by the `int()` [[Python built-in functions|built-in function]].
- `__float__`: Called by the `float()` [[Python built-in functions|built-in function]].
- `__abs__`: Called by the `abs()` [[Python built-in functions|built-in function]].
- `__index__`: Called by the `bin()`, `hex()` and `oct()` [[Python built-in functions|built-in functions]].
- `__round__`: Called by the `round()` [[Python built-in functions|built-in function]].
- `__trunc__`: Called by the `math.trunc()` from the [[Python math module|math module]].
- `__floor__`: Called by the `math.floor()` from the [[Python math module|math module]].
- `__ceil__`: Called by the `math.ceil()` from the [[Python math module|math module]].

**Operators**:
- `__lt__`, `__le__`, `__eq__`, `__ne__`, `__gt__`, `__ge__`: Rich comparison methods.
- `__call__`: Used when the instance is [[Python callable|called]].
- `__add__`, `__radd__`, `__iadd__`: Addition `x+o`, `o+x`, `x += o`.
- `__sub__`, `__rsub__`, `__isub__`: Subtraction `x-o`, `o-x`, `x -= o`.
- `__mul__`, `__rmul__`, `__imul__`: Multiplication `x*o`, `o*x`, `x *= o`.
- `__matmul__`, `__rmatmul__`, `__imatmul__`: Matrix multiplication `x@o`, `o@x`, `x @= o`.
- `__truediv__`, `__rtruediv__`, `__itruediv__`: Division `x/o`, `o/x`, `x /= o`.
- `__floordiv__`, `__rfloordiv__`, `__ifloordiv__`: Int division `x//o`, `o//x`, `x //= o`.
- `__mod__`, `__rmod__`, `__imod__`: Modulo `x%o`, `o%x`, `x %= o`.
- `__divmod__`, `__rdivmod__`: Division with remainder `divmod(x, o)`, `divmod(o, x)`.
- `__pow__`, `__rpow__`, `__ipow__`: Power `x**o`, `o**x`, `x **= o`.
- `__lshift__`, `__rlshift__`, `__ilshift__`: Left shift `x<<o`, `o<<x`, `x <<= o`.
- `__rshift__`, `__rrshift__`, `__irshift__`: Right shift `x>>o`, `o>>x`, `x >>= o`.
- `__and__`, `__rand__`, `__iand__`: And `x&o`, `o&x`, `x &= o`.
- `__xor__`, `__rxor__`, `__ixor__`: Xor `x^o`, `o^x`, `x ^= o`.
- `__or__`, `__ror__`, `__ior__`: Or `x|o`, `o|x`, `x |= o`.
- `__neg__`: Negation `-x`.
- `__pos__`: Positive `+x`.
- `__invert__`: Inversion `~x`.

**Containers**:
- `__getitem__`: Get elements of [[Python sequence|sequences]] or [[Python dict|dicts]] (`a[1]`).
- `__setitem__`: Set elements of [[Python sequence|sequences]] or [[Python dict|dicts]] (`a[1] = 2`).
- `__delitem__`: Delete elements of [[Python sequence|sequences]] or [[Python dict|dicts]] (`del a[1]`).
- `__missing__`: Called by [[Python dict|dicts]] when a key is missing.
- `__iter__`: Creates an iterator for a container.
- `__contains__`: Checks if an element is in a container.
 **Other**:
- `__enter__`: Used by the `with` [[Python with statement|statement]] context managers.
- `__exit__`: Used by the `with` [[Python with statement|statement]] context managers.
- `__match_args__`: Specify the argument names for `match` [[Python match statement|statements]].
- `__buffer__`: Called when a buffer is requested. (e.g. [[Python memoryview|memoryview]])
- `__release_buffer__`: Called when a buffer is released. (e.g. [[Python memoryview|memoryview]])
