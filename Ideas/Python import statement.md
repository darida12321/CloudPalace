Finds and loads a [[Python module|module]], then binds a [[Python variable|variable]] to it.
```python
import a             # a imported and bound locally
import a.b.c         # a, a.b, and a.b.c imported, a bound locally
import a.b.c as abc  # a, a.b, and a.b.c imported, a.b.c bound as abc
from a.b import c    # a, a.b, and a.b.c imported, a.b.c bound as baz
from a import attr   # a imported and a.attr bound as attr

# In a package pkg.subpkg1
from . import mod          # pkg.subpkg1.mod
from ..subpkg2 import mod  # pkg.subpkg2.mod
```