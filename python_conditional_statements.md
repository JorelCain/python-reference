### Python Conditional Statements

## Conditional Statements
### What is a Conditional Statement?
- **Conditional Statement**: A statement that allows you to execute certain pieces of code based on whether a condition is true or false.

### `if` Statement
- The `if` statement is used to test a specific condition. If the condition is true, the code block under the `if` statement is executed.

```python
if condition:
    # code block to be executed if condition is true
```

### `else` Statement
- The `else` statement is used to execute a code block if the condition in the `if` statement is false.

```python
if condition:
    # code block to be executed if condition is true
else:
    # code block to be executed if condition is false
```

### `elif` Statement
- The `elif` statement stands for "else if" and is used to check multiple conditions.

```python
if condition1:
    # code block to be executed if condition1 is true
elif condition2:
    # code block to be executed if condition2 is true
else:
    # code block to be executed if none of the conditions are true
```

### Nested `if` Statements
- You can nest `if` statements inside other `if` statements to create more complex conditions.

```python
if condition1:
    if condition2:
        # code block to be executed if both condition1 and condition2 are true
```

### `if` Statements with Logical Operators
- Logical operators such as [`and`](command:_github.copilot.openSymbolFromReferences?%5B%7B%22%24mid%22%3A1%2C%22path%22%3A%22%2Fc%3A%2FUsers%2FJ%2FDocuments%2FPython%20Resources%2FMD%20Files%2Fpython_variables_datatypes.md%22%2C%22scheme%22%3A%22file%22%7D%2C%7B%22line%22%3A0%2C%22character%22%3A0%7D%5D "python_variables_datatypes.md"), `or`, and `not` can be used to combine multiple conditions.

```python
if condition1 and condition2:
    # code block to be executed if both condition1 and condition2 are true

if condition1 or condition2:
    # code block to be executed if either condition1 or condition2 is true

if not condition:
    # code block to be executed if condition is false
```

### Conditional Expressions (Ternary Operator)
- Python supports conditional expressions, which allow you to write `if`-`else` statements in a single line.

```python
x = value_if_true if condition else value_if_false
```

### Examples

#### Basic `if` Statement
```python
x = 10
if x > 5:
    print("x is greater than 5")
```

#### `if`-`else` Statement
```python
x = 10
if x > 15:
    print("x is greater than 15")
else:
    print("x is not greater than 15")
```

#### `if`-`elif`-`else` Statement
```python
x = 10
if x > 15:
    print("x is greater than 15")
elif x > 5:
    print("x is greater than 5 but not greater than 15")
else:
    print("x is 5 or less")
```

#### Nested `if` Statements
```python
x = 10
y = 20
if x > 5:
    if y > 15:
        print("x is greater than 5 and y is greater than 15")
```

#### Using Logical Operators
```python
x = 10
y = 20
if x > 5 and y > 15:
    print("x is greater than 5 and y is greater than 15")

if x > 15 or y > 15:
    print("Either x or y is greater than 15")

if not x > 15:
    print("x is not greater than 15")
```

#### Conditional Expression
```python
x = 10
result = "x is greater than 5" if x > 5 else "x is 5 or less"
print(result)
```