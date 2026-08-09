This is the way that module **finders** and **loaders** communicate. It is stored in the final [[Python module|module]] as the `module.__spec__` attribute. It's usually created by the **finder**.


**Attributes**:
- `name`: The fully qualified name.
- `loader`: The **loader** used to load the module.
- `origin`: Location to use for the loader (e.g. for a `.py` file, the file's name).
- `submodule_search_locations`: [[Python string|Strings]] for the submodule locations (`module.__path__`).
- `loader_state`: Any [[Python object|object]], can be used to send additional data.
- `cached`: Filename of a compiled version of the module's compiled code (`.pyc`).
- `parent`: Fully qualified name of the package this module is in.
- `has_location`: If the `origin` refers to a loadable location.