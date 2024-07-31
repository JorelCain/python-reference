### Python Dictionaries

## Dictionaries
### What is a Dictionary?
- **Dictionary**: A collection of key-value pairs. Each key is unique and maps to a value.

### Creating Dictionaries
- Dictionaries can be created using curly braces `{}` or the `dict()` function.

```python
# Using curly braces
my_dict = {"name": "Alice", "age": 30, "city": "New York"}

# Using the dict() function
my_dict = dict(name="Alice", age=30, city="New York")
```

### Accessing Values
- Use the key inside square brackets `[]` or the `get()` method to access values.

```python
my_dict = {"name": "Alice", "age": 30, "city": "New York"}

# Using square brackets
print(my_dict["name"])  # Output: Alice

# Using get() method
print(my_dict.get("age"))  # Output: 30
```

### Adding and Updating Values
- Assign a value to a key to add or update an entry.

```python
my_dict = {"name": "Alice", "age": 30}

# Adding a new key-value pair
my_dict["city"] = "New York"

# Updating an existing key-value pair
my_dict["age"] = 31
```

### Removing Values
- Use the `del` statement or the `pop()` method to remove a key-value pair.

```python
my_dict = {"name": "Alice", "age": 30, "city": "New York"}

# Using del statement
del my_dict["city"]

# Using pop() method
age = my_dict.pop("age")
```

### Dictionary Methods
- Dictionaries have several built-in methods for various operations.

#### `keys()`
- Returns a view object containing the dictionary's keys.

```python
my_dict = {"name": "Alice", "age": 30}
print(my_dict.keys())  # Output: dict_keys(['name', 'age'])
```

#### `values()`
- Returns a view object containing the dictionary's values.

```python
my_dict = {"name": "Alice", "age": 30}
print(my_dict.values())  # Output: dict_values(['Alice', 30])
```

#### `items()`
- Returns a view object containing the dictionary's key-value pairs.

```python
my_dict = {"name": "Alice", "age": 30}
print(my_dict.items())  # Output: dict_items([('name', 'Alice'), ('age', 30)])
```

#### `update()`
- Updates the dictionary with key-value pairs from another dictionary or an iterable of key-value pairs.

```python
my_dict = {"name": "Alice", "age": 30}
my_dict.update({"city": "New York", "age": 31})
```

### Checking Keys
- Use the `in` keyword to check if a key exists in the dictionary.

```python
my_dict = {"name": "Alice", "age": 30}
print("name" in my_dict)  # Output: True
print("city" in my_dict)  # Output: False
```

### Examples

#### Creating Dictionaries
```python
# Using curly braces
my_dict = {"name": "Alice", "age": 30, "city": "New York"}

# Using the dict() function
my_dict = dict(name="Alice", age=30, city="New York")
```

#### Accessing Values
```python
my_dict = {"name": "Alice", "age": 30, "city": "New York"}

# Using square brackets
print(my_dict["name"])  # Output: Alice

# Using get() method
print(my_dict.get("age"))  # Output: 30
```

#### Adding and Updating Values
```python
my_dict = {"name": "Alice", "age": 30}

# Adding a new key-value pair
my_dict["city"] = "New York"

# Updating an existing key-value pair
my_dict["age"] = 31
```

#### Removing Values
```python
my_dict = {"name": "Alice", "age": 30, "city": "New York"}

# Using del statement
del my_dict["city"]

# Using pop() method
age = my_dict.pop("age")
```

#### Dictionary Methods
```python
my_dict = {"name": "Alice", "age": 30}

# keys()
print(my_dict.keys())  # Output: dict_keys(['name', 'age'])

# values()
print(my_dict.values())  # Output: dict_values(['Alice', 30])

# items()
print(my_dict.items())  # Output: dict_items([('name', 'Alice'), ('age', 30)])

# update()
my_dict.update({"city": "New York", "age": 31})
```

#### Checking Keys
```python
my_dict = {"name": "Alice", "age": 30}
print("name" in my_dict)  # Output: True
print("city" in my_dict)  # Output: False