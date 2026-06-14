Python is one of the most popular programming languages especially for **data analysis** and **machine learning** because of its readable syntax, large number of libraries, and that it's interpreted rather than compiled.

# Example code
```python
class User:  
	@staticmethod
	def grade(score, pass_level=70):
		return "PASS" if score >= pass_level else "FAIL"
	    
	def __init__(self, name, scores):  
		self.name = name  
		self.scores = scores  
  
	def average(self):  
		return sum(self.scores) / len(self.scores)  

user = User("Sam", [72, 88, 95])  
for score in user.scores:  
	print(f"{score}: {User.grade(score, pass_level=50)}")  
print(f"Average: {user.average():.2f}")  # Round to two decimals
```

# Language definition
Python defines a few types by default:

- [x] default functions
- [ ] types
- [ ] type functions




# Default Types


# Numeric types `int, float, complex`
Integer: unlimited precision
- subtype: Boolean.
Floats: double-precision [[Floating-point representation|float]].
Complex numbers: two floats.

hex, octal and binary numbers are integers.
when doing arithmetic, ints are cast to floats, or floats to complex numbers.

number operations: `x+y, x-y, x*y, x/y, x//y, x%y, -x, +x, x**y`
bitwise operations on integers: `x | y, x ^ y, x & y, x << n, x >> n, ~x` (or, xor, and, lshift, rshift, not)

##### Methods on Integer type:
`x.bit_length()`: Return number of bits it takes up. (minus sign and leading zeros)
`x.bit_count()`: Return number of ones in the binary representation.
`x.to_bytes()`: Return array of bytes representing the integer.
`x.from_bytes()`: Convert byte array to integer
`x.as_integer_ratio()`: Return the int itself as 0. Exists to match floats.
`x.is_integer()`: Return True. Exists to match floats.
##### Methods on Float type:
`float.from_number()`: Return a float from a number.
`float.fromhex()`: Return float from hexadecimal string.
`x.as_integer_ratio()`: Return pair of ints whose ratio is x.
`x.is_integer()`: True if it has an integral value.
`x.hex()`: Convert x to a hexadecimal string. 
##### Methods on Complex type:
`complex.from_number()`: Convert a number to a complex number.

# Boolean types `bool`
The bool type has two constant instances `True` and `False`.
it's a subclass of `int`, but relying on this is discouraged.

##### Operators
Boolean operators: `not x`, `x and y`, `x or y`.
Objects are `True`, unless they have a `__bool__()` that's `False`, or a `__len__()` that's `0`.
Numerics are `True` unless their value is `0`.


Comparisons: `<`, `<=`, `>`, `>=`, `==`, `!=`, `is`, `is not`, `in`, `not in`.
For `<`, `<=`, `>`, `>=`, `==`: Instances are generally not equal and incomparable, unless `__lt__()`, `__le__()`, `__gt__()`, `__ge__()` and `__eq__()` are defined. These can be inferred from `__lt__()` and `__eq__()` alone.
For `is`, `is not`: Compares if two objects are the same. (have the same `id()`)
For `in`, `not in`: They apply to **iterable** objects, or ones that implement `__contains__()`


# Sequence types `list`, `tuple`, `range`
Iterable containers must implement `__iter__()` that returns an iterator, which has a `__iter__()` function returning itself, and a `__next__()` function for getting the next element. This is used for `for` loops 

There are mutable and immutable sequences.

operations:
`x in s`, `x not in s`, `s + t` (concat), `s * n` (concatting n times), `s[i]` (ith item), `s[i:j]` (slice from i to j), `s[i:j:k]` (slice from i to j with step k)

sequences of the same type support comparisons.
- `in` and `not in` are used by str, bytes and bytearray for subsequence-testing (`'gg' in 'eggs'`)
- `s * n` does not copy s, it's just a reference. use list comprehension for that.
- `s[i:j:k]`: i and j are truncated to -len(s) and len(s)

##### Sequence methods
`s.count()`: Return number of occurrences of a value.
`s.index()`: Return index of first occurrence of a value.


Immutable sequence types: implement the hash functions, so can be used as dict keys.
Mutable sequence types:
additional operations: 
`s[i:j:k] = t`: Slice elements are replaced by those in `t`.
`del s[i:j:k]`: Slice elements are removed.
`s += t`: Extend s with contents of `t`
`s *= n`: Extend s with itself `n` times.

##### Mutable sequence methods
`s.append()`: Append something to the end
`s.clear()`: Remove every item
`s.copy()`: Create a shallow copy.
`s.extend()`: Extend sequence with iterable
`s.insert()`: Insert element into position
`s.pop()`: Retrieve item at position and delete it
`s.remove()`: Remove item at position.
`s.reverse()`: Reverse sequence.


Lists: mutable sequences, constructed by `[a, b, c]`, `[x for x in iterable]`
`l.sort()`: Sort list

Tuples: immutable sequences, constructed by `(a, b, c)` or `a, b, c` or `a,`.

Ranges: Immutable sequences, constructed by `range()`. 
Implements negative indeces.


# Text and binary sequence type methods

#TODO string formatting guide
#TODO decimal/digit/numeric

formatting:
```python 
# Formatting
s.format() # Perform string formatting
s.format_map() # Similar to format (todo string formatting)

# Searching and replacing
x.find(), x.rfind()   # Find first/last index of substring. -1 if no
x.index(), x.rindex() # Same as find, but throw error instead of -1
x.startswith() # Return true if str starts with that
x.endswith() # Return true if str ends with that
x.count() # Number of non-overlapping occurrances of substring
x.replace() # Replace all occurrances of substr with something else

# Splitting and joining
x.split() # Return list of words split on a delimiter.
x.rsplit() # Split, but if maxsplit is defined, prioritize the right.
x.splitlines() # Split the string into lines
x.partition() # Split into left side, separator, right side
x.rpartition() # Partition, but find rightmost occurance.
x.join() # Concat a list of strings with str as a joiner.

# String classification
x.isalpha() # Are all characters alphanumeric
s.isdecimal() # Is it a base 10 number in any language.
x.isdigit() # Are all characters digits
s.isnumeric() # Are all characters numeric? 
x.isalnum() # Check if all digits are in the above 4.
s.isidentifier() # Is the str a valid identifier
x.islower() # Are all characters lowercase?
x.isupper() # Are all characters uppercase?
x.istitle() # Is the string in title case?
x.isspace() # Is the string only whitespace?
s.isprintable() # Is the string printable?

# Case manipulation
x.lower() # Convert cased characters to lowercase
x.upper() # Convert cased characters to upporcase
s.casefold() # Remove casing as much as possible (ß to ss) ????? TODO
x.capitalize() # Capitalize first letter, lower the rest.
x.title() # First letter of each word uppercase, the rest lower.
x.swapcase() # Swap the cases of letters.

# Padding and stripping
x.ljust() x.rjust() # Make str certain width, left/right align.
x.center() # Make str certain width, center aligned.
x.expandtabs() # Expand tabs to spaces
x.strip() # Strip leading and trailing characters.
x.lstrip(), x.rstrip() # Strip only leading, or trailing chars.

# Translation and encoding
x.translate() # Translate string using translation table
x.maketrans() # Create translation table
s.encode() # Encode string to bytes.
b.decode() # Decode bytes to string.


```


Strings: Immutable character sequence. object.
Can be `'str', "str", '''str''', """str"""`,
`('str1' 'str2') = 'str1str2`

`str()`: call `__str__()`, or `__repr__()`.
it has the common sequence operations (`in`), and the str functions.

`f'str'`: formatted string literal, or f-string. 
- In `{}`, you can write expressions that will get evaluated.
- Putting `=` at the end will print the expression, then its value.
- Putting `!s`, `!r` or `!a` will format it using `str()`, `repr()` or `ascii()`.
- Putting `:` will format it using `format()`.  #TODO

`t'str'`: template string literal, or t-string.
- Same format as f-strings. Instead of producing a string, it makes a `string.templatelib.Template`.
- #TODO examples of this shit. what is it?

Strings also have a `%` operator. (string formatting / interpolation operator).
`'%s has %d quote types' % ('Python', 2) # Python has 2 quote types`

A conversion specifier looks like this:
1. Start character: `%`
2. Mapping key: Optional. Names the mapping. `(name)`
3. Conversion flags: Optional. 
	- `#`: Use alternative form.
	- `0`: Conversion will be zero padded for **numeric** values.
	- `-`: Conversion will be left adjusted.
	- ` `: Blank space should be left before positive number.
	- `+`: A sign character will precede conversion.
4. Min field width: Optional. `*` means read from the next element of the tuple. 
5. Precision: Optional. Dot, followed by precision `.2`. An `*` means read from next element.
6. Length modifier: Optional. `h`, `l` or `L`, but it's ignored by python.
7. Conversion type.
	1. `d`, `i`: Signed integer decimal.
	2. `o`: Signed octal.
	3. `x`, `X`: Signed hexadecimal (lower/uppercase)
	4. `e`, `E`: Floating-point exponential format (lower/uppercase)
	5. `f`, `F`: Floating-point decimal format (lower/uppercase)
	6. `g`, `G`: Exponential if exponent < -4, decimal otherwise. (lower/uppercase) #TODO
	7. `c`: Single character.
	8. `r`, `s`, `a`: String using `repr()`, `str()` or `ascii()`.
	9. `%`: No conversion, results in % character.

The right side is either a single value, a tuple, or a dictionary.


# String formatting

`[[fill]align][sign] [z][#] [0][width][grouping] .[precision][grouping] [type]`

`fill`: Only valid when `align` is defined. 
- The character used for filling. default is `' '`. 
`align`: 
- `=` Only valid for **numbers**. Padding between sign and number. (default when `fill` is `0`)
- `<` Left align. (default usually)
- `>` Right align. (default for numbers)
- `^` Centre aligned.
`sign`: Only valid for **numbers**. 
- `+`: Use sign for both positive and negative numbers.
- `-`: Only use sign for negative numbers. (default)
- ` `: Leading space on positive numbers, sign on negatives.

`z`: Only valid for **floating-point numbers**.
- Turn negative zero to positive zero after rounding.
`#`: Use alternate form. Valid for **integer**, **float** and **complex** numbers.
- **Integer**: when binary/octal/hexadecimal output is used, add `0b`, `0o`, `0x` or `0X`.
- **Float** and **complex**: Always contain a decimal point character.

`0`: When preceding `width`, enables sign-aware zero padding. Same as `fill` being `0`.
`width`: Minimum field width.
`precision`: Start with `.`, then a decimal integer.
- For `f`, `F`, `g`, `G` types, show how many digits to print after the decimal point.
- For **string** types, maximum field size.
- Not allowed for **integers**.
`grouping`: Digit groups for integral (after `width`) and fractional (after `precision`) parts.
- `,`: Insert a comma ever 3 digits for `d` and **float** types except `n`.
- `_`: Insert underscore every 3 digits for `d`, **float** types except `n`.
	- For `b`, `o`, `x`, and `X` types, it's every 4 digits.

`type`: How the data should be represented.
	- **String**: `s`.
	- **Integer**: 
		- `b` Binary.
		- `c` Character.
		- `d` Decimal.
		- `o` Octal.
		- `x` Hexadecimal lowercase.
		- `X` Hexadecimal uppercase.
		- `n` Number. Same as `d`, but uses locale.
	- **Float** and **integer** (converted to float using `float()`):
		- `e`: Scientific notation. (`1.23e3`)
		- `E`: Scientific notation uppercased.
		- `f`: Fixed-point notation. (`1.23`, `nan`, `inf`) #TODO am I sure?
		- `F`: Fixed-point notation uppercased.
		- `g`: General format. For small numbers it's `f`, for big ones it's `e`. #TODO
		- `G`: General format uppercased.
		- `n`: Same as `g` but uses locale settings.
		- `%`: Percentage. Multiply number by 100 and add % sign.



numerics
sequences
mappings
classes
instances
exceptions









# Default functions

```python
# Math
abs() # Absolute value (int, float or __abs__())
all() # Return true if all elements in iterable are true
any() # Return true if any elements in iterable are true
divmod() # Return quotient and remainder of int division as a pair
pow() # Raise to the power of
round() # Round number to some digits.
hash() # Get hash value of object (__hash__())

# Type conversion
bool()    # Convert to bool (__bool__() or __len__() == 0)
complex() # Convert to complex number
float()   # Convert to float
int()     # Convert to int
set()     # Convert to set
str()     # Convert to string
list()    # Convert to list
range()   # Convert to range
tuple()   # Convert to tuple
frozenset() # Convert to frozenset

bytearray() # Create a new array of bytes (mutable)
bytes()     # Create a new bytes object (immutable)
dict()      # Create a new dictionary



# String manipulation
repr() # String representation or <obj> (__repr__())
ascii() # Similar to repr() but escape non-ASCII characters
ord()  # Return integer value of unicode character
chr()  # Return string representation of unicode character
format() # Format a value according to a format spec. (__format__()) TODO TODO TODO
hex()    # Convert integer to hexadecimal string (0x)
oct()    # Convert integer to octal (0o)
bin()    # Convert integer to binary string (0b)

print() # Print to stdout
input() # Get line from stdin
open() # Open file and return a file object


# Array utils
enumerate() # Return (index, elem) tuples of an iterable.
zip() # Zip two iterables together.
filter() # Filter an iterable.
map() # Map a function over an iterable.
len() # Get length of object
max() # Get maximum element of sequence
min() # Get minimum element of sequence
sum() # Get sum of sequence
sorted() # Return sorted list from items

slice() # Return a slice object (a[start:stop, i])



# Code manipulation
compile() # Compile source code into a code or AST object.
eval() # Evaluate a string of code with environment.
exec() # Execute a string of code with environment.

breakpoint() # Calls sys.breakpointhook() to enter debugging mode.
memoryview() # Get memory view of argument
help() # Invoke built-in help system

type() # Return type of object.
callable() # Return True if argument is callable. (__call__())
globals() # Get dictionary of the module's namespace.
locals()  # Get dictionary of local symbol table.
dir() # Get names in local scope, or attributes of object (__dir__())
vars() # Get the writable attributes of object/module

isinstance() # Return if object is instance of classinfo
issubclass() # Return if class is sublass of classinfo
getattr() # Get attribute of an object (obj.attr) (__getattribute__())
setattr() # Set attribute of an object (obj.attr = 0)
delattr() # Del attribute of an object (del obj.attr)
id()      # Get identity of an object (unique integer)



# Iterables 
iter() # Return an iterator object (__iter__())
reversed() # Return a reverse iterator. (__reversed__())
next() # Get the next elem in iter (__next__())
aiter() # Return an asynchronous iterator (__aiter__())
anext() # Get next elem in async iterator (__anext__())




# Syntax
# @classmethod # Transform a method to a class method (class can call)
# @staticmethod # Transform a method to static (no first argument)
super() # Proxy that delegates method calls to parent/sibling
object() # Base class of all other classes
property() # Set property of object (getx, setx, delx)
    # @property, @x.setter, @x.deleter # decorators for the same thing
__import__() # Import module

```









---

```python ln:false

# Data types
420 # Integer
6.9 # Float
True  # Boolean
False # Boolean
'hello' # String
f'embed {number + 2} here' # String
"hello" # String
b'a' # byte array
[1, 'a', True] # List
(1, 2, 3) # Tuple

# Operators
1 + 2 # Addition
1 * 2 # Multiplication
'a' + 'b' # 'ab'
'a' * 3 # 'aaa'
2 ** 2 # Power
5 // 2 # Initger division
5 % 2 # Modulo
== != >= <= > < # more of these
and or not # boolean operators

# Built-in Functions
print('Msg1', 'msg2', end='|') # Print with spaces
input('Prompt: ')
int('12')
float(12) 
str(12.0) 
type(12) # type of variable
ord() # ordinal of character
chr() # Character with this code
list()
len() # length of list
range(start, stop, step) # generator with these
enumerate(array) # create index-element tuples
set()
dict()
tuple()
map(func, my_list)
filter(func, my_list)


string = 'my string'
string.upper()
string.lower()
string.capitalize() # First letter capitalize
string.count('st') # how many of it exists

my_list = [1]
my_list.append(2)
my_list.extend(['hi', 4, []])
my_list.pop() # return last element
my_list.remove()
my_list[1]
my_list[start:stop:step] # start at start, stop at stop, step by step
func(*my_list) # pass elements as variables


my_tuple = (2, True) 
my_tuple[0] # no assignment

my_set = set()
my_set = {1, 2, 4}
my_set.add(5)
my_set.remove(5)
my_set.union(my_set)
my_set.intersection(my_set)
4 in my_set

my_dict = {}
my_dict = {'key': 2, True: []}
my_dict['other'] = 6.7
del my_dict['other']
my_dict.values()
my_dict.keys()
my_dict.items() # iterator for elements
func(**my_dict) # pass elements as keywordargs


# Syntax
variable_name = 'string value'
global glob_variable = 'don\'t use this'

if (False):
	pass
elif (True):
	pass
else: 
	pass

while True:
	pass
	
for i in range(5):
	pass
for i in my_array:
	pass
for key, value in my_dict.items()
	pass
[x for x in range(5) if True]

def func(arg1, arg2=2, *args, **kwargs):
	# args: regular arguments, keyword arguments
	return 5, 2 # tuple
r1, r2 = func(7)

func2 = lambda x, y: x + y

try:
	raise Exception('Sussy')
except Exception as e:
	print(e)
finally:
	pass



class Animal:
	total_count = 2;
	def __init__(self, age):
		self.age = age
		total_count += 1
	
	@classmethod
	def something(cls):
		return cls.total_count
	
	@staticmethod
	def something_else():
		print('idk')

class Dog(Animal):
	def __init__(self, age, name):
		super().__init__(age)
		self.name = name
	def speak(self):
		print('Woof')
	def __str__(self):
		print(f'Dog: {name}')

dog = Dog('Zulu')
Animal.total_count;
Animal.something();

with open('file.txt') as f:
	f.read()

```


#TODO import, export, decorators

list of functions: https://docs.python.org/3/library/functions.html
list of everything: https://docs.python.org/3/library/index.html


---
source: [Python 3 documentation](https://docs.python.org/3/library/index.html)
source: [Inside The Python Virtual Machine](https://leanpub.com/read/insidethepythonvirtualmachine)
source: [Python for Data Analysis Third Edition](https://www.lkhibra.ma/books/Python-for-Data-Analysis.pdf)


