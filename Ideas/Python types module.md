Helps in the dynamic creation of **types**, and defines some that the standard interpreter uses. Documentation available [here](https://docs.python.org/3/library/types.html).

##### Dynamic type creation
Functions like `types.new_class()` can create classes dynamically.

##### Standard interpreter types
Names many of the types in python. Useful for `isinstance()` and `issubclass()` checks.

Simple types:
- `types.NoneType`: Type for [[Python none|None]].
- `types.NotImplementedType`: Type for [[Python notImplemented|NotImplemented]]
- `types.EllipsisType`: Type for [[Python ellipsis|Ellipsis]]

More complex type classes:
- [[Python types module mapping proxy type class|types.MappingProxyType]]: Dynamic view of a [[Python dict|dict]], used by [[Python dictionary view|dictionary views]]


##### Additional utility classes
It has some utility classes for namespaces, dynamic class attributes and coroutines.