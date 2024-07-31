# Python Variables and Data Types

## Variables
### What is a Variable?
- **Variable**: A reserved memory location to store values. In Python, variables are created when you assign a value to them.

### Variable Naming Rules
- Must start with a letter (a-z, A-Z) or an underscore (_)
- Cannot start with a number
- Can only contain alpha-numeric characters and underscores (A-z, 0-9, and _)
- Case-sensitive (e.g., `myVar` and `myvar` are different)

### Assigning Values to Variables
- Use the `=` operator to assign a value to a variable.

```python
x = 5
y = "Hello, World!"
```

### Multiple Assignments
- Assign multiple variables in one line.

```python
a, b, c = 1, 2, "Three"
```

### Swapping Variables
- Swap the values of two variables.

```python
x, y = y, x
```

## Data Types
### Built-in Data Types
Python has several built-in data types, including:

1. **Numeric Types**: `int`, `float`, `complex`
2. **Sequence Types**: `list`, `tuple`, `range`
3. **Text Type**: `str`
4. **Mapping Type**: `dict`
5. **Set Types**: `set`, `frozenset`
6. **Boolean Type**: `bool`
7. **Binary Types**: `bytes`, `bytearray`, `memoryview`

### Numeric Types
#### Integer (`int`)
- Whole numbers, positive or negative, without decimals.

```python
x = 10
y = -5
```

#### Float (`float`)
- Numbers with a decimal point or in exponential form.

```python
x = 10.5
y = -3.14
z = 1.5e2  # 1.5 * 10^2 = 150.0
```

#### Complex (`complex`)
- Numbers with a real and imaginary part.

```python
x = 1 + 2j
y = complex(1, 2)
```

### Sequence Types
#### List (`list`)
- Ordered, mutable collection of items.

```python
my_list = [1, 2, 3, "four", 5.0]
```

#### Tuple (`tuple`)
- Ordered, immutable collection of items.

```python
my_tuple = (1, 2, 3, "four", 5.0)
```

#### Range (`range`)
- Represents a sequence of numbers, commonly used in loops.

```python
my_range = range(1, 10)  # 1 to 9
```

### Text Type
#### String (`str`)
- Ordered, immutable sequence of characters.

```python
my_string = "Hello, World!"
```

### Mapping Type
#### Dictionary (`dict`)
- Unordered, mutable collection of key-value pairs.

```python
my_dict = {"name": "Alice", "age": 25}
```

### Set Types
#### Set (`set`)
- Unordered collection of unique items.

```python
my_set = {1, 2, 3, 4, 5}
```

#### Frozen Set (`frozenset`)
- Immutable version of a set.

```python
my_frozenset = frozenset([1, 2, 3, 4, 5])
```

### Boolean Type
#### Boolean (`bool`)
- Represents one of two values: `True` or `False`.

```python
is_active = True
is_deleted = False
```

### Binary Types
#### Bytes (`bytes`)
- Immutable sequence of bytes.

```python
my_bytes = b"Hello"
```

#### Byte Array (`bytearray`)
- Mutable sequence of bytes.

```python
my_bytearray = bytearray(5)  # bytearray of size 5
```

#### Memory View (`memoryview`)
- Allows Python code to access the internal data of an object that supports the buffer protocol without copying.

```python
my_memoryview = memoryview(b"Hello")
```

## Type Conversion
### Implicit Type Conversion
- Python automatically converts one data type to another.

```python
x = 10
y = 2.5
z = x + y  # z will be 12.5 (float)
```

### Explicit Type Conversion
- Use built-in functions to convert between types.

```python
x = 10
y = "20"
z = int(y)  # Convert string to integer
result = x + z  # result will be 30
```

### Common Type Conversion Functions
- `int()`: Converts to integer
- `float()`: Converts to float
- `str()`: Converts to string
- `list()`: Converts to list
- `tuple()`: Converts to tuple
- `set()`: Converts to set
- `dict()`: Converts to dictionary

```python
x = 10.5
y = int(x)  # y will be 10

a = "123"
b = float(a)  # b will be 123.0
```

## Checking Data Types
### Using `type()`
- Determine the type of a variable.

```python
x = 10
print(type(x))  # Output: <class 'int'>
```

### Using `isinstance()`
- Check if an object is an instance of a specific type.

```python
x = 10
print(isinstance(x, int))  # Output: True
```

