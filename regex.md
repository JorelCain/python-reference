# Python Regular Expressions (Regex)

## Introduction to Regular Expressions
Regular expressions (regex) are sequences of characters that form search patterns. They are used for string matching and manipulation. Python provides the `re` module to work with regular expressions.

### Importing the `re` Module
```python
import re
```

## Basic Functions
### `re.search()`
Searches for the first occurrence of the pattern in the string.

```python
import re

pattern = r"hello"
string = "hello world"
match = re.search(pattern, string)
if match:
    print("Match found:", match.group())
else:
    print("No match")
# Output: Match found: hello
```

### `re.match()`
Checks for a match only at the beginning of the string.

```python
import re

pattern = r"hello"
string = "hello world"
match = re.match(pattern, string)
if match:
    print("Match found:", match.group())
else:
    print("No match")
# Output: Match found: hello
```

### `re.findall()`
Finds all occurrences of the pattern in the string and returns them as a list.

```python
import re

pattern = r"hello"
string = "hello hello world"
matches = re.findall(pattern, string)
print("Matches found:", matches)
# Output: Matches found: ['hello', 'hello']
```

### `re.sub()`
Replaces occurrences of the pattern in the string with a replacement string.

```python
import re

pattern = r"hello"
replacement = "hi"
string = "hello world"
new_string = re.sub(pattern, replacement, string)
print("New string:", new_string)
# Output: New string: hi world
```

### `re.split()`
Splits the string by occurrences of the pattern.

```python
import re

pattern = r"\s+"
string = "hello world"
split_string = re.split(pattern, string)
print("Split string:", split_string)
# Output: Split string: ['hello', 'world']
```

## Special Characters
### Metacharacters
Metacharacters are characters that have a special meaning in a regex pattern.

- `.` (Dot): Matches any single character except a newline (`\n`).
- `^` (Caret): Matches the start of the string.
- `$` (Dollar): Matches the end of the string.
- `*` (Asterisk): Matches 0 or more repetitions of the preceding element.
- `+` (Plus): Matches 1 or more repetitions of the preceding element.
- `?` (Question Mark): Matches 0 or 1 repetition of the preceding element.
- `{n}` (Braces): Matches exactly `n` repetitions of the preceding element.
- `{n,}` (Braces with Comma): Matches `n` or more repetitions of the preceding element.
- `{n,m}` (Braces with Range): Matches between `n` and `m` repetitions of the preceding element.
- `[]` (Square Brackets): Matches any one of the characters inside the brackets.
- `|` (Pipe): Matches either the pattern before or the pattern after the `|`.
- `()` (Parentheses): Groups patterns and captures the matched sub-pattern.

### Examples
```python
import re

# . (Dot)
# Matches any single character except a newline.
pattern = r"h.llo"
string = "hello"
match = re.search(pattern, string)
print("Match found:", match.group())
# Output: Match found: hello

# ^ (Caret)
# Matches the start of the string.
pattern = r"^hello"
string = "hello world"
match = re.search(pattern, string)
print("Match found:", match.group())
# Output: Match found: hello

# $ (Dollar)
# Matches the end of the string.
pattern = r"world$"
string = "hello world"
match = re.search(pattern, string)
print("Match found:", match.group())
# Output: Match found: world

# * (Asterisk)
# Matches 0 or more repetitions of the preceding element.
pattern = r"ab*"
string = "a ab abb abbb"
matches = re.findall(pattern, string)
print("Matches found:", matches)
# Output: Matches found: ['a', 'ab', 'abb', 'abbb']

# + (Plus)
# Matches 1 or more repetitions of the preceding element.
pattern = r"ab+"
string = "a ab abb abbb"
matches = re.findall(pattern, string)
print("Matches found:", matches)
# Output: Matches found: ['ab', 'abb', 'abbb']

# ? (Question Mark)
# Matches 0 or 1 repetition of the preceding element.
pattern = r"ab?"
string = "a ab abb abbb"
matches = re.findall(pattern, string)
print("Matches found:", matches)
# Output: Matches found: ['a', 'ab', 'ab', 'ab']

# {n} (Braces)
# Matches exactly n repetitions of the preceding element.
pattern = r"ab{2}"
string = "a ab abb abbb"
matches = re.findall(pattern, string)
print("Matches found:", matches)
# Output: Matches found: ['abb']

# {n,} (Braces with Comma)
# Matches n or more repetitions of the preceding element.
pattern = r"ab{2,}"
string = "a ab abb abbb"
matches = re.findall(pattern, string)
print("Matches found:", matches)
# Output: Matches found: ['abb', 'abbb']

# {n,m} (Braces with Range)
# Matches between n and m repetitions of the preceding element.
pattern = r"ab{1,2}"
string = "a ab abb abbb"
matches = re.findall(pattern, string)
print("Matches found:", matches)
# Output: Matches found: ['ab', 'abb']

# [] (Square Brackets)
# Matches any one of the characters inside the brackets.
pattern = r"[aeiou]"
string = "hello world"
matches = re.findall(pattern, string)
print("Matches found:", matches)
# Output: Matches found: ['e', 'o', 'o']

# | (Pipe)
# Matches either the pattern before or the pattern after the |.
pattern = r"cat|dog"
string = "I have a cat and a dog."
matches = re.findall(pattern, string)
print("Matches found:", matches)
# Output: Matches found: ['cat', 'dog']

# () (Parentheses)
# Groups patterns and captures the matched sub-pattern.
pattern = r"(ab)+"
string = "ababab"
match = re.search(pattern, string)
print("Match found:", match.group())
# Output: Match found: ababab
```

### Additional Examples
```python
import re

# . (Dot)
# Matches any single character except a newline.
pattern = r"a.b"
string = "aab acb adb aeb"
matches = re.findall(pattern, string)
print("Matches found:", matches)
# Output: Matches found: ['aab', 'acb', 'adb', 'aeb']

# ^ (Caret)
# Matches the start of the string.
pattern = r"^The"
string = "The quick brown fox"
match = re.search(pattern, string)
print("Match found:", match.group())
# Output: Match found: The

# $ (Dollar)
# Matches the end of the string.
pattern = r"fox$"
string = "The quick brown fox"
match = re.search(pattern, string)
print("Match found:", match.group())
# Output: Match found: fox

# * (Asterisk)
# Matches 0 or more repetitions of the preceding element.
pattern = r"ba*"
string = "b ba baa baaa"
matches = re.findall(pattern, string)
print("Matches found:", matches)
# Output: Matches found: ['b', 'ba', 'baa', 'baaa']

# + (Plus)
# Matches 1 or more repetitions of the preceding element.
pattern = r"ba+"
string = "b ba baa baaa"
matches = re.findall(pattern, string)
print("Matches found:", matches)
# Output: Matches found: ['ba', 'baa', 'baaa']

# ? (Question Mark)
# Matches 0 or 1 repetition of the preceding element.
pattern = r"ba?"
string = "b ba baa baaa"
matches = re.findall(pattern, string)
print("Matches found:", matches)
# Output: Matches found: ['b', 'ba', 'ba', 'ba']

# {n} (Braces)
# Matches exactly n repetitions of the preceding element.
pattern = r"a{2}"
string = "a aa aaa aaaa"
matches = re.findall(pattern, string)
print("Matches found:", matches)
# Output: Matches found: ['aa', 'aa', 'aa']

# {n,} (Braces with Comma)
# Matches n or more repetitions of the preceding element.
pattern = r"a{2,}"
string = "a aa aaa aaaa"
matches = re.findall(pattern, string)
print("Matches found:", matches)
# Output: Matches found: ['aa', 'aaa', 'aaaa']

# {n,m} (Braces with Range)
# Matches between n and m repetitions of the preceding element.
pattern = r"a{2,3}"
string = "a aa aaa aaaa"
matches = re.findall(pattern, string)
print("Matches found:", matches)
# Output: Matches found: ['aa', 'aaa', 'aaa']

# [] (Square Brackets)
# Matches any one of the characters inside the brackets.
pattern = r"[abc]"
string = "a b c d e f"
matches = re.findall(pattern, string)
print("Matches found:", matches)
# Output: Matches found: ['a', 'b', 'c']

# | (Pipe)
# Matches either the pattern before or the pattern after the |.
pattern = r"apple|orange"
string = "I like apple and orange."
matches = re.findall(pattern, string)
print("Matches found:", matches)
# Output: Matches found: ['apple', 'orange']

# () (Parentheses)
# Groups patterns and captures the matched sub-pattern.
pattern = r"(abc)+"
string = "abc abcabc abcabcabc"
matches = re.findall(pattern, string)
print("Matches found:", matches)
# Output: Matches found: ['abc', 'abc', 'abc']