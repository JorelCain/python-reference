### Python `for` Loops

## `for` Loops
### What is a `for` Loop?
- **`for` Loop**: A control flow statement that is used to iterate over a sequence (such as a list, tuple, dictionary, set, or string) and execute a block of code for each item in the sequence.

### Basic `for` Loop
- The `for` loop in Python is used to iterate over a sequence (list, tuple, dictionary, set, or string).

```python
for item in sequence:
    # code block to be executed for each item in the sequence
```

### Looping Through a List
- You can loop through the items of a list using a `for` loop.

```python
my_list = [1, 2, 3, 4, 5]
for item in my_list:
    print(item)
```

### Looping Through a String
- You can loop through the characters of a string using a `for` loop.

```python
my_string = "hello"
for char in my_string:
    print(char)
```

### Looping Through a Tuple
- You can loop through the items of a tuple using a `for` loop.

```python
my_tuple = (1, 2, 3, 4, 5)
for item in my_tuple:
    print(item)
```

### Looping Through a Dictionary
- You can loop through the keys of a dictionary using a `for` loop.

```python
my_dict = {'a': 1, 'b': 2, 'c': 3}
for key in my_dict:
    print(key)
```

- You can loop through the values of a dictionary using the `values()` method.

```python
my_dict = {'a': 1, 'b': 2, 'c': 3}
for value in my_dict.values():
    print(value)
```

- You can loop through the key-value pairs of a dictionary using the `items()` method.

```python
my_dict = {'a': 1, 'b': 2, 'c': 3}
for key, value in my_dict.items():
    print(key, value)
```

### Looping Through a Set
- You can loop through the items of a set using a `for` loop.

```python
my_set = {1, 2, 3, 4, 5}
for item in my_set:
    print(item)
```

### Using `range()` Function
- The `range()` function generates a sequence of numbers, which is useful for looping a specific number of times.

```python
for i in range(5):
    print(i)  # Output: 0 1 2 3 4
```

- You can specify the start, stop, and step values in the `range()` function.

```python
for i in range(1, 10, 2):
    print(i)  # Output: 1 3 5 7 9
```

### Nested `for` Loops
- You can use nested `for` loops to iterate over multiple sequences.

```python
for i in range(3):
    for j in range(2):
        print(i, j)
```

### `for` Loop with `else`
- The `else` block in a `for` loop is executed when the loop has exhausted iterating over the sequence.

```python
for item in [1, 2, 3]:
    print(item)
else:
    print("Loop is done")
```

### `break` Statement
- The `break` statement is used to exit the loop prematurely when a certain condition is met.

```python
for item in [1, 2, 3, 4, 5]:
    if item == 3:
        break
    print(item)  # Output: 1 2
```

### `continue` Statement
- The `continue` statement is used to skip the current iteration and continue with the next iteration of the loop.

```python
for item in [1, 2, 3, 4, 5]:
    if item == 3:
        continue
    print(item)  # Output: 1 2 4 5
```

### List Comprehension with `for` Loop
- List comprehension provides a concise way to create lists using a `for` loop in a single line.

```python
my_list = [1, 2, 3, 4, 5]
squared_list = [x**2 for x in my_list]
print(squared_list)  # Output: [1, 4, 9, 16, 25]
```

### Examples

#### Basic `for` Loop
```python
my_list = [1, 2, 3, 4, 5]
for item in my_list:
    print(item)
```

#### Looping Through a String
```python
my_string = "hello"
for char in my_string:
    print(char)
```

#### Using `range()` Function
```python
for i in range(5):
    print(i)  # Output: 0 1 2 3 4
```

#### Nested `for` Loops
```python
for i in range(3):
    for j in range(2):
        print(i, j)
```

#### `for` Loop with `else`
```python
for item in [1, 2, 3]:
    print(item)
else:
    print("Loop is done")
```

#### `break` Statement
```python
for item in [1, 2, 3, 4, 5]:
    if item == 3:
        break
    print(item)  # Output: 1 2
```

#### `continue` Statement
```python
for item in [1, 2, 3, 4, 5]:
    if item == 3:
        continue
    print(item)  # Output: 1 2 4 5
