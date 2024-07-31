### Python Lists

## Lists
### What is a List?
- **List**: A collection of items that are ordered and changeable. Allows duplicate members.

### Creating a List
- Lists are created using square brackets `[]`.

```python
my_list = [1, 2, 3, 4, 5]
```

### Accessing List Items
- List items are accessed by their index. The first item has index `0`.

```python
my_list = [1, 2, 3, 4, 5]
print(my_list[0])  # Output: 1
```

### Negative Indexing
- Negative indexing means starting from the end, `-1` refers to the last item.

```python
my_list = [1, 2, 3, 4, 5]
print(my_list[-1])  # Output: 5
```

### Slicing a List
- You can return a range of items by specifying the start and end index.

```python
my_list = [1, 2, 3, 4, 5]
print(my_list[1:3])  # Output: [2, 3]
```

### Changing List Items
- You can change the value of a specific item by referring to its index.

```python
my_list = [1, 2, 3, 4, 5]
my_list[1] = 10
print(my_list)  # Output: [1, 10, 3, 4, 5]
```

### Looping Through a List
- You can loop through the list items by using a `for` loop.

```python
my_list = [1, 2, 3, 4, 5]
for item in my_list:
    print(item)
```

### Checking if Item Exists
- Use the `in` keyword to check if an item exists in the list.

```python
my_list = [1, 2, 3, 4, 5]
if 3 in my_list:
    print("3 is in the list")
```

### List Length
- Use the `len()` function to return the number of items in a list.

```python
my_list = [1, 2, 3, 4, 5]
print(len(my_list))  # Output: 5
```

### Adding Items to a List
- Use the `append()` method to add an item to the end of the list.

```python
my_list = [1, 2, 3, 4, 5]
my_list.append(6)
print(my_list)  # Output: [1, 2, 3, 4, 5, 6]
```

- Use the `insert()` method to add an item at a specified index.

```python
my_list = [1, 2, 3, 4, 5]
my_list.insert(1, 10)
print(my_list)  # Output: [1, 10, 2, 3, 4, 5]
```

### Removing Items from a List
- Use the `remove()` method to remove a specified item.

```python
my_list = [1, 2, 3, 4, 5]
my_list.remove(3)
print(my_list)  # Output: [1, 2, 4, 5]
```

- Use the `pop()` method to remove an item at a specified index (or the last item if index is not specified).

```python
my_list = [1, 2, 3, 4, 5]
my_list.pop(1)
print(my_list)  # Output: [1, 3, 4, 5]

my_list.pop()
print(my_list)  # Output: [1, 3, 4]
```

- Use the `clear()` method to remove all items from the list.

```python
my_list = [1, 2, 3, 4, 5]
my_list.clear()
print(my_list)  # Output: []
```

### List Comprehension
- List comprehension offers a shorter syntax to create a new list based on the values of an existing list.

```python
my_list = [1, 2, 3, 4, 5]
new_list = [x * 2 for x in my_list]
print(new_list)  # Output: [2, 4, 6, 8, 10]
```

### Sorting a List
- Use the `sort()` method to sort the list in ascending order.

```python
my_list = [5, 2, 3, 1, 4]
my_list.sort()
print(my_list)  # Output: [1, 2, 3, 4, 5]
```

- Use the `sort(reverse=True)` method to sort the list in descending order.

```python
my_list = [5, 2, 3, 1, 4]
my_list.sort(reverse=True)
print(my_list)  # Output: [5, 4, 3, 2, 1]
```

### Copying a List
- Use the `copy()` method to make a copy of a list.

```python
my_list = [1, 2, 3, 4, 5]
new_list = my_list.copy()
print(new_list)  # Output: [1, 2, 3, 4, 5]
```

### Joining Lists
- Use the `+` operator to join two lists.

```python
list1 = [1, 2, 3]
list2 = [4, 5, 6]
joined_list = list1 + list2
print(joined_list)  # Output: [1, 2, 3, 4, 5, 6]
