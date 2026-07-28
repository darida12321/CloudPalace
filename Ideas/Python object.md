**Objects** are the abstraction of all data.

They have three components:
- **Identity**: Unique identifier. In [[CPython]] it's the address in memory. Unchangeable
	- Use `id(obj)` to get the identity.
- **Type**: Determines the operations it supports, and its possible values. Unchangeable.
	- Use `type(obj)` to get the type.
- **Value**: This can change only if the object is [[Mutability|mutable]].
	- Cannot be destroyed, only garbage collected.

