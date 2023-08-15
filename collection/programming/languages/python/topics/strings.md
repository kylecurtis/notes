In Python, a string is a sequence of characters. It is a derived data type. Strings are immutable. This means that once defined, they cannot be changed. Strings can be defined using single, double, or triple quotes.

<br>

---

<br>

## String Examples

<br>

#### Single-Line Strings

```python
# Using double quotes
s1 = "Python"
print(s1)  # Python 

# Using single quotes
s2 = 'Python'
print(s2)  # Python 
```

<br>

#### Multi-Line Strings
```
multiline_str = """This is a
multiline string"""

print(multiline_str)
```

<br>

---

<br>

## Escape Sequences

| Sequence | Explanation | Syntax |
| :--- | :--- | :---: |
| Double quote | Adds double quote to string | `\"` |
| Single quote | Adds single quote to string | `\'` |
| Backslash | Adds backslash to string | `\\` | 
| New line | Adds a new line to string | `\n` |
| Tab | Adds a tab to string | `\t` | 
| Carriage return | Moves cursor to the beginning of the line | `\r` |

<br>

---

<br>

## String Concatenation

Strings in Python can be concatenated (joined) using the plus (+) operator:

```python
s1 = "Hello"
s2 = "World"
print(s1 + s2)  # HelloWorld
```

<br>

They can also be repeated using the star (*) operator:

```python
s = "Python"
print(s * 3)  # PythonPythonPython
```

<br>

---

<br>

## Formatted Strings

```python
first_name = "John"
last_name = "Smith"

# Formatted String
full_name = f"{first_name} {last_name}"

print(full_name) # "John Smith" 
```

<br>

Formatting can also contain methods and expressions:

```python
four = "four"

print(f"{2 + 2} is equal to {len(four)}!")

# 4 is equal to 4!
```

<br>

---

<br>

## String Slicing

String slicing is a way to extract a part of a string. It allows you to obtain a substring from the original string. To slice a string, you need to specify a starting index and an ending index, separated by a colon `:`. Python uses zero-based indexing, so the first character is at index `0`.

<br>

#### Basic Slicing

```python
s = "Python Programming"

# Get substring from index 0 to 5 (excluding 6)
print(s[0:6])  # Output: "Python"

# Get substring from index 7 to the end
print(s[7:])  # Output: "Programming"
```

<br>

#### Slicing Steps

You can also specify a step value, which determines the characters to skip.

```python
# Get every second character in the string
print(s[0:6:2])  # Output: "Pto"
```

<br>

#### Negative Index Slicing

Python allows negative indexing for its sequences. The index of `-1` represents the last character in the string.

```python
# Reverse a string using slicing
print(s[::-1])  # Output: "gnimmargorP nohtyP"

# Get last 4 characters of the string
print(s[-4:])  # Output: "ming"
```

<br>

---

<br>

## String Length

To get the length of a string in Python, you use the `len()` function:

```python
s = "Python"
print(len(s))  # Output: 6
```

<br>

---

<br>

## Checking String Membership

To check if a certain phrase or character is present in a string, you can use the `in` keyword:

```python
text = "Python is easy to learn."

# Check if 'easy' is present in the text
print('easy' in text)  # Output: True
```

<br>

---

<br>

## String Immutability

Strings in Python are immutable. This means that you can’t change an existing string, but you can create a new one with the desired changes (Adding another string to memory):

```python
s = "Python"
s = "J" + s[1:]
print(s)  # Output: "Jython"
```

<br>

---

<br>

## String Encoding and Decoding

Understanding how strings are encoded to bytes and decoded back to strings is crucial when you are working with files, network data, or other binary data sources. Python uses UTF-8 encoding by default.

```python
# Encoding a string
s = "Python"
encoded_s = s.encode('UTF-8')
print(encoded_s)  # Output: b'Python'

# Decoding back to string
decoded_s = encoded_s.decode('UTF-8')
print(decoded_s)  # Output: 'Python'
```

<br>

---

<br>

## Common String Methods

<br>

#### capitalize()

**args**: none

Converts the first character of the string to upper case and the rest to lower case.

```python
s = "hello WORLD"
print(s.capitalize())  # Hello world
```

<br>

#### casefold()

**args**: none

Converts string into lower case. This is more aggressive than the lower() method and may modify strings that are already in lower case or cause strings to grow in length, and is used for caseless matching, i.e. ignores cases when comparing.

```python
s = "der Fluß"
print(s.casefold())  # der fluss
```

<br>

#### center()

**args**: (`width` [`, fillchar`])

Returns a centered string of length `width`. Padding is done using the specified `fillchar` (default is a space). The original string is returned if `width` is less than or equal to len(s).

```python
s = "hello"
print(s.center(10, '*'))  # "**hello***"
```

<br>

#### count()

**args**: (`sub`[, `start`[, `end`]])

Returns the number of non-overlapping occurrences of substring `sub` in the range [`start`, `end`].

```python
s = "hello world"
print(s.count('o'))  # 2
```

<br>

#### encode()

**args**: ([`encoding="utf-8"`[, `errors="strict"`]])

Returns an encoded version of the string as a bytes object. Default encoding is 'utf-8'. `errors` may be given to set a different error handling scheme.

```python
s = "hello"
print(s.encode())  # b'hello'
```

<br>

#### endswith()

**args**: (`suffix`[, `start`[, `end`]])

Returns `True` if the string ends with the specified `suffix`, otherwise return `False`.

```python
s = "hello"
print(s.endswith("lo"))  # True
```

<br>

#### expandtabs()

**args**: ([`tabsize=8`])

Returns a string where all '\t' characters are replaced by one or more spaces, depending on the current column and the given tab size.

```python
s = "h\te\tl\tl\to"
print(s.expandtabs(2))  # 'h e l l o'
```

<br>

#### find()

**args**: (`sub`[, `start`[, `end`]])

Returns the lowest index in the string where substring `sub` is found within the slice `s[start:end]`. Returns -1 if `sub` is not found.

```python
s = "hello world"
print(s.find('o'))  # 4
```

<br>

#### format()

**args**: (`*args`, `**kwargs`)

Performs a string formatting operation. This method is very complex and allows you to use format codes.

```python
s = "Hello, {}"
print(s.format("world"))  # "Hello, world"
```

<br>

#### format_map()

**args**: (`mapping`)

Similar to `str.format(**mapping)`, but takes a `mapping` directly rather than via unpacking.

```python
s = "Hello, {name}"
print(s.format_map({"name": "world"}))  # "Hello, world"
```

<br>

#### index()

**args**: (`sub`[, `start`[, `end`]])

Like `find()`, but raises `ValueError` when the substring `sub` is not found.

```python
s = "hello world"
print(s.index('o'))  # 4
```

<br>

#### isalnum()

**args**: `()`

Returns `True` if all characters in the string are alphanumeric and there is at least one character, `False` otherwise.

```python
s = "hello123"
print(s.isalnum())  # True
```

<br>

#### isalpha()

**args**: `()`

Returns `True` if all characters in the string are alphabets and there is at least one character, `False` otherwise.

```python
s = "hello"
print(s.isalpha())  # True
```

<br>

#### isascii()

**args**: `()`

Returns `True` if the string is empty or all characters in the string are ASCII, `False` otherwise.

```python
s = "hello"
print(s.isascii())  # True
```

<br>

#### isdecimal()

**args**: `()`

Returns `True` if all characters in the string are decimals (0-9).

```python
s = "123"
print(s.isdecimal())  # True
```

<br>

#### isdigit()

**args**: `()`

Returns `True` if all characters in the string are digits (0-9).

```python
s = "123"
print(s.isdigit())  # True
```

<br>

#### isidentifier()

**args**: `()`

Returns `True` if the string is a valid identifier according to Python’s language definition.

```python
s = "hello_123"
print(s.isidentifier())  # True
```

<br>

#### islower()

**args**: `()`

Returns `True` if all cased characters in the string are lowercase and there is at least one cased character, `False` otherwise.

```python
s = "hello"
print(s.islower())  # True
```

<br>

#### isnumeric()

**args**: `()`

Returns `True` if all characters in the string are numeric characters, and there is at least one character.

```python
s = "123"
print(s.isnumeric())  # True
```

<br>

#### isprintable()

**args**: `()`

Returns `True` if all characters in the string are printable or the string is empty, `False` otherwise.

```python
s = "hello"
print(s.isprintable())  # True
```

<br>

#### isspace()

**args**: `()`

Returns `True` if there are only whitespace characters in the string and there is at least one character, `False` otherwise.

```python
s = "     "
print(s.isspace())  # True
```

<br>

#### istitle()

**args**: `()`

Returns `True` if the string is a titlecased string and there is at least one character, i.e., uppercase characters may only follow uncased characters and lowercase characters only cased ones.

```python
s = "Hello World"
print(s.istitle())  # True
```

<br>

#### isupper()

**args**: `()`

Returns `True` if all cased characters in the string are uppercase and there is at least one cased character, `False` otherwise.

```python
s = "HELLO"
print(s.isupper())  # True
```

<br>

#### join()

**args**: (`iterable`)

Concatenates any number of strings contained in an iterable (such as a list or a tuple). The string on which `join()` is called is used as a separator.

```python
s = " "
seq = ("hello", "world")
print(s.join(seq))  # "hello world"
```

<br>

#### ljust()

**args**: (`width`[, `fillchar`])

Returns the string left justified in a string of length `width`. Padding is done using the specified `fillchar` (default is a space). The original string is returned if `width` is less than `len(s)`.

```python
s = "hello"
print(s.ljust(10, '*'))  # "hello*****"
```

<br>

#### lower()

**args**: `()`

Returns a copy of the string with all the cased characters converted to lowercase.

```python
s = "HELLO"
print(s.lower())  # "hello"
```

<br>

#### lstrip()

**args**: ([`chars`])

Returns a copy of the string with leading characters removed. The `chars` argument is a string specifying the set of characters to be removed. If omitted or `None`, the chars argument defaults to removing whitespace.

```python
s = "   hello"
print(s.lstrip())  # "hello"
```

<br>

#### maketrans()

**args**: (`x`[, `y`[, `z`]])

This static method returns a translation table usable for `str.translate()`.

```python
intab = "aeiou"
outtab = "12345"
trantab = str.maketrans(intab, outtab)
s = "hello"
print(s.translate(trantab))  # "h2ll4"
```

<br>

#### partition()

**args**: (`sep`)

Splits the string at the first occurrence of the separator `sep`, and returns a 3-tuple containing the part before the separator, the separator itself, and the part after the separator.

```python
s = "hello world"
print(s.partition(" "))  # ("hello", " ", "world")
```

<br>

#### replace()

**args**: (`old`, `new`[, `count`])

Returns a copy of the string with all occurrences of substring `old` replaced by `new`. If the optional argument `count` is given, only the first `count` occurrences are replaced.

```python
s = "hello world"
print(s.replace("world", "python"))  # "hello python"
```

<br>

#### rfind()

**args**: (`sub`[, `start`[, `end`]])

Returns the highest index in the string where substring `sub` is found within the slice `s[start:end]`. Returns -1 on failure.

<br>

```python
s = "hello world"
print(s.rfind('o'))  # 7
```

<br>

#### rindex()

**args**: (`sub`[, `start`[, `end`]])

Like `rfind()`, but raises `ValueError` when the substring `sub` is not found.

```python
s = "hello world"
print(s.rindex('o'))  # 7
```

<br>

#### rjust()

**args**: (`width`[, `fillchar`])

Returns the string right justified in a string of length `width`. Padding is done using the specified `fillchar` (default is a space). The original string is returned if `width` is less than `len(s)`.

```python
s = "hello"
print(s.rjust(10, '*'))  # "*****hello"
```

<br>

#### rpartition()

**args**: (`sep`)

Splits the string at the last occurrence of the separator `sep`, and returns a 3-tuple containing the part before the separator, the separator itself, and the part after the separator.

```python
s = "hello world"
print(s.rpartition(" "))  # ("hello", " ", "world")
```

<br>

#### rsplit()

**args**: ([`sep`[, `maxsplit`]])

Returns a list of the words in the string, using `sep` as the delimiter string. If `maxsplit` is given, at most `maxsplit` splits are done, the rightmost ones.

```python
s = "hello world"
print(s.rsplit(" "))  # ['hello', 'world']
```

<br>

#### rstrip()

**args**: ([`chars`])

Returns a copy of the string with trailing characters removed. The `chars` argument is a string specifying the set of characters to be removed. If omitted or `None`, the `chars` argument defaults to removing whitespace.

```python
s = "hello   "
print(s.rstrip())  # "hello"
```

<br>

#### split()

**args**: ([`sep`[, `maxsplit`]])

Returns a list of the words in the string, using `sep` as the delimiter string. If `maxsplit` is given, at most `maxsplit` splits are done.

```python
s = "hello world"
print(s.split(" "))  # ['hello', 'world']
```

<br>

#### splitlines()

**args**: ([`keepends`])

Returns a list of the lines in the string, breaking at line boundaries. This method uses the universal newline support. Line breaks are not included in the resulting list unless `keepends` is given and true.

```python
s = "hello\nworld"
print(s.splitlines())  # ['hello', 'world']
```

<br>

#### startswith()

**args**: (`prefix`[, `start`[, `end`]])

Returns `True` if string starts with the `prefix`, otherwise returns `False`.

```python
s = "hello"
print(s.startswith("he"))  # True
```

<br>

#### strip()

**args**: ([`chars`])

Returns a copy of the string with the leading and trailing characters removed. The `chars` argument is a string specifying the set of characters to be removed. If omitted or `None`, the `chars` argument defaults to removing whitespace.

```python
s = "   hello   "
print(s.strip())  # "hello"
```

<br>

#### swapcase()

**args**: `()`

Returns a copy of the string with uppercase characters converted to lowercase and vice versa.

```python
s = "Hello World"
print(s.swapcase())  # "hELLO wORLD"
```

<br>

#### title()

**args**: none

Returns a copy of the string in which the first characters of all the words are capitalized.

```python
s = "hello world"
print(s.title())  # "Hello World"
```

<br>

#### translate()

**args**: (`table`)

Returns a copy of the string in which each character has been mapped through the given translation table (which must be created with `maketrans()`).

```python
intab = "aeiou"
outtab = "12345"
trantab = str.maketrans(intab, outtab)
s = "hello"
print(s.translate(trantab))  # "h2ll4"
```

<br>

#### upper()

**args**: `()`

Returns a copy of the string with all the cased characters converted to uppercase.

```python
s = "hello"
print(s.upper())  # "HELLO"
```

<br>

#### zfill()

**args**: (`width`)

Returns a copy of the string left filled with zeros in a string of length `width`. A sign prefix is handled correctly.

```python
s = "123"
print(s.zfill(5))  # "00123"
```