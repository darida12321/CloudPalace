A way of encoding [[Unicode|Unicode]] in [[Binary|binary]]. **UTF-16** (Unicode Transformation Format) simply uses 16 bits to represent a character. 

One caveat is that at 16 bits, the [[Endianness|endianness]] of the system starts to matter. To know what [[Endianness|endianness]] a **UTF-16** file was encoded in, a **byte order mark (BOM)** was introduced. It's placed at the beginning of the file, and it has a value `FE FF`.
- If the file starts with `FE FF`, it was encoded in big-endian.
- If the file starts wit h`FF FE`, it was encoded in little-endian.

Problems:
- 16 bits aren't enough to represent every [[Unicode]] **code point**.
- It's not [[ASCII]] compatible, as **UTF-16** uses 16-bit values instead of 8.
- If you only want to store [[ASCII]] characters, your storage requirement just doubled.



