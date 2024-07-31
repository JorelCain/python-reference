### Python Strings

## Strings
### What is a String?
- **String**: A sequence of characters enclosed in single quotes (`'`), double quotes (`"`), or triple quotes (`'''` or `"""`).

### Creating Strings
- Strings can be created using single, double, or triple quotes.

```python
single_quote_str = 'Hello'
double_quote_str = "World"
triple_quote_str = '''Hello
World'''
```

### Accessing Characters
- Use indexing to access individual characters in a string.

```python
my_string = "Hello"
print(my_string[0])  # Output: H
print(my_string[-1])  # Output: o
```

### Slicing Strings
- Use slicing to get a substring.

```python
my_string = "Hello, World"
print(my_string[0:5])  # Output: Hello
print(my_string[7:])  # Output: World
print(my_string[:5])  # Output: Hello
print(my_string[::2])  # Output: Hlo ol
```

### String Length
- Use the `len()` function to get the length of a string.

```python
my_string = "Hello"
print(len(my_string))  # Output: 5
```

### String Concatenation
- Use the `+` operator to concatenate strings.

```python
str1 = "Hello"
str2 = "World"
result = str1 + " " + str2
print(result)  # Output: Hello World
```

### String Repetition
- Use the `*` operator to repeat strings.

```python
my_string = "Hello"
print(my_string * 3)  # Output: HelloHelloHello
```

### String Methods
- Strings have many built-in methods for various operations.

#### `upper()`
- Converts all characters to uppercase.

```python
my_string = "hello"
print(my_string.upper())  # Output: HELLO
```

#### `lower()`
- Converts all characters to lowercase.

```python
my_string = "HELLO"
print(my_string.lower())  # Output: hello
```

#### `strip()`
- Removes leading and trailing whitespace.

```python
my_string = "  hello  "
print(my_string.strip())  # Output: hello
```

#### `replace()`
- Replaces a substring with another substring.

```python
my_string = "Hello, World"
print(my_string.replace("World", "Python"))  # Output: Hello, Python
```

#### `split()`
- Splits the string into a list of substrings.

```python
my_string = "Hello, World"
print(my_string.split(","))  # Output: ['Hello', ' World']
```

#### `join()`
- Joins a list of strings into a single string.

```python
my_list = ["Hello", "World"]
print(" ".join(my_list))  # Output: Hello World
```

### String Formatting
- Use formatted string literals (f-strings) for string interpolation.

```python
name = "Alice"
age = 30
print(f"My name is {name} and I am {age} years old.")  # Output: My name is Alice and I am 30 years old.
```

### Checking Substrings
- Use the `in` keyword to check if a substring exists within a string.

```python
my_string = "Hello, World"
print("World" in my_string)  # Output: True
print("Python" in my_string)  # Output: False
```

### Examples

#### Creating Strings
```python
single_quote_str = 'Hello'
double_quote_str = "World"
triple_quote_str = '''Hello
World'''
```

#### Accessing Characters
```python
my_string = "Hello"
print(my_string[0])  # Output: H
print(my_string[-1])  # Output: o
```

#### Slicing Strings
```python
my_string = "Hello, World"
print(my_string[0:5])  # Output: Hello
print(my_string[7:])  # Output: World
print(my_string[:5])  # Output: Hello
print(my_string[::2])  # Output: Hlo ol
```

#### String Length
```python
my_string = "Hello"
print(len(my_string))  # Output: 5
```

#### String Concatenation
```python
str1 = "Hello"
str2 = "World"
result = str1 + " " + str2
print(result)  # Output: Hello World
```

#### String Repetition
```python
my_string = "Hello"
print(my_string * 3)  # Output: HelloHelloHello
```

#### String Methods
```python
my_string = "hello"
print(my_string.upper())  # Output: HELLO

my_string = "HELLO"
print(my_string.lower())  # Output: hello

my_string = "  hello  "
print(my_string.strip())  # Output: hello

my_string = "Hello, World"
print(my_string.replace("World", "Python"))  # Output: Hello, Python

my_string = "Hello, World"
print(my_string.split(","))  # Output: ['Hello', ' World']

my_list = ["Hello", "World"]
print(" ".join(my_list))  # Output: Hello World
```

#### String Formatting
```python
name = "Alice"
age = 30
print(f"My name is {name} and I am {age} years old.")  # Output: My name is Alice and I am 30 years old.
```

#### Checking Substrings
```python
my_string = "Hello, World"
print("World" in my_string)  # Output: True
print("Python" in my_string)  # Output: False