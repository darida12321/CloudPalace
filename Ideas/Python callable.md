Functions are objects that the **function call operator** (`()`) can be applied to. The most common case of this is a [[Python function definition statement|user-defined function]]:
```python
def func(arg1, arg2, arg3=1, *args, **kwargs):
	return args[0] + kwargs['num']

func(1, 2, 3, 4, num=5) # Returns 4+5
```

**Read-only attributes**:
- `func.__builtins__`: [[Python dict|Dictionary]] holding the [[Python builtins module|builtin]] name space.
- `func.__globals__`: [[Python dict|Dictionary]] holding the global variables.
- `func.__closure__`: [[Python tuple|Tuple]] of bindings for closure.
**Writable attributes**:
- `func.__doc__`: The documentation string, or [[Python none|None]].
- `func.__name__`: The functions name.
- `func.__qualname__`: The function's qualified name (full path for nested classes).
- `func.__module__`: The name of the [[Python module|module]] the function was defined in.
- `func.__defaults__`: [[Python tuple|Tuple]] containing the default parameters.
- `func.__code__`: A code object representing the compiled body.
- `func.__dict__`: Namespace for arbitrary attributes.
- `func.__annotations__`:  [[Python dict|Dictionary]] of [[Python annotation|annotation]] parameters.
- `func.__annotate__`: Function generating the [[Python annotation|annotation]] because it's lazily evaluated.
- `func.__kwdefaults__`: [[Python dict|Dictionary]] of defaults for keyword-only parameters.
- `func.__type_params__`: [[Python tuple|Tuple]] of [[Python type parameter list statement|type parameters]].


# Other callables
Beyond this basic one, there are a few other kinds of callables:

##### Methods
Combines a [[Python function definition statement|function]], a [[Python class definition statement|class]] and an instance. It's a function of a class, or a `@classmethod`.
**Read-only attributes**:
- `method.__self__`: The class instance to which this method is bound.
- `method.__func__`: The original [[Python function definition statement|function]] object.
- `method.__doc__`: The method's documentation (same as `method.__func__.__doc__`).
- `method.__name__`: The name of the method (same as `method.__func__.__name__`).
- `method.__module__`: The name of the module the method was defined in.

When it is called, `__func__` is called with `__self__` appended to the front of the list.

##### Generator functions
A [[Python function definition statement|function]] using `yield` [[Python yield statement|statement]]. They return an iterator. 

##### Coroutine functions
Created with the `async def` [[Python coroutine definition statement|statement]]. May contain `await`, `async with` and `async for`.

##### Asynchronous generator functions
A **coroutine** that's a **generator**.

##### Built-in functions/methods
These are just wrappers around a C function. 
**Read-only attributes**:
- `func.__doc__`: The documentation string, or [[Python none|None]].
- `func.__name__`: The functions name.
- `func.__self__`: Set to [[Python none|None]], or to the object calling this.
- `func.__module__`: The name of the module the function was defined in.

##### Classes
A [[Python class|class]] can be called, triggering the `__new__()` function.
If `__new__()` returns an **instance** of the class, its `__init__()` function gets called.

##### Class instances
Instances can be called by defining a `__call__()` function on them.