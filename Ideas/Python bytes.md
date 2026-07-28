Inherits from [[Python immutable sequence|immutable sequences]]. Strings contain a sequence of 8-bit integers.

**Constructor**:
- `b'string'`, `b"string"`, `b'''string'''`, `b"""string"""`.
- `bytes(10)`: 10 bytes, all 0.
- `bytes(iterable)`: Only accepts [[ASCII]] characters.
- `bytes(obj)`: Copy binary data.
**Static methods**:
- `bytes.maketrans(dict)`: Create translation table mapping unicode ordinals to strings.
- `bytes.fromhex(str)`: Create bytes from hexadecimal string.
**Functions**:
- Formatting
	- `bytes.format()`: Perform [[Python string formatting|string formatting]].
	- `bytes.format_map(mapping)`: Similar to format but `mapping` is not cast to a [[Python dict|dict]].
- Searching and replacing
	- `bytes.find(sub, start, end)`: Find first index of substring. Return `-1` if not found.
	- `bytes.rfind(sub, start, end)`: Find last index of substring. Return `-1` if not found.
	- `bytes.index(sub, start, end)`: Find, but throw error instead of returning `-1`.
	- `bytes.rindex(sub, start, end)`: Find, but throw error instead of returning `-1`.
	- `bytes.startswith(prefix, start, end)`: Return `True` if string starts with `prefix`.
	- `bytes.endswith(suffix, start, end)`: Return `True` if string ends with `suffix`.
	- `bytes.removeprefix(prefix)`: If the string starts with `prefix`, remove it.
	- `bytes.removesuffix(suffix)`: If the string starts with `suffix`, remove it.
	- `bytes.count(sub, start, end)`: Number of non-overlapping cases of `sub`string.
	- `bytes.replace(old, new, count=-1)`: Replace `count` cases of `old` with `new`.
- Splitting and joining
	- `bytes.split(sep=None, maxsplit=-1)`: Return words split on `sep` or whitespace.
	- `bytes.rsplit(sep=None, maxsplit=-1)`: Split, but go from the right if `maxsplit`.
	- `bytes.splitlines(keepends=False)`: Split the string into lines.
	- `bytes.partition(sep)`: Split into left side, separator, right side.
	- `bytes.rpartition(sep)`: Partition, but on the rightmost occurrence of `sep`.
	- `bytes.join(iterable)`: Concatenate a list of strings with `s` as a joiner.
- String classification
	- `bytes.isalpha()`: Are all characters alphabetic according to [[Unicode|unicode]]?
	- `bytes.isdigit()`: Are all characters digits? Includes `²` for example.
	- `bytes.isalnum()`: Are all characters [[ASCII]] characters or digits?
	- `bytes.isascii()`: Are all digits [[ASCII|ASCII]] characters?
	- `bytes.islower()`: Are all characters lowercase?
	- `bytes.isupper()`: Are all characters uppercase?
	- `bytes.istitle()`: Is the string in title case?
	- `bytes.isspace()`: Is the string only whitespace?
- Case manipulation
	- `bytes.lower()`: Convert cased characters to lowercase.
	- `bytes.upper()`: Convert cased characters to uppercase.
	- `bytes.capitalize()`: Capitalize first letter, lower the rest.
	- `bytes.title()`: First letter of each word uppercase, the rest lower.
	- `bytes.swapcase()`: Swap the cases of letters.
- Padding and stripping
	- `bytes.ljust(width, fillchar=' ')`: Make string a certain width, left align.
	- `bytes.rjust(width, fillchar=' ')`: Make string a certain width, right align.
	- `bytes.zfill(width)`: Fill the left side with `0`-s and possibly a sign prefix `+`/`-`.
	- `bytes.center(width, fillchar=' ')`: Make str certain `width`, centre aligned.
	- `bytes.expandtabs(tabsize=8)`: Expand tabs to spaces.
	- `bytes.strip(chars=None)`: Strip leading and trailing characters in `chars` or whitespace.
	- `bytes.lstrip(chars=None)`: Strip leading characters in `chars`, or whitespace.
	- `bytes.rstrip(chars=None)`: Strip trailing characters in `chars`, or whitespace.
- Translation and encoding
	- `bytes.translate(table)`: Translate string using translation table made by `maketrans()`.
	- `bytes.decode()`: Encode bytes to [[Python string|string]].
**Operations**:
- `%`: [[Python printf-style string formatting|Printf-style string formatting]].


