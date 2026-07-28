Functions are objects that the **function call operator** (`()`) can be applied to. The most common case of this is a **user defined function**:
```python
def func(arg1, arg2, arg3=1, *args, **kwargs):
	return args[0] + kwargs['num']

func(1, 2, 3, 4, num=5) # Returns 4+5
```

**Read-only attributes**:
- `func.__builtins__`: [[Python dict|Dictionary]] holding the builtins name space.
- `func.__globals__`: [[Python dict|Dictionary]] holding the global variables.
- `func.__closure__`: [[Python tuple|Tuple]] of bindings for closure.
**Writable attributes**:
- `func.__doc__`: The documentation string, or [[Python none|None]].
- `func.__name__`: The functions name.
- `func.__qualname__`: The function's qualified name (full path for nested classes).
- `func.__module__`: The name of the module the function was defined in.
- `func.__defaults__`: [[Python tuple|Tuple]] containing the default parameters.
- `func.__code__`: A code object representing the compiled body.
- `func.__dict__`: Namespace for arbitrary attributes.
- `func.__annotations__`:  [[Python dict|Dictionary]] of annotation parameters.
- `func.__annotate__`: Function generating the annotations cause it's lazily evaluated.
- `func.__kwdefaults__`: [[Python dict|Dictionary]] of defaults for keyword-only parameters.
- `func.__type_params__`: [[Python tuple|Tuple]] of type parameters.
















---


##### User defined functions (function object)




##### Instance methods
combines a class, a class instance and a callable object (usually function).
created by a function of a class, or a classmethod (`@classmethod`).

Read-only attributes:
- `method.__self__`: The class instance to which this method is bound.
- `method.__func__`: The original function object.
- `method.__doc__`: The method's documentation (same as `method.__func__.__doc__`).
- `method.__name__`: The name of the method (same as `method.__func__.__name__`).
- `method.__module__`: The name of the module the method was defined in.

They can access (but not set) the underlying function attributes.

When a function is called, `__func__` is called with `__self__` appended to the front of the list.




##### Generator functions
functions that use the `yield` statement. They return iterator objects whose `__next__()` method executes the function until a `yield` statement. `return` causes a `StopIteration` exception.

##### Coroutine functions
Created with `async def`. Returns a `coroutine` object.
May contain `await` and `async with` and `async for` statement.


##### Asynchronous generator functions
Created with `async def` and uses `yield`. Returns an `asynchronous iterator` which can be used in `async for` statements.


##### Built-in functions
Just a wrapper around a C function. Special read-only attributes:
- `func.__doc__`: The documentation string, or [[Python none|None]].
- `func.__name__`: The functions name.
- `func.__self__`: Set to [[Python none|None]], or to the object calling this.
- `func.__module__`: The name of the module the function was defined in.

##### Built-in methods
Same as built-in functions

##### Classes
Classes can be called. this triggers the `__new__()` function, which if returns an instance of the class, gets `__init__()` called on it.

##### Class instances
Instances can be called by defining a `__call__()`.