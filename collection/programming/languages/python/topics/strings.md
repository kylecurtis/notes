
<br>

---

<br>

In Python, a string is a sequence of characters. It is a derived data type. Strings are immutable, which means once defined, they cannot be changed. Strings can be defined using single, double, or triple quotes.

<br>

---

<br>

## **String Examples**

<br>

#### **Single-Line Strings**

```python
# Using double quotes
s1 = "Python"
print(s1)  # Python 

# Using single quotes
s2 = 'Python'
print(s2)  # Python 
```

<br>

#### **Multi-Line Strings**

You can use both triple double quotes and triple single quotes for multi-line strings.

```python
multiline_str = """This is a
multiline string using triple double quotes"""

print(multiline_str)

multiline_str_2 = '''This is also a
multiline string but using triple single quotes'''

print(multiline_str_2)
```

<br>

---

<br>

## **Escape Sequences**

| Sequence | Explanation | Syntax |
| :--- | :--- | :---: |
| Double quote | Adds double quote to string | `\"` |
| Single quote | Adds single quote to string | `\'` |
| Backslash | Adds backslash to string | `\\` | 
| New line | Adds a new line to string | `\n` |
| Tab | Adds a tab to string | `\t` | 
| Carriage return | Moves cursor to the beginning of the line | `\r` |
| Backspace | Removes the character before the sequence | `\b` |
| Form feed | Advances to the next "page" or "form" | `\f` |

<br>

---

<br>

## **String Concatenation**

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

## **Formatted Strings**

Formatted strings provide a concise way to embed expressions inside string literals.

```python
first_name = "John"
last_name = "Smith"

# Formatted String
full_name = f"{first_name} {last_name}"
print(full_name)  # John Smith
```

<br>

Formatting can also contain methods and expressions:

```python
four = "four"
print(f"{2 + 2} is equal to {len(four)}!")  # 4 is equal to 4!
```

Note: There are older formatting methods like `.format()` and `%` formatting which can be found in older Python code.

<br>

---

<br>

## **String Slicing**

String slicing is a way to extract a part of a string, allowing you to obtain a substring from the original string. To slice a string, you need to specify a starting index and an ending index, separated by a colon `:`. Python uses zero-based indexing, so the first character is at index `0`.

<br>

#### **Basic Slicing**

```python
s = "Python Programming"

# Get substring from index 0 to 5 (excluding 6)
print(s[0:6])  # Python

# Get substring from index 7 to the end
print(s[7:])  # Programming

# Default behavior
print(s[:])  # Python Programming
```

<br>

#### **Slicing Steps**

You can also specify a step value, which determines the characters to skip.

```python
# Get every second character in the string
print(s[0:6:2])  # Pto
```

<br>

#### **Negative Index Slicing**

Python allows negative indexing for its sequences. The index `-1` represents the last character, `-2` is the second last, and so on.

```python
# Reverse a string using slicing
print(s[::-1])  # gnimmargorP nohtyP

# Get last 4 characters of the string
print(s[-4:])  # ming
```

<br>

---

<br>

## **String Length**

To get the length of a string in Python, you use the `len()` function:

```python
s = "Python"
print(len(s))  # 6
```

<br>

---

<br>

## **Checking String Membership**

To check if a certain phrase or character is present in a string, you can use the `in` keyword:

```python
text = "Python is easy to learn."
print('easy' in text)  # True
```

<br>

---

<br>

## **String Immutability**

Strings in Python are immutable. This means that you can't change an existing string. Instead, operations that manipulate strings return new string objects. This property has performance and memory implications, especially in scenarios where many manipulations are done.

```python
s = "Python"
s = "J" + s[1:]
print(s)  # Jython
```

<br>

---

<br>

## **String Encoding and Decoding**

Understanding how strings are encoded to bytes and decoded back to strings is crucial when you are working with files, network data, or other binary data sources. This is especially relevant when handling non-ASCII characters in strings. Python uses UTF-8 encoding by default.

```python
# Encoding a string
s = "Python"
encoded_s = s.encode('UTF-8')
print(encoded_s)  # b'Python'

# Decoding back to string
decoded_s = encoded_s.decode('UTF-8')
print(decoded_s)  # Python
```

<br>

---

<br>


## Common String Methods

<br>

---

<br>

#### capitalize()

**args**: `None`

Returns a copy of the original string with its first character capitalized and the rest of the characters in lowercase.

```python
text = "hello world"
print(text.capitalize())  # "Hello world"
```

<br>

#### casefold()

**args**: `None`

Returns a case-folded version of the string which is suitable for case-insensitive comparisons.

```python
text = "HELLO World"
print(text.casefold())  # "hello world"
```

<br>

#### center()

**args**: (`width`, [`fillchar`])

Returns the string centered in a field of specified width. The padding is done using the specified `fillchar` (default is a space).

```python
text = "hello"
print(text.center(20, '-'))  # "-------hello--------"
```

<br>

#### count()

**args**: (`sub`[, `start`[, `end`]])

Returns the number of non-overlapping occurrences of substring `sub` in the range `[start, end]`.

```python
text = "banana"
print(text.count("a"))  # 3
```

<br>

#### encode()

**args**: ([`encoding`[, `errors`]])

Returns an encoded version of the string using the specified encoding (default is 'utf-8').

```python
text = "hello"
print(text.encode('utf-8'))  # b'hello'
```

<br>

#### endswith()

**args**: (`suffix`[, `start`[, `end`]])

Returns `True` if the string ends with the specified `suffix`, otherwise returns `False`. Optionally, the starting and ending positions can be specified.

```python
text = "tutorial.txt"
print(text.endswith(".txt"))  # True
```

<br>

#### expandtabs()

**args**: ([`tabsize`=8])

Returns a copy of the string where all tab characters `\t` are replaced by the appropriate number of spaces, depending on the current column and the given tab size.

```python
text = "hello\tworld"
print(text.expandtabs(4))  # "hello   world"
```

<br>

#### find()

**args**: (`sub`[, `start`[, `end`]])

Returns the lowest index of the substring `sub` if found, otherwise returns `-1`.

```python
text = "hello world"
print(text.find("world"))  # 6
```

<br>

#### format()

**args**: (`*args`, `**kwargs`)

Performs a string formatting operation, replacing placeholders with values.

```python
text = "Hello {}, welcome to {}."
print(text.format("Alice", "Wonderland"))  # "Hello Alice, welcome to Wonderland."
```

<br>

#### format_map()

**args**: (`mapping`)

Formats the string using the given mapping (like a dictionary).

```python
text = "Hello {name}, welcome to {place}."
print(text.format_map({'name': 'Bob', 'place': 'Earth'}))  # "Hello Bob, welcome to Earth."
```

<br>

#### index()

**args**: (`sub`[, `start`[, `end`]])

Similar to `find()`, but raises `ValueError` when the substring is not found.

```python
text = "hello world"
print(text.index("world"))  # 6
```

<br>

#### isalnum()

**args**: `None`

Returns `True` if all characters in the string are alphanumeric (letters or numbers), and the string is not empty; otherwise, returns `False`.

```python
text = "abc123"
print(text.isalnum())  # True
```

<br>

#### isalpha()

**args**: `None`

Returns `True` if all characters in the string are alphabetic and the string is not empty; otherwise, returns `False`.

```python
text = "abcXYZ"
print(text.isalpha())  # True
```

<br>

#### isascii()

**args**: `None`

Returns `True` if all characters in the string are ASCII, and the string is not empty; otherwise, returns `False`.

```python
text = "hello"
print(text.isascii())  # True
```

<br>

#### isdecimal()

**args**: `None`

Returns `True` if all characters in the string are decimals (0-9) and the string is not empty; otherwise, returns `False`.

```python
text = "12345"
print(text.isdecimal())  # True
```

<br>

#### isdigit()

**args**: `None`

Returns `True` if all characters in the string are digits and the string is not empty; otherwise, returns `False`.

```python
text = "45678"
print(text.isdigit())  # True
```

<br>

#### isidentifier()

**args**: `None`

Returns `True` if the string is a valid identifier in Python (e.g., a variable name), otherwise returns `False`.

```python
text = "variable_name"
print(text.isidentifier())  # True
```

<br>

#### islower()

**args**: `None`

Returns `True` if all alphabetic characters in the string are lowercase and there is at least one alphabetic character; otherwise, returns `False`.

```python
text = "hello"
print(text.islower())  # True
```

<br>

#### isnumeric()

**args**: `None`

Returns `True` if all characters in the string are numeric characters, and the string is not empty; otherwise, returns `False`.

```python
text = "12345"
print(text.isnumeric())  # True
```

<br>

#### isprintable()

**args**: `None`

Returns `True` if all characters in the string are printable or the string is empty; otherwise, returns `False`.

```python
text = "Hello!"
print(text.isprintable())  # True
```

<br>

#### isspace()

**args**: `None`

Returns `True` if all characters in the string are whitespace and the string is not empty; otherwise, returns `False`.

```python
text = "   "
print(text.isspace())  # True
```

<br>

#### istitle()

**args**: `None`

Returns `True` if the string is a titlecased string and there is at least one character; otherwise, returns `False`.

```python
text = "Hello World"
print(text.istitle())  # True
```

<br>

#### isupper()

**args**: `None`

Returns `True` if all alphabetic characters in the string are uppercase and there is at least one alphabetic character; otherwise, returns `False`.

```python
text = "HELLO"
print(text.isupper())  # True
```

<br>

#### join()

**args**: (`iterable`)

Concatenates any number of strings contained within an iterable (such as a list or a tuple). The string on which `join()` is called is used as the separator (delimiter) between each element of the iterable.

<br>

- Using an empty string as the separator:

```python
characters = ['h', 'e', 'l', 'l', 'o']
print(''.join(characters))  # "hello"
```

<br>

- Using space as the separator:

```python
words = ["hello", "world"]
print(' '.join(words))  # "hello world"
```

<br>

- Using a comma and space as the separator:

```python
items = ["apple", "banana", "cherry"]
print(', '.join(items))  # "apple, banana, cherry"
```

<br>

**Note**: While `join()` is a string method, it's frequently used in conjunction with lists and other iterables to efficiently concatenate their elements into a single string.

<br>

#### ljust()

**args**: `width[, fillchar]`

Returns the string left justified in a string of length `width`. `fillchar` is the padding character, default is a space.

```python
text = "hello"
print(text.ljust(10, '-'))  # 'hello-----'
```

<br>

#### lower()

**args**: `None`

Returns a copy of the string with all the characters converted to lowercase.

```python
text = "HELLO"
print(text.lower())  # 'hello'
```

<br>

#### lstrip()

**args**: `[chars]`

Returns a copy of the string with leading characters (default is whitespace) removed.

```python
text = "  hello  "
print(text.lstrip())  # 'hello  '
```

<br>

#### maketrans() & translate()

**args**: 
- `maketrans`: `x[, y[, z]]`
- `translate`: `table[, deletechars]`

`maketrans()` returns a translation table usable for `str.translate()`. This method is a static method of `str` class.

`translate()` returns a string where some specified characters are replaced with the character described in a dictionary or in the translation table.

```python
input_str = 'abc'
output_str = '123'
trans = str.maketrans(input_str, output_str)
text = "abc"
print(text.translate(trans))  # '123'
```

<br>

#### partition()

**args**: `sep`

Splits the string at the first occurrence of the separator and returns a tuple containing the part before the separator, the separator itself, and the part after it.

```python
text = "hello-world"
print(text.partition('-'))  # ('hello', '-', 'world')
```

<br>

#### replace()

**args**: `old, new[, count]`

Returns a copy of the string with all occurrences of the substring `old` replaced by `new`. If the optional argument `count` is given, only the first `count` occurrences are replaced.

```python
text = "hello world"
print(text.replace("world", "Python"))  # 'hello Python'
```

<br>

#### rfind()

**args**: `sub[, start[, end]]`

Returns the highest index of the substring if found. If not found, it returns -1. `start` and `end` are optional arguments to specify where to start and end the search.

```python
text = "hello world"
print(text.rfind("l"))  # 9
```

<br>

#### rindex()

**args**: `sub[, start[, end]]`

Similar to `rfind()`, but raises `ValueError` when the substring is not found.

```python
text = "hello world"
print(text.rindex("l"))  # 9
```

<br>

#### rjust()

**args**: `width[, fillchar]`

Returns the string right justified in a string of length `width`. `fillchar` is the padding character, default is a space.

```python
text = "hello"
print(text.rjust(10, '-'))  # '-----hello'
```

<br>

#### rpartition()

**args**: (`sep`)

Splits the string at the last occurrence of a substring.

```python
s = "hello-world-hi"
print(s.rpartition("-"))  # ('hello-world', '-', 'hi')
```

<br>

#### rsplit()

**args**: `sep=None, maxsplit=-1`

Behaves like `split()` but splits from the right. If `sep` is not specified or `None`, any whitespace string is a separator.

```python
text = "apple,banana,cherry"
print(text.rsplit(',', 1))  # ['apple,banana', 'cherry']
```

<br>

#### rstrip()

**args**: `[chars]`

Returns a copy of the string with trailing characters (default is whitespace) removed.

```python
text = "  hello  "
print(text.rstrip())  # '  hello'
```

<br>

#### splitlines()

**args**: `[keepends]`

Splits the string at line breaks and returns a list of lines in the string. If `keepends` is provided and true, line breaks are also included in items of the list.

```python
text = "hello\nworld"
print(text.splitlines())  # ['hello', 'world']
```

<br>

#### startswith()

**args**: `prefix[, start[, end]]`

Returns `True` if the string starts with the specified prefix, otherwise returns `False`. `start` and `end` are optional arguments to specify where to start and end the check.

```python
text = "hello"
print(text.startswith("he"))  # True
```

<br>

#### strip()

**args**: `[chars]`

Returns a copy of the string with leading and trailing characters (default is whitespace) removed.

```python
text = "  hello  "
print(text.strip())  # 'hello'
```

<br>

#### swapcase()

**args**: `None`

Returns a string with uppercase characters converted to lowercase and vice versa.

```python
text = "hElLo"
print(text.swapcase())  # 'HeLlO'
```

<br>

#### title()

**args**: `None`

Returns a title-cased version of the string where words start with an uppercase character and the remaining characters are lowercase.

```python
text = "hello world"
print(text.title())  # 'Hello World'
```

<br>

#### upper()

**args**: `None`

Returns a copy of the string with all the characters converted to uppercase.

```python
text = "hello"
print(text.upper())  # 'HELLO'
```

<br>

#### zfill()

**args**: `width`

Returns a copy of the string with '0' characters padded to the left, making the string's total width equal to the provided width.

```python
number = "42"
print(number.zfill(5))  # '00042'
```

<br>

That covers a majority of the string methods in Python. There are other methods and variations not covered in this overview, but this list should give a good foundation for most string manipulations.