

https://docs.python.org/3/library/builtins.html#module-builtins
#TODO built-in constants
#TODO built-in exceptions
#TODO built-in types


**Math**:
- `abs()`:  Absolute value (int, float or __abs__())
- `all()`:  Return true if all elements in iterable are true
- `any()`:  Return true if any elements in iterable are true
- `divmod()`:  Return quotient and remainder of int division as a pair
- `pow()`:  Raise to the power of
- `round()`:  Round number to some digits.
- `hash()`:  Get hash value of object (`__hash__()`)

**Type conversion**:
- `bool()`:   Convert to bool (`__bool__()` or `__len__() == 0`)
- `complex()`:  Convert to complex number
- `float()`:  Convert to float
- `int()`:    Convert to int
- `set()`:    Convert to set
- `str()`:    Convert to string
- `list()`:   Convert to list
- `range()`:  Convert to range
- `tuple()`:  Convert to tuple
- `frozenset()`:  Convert to frozenset
- `bytearray()`:  Create a new array of bytes (mutable)
- `bytes()`: Create a new bytes object (immutable)
- `dict()`: Create a new dictionary

**String manipulation**:
- `repr()`:  String representation or `<obj>` (`__repr__()`)
- `ascii()`:  Similar to repr() but escape non-ASCII characters
- `ord()`:   Return integer value of unicode character
- `chr()`:   Return string representation of unicode character
- `format()`:  Format a value according to a format spec. (`__format__()`)
- `hex()`:   Convert integer to hexadecimal string (0x)
- `oct()`:   Convert integer to octal (0o)
- `bin()`:   Convert integer to binary string (0b)
- `print()`:  Print to stdout
- `input()`:  Get line from stdin
- `open()`:  Open file and return a file object

**Array utils**:
- `enumerate()`:  Return (index, elem) tuples of an iterable.
- `zip()`:  Zip two iterables together.
- `filter()`:  Filter an iterable.
- `map()`:  Map a function over an iterable.
- `len()`:  Get length of object
- `max()`:  Get maximum element of sequence
- `min()`:  Get minimum element of sequence
- `sum()`:  Get sum of sequence
- `sorted()`:  Return sorted list from items
- `slice()`:  Return a slice object (`a[start:stop, i]`)

**Code manipulation**: 
- `compile()`:  Compile source code into a code or AST object.
- `eval()`:  Evaluate a string of code with environment.
- `exec()`:  Execute a string of code with environment.
- `breakpoint()`:  Calls `sys.breakpointhook()` to enter debugging mode.
- `memoryview()`:  Get memory view of argument
- `help()`:  Invoke built-in help system
- `type()`:  Return type of object.
- `callable()`:  Return True if argument is callable. (`__call__()`)
- `globals()`:  Get dictionary of the module's namespace.
- `locals()`:   Get dictionary of local symbol table.
- `dir()`:  Get names in local scope, or attributes of object (`__dir__()`)
- `vars()`:  Get the writable attributes of object/module
- `isinstance()`:  Return if object is instance of classinfo
- `issubclass()`:  Return if class is sublass of classinfo
- `getattr()`:  Get attribute of an object (obj.attr) (`__getattribute__()`)
- `setattr()`:  Set attribute of an object (obj.attr = 0)
- `delattr()`:  Del attribute of an object (del obj.attr)
- `id()`:     # Get identity of an object (unique integer)

**Iterables**:  
- `iter()`:  Return an iterator object (`__iter__()`)
- `reversed()`:  Return a reverse iterator. (`__reversed__()`)
- `next()`:  Get the next elem in iter (`__next__()`)
- `aiter()`:  Return an asynchronous iterator (`__aiter__()`)
- `anext()`:  Get next elem in async iterator (`__anext__()`)

**Syntax**: 
- `@classmethod`: # Transform a method to a class method (class can call)
- `@staticmethod`: # Transform a method to static (no first argument)
- `super()`:  Proxy that delegates method calls to parent/sibling
- `object()`:  Base class of all other classes
- `property()`:  Set property of object (getx, setx, delx)
- `@property`, `@x.setter`, `@x.deleter`: decorators for the same thing
- `__import__()`:  Import a module

