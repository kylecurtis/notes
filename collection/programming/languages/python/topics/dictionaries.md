<br>

---

<br>

A dictionary in Python is an unordered collection of data values, stored as key-value pairs. Each key must be unique, and keys can be of any immutable type. Dictionaries are mutable, meaning you can change their content without changing their identity.

<br>

---

<br>

## Creating Dictionaries

<br>

#### Using Curly Braces

  ```python
  d = {"key1": "value1", "key2": "value2"}
  ```

<br>

#### Using the `dict()` Constructor

  ```python
  d = dict(key1="value1", key2="value2")
  ```

<br>

#### From Lists of Tuples

  ```python
  d = dict([("key1", "value1"), ("key2", "value2")])
  ```

<br>

---

<br>

## Accessing Dictionary Values

<br>

Use the key to get the value:

```python
print(d["key1"])  # Outputs: value1
```

<br>

Using `get()` method (avoids KeyError if the key doesn't exist):

```python
print(d.get("key1"))  # Outputs: value1
```

<br>

---

<br>

## Modifying Dictionaries

<br>

#### Add or Update an Entry

  ```python
  d["key3"] = "value3"
  ```

<br>

#### Delete an Entry

  ```python
  del d["key2"]
  ```

<br>

#### Pop an Entry

  ```python
  d.pop("key1")  # Removes the item with key "key1"
  ```

<br>

#### Clear the Dictionary

  ```python
  d.clear()
  ```

<br>

---

<br>

## Dictionary Methods

<br>

- `d.keys()`: Returns a list of all keys.
  
- `d.values()`: Returns a list of all values.
  
- `d.items()`: Returns a list of all key-value tuple pairs.

- `d.copy()`: Returns a shallow copy of the dictionary.

- `d.setdefault(key[, default])`: If key exists, returns its value. If not, inserts key with a value of default and returns default (default is None if not provided).

- `d.update(dict2)`: Merges dictionary `dict2` into `d`. It overwrites existing keys.

<br>

---

<br>

## Iterating through Dictionaries

<br>

#### Loop through keys

```python
for key in d:
    print(key)
```

<br>

#### Loop through values

```python
for value in d.values():
    print(value)
```

<br>

#### Loop through key-value pairs

```python
for key, value in d.items():
    print(key, value)
```

<br>

---

<br>

## Dictionary Comprehensions

<br>

They provide a concise way to create dictionaries:

```python
squared_dict = {x: x**2 for x in (1, 2, 3, 4, 5)}
```

<br>

With conditions:

```python
even_squares = {x: x**2 for x in range(10) if x % 2 == 0}
```

<br>

---

<br>

## Key Points to Remember

- Dictionary keys are unique and immutable. This means you can use numbers, strings, and tuples as dictionary keys.

- Dictionary values can be of any type and can be duplicated.

- Dictionaries are mutable, which means you can add, remove, and modify entries after the dictionary is created.

- The `in` keyword can be used to check if a key exists in a dictionary.

- The order of items in a dictionary is preserved as of Python 3.7. This means when you add new items, they are added to the end of the dictionary. However, this wasn't the case in earlier versions.

<br>

---

<br>

Mastering dictionaries can significantly enhance your efficiency in many data manipulation tasks in Python. Given their flexibility and the speed at which they allow access to values (thanks to the underlying hash table structure), they're a foundational tool in the Python programmer's toolkit.

<br>

---

<br>