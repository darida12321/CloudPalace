A **file** object represents an open file. Can be created by the `open()` [[Python built-in functions|built-in function]], among many others. They are `with` [[Python with statement|statement]] context managers.


**Attributes**:
- `encoding`: The name of the [[String representation|encoding]].
- `errors`: The error setting of the decoder/encoder.
- `newlines`: A string or [[Python tuple|tuple]] of newlines translated so far.
- `buffer`: The underlying binary buffer.
**Functions**:
- `file.detach()`: Separate the underlying binary buffer and return it.
- `file.read(size=-1)`: Retrieve up to `size` amount of data. 
- `file.readline(size=-1)`: Read line until newline or EOF.
- `file.seek(offset)`: Change the stream position.
- `file.tell()`: Return current stream position.
- `file.write(data)`: Store `data` to file.
- `file.close()`: Flush buffers and close the file.