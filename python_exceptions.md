### Python Exceptions

## Exceptions
### What is an Exception?
- **Exception**: An error that occurs during the execution of a program. Exceptions disrupt the normal flow of the program.

### Common Built-in Exceptions
- `Exception`: Base class for all exceptions.
- `ValueError`: Raised when a function receives an argument of the correct type but inappropriate value.
- `TypeError`: Raised when an operation or function is applied to an object of inappropriate type.
- `IndexError`: Raised when a sequence subscript is out of range.
- `KeyError`: Raised when a dictionary key is not found.
- `AttributeError`: Raised when an attribute reference or assignment fails.
- `IOError`: Raised when an I/O operation fails.
- `ZeroDivisionError`: Raised when division or modulo by zero takes place.

### Raising Exceptions
- Use the `raise` statement to raise an exception.

```python
raise ValueError("Invalid value")
```

### Handling Exceptions
- Use `try`, `except`, `else`, and `finally` blocks to handle exceptions.

```python
try:
    # code that may raise an exception
    pass
except ExceptionType as e:
    # code that runs if the exception occurs
    pass
else:
    # code that runs if no exception occurs
    pass
finally:
    # code that runs no matter what
    pass
```

### Example of Handling Exceptions
- Handling a `ZeroDivisionError`.

```python
try:
    result = 10 / 0
except ZeroDivisionError as e:
    print(f"Error: {e}")
else:
    print("No error occurred")
finally:
    print("This will always execute")
```

### Custom Exceptions
- Define custom exceptions by creating a new class derived from the `Exception` class.

```python
class CustomError(Exception):
    pass

try:
    raise CustomError("This is a custom error")
except CustomError as e:
    print(f"Caught custom error: {e}")
```

### Examples

#### Raising an Exception
```python
raise ValueError("Invalid value")
```

#### Handling Exceptions
```python
try:
    result = 10 / 0
except ZeroDivisionError as e:
    print(f"Error: {e}")
else:
    print("No error occurred")
finally:
    print("This will always execute")
```

#### Custom Exceptions
```python
class CustomError(Exception):
    pass

try:
    raise CustomError("This is a custom error")
except CustomError as e:
    print(f"Caught custom error: {e}")