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

A **finder** returns a [[Python importlib module module spec|module spec]] and sends it to a **loader**.

##### Loading
If the **loader** has a `create_module(spec)` function defined, it's used to create the actual [[Python module|module]]. Otherwise, the `types.ModuleType(spec.name)` is used.

**Loaders** must define an `exec_module(module)` function. They execute the [[Python module|module]]'s code using the `module.__dict__` namespace.
