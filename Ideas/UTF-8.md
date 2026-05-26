A way of encoding [[Unicode|Unicode]] in [[Binary|binary]]. **UTF-8** (Unicode Transformation Format) was an answer to many of [[UTF-16]]'s problems. It uses 8-bit blocks, but it uses a variable amount of bytes per character.
- Characters from `U+0000` to `U+007F` (0 - 127, 7 bit) take 1 byte
- Characters from `U+0080` to `U+07FF` (128 - 2047, 11bit) take 2 bytes
- Characters from `U+0800` to `U+FFFF` (2048 - 65536, 16bit) take 3 bytes
- Characters from `U+10000` to `U+10FFFF` take 4 bytes

The problems addressed:
- 4 bytes are enough to store every [[Unicode]] **code point**.
- It's [[ASCII]]-compatible by design. `U+0041: A` is stored as `41`.
- Since [[ASCII]] is represented one-to-one, there is no wasted space.

**UTF-8** does this by employing specific binary patterns:
- `1 byte`: `0xxxxxxx`
- `2 byte`: `110xxxxx 10xxxxxx`
- `3 byte`: `1110xxxx 10xxxxxx 10xxxxxx`
- `4 byte`: `11110xxx 10xxxxxx 10xxxxxx 10xxxxxx`
Each extra byte starts with `10`, so text can be iterated over forwards and backwards.

It basically checked every checkbox for representing text, so it's the most widely used one.
