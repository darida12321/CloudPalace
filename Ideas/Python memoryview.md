Memory views give access to the internal data of an object that supports the buffer protocol. By default, these are [[Python bytes|bytes]] and [[Python bytearray|byte array]].

**Constructor**:
- `memoryview(obj)`
**Fields**:
- `obj`: The underlying object.
- `nbytes`: Amount of space the memoryview takes up, in bytes.
- `readonly`: Whether or not it's readonly.
- `format`: The format of the binary data in a string, using the [[Python struct module|struct module]]'s syntax.
- `itemsize`: The size in bytes of each element.
- `ndim`: How many dimensions the data has.
- `shape`: [[Python tuple|n-tuple]] (n being `.ndim`) denoting the shape of n-dimensional data.
- `strides`: Tuple of ints giving the offset along each dimension when indexing.
- `suboffsets`: Used for PIL-style arrays (`Pillow` image library).
- `c_contiguous`: Whether it's C-contiguous (last index varies the fastest).
- `f-contiguous`: Whether it's Fortran-contiguous (first index varies the fastest).
- `contiguous`: Whether it's contiguous. (Either C-contiguous or F-contiguous).
**Functions**:
- `m.tobytes()`: Return data as a bytestring (`b'abc'`).
- `m.hex()`: Return data as a hexadecimal string representation.
- `m.tolist()`: Return data as a [[Python list|list]].
- `m.toreadonly()`: Return a read-only version.
- `m.release()`: Release underlying buffer (allow resizing for `bytearray`s, etc.)
- `m.cast(format, shape)`: Cast to different data type, and change data dimensionality.
- `m.count(value)`: Count occurrences of `value`.
- `m.index(value, start, stop)`: First occurrence of `value` between `start` and `stop`.
**Operations**:
- `m[0]`: Indexing
- `m[i:j:k]`: Slicing
- `m[i:j:k] = x`: Slice assignment (if `m` is mutable).



