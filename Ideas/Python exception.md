All exceptions derive from `BaseException`, and there's a number of [[Python built-in exceptions|predefined exceptions]].
They usually have an "associated value" specifying the details of the exception, which usually is a [[Python string|string]] or a [[Python tuple|tuple]].
It's encouraged to define custom exceptions by **inheriting** from `Exception`.

##### Raising and handling
An exception can be raised in one of these ways:
```python
raise exception
raise exception from original_exception
```
And they can be handled via a `except`, `finally` or a `with` [[Python statements|statement]].

##### Fields
**Fields**:
- `__context__`: The original **exception** if it was handled.
- `__cause__`: The **exception** in the `from` portion.
- `__suppress_context__`: Set to `True` if it's raised `from` another **exception**.
- `__traceback__`: A traceback object storing the stack where the **exception** happened.
- `__notes__`: List of notes.
**Functions**:
- `with_traceback(tb)`: Overwrite the `__traceback__` field.
- `add_note(note)`: Adds a note [[Python string|string]].

