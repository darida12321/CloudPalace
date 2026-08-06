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

# Objects
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
	- **Other**: (e.g. [[Python memoryview|memoryview]], [[Python generic alias type|generic alias type]], [[Python union type|union type]], [[Python exception|exceptions]]).
	- Callable:  [[Python callable|callables]]. #TODO classes, modules. #TODO code stuff

# Language features
- **Variables**: [[Python assignment statement|assignment]], [[Python del statement|del]], [[Python global statement|global]], [[Python nonlocal statement|nonlocal]], [[Python import statement|import]].
- **Logic**: [[Python assert statement|assert]], [[Python if statement|if]], [[Python match statement|match]], [[Python for statement|for]], [[Python while statement|while]].
- **Flow control**: [[Python pass statement|pass]], [[Python break statement|break]], [[Python continue statement|continue]], [[Python return statement|return]], [[Python yield statement|yield]].
- **Exceptions**: [[Python raise statement|raise]], [[Python try statement|try]], [[Python with statement|with]].
- **Definitions**: [[Python function definition statement|function definition]], [[Python coroutine definition statement|coroutine definition]], [[Python class definition statement|class definition]].
- **Types**: [[Python type statement|type]], [[Python type parameter list statement|type parameter list]].

# Modules
Python has plenty of built-in, and external modules.
- [[Python numbers module|numbers]]: Creates abstract classes for numbers.
- [[Python types module|types]]: Helps with dynamic data types.
- [[Python builtins module|builtins]]: Definition of built-in values.




--- 
done:
[[Python exception]]
[[Python variable]]
[[Python callable]]
[[Python module]]
[[Python package]]


[[Python built-in constants]]
[[Python built-in exceptions]]
[[Python built-in functions]]
[[Python built-in types]]

wip:
[[Python sys module]].
[[Python site module]].

[[Python class]]

---

[[Python import system]]
# Python import system
The `import` [[Python import statement|statement]] and the [[Python importlib module|importlib]] module handle the logic behind **searching** and **loading** [[Python package|packages]]. `import` also binds the loaded module to a [[Python variable|variable]].

##### Searching
Searching is done using the **qualified name** (`a.b.c`) of a package. A lot of this process is aided by the [[Python sys module|sys module]].

When searching for a module, there are a few places python looks:
1. The **module cache** stores already loaded modules (`sys.modules`).
2. The **meta hooks** go through a list of **finders** (`sys.meta_path`). 
	1. `BuiltinImporter`: Locates built-in [[Python module|modules]].
	2. `FrozenImporter`: Locates [[Python module|modules]] that were built into a custom interpreter.
	3. `PathFinder`: Looks through paths, links, arbitrary strings.
		1. For every **path** (`sys.path` from `PYTHONPATH` and `__path__` for [[Python package|subpackages]]).
		2. Check if it's cached in `sys.path_importer_cache`
		3. Looks for a **path entry finder** by executing `sys.path_hooks`:
			1. By default, handles `.py`, `.pyc` and `.so` files, possibly in zips.
			2. Can be expended with [[Python callable|callables]] that return a **path entry finder**.
		4. The **path entry finder**'s `find_spec()` function is called.
	4. Can be extended with **meta path finders** implementing `find_spec()`.

A **finder** return a [[Python module spec]].

##### Loading
#TODO continue with loading I guess...


[[Python module spec]]
# Module spec




---
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











---
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
source: [Python 3 documentation](https://docs.python.org/3/library/index.html)
source: [Inside The Python Virtual Machine](https://leanpub.com/read/insidethepythonvirtualmachine)



