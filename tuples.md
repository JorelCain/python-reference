### Python Tuples

## Tuples
### What is a Tuple?
- **Tuple**: An immutable, ordered collection of elements. Tuples are similar to lists but cannot be changed after creation.

### Creating Tuples
- Tuples can be created using parentheses `()` or the `tuple()` function.

```python
# Using parentheses
my_tuple = (1, 2, 3)

# Using the tuple() function
my_tuple = tuple([1, 2, 3])
```

### Accessing Elements
- Use indexing to access elements in a tuple.

```python
my_tuple = (1, 2, 3)
print(my_tuple[0])  # Output: 1
print(my_tuple[1])  # Output: 2
print(my_tuple[2])  # Output: 3
```

### Slicing Tuples
- Use slicing to access a range of elements in a tuple.

```python
my_tuple = (1, 2, 3, 4, 5)
print(my_tuple[1:3])  # Output: (2, 3)
print(my_tuple[:2])   # Output: (1, 2)
print(my_tuple[3:])   # Output: (4, 5)
```

### Tuple Methods
- Tuples have a limited set of methods because they are immutable.

#### `count()`
- Returns the number of times a specified value appears in the tuple.

```python
my_tuple = (1, 2, 2, 3)
print(my_tuple.count(2))  # Output: 2
```

#### `index()`
- Returns the index of the first occurrence of a specified value.

```python
my_tuple = (1, 2, 3)
print(my_tuple.index(2))  # Output: 1
```

### Unpacking Tuples
- Assign the elements of a tuple to multiple variables.

```python
my_tuple = (1, 2, 3)
a, b, c = my_tuple
print(a)  # Output: 1
print(b)  # Output: 2
print(c)  # Output: 3
```

### Nested Tuples
- Tuples can contain other tuples as elements.

```python
nested_tuple = (1, (2, 3), 4)
print(nested_tuple[1])     # Output: (2, 3)
print(nested_tuple[1][0])  # Output: 2
```

### Examples

#### Creating Tuples
```python
# Using parentheses
my_tuple = (1, 2, 3)

# Using the tuple() function
my_tuple = tuple([1, 2, 3])
```

#### Accessing Elements
```python
my_tuple = (1, 2, 3)
print(my_tuple[0])  # Output: 1
print(my_tuple[1])  # Output: 2
print(my_tuple[2])  # Output: 3
```

#### Slicing Tuples
```python
my_tuple = (1, 2, 3, 4, 5)
print(my_tuple[1:3])  # Output: (2, 3)
print(my_tuple[:2])   # Output: (1, 2)
print(my_tuple[3:])   # Output: (4, 5)
```

#### Tuple Methods
```python
my_tuple = (1, 2, 2, 3)

# count()
print(my_tuple.count(2))  # Output: 2

# index()
print(my_tuple.index(2))  # Output: 1
```

#### Unpacking Tuples
```python
my_tuple = (1, 2, 3)
a, b, c = my_tuple
print(a)  # Output: 1
print(b)  # Output: 2
print(c)  # Output: 3
```

#### Nested Tuples
```python
nested_tuple = (1, (2, 3), 4)
print(nested_tuple[1])     # Output: (2, 3)
print(nested_tuple[1][0])  # Output: 2