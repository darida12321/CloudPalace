Same syntax as [[Python function definition statement|function definitions]], but using `async def`. **Coroutines** can use the `await`, `async for` and `async with` keywords.
```python
@decorator1
@decorator2()
async def func[T](arg1: T, arg2: T = 1, *args, **kwargs) -> None:
	pass
```

##### Await
Suspend the execution of a **coroutine** on an awaitable object (`__await__()`).
```python
await func()
```

##### Async for
An **asynchronous iterable** provides an `__aiter__()` method, which returns an **asynchronous iterator** that has a `__anext__()` method. `async for` iterates over asynchronous iterables.

The syntax is similar to a [[Python for statement|for loop]].
```python
async for x in iterable:
	pass
else:
	pass
```

##### Async with
Uses an **asynchronous context manager**, which has asynchronous `__enter__()` and `__exit__()` functions.

The syntax is similar to a [[Python with statement|with]] statement.
```python
async with A() as a:
	pass
```