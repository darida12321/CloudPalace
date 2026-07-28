Inherits from [[Python immutable sequence|immutable sequences]]. Strings contain a sequence of [[Unicode|unicode]] codepoints.

There are multiple ways of templating strings:
- [[Python printf-style string formatting|Printf-style string formatting]]: With the `%` operator. Can be clunky.
- [[Python string formatting|String formatting]]: Using `format(value, format)` or `str.format()`.
- [[Python f-string|F-strings]]: Concise, but they execute arbitrary code.
- [[Python t-string|T-strings]]: Uses templates for higher control.

**Constructor**:
- `'string'`, `"string"`, `'''string'''`, `"""string"""`.
- `'stri' 'ng'`: When only separated by whitespace, they combine.
- `str(object)`: Calls `__str__()`, or `__repr__()`.
- `f'string'`: [[Python f-string|F-strings]] can include variables.
- `t'string'`: [[Python t-string|T-strings]] are similar to f-strings, but safer due to being template-based.
**Static methods**:
- `s.maketrans(dict)`: Create translation table mapping unicode ordinals to strings.
**Functions**:
- Formatting
	- `s.format()`: Perform [[Python string formatting|string formatting]].
	- `s.format_map(mapping)`: Similar to format but `mapping` is not cast to a [[Python dict|dict]].
- Searching and replacing
	- `s.find(sub, start, end)`: Find first index of substring. Return `-1` if not found.
	- `s.rfind(sub, start, end)`: Find last index of substring. Return `-1` if not found.
	- `s.index(sub, start, end)`: Same as find, but throw error instead of returning `-1`.
	- `s.rindex(sub, start, end)`: Same as find, but throw error instead of returning `-1`.
	- `s.startswith(prefix, start, end)`: Return `True` if string starts with `prefix`.
	- `s.endswith(suffix, start, end)`: Return `True` if string ends with `suffix`.
	- `s.removeprefix(prefix)`: If the string starts with `prefix`, remove it.
	- `s.removesuffix(suffix)`: If the string starts with `suffix`, remove it.
	- `s.count(sub, start, end)`: Number of non-overlapping occurrences of `sub`string.
	- `s.replace(old, new, count=-1)`: Replace `count` occurrences of `old` with `new`.
- Splitting and joining
	- `s.split(sep=None, maxsplit=-1)`: Return list of words split on `sep` or whitespace.
	- `s.rsplit(sep=None, maxsplit=-1)`: Split, but go from the right side with `maxsplit`.
	- `s.splitlines(keepends=False)`: Split the string into lines.
	- `s.partition(sep)`: Split into left side, separator, right side.
	- `s.rpartition(sep)`: Partition, but on the rightmost occurrence of `sep`.
	- `s.join(iterable)`: Concatenate a list of strings with `s` as a joiner.
- String classification
	- `s.isalpha()`: Are all characters alphabetic according to [[Unicode|unicode]]?
	- `s.isdecimal()`: Are all characters a base 10 number in some language?
	- `s.isdigit()`: Are all characters digits? Includes `²` for example.
	- `s.isnumeric()`: Are all characters numeric? Includes `⅕` for example.
	- `s.isalnum()`: Check if all characters are **alphabetic**, **decimal**, **digit** or **numeric**.
	- `s.isascii()`: Are all digits [[ASCII|ASCII]] characters?
	- `s.isidentifier()`: Is the string a valid identifier in [[Python|python]]?
	- `s.islower()`: Are all characters lowercase?
	- `s.isupper()`: Are all characters uppercase?
	- `s.istitle()`: Is the string in title case?
	- `s.isspace()`: Is the string only whitespace?
	- `s.isprintable()`: Is the string printable?
- Case manipulation
	- `s.lower()`: Convert cased characters to lowercase.
	- `s.upper()`: Convert cased characters to uppercase.
	- `s.casefold()`: Casefold string (ß to ss, cause it's sometimes capitalized as SS).
	- `s.capitalize()`: Capitalize first letter, lower the rest.
	- `s.title()`: First letter of each word uppercase, the rest lower.
	- `s.swapcase()`: Swap the cases of letters.
- Padding and stripping
	- `s.ljust(width, fillchar=' ')`: Make string a certain width, left align.
	- `s.rjust(width, fillchar=' ')`: Make string a certain width, right align.
	- `s.zfill(width)`: Fill the left side with `0`-s and possibly a sign prefix `+`/`-`.
	- `s.center(width, fillchar=' ')`: Make str certain `width`, centre aligned.
	- `s.expandtabs(tabsize=8)`: Expand tabs to spaces.
	- `s.strip(chars=None)`: Strip leading and trailing characters in `chars` or whitespace.
	- `s.lstrip(chars=None)`: Strip leading characters in `chars`, or whitespace.
	- `s.rstrip(chars=None)`: Strip trailing characters in `chars`, or whitespace.
- Translation and encoding
	- `s.translate(table)`: Translate string using translation table made by `maketrans()`.
	- `s.encode()`: Encode string to [[Python bytes|bytes]].
**Operations**:
- `%`: [[Python printf-style string formatting|Printf-style string formatting]].




