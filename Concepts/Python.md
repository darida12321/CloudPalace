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
format() # Format a value according to a format spec. (__format__())
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


