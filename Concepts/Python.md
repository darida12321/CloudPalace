Python is one of the most popular programming languages especially for **data analysis** and **machine learning** because of its readable syntax, large number of libraries, and that it's interpreted rather than compiled.

It has multiple interpreters like [[Pypy]], but the most commonly used one is the one implemented in C, called [[CPython]].

# Example code
```python
class User:  
	@staticmethod
	def grade(score, pass_level=70):
		return "PASS" if score >= pass_level else "FAIL"
	    
	def __init__(self, name, scores):  
		self.name = name  
		self.scores = scores  
  
	def average(self):  
		return sum(self.scores) / len(self.scores)  

user = User("Sam", [72, 88, 95])  
for score in user.scores:  
	print(f"{score}: {User.grade(score, pass_level=50)}")  
print(f"Average: {user.average():.2f}")  # Round to two decimals
```

# Language definition
Python is an [[Object oriented programming language|object oriented]] language with this pre-defined hierarchy:
- [[Python object|Object]]: An empty object that everything else inherits from.
	- **Singletons**: Special types that only have a single possible value.
		- (e.g. [[Python none|None]], [[Python notImplemented|NotImplemented]], [[Python ellipsis|Ellipsis]]).
	- **[[Python numbers module|Numbers]]**: Things to do arithmetic with. 
		- (e.g. [[Python int|int]], [[Python bool|bool]], [[Python float|float]], [[Python complex|complex]]).
	- **[[Python sequence|Sequences]]**:  Sequence of items that can be iterated.
		- (e.g. [[Python range|range]], [[Python tuple|tuple]], [[Python string|string]], [[Python bytes|bytes]], [[Python list|list]], [[Python bytearray|bytearray]]).
	- **Set type**: A collection of hashable objects (e.g. [[Python set|set]], [[Python frozenset|frozenset]]).
	- **Mapping**: Map hashable values to other values (e.g. [[Python dict|dict]]).
	- **Other**: (e.g. [[Python memoryview|memoryview]], [[Python generic alias type|generic alias type]], [[Python union type|union type]]).
	- Callable:  

# Modules
- [[Python numbers module|numbers]]: Creates abstract classes for numbers.
- [[Python types module|types]]: Helps with dynamic data types.
- [[Python builtins module|builtins]]: Definition of built in values. #TODO values, exceptions, types?

#TODO sys module


--- 
[[Python function]]
[[Python module]]
[[Python class]]

---



[[Python variables]]
# Python variables


[[Python annotations]]
# Python annotations
`__annotations__`




[[Python exceptions]]
# Python exceptions

- `BaseException`: 
	- `BaseExceptionGroup`: 
	- `GeneratorExit`: 
	- `KeyboardInterrupt`: 
	- `SystemExit`: 
	- `Exception`: 
		- `ArithmeticError`: 
			- `FloatingPointError`: 
			- `OverflowError`: 
			- `ZeroDivisionError`: 
		- `AssertionError`: 
		- `AttributeError`: 
		- `BufferError`: 
		- `EOFError`: 
		- `ExceptionGroup [BaseExceptionGroup]`: 
		- `ImportError`: 
			- `ModuleNotFoundError`: 
		- `LookupError`: 
			- `IndexError`: 
			- `KeyErr: or`
		- `MemoryError`: 
		- `NameError`: 
			- `UnboundLocalError`: 
		- `OSError`: 
			- `BlockingIOError`: 
			- `ChildProcessError`: 
			- `ConnectionError`: 
				- `BrokenPipeError`: 
				- `ConnectionAbortedError`: 
				- `ConnectionRefusedError`: 
				- `ConnectionResetError`: 
			- `FileExistsError`: 
			- `FileNotFoundError`: 
			- `InterruptedError`: 
			- `IsADirectoryError`: 
			- `NotADirectoryError`: 
			- `PermissionError`: 
			- `ProcessLook: upError`
			- `TimeoutError`: 
		- `ReferenceError`: 
		- `RuntimeError`: 
			- `NotImplementedError`: 
			- `PythonFinalizationError`: 
			- `RecursionError`: 
		- `StopAsyncIteration`: 
		- `StopIteration`: 
		- `SyntaxError`: 
			- `IndentationError`: 
				- `TabError`: 
		- `SystemError`: 
		- `TypeError`: 
		- `ValueError`: 
			- `UnicodeError`: 
				- `UnicodeDecodeError`: 
				- `UnicodeEncodeError`: 
				- `UnicodeTranslateError`: 
		- `Warning`: 
			- `BytesWarning`: 
			- `DeprecationWarning`: 
			- `EncodingWarning`: 
			- `FutureWarning`: 
			- `ImportWarning`: 
			- `PendingDeprecationWarning`: 
			- `ResourceWarning`: 
			- `RuntimeWarning`: 
			- `SyntaxWarning`: 
			- `UnicodeWarning`: 
			- `UserWarning`: 





[[Python statements]]
# Python statements
There are various keyword statements in python.


##### Assignment
Assign a value to a variable
```python
my_var = 1
a, (b, c), [d, e], obj.val, f[i, j, k], *g = ...
```

starred assignment takes the rest of the argument list
augmented assignment: `+=`, `-=`, `*=`, `@=`, `/=`, `//=`, `%=`, `**=`, `>>=`, `<<=`, `&=`, `^=`, `|=`.
annotated assignment: single expression

##### Assert
Raise an [[Python exceptions|AssertionError]] if any elements are false.
```python
assert True, True, False
```

##### Global
```python
global x, y

```





##### Nonlocal
```python
nonlocal x, y

```




---
---
---
# Execution model

Python is made from **code blocks**: modules, functions, classes, commands, etc...
A **code block** is executed in an **execution frame**. Contains debugging info, and where to continue after it stopped executing.

##### Binding of names
Names refer to objects. These are bound via binding operations:
- function parameters, classes, functions, assignment expressions
- `for` loop, `with`, `except`, pattern matching, etc..
- `import` and `type` statements, type parameter list `func[T]()`
- `exec()`, `eval()`.

A **name** bound at the module level is a **global** variable.
A **name** in the program refers to the **binding** of that name.

##### Resolution of names
A **scope** defines the visibility of a name in a **code block**.
A **name** is resolved with the nearest **scope**. 

A global variable is something that's defined in the module scope.
You can't use a global variable before defining it using `global`. (`SyntaxError`)

When a `global` expression happens, resolving names goes outside-in:
- First the **global** namespace (namespace of module)
- Namespace of the [[Python builtins module|builtins module]].
- New global variable is created.

`nonlocal` variables go inside-out, finding the "nearest" variable with that name. If none exist, a `SyntaxError` is raised.

A namespace is automatically created for an imported module.
The main module is called `__main__`.

Class definition blocks, `exec()` and `eval()` are special 
- `class` is an executable statement that uses and defines names. unbound local variables are looked up in the global namesapce. namespace of the class becomes the attribute dictionary of the class. It doesn't carry over to **annotation scopes** 


( #TODO wtf??? why can't functions in classes access the class's scope? )
#TODO wtf is nonlocal??? what about global?

##### Annotation scopes
Annotations, type parameter lists and `type` statements create **annotation scopes**

differences from regular **scopes**:
- They have access to enclosing class namespace.
- They can't have `yield` `await` or `:=` expressions
- Names in annotation scope cannot be rebound with `nonlocal` in inner scope.
- Annotation scopes have an internal name, which is not reflected in the qualified name of objects. `__qualname__` of the objects is as if it was defined in the enclosing scope.

##### Lazy evaluation
Annotation scopes are usually **lazily evaluated**. Only when a `type_alias.__value__` is accessed.


##### Builtins and restricted execution
`__builtins__` is an implementation detail. don't touch.

##### Interaction with dynamic features
Free variables are resolved in the global namespace, not the nearest enclosing one.


### Exceptions
**Exceptions** let you break out of the normal flow of a code block. 
- Runtime error (division by 0)
- `raise` statement.
They can be handles with the `try`, `except`, `finally` statement.

Exceptions are also classes.

#TODO https://docs.python.org/3/library/exceptions.html list exceptions...


### Runtime components
##### General computing model
**host machine**
**process** (one for each program running on the host)
**thread** (starts with one thread, but can become multi-threaded)

##### Python runtime model
**host machine**
**process**
python global runtime (state)
python interpreter (state)
**thread**
python thread state

One runtime can have multiple interpreter
One interpreter can have multiple thread states



#TODO list all statements https://docs.python.org/3/reference/index.html
#TODO python runtime model??? wtf is this shit??? huh??? 








# Modules!!!!!!

Imported by `import`, or the [[Python importlib module|importlib module]].
`m.x = 1` gets translated to `m.__dict__["x"] = 1`.

##### Import-related attributes of module objects
Populated based on the module's spec, dynamically by the import system.
Alternatively, `importlib.util.module_from_spec()` can do it.
In general, use the `module.__spec__` for viewing stuff. (idk why?)

- `module.__name__`: Unique name. For directly executed modules, it's `"__main__"`.
- `module.__spec__`: The module's import-related state.
- `module.__package__`: The package (module with `__path__`) a module belongs to. DEPR
	- use `module.__spec__.parent` instead.
- `module.__loader__`: The loader that loads the module. DEPR.
	- use `module.__spec__.loader` instead.
- `module.__path__`: Sequence of string enumerating a package's submodules.
	- use `module.__spec__.submodule_search_locations` instead.
- `module.__file__`: Path for the file where the module was loaded. DEPR.
- `module.__cached__`: Path for the compiled version of the code. DEPR.
	- use `module.__spec__.cached` instead.

##### Other writable attributes on module objects

- `module.__doc__`: Documentation string
- `module.__annotations__`: [[Python dict|Dictionary]] of variable annotations
- `module.__annotate__`: The annotation function

##### Module dictionaries
Cannot be accessed as a global variable from the module.
- `module.__dict__`: The namespace of the module.








# Module inner workings
Import modules by `import`, `__import__()` or `importlib.import_module()`.
Import searches for the named module, then binds it to a name in the local scope.

`import` searches the for the named module using `__import__()`, then binds the results.
`__import__()` performs a module search and a module creation.
`importlib` is a module that gives ways of interacting with this import system.

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

# Packages
There is one, and only one module object. To organize them and give a naming hierarchy, there is a concept of packages.
Similar to directories on a file system (but not really that under the hood). packages are organized hierarchically, and can have sub-packages, a module with `__path__` is a package.
Subpackage names are separated from parent's names by a dot.

##### Regular packages
This is the older one (before Python 3.2)
A directory containing an `__init__.py` file.
When it's imported, `__init__.py` is executed, the objects defined get bound to the package's namespace 
A subdirectory without an `__init__.py` is treated as an implicit namespace package.

##### Namespace packages
Consists of **portions** where each portion is a subpackages to the parent package.
**Portions** can reside in different locations, zip files, on the network, wherever python searches during importing.
The `__path__` is not a list, but a custom iterable type will perform a new search for package portions the next time the parent's path changes.
It can appear as part of regular packages. it's treated as a **portion** contributing to a namespace subpackage of the regular package.

# Searching
It needs the qualified name (`a.b.c`).

##### The module cache
The first place to check is `sys.modules`. It's a cache for already loaded modules.
This can be written to and manipulated.

##### Finders and loaders
A finder determines if it can find the named module. 
An object that's a finder and a loader is an **importer**.

1. Locates built-in modules
2. Locates frozen modules (a python module that was compiled and built into a custom interpreter by python's freeze utility)
3. Searches an import path for modules (`sys.path`)

Finders return a module spec.

##### Import hooks
The import mechanism is extensible. This is done via import hooks.
- **meta hooks**: After `sys.modules` cache lookup, before `sys.path` processing.
	- Registered by adding a new finder to `sys.meta_path`.
- **import path hooks**:

##### The meta path
After checking `sys.modules`, python looks at `sys.meta_path`. which has meta path finder objects. The objects there have a `find_spec(fullname, path, target=None)` function. It determines if it can handle the named module or not.
If it knows how to handle it, it returns a spec object. otherwise, a `None`.
If none of them could manage, a `ModuleNotFoundError` is raised.

`find_spec()`: 
- The fully qualified name (`a.b.c`), 
- The path entries (for top-level modules, `None`. for submodules, the parent's `__path__`).
- Existing module that will be the target of the loading. optional. good for reloads.

Importing `foo.bar.baz`:
1. `mpf.find_spec("foo", None, None)`
2. `mpf.find_spec("foo.bar", foo.__path__, None)`
3. `mpf.find_spec("foo.bar.baz", foo.bar.__path__, None)`

By default there are 3 meta path finders:
1. Built-in modules
2. Frozen modules
3. Import from import path (path based finder).


# Loading
Loading a module has a whole complex module tree...


##### Loaders
If the finder and the loader is the same, the finder should return a spec with the loader as `self`.
Loaders get a module and execute them via `exec_module(module)
If the module is a Python module, execute the code in the module's global name space (`module.__dict__`).
Loaders can choose to create the module object by defining a `create_module(spec)` function.

##### Submodules
When a submodule is imported, a binding is created in the parent module's namespace.
This is stored in the `__dirs__` (I think? ????? confirm with test.)

##### Module specs
This is the way the finder and loader communicate. 
It's exposed as `module.__spec__`.

ModuleSpec definition:
Python importlib module modulespec
- `name`: The fully qualified name. Finder must set this.
- `loader`: The loader used to load the module. Finder must set this.
- `origin`: Location to use for the loader. for a `.py` file, use filename. Finder should use something meaningful. (`module.__file__`)
- `submodule_search_locations`: Sequence of strings enumerating the locations of the submodules. (`module.__path__`). Finder must set it to a sequence.
- `loader_state`: Any object with additional data.
- `cached`: Filename of a compiled version of the module's code. (`module.__cached__`) Finder must always set it except if a module needs no compiled code.
- `parent`: Fully qualified name of the package this module is in. (`module.__package__`). If this is a package, then same as `name`.
- `has_location`: If the `origin` refers to a loadable location.

##### `__path__` attributes on modules
The `__path__` should be a sequence of strings with the locations for the package's submodules.
It's used during imports of its subpackages.
`sys.path_hooks` are consulted(???) when traversing a package's `__path__`.

##### Module reprs
Modules have a usable `repr`. 
It uses the `__spec__` or `__file__` or `__loader__` or `__name__`.

##### Cached bytecode invalidation
Before loading bytecode from `.pyc` file, check if it's up to date with the source `.py` file.




# The path based finder
The path based finder searches `sys.path` list.
The **path based finder** doesn't know how to import. It associates each path from `sys.path` with a **path entry finder**. By default, it handles `.py`, `.pyc` and `.so` files possibly in zips.
Path entries can refer to URLs, database queries, or any other string.

meta path finders and path entry finders are different!!!!

##### Path entry finders
There are some additional hooks that can customize how modules are found and loaded from the import path (`sys.path`, and for subpackages, the parent's `__path__`).
Three variables are used: `sys.path`, `sys.path_hooks` and `sys.path_importer_cache`. A parent package's `__path__` is also used.

- `sys.path`: List of strings with search locations for modules and packages.
	- Comes from `PYTHONPATH` environment variable.

The path based finder iterates over every path in the search path, and for each, looks for a **path entry finder**. This can be expensive, so the path based finder has a cache mapping path entries to path entry finders. `sys.path_importer_cache` (despite the name, it stores finder objects, not just importer objects).

If the path entry is not in `sys.path_importer_cache`, the path based finder iterates over `sys.path_hooks`. These are callable, are given the path as input, and they return a path entry finder if they know one.
Once that ends, the path based finder's `sys.path_importer_cache` will get a `None`.

If a path entry finder was found the protocol (below) is used.

##### Path entry finder protocol
path entry finders must implement the `find_spec(fullname, target=None)` method. It returns a fully populated spec.













---
wtf is in `__path__`????? make toy modules and find out!
PEP system for changes. 













##### Operators
number operations: `x+y, x-y, x*y, x/y, x//y, x%y, -x, +x, x**y`
bitwise operations on integers: `x | y, x ^ y, x & y, x << n, x >> n, ~x` (or, xor, and, lshift, rshift, not)
Boolean operators: `not x`, `x and y`, `x or y`.
Comparisons: `<`, `<=`, `>`, `>=`, `==`, `!=`, `is`, `is not`, `in`, `not in`.
Function call operator `func(val1, name=val2)`

For `<`, `<=`, `>`, `>=`, `==`: Instances are generally not equal and incomparable, unless `__lt__()`, `__le__()`, `__gt__()`, `__ge__()` and `__eq__()` are defined. These can be inferred from `__lt__()` and `__eq__()` alone.
For `is`, `is not`: Compares if two objects are the same. (have the same `id()`)
For `in`, `not in`: They apply to **iterable** objects, or ones that implement `__contains__()`





---

```python ln:false


# Syntax
variable_name = 'string value'
global glob_variable = 'don\'t use this'

if (False):
	pass
elif (True):
	pass
else: 
	pass

while True:
	pass
	
for i in range(5):
	pass
for i in my_array:
	pass
for key, value in my_dict.items()
	pass
[x for x in range(5) if True]

def func(arg1, arg2=2, *args, **kwargs):
	# args: regular arguments, keyword arguments
	return 5, 2 # tuple
r1, r2 = func(7)

func2 = lambda x, y: x + y

try:
	raise Exception('Sussy')
except Exception as e:
	print(e)
finally:
	pass



class Animal:
	total_count = 2;
	def __init__(self, age):
		self.age = age
		total_count += 1
	
	@classmethod
	def something(cls):
		return cls.total_count
	
	@staticmethod
	def something_else():
		print('idk')

class Dog(Animal):
	def __init__(self, age, name):
		super().__init__(age)
		self.name = name
	def speak(self):
		print('Woof')
	def __str__(self):
		print(f'Dog: {name}')

dog = Dog('Zulu')
Animal.total_count;
Animal.something();

with open('file.txt') as f:
	f.read()

```


#TODO import, export, decorators

list of functions: https://docs.python.org/3/library/functions.html
list of everything: https://docs.python.org/3/library/index.html


---
source: [Python 3 documentation](https://docs.python.org/3/library/index.html)
source: [Inside The Python Virtual Machine](https://leanpub.com/read/insidethepythonvirtualmachine)
source: [Python for Data Analysis Third Edition](https://www.lkhibra.ma/books/Python-for-Data-Analysis.pdf)


