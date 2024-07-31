# Python `while` Loops

## Introduction to `while` Loops
A `while` loop in Python repeatedly executes a block of code as long as a given condition is true. It is useful for scenarios where the number of iterations is not known beforehand.

### Syntax
```python
while condition:
    # code block to be executed
```

### Flowchart
1. Evaluate the condition.
2. If the condition is `True`, execute the code block.
3. Repeat step 1.
4. If the condition is `False`, exit the loop.

## Basic Example
```python
count = 0
while count < 5:
    print(count)
    count += 1
# Output: 0 1 2 3 4
```

## Infinite Loop
A `while` loop can run indefinitely if the condition never becomes `False`.

```python
while True:
    print("This is an infinite loop")
    break  # Use break to exit the loop
```

## Using `break` Statement
The `break` statement can be used to exit the loop prematurely.

```python
count = 0
while count < 10:
    print(count)
    if count == 5:
        break
    count += 1
# Output: 0 1 2 3 4 5
```

## Using `continue` Statement
The `continue` statement skips the rest of the code inside the loop for the current iteration and moves to the next iteration.

```python
count = 0
while count < 10:
    count += 1
    if count % 2 == 0:
        continue
    print(count)
# Output: 1 3 5 7 9
```

## Using `else` with `while` Loop
An `else` block can be attached to a `while` loop. The `else` block is executed when the loop condition becomes `False`.

```python
count = 0
while count < 5:
    print(count)
    count += 1
else:
    print("Loop ended")
# Output: 0 1 2 3 4
#         Loop ended
```

## Nested `while` Loops
You can nest one `while` loop inside another `while` loop.

```python
outer_count = 0
while outer_count < 3:
    inner_count = 0
    while inner_count < 3:
        print(f"outer_count: {outer_count}, inner_count: {inner_count}")
        inner_count += 1
    outer_count += 1
# Output:
# outer_count: 0, inner_count: 0
# outer_count: 0, inner_count: 1
# outer_count: 0, inner_count: 2
# outer_count: 1, inner_count: 0
# outer_count: 1, inner_count: 1
# outer_count: 1, inner_count: 2
# outer_count: 2, inner_count: 0
# outer_count: 2, inner_count: 1
# outer_count: 2, inner_count: 2
```

## Common Pitfalls
### Infinite Loops
Ensure that the loop condition will eventually become `False` to avoid infinite loops.

```python
count = 0
while count < 5:
    print(count)
    # Missing count += 1 will cause an infinite loop
```

### Off-by-One Errors
Be careful with loop conditions to avoid off-by-one errors.

```python
count = 0
while count <= 5:  # This will print 0 to 5 inclusive
    print(count)
    count += 1
# Output: 0 1 2 3 4 5
```

## Practical Examples
### Example 1: Summing Numbers
```python
total = 0
number = 1
while number <= 10:
    total += number
    number += 1
print(total)  # Output: 55
```

### Example 2: User Input Validation
```python
while True:
    user_input = input("Enter a number (or 'q' to quit): ")
    if user_input.lower() == 'q':
        break
    elif user_input.isdigit():
        print(f"You entered: {user_input}")
    else:
        print("Invalid input, please enter a number.")
```

### Example 3: Factorial Calculation
```python
number = 5
factorial = 1
while number > 0:
    factorial *= number
    number -= 1
print(factorial)  # Output: 120