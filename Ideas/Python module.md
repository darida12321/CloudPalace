Python code is organized into **modules**. They are created by the `import` [[Python import statement|statement]], or the [[Python importlib module|importlib module]]. [[Python global statement|Global]] [[Python variable|variables]] are in the module's `__dict__` [[Python dict|dictionary]]. In fact, any variable access such as `m.x` gets translated to `m.__dict__['x']`.

In older versions, import-related information was spread across `__file__`, `__cached__`, `__loader__`, `__package__` and `__path__`. These were moved to `module.__spec__`, which is a [[Python module spec|ModuleSpec]] object.


**Attributes**:
- `module.__name__`: Unique name. For directly executed modules, it's `"__main__"`.
- `module.__spec__`: The module's import-related [[Python module spec|module spec]].
- `module.__doc__`: Documentation string.
- `module.__annotations__`: [[Python dict|Dictionary]] of [[Python annotation|annotations]].
- `module.__annotate__`: The [[Python annotation|annotation]] function.
- `module.__dict__`: The namespace of the module. (Cannot be accessed as a [[Python variable|variable]]).
