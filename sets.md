# Python Sets

## Introduction to Sets
- A set is an unordered collection of unique elements.
- Sets are defined using curly braces `{}` or the `set()` function.

```python
# Using curly braces
my_set = {1, 2, 3, 4, 5}

# Using the set() function
my_set = set([1, 2, 3, 4, 5])
```

## Adding Elements to a Set
- Use the `add()` method to add a single element to a set.

```python
my_set = {1, 2, 3}
my_set.add(4)
print(my_set)  # Output: {1, 2, 3, 4}
```

## Removing Elements from a Set
- Use the `remove()` method to remove a specific element. Raises a `KeyError` if the element is not found.
- Use the `discard()` method to remove a specific element. Does not raise an error if the element is not found.
- Use the `pop()` method to remove and return an arbitrary element from the set. Raises a `KeyError` if the set is empty.
- Use the `clear()` method to remove all elements from the set.

```python
my_set = {1, 2, 3, 4, 5}

# remove()
my_set.remove(3)
print(my_set)  # Output: {1, 2, 4, 5}

# discard()
my_set.discard(2)
print(my_set)  # Output: {1, 4, 5}

# pop()
element = my_set.pop()
print(element)  # Output: 1 (or any other element, as sets are unordered)
print(my_set)  # Output: {4, 5}

# clear()
my_set.clear()
print(my_set)  # Output: set()
```

## Checking Membership
- Use the `in` keyword to check if an element is in the set.

```python
my_set = {1, 2, 3, 4, 5}
print(3 in my_set)  # Output: True
print(6 in my_set)  # Output: False
```

## Set Operations
### Union
- Use the `union()` method or the `|` operator to combine two sets.

```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}
union_set = set1.union(set2)
print(union_set)  # Output: {1, 2, 3, 4, 5}

# Using the | operator
union_set = set1 | set2
print(union_set)  # Output: {1, 2, 3, 4, 5}
```

### Intersection
- Use the `intersection()` method or the `&` operator to find common elements.

```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}
intersection_set = set1.intersection(set2)
print(intersection_set)  # Output: {3}

# Using the & operator
intersection_set = set1 & set2
print(intersection_set)  # Output: {3}
```

### Difference
- Use the `difference()` method or the `-` operator to find elements in one set but not the other.

```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}
difference_set = set1.difference(set2)
print(difference_set)  # Output: {1, 2}

# Using the - operator
difference_set = set1 - set2
print(difference_set)  # Output: {1, 2}
```

### Symmetric Difference
- Use the `symmetric_difference()` method or the `^` operator to find elements in either set but not both.

```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}
symmetric_difference_set = set1.symmetric_difference(set2)
print(symmetric_difference_set)  # Output: {1, 2, 4, 5}

# Using the ^ operator
symmetric_difference_set = set1 ^ set2
print(symmetric_difference_set)  # Output: {1, 2, 4, 5}
```

## Set Comprehensions
- Similar to list comprehensions, set comprehensions allow for creating sets in a concise way.

```python
squared_set = {x**2 for x in range(1, 6)}
print(squared_set)  # Output: {1, 4, 9, 16, 25}
```

## Frozen Sets
- A frozenset is an immutable version of a set. Use the `frozenset()` function to create one.

```python
my_set = frozenset([1, 2, 3, 4, 5])
print(my_set)  # Output: frozenset({1, 2, 3, 4, 5})

# Attempting to add or remove elements will raise an AttributeError
# my_set.add(6)  # Raises AttributeError