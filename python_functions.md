### Python Functions

## Functions
### What is a Function?
- **Function**: A block of reusable code that performs a specific task. Functions help in organizing code, making it more readable and reusable.

### Defining a Function
- Use the `def` keyword to define a function.

```python
def function_name(parameters):
    # code block
    return value
```

### Calling a Function
- Call a function by using its name followed by parentheses.

```python
function_name(arguments)
```

### Example of a Simple Function
- A function that prints "Hello, World!".

```python
def greet():
    print("Hello, World!")

greet()  # Output: Hello, World!
```

### Function with Parameters
- Functions can take parameters to process data.

```python
def greet(name):
    print(f"Hello, {name}!")

greet("Alice")  # Output: Hello, Alice!
```

### Function with Return Value
- Functions can return a value using the `return` statement.

```python
def add(a, b):
    return a + b

result = add(3, 4)
print(result)  # Output: 7
```

### Default Parameters
- Functions can have default parameter values.

```python
def greet(name="World"):
    print(f"Hello, {name}!")

greet()         # Output: Hello, World!
greet("Alice")  # Output: Hello, Alice!
```

### Keyword Arguments
- You can call functions using keyword arguments.

```python
def greet(name, message):
    print(f"{message}, {name}!")

greet(name="Alice", message="Good morning")  # Output: Good morning, Alice!
```

### Variable-Length Arguments
- Use `*args` for variable-length positional arguments and `**kwargs` for variable-length keyword arguments.

```python
def print_numbers(*args):
    for number in args:
        print(number)

print_numbers(1, 2, 3)  # Output: 1 2 3

def print_info(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

print_info(name="Alice", age=30)  # Output: name: Alice age: 30
```

### Lambda Functions
- Lambda functions are small anonymous functions defined using the `lambda` keyword.

```python
add = lambda x, y: x + y
print(add(2, 3))  # Output: 5
```

### Nested Functions
- Functions can be nested within other functions.

```python
def outer_function():
    def inner_function():
        print("Hello from inner function")
    inner_function()

outer_function()  # Output: Hello from inner function
```

### Higher-Order Functions
- Functions that take other functions as arguments or return them as results.

```python
def apply_function(func, value):
    return func(value)

def square(x):
    return x * x

result = apply_function(square, 5)
print(result)  # Output: 25
```

### Examples

#### Simple Function
```python
def greet():
    print("Hello, World!")

greet()  # Output: Hello, World!
```

#### Function with Parameters
```python
def greet(name):
    print(f"Hello, {name}!")

greet("Alice")  # Output: Hello, Alice!
```

#### Function with Return Value
```python
def add(a, b):
    return a + b

result = add(3, 4)
print(result)  # Output: 7
```

#### Default Parameters
```python
def greet(name="World"):
    print(f"Hello, {name}!")

greet()         # Output: Hello, World!
greet("Alice")  # Output: Hello, Alice!
```

#### Keyword Arguments
```python
def greet(name, message):
    print(f"{message}, {name}!")

greet(name="Alice", message="Good morning")  # Output: Good morning, Alice!
```

#### Variable-Length Arguments
```python
def print_numbers(*args):
    for number in args:
        print(number)

print_numbers(1, 2, 3)  # Output: 1 2 3

def print_info(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

print_info(name="Alice", age=30)  # Output: name: Alice age: 30
```

#### Lambda Functions
```python
add = lambda x, y: x + y
print(add(2, 3))  # Output: 5
```

#### Nested Functions
```python
def outer_function():
    def inner_function():
        print("Hello from inner function")
    inner_function()

outer_function()  # Output: Hello from inner function
```

#### Higher-Order Functions
```python
def apply_function(func, value):
    return func(value)

def square(x):
    return x * x

result = apply_function(square, 5)
print(result)  # Output: 25