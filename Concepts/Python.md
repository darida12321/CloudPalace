Python is one of the most popular programming languages especially for **data analysis** and **machine learning** because of its readable syntax, large number of libraries, and that it's interpreted rather than compiled.

It has multiple interpreters like [[Pypy]], but the most commonly used one is the one implemented in C, called [[CPython]].

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

# Objects
Python is an [[Object oriented programming language|object oriented]] language with this pre-defined hierarchy:
- [[Python object|Object]]: An empty object that everything else inherits from.
	- **Singletons**: Special types that only have a single possible value.
		- (e.g. [[Python none|None]], [[Python notImplemented|NotImplemented]], [[Python ellipsis|Ellipsis]]).
	- **[[Python numbers module|Numbers]]**: Things to do arithmetic with. 
		- (e.g. [[Python int|int]], [[Python bool|bool]], [[Python float|float]], [[Python complex|complex]]).
	- **[[Python sequence|Sequences]]**:  Sequence of items that can be iterated.
		- (e.g. [[Python range|range]], [[Python tuple|tuple]], [[Python string|string]], [[Python bytes|bytes]], [[Python list|list]], [[Python bytearray|bytearray]]).
	- **Set type**: A collection of hashable objects (e.g. [[Python set|set]], [[Python frozenset|frozenset]]).
	- **Mapping**: Map hashable values to other values (e.g. [[Python dict|dict]]).
	- **Other**: (e.g. [[Python memoryview|memoryview]], [[Python generic alias type|generic alias type]], [[Python union type|union type]], [[Python exception|exceptions]], [[Python file|files]]).
	- Internal types: #TODO code stuff [here](https://docs.python.org/3/reference/datamodel.html#internal-types).

# Language features
Python defines a large number of [[Python operations|operations]], [[Python built-in constants|constants]], [[Python built-in exceptions|exceptions]], [[Python built-in functions|functions]], [[Python built-in types|types]]. These can be further manipulated by the different language features:
- **[[Python variable|Variables]]**: [[Python assignment statement|assignment]], [[Python del statement|del]], [[Python global statement|global]], [[Python nonlocal statement|nonlocal]], [[Python import statement|import]].
- **Logic**: [[Python assert statement|assert]], [[Python if statement|if]], [[Python match statement|match]], [[Python for statement|for]], [[Python while statement|while]].
- **Flow control**: [[Python pass statement|pass]], [[Python break statement|break]], [[Python continue statement|continue]], [[Python return statement|return]], [[Python yield statement|yield]].
- **Exceptions**: [[Python raise statement|raise]], [[Python try statement|try]], [[Python with statement|with]].
- **Definitions**: [[Python function definition statement|function definition]], [[Python coroutine definition statement|coroutine definition]], [[Python class definition statement|class definition]].
- **Types**: [[Python type statement|type]], [[Python type parameter list statement|type parameter list]].

You can define [[Python callable|functions and methods]] that execute code. These can be organized into [[Python class|classes]], which can be [[Python class instance|instantiated]]. A lot of Python's functionality works by using some [[Python special class methods|special class methods]].

Things can further be organized into [[Python module|modules]] and [[Python package|packages]], which are managed by the [[Python import system|import system]].

# Modules
Python has plenty of built-in, and external modules.
- [[Python numbers module|numbers]]: Creates abstract classes for numbers.
- [[Python math module|math]]: Common mathematical functions.
- [[Python types module|types]]: Helps with dynamic data types.
- [[Python builtins module|builtins]]: Definition of built-in values.
- [[Python importlib module|importlib]]: Functions aiding with the import mechanisms.
- [[Python site module|site]]: Usually automatically imported. Helps with command line interactions.
- [[Python sys module|sys]]: Automatically imported. Stores internal values and handles system interactions.

---
source: [Python 3 documentation](https://docs.python.org/3/library/index.html)
source: [Inside The Python Virtual Machine](https://leanpub.com/read/insidethepythonvirtualmachine)



 
