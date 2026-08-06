Python programs have a hierarchy:
- Python code consists of **code blocks** defined by [[Python module|modules]], [[Python class definition statement|classes]], [[Python function definition statement|functions]], etc...
- Each **code block** sets a **scope**.
- Scopes map **names** to objects. These are created by [[Python class definition statement|class definition]], [[Python function definition statement|function definition]], [[Python assignment statement|assignments]], [[Python for statement|for loops]], [[Python with statement|with statements]], [[Python match statement|match statements]], [[Python import statement|import statements]], [[Python type statement|type statements]], `exec()` and `eval()`.

A name bound at the [[Python module|module]] level is a **global variable**.

##### Creating variables
A new **binding** is added to the smallest **scope**. This can be changed by:
- Using [[Python global statement|global]] variables, which create the binding in the module's **namespace**.
- Using [[Python nonlocal statement|nonlocal]] variables, which reuses the binding in the nearest scope.

There is an exception. **Bindings** defined in [[Python class definition statement|class]] block stays in the class block, and don't trickle down to functions.

##### Resolving variables.
A variable is resolved by searching inside-out starting from the nearest scope.
- [[Python global statement|Global]] variables check the [[Python module|module]]'s namespace, then the [[Python builtins module|builtins module]].
- [[Python nonlocal statement|Nonlocal]] variables also check inside-out, from the second nearest scope.