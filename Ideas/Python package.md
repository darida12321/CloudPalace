Python **packages** are [[Python module|modules]] with a hierarchical structure. They have a `__path__` variable containing sub-packages or sub-modules.
Subpackage `__name__`-s are separated from its parent's name by a dot.

##### Regular packages
This is the older package style. It's a folder that has a `__init__.py` file. When importing the package, the init file is executed, and the [[Python variable|variables]] get bound to the package's namespace.

A subdirectory without a `__init__.py` is treated as an implicit **namespace package**.

##### Namespace packages
Consists of **portions** where each portion is a subpackages to the parent package.
**Portions** can be in zip files, on the network, or wherever python searches during importing.

The `__path__` is not a list, but a custom iterable that will perform a new search for package portions the next time the parent's `__path__` changes.