<br>

---

<br>

Tuples are similar to lists in Python. The main distinctions are:
- Tuples are immutable: once defined, you can't modify, add, or delete items.
- Tuples are defined using parentheses `()` rather than square brackets `[]`.

<br>

---

<br>

#### Example

```python
planets = ("Mercury", "Venus", "Earth", "Mars")
```

<br>

---

<br>

## Creating Tuples

<br>

#### Empty tuple

Just open and close parentheses.

  ```python
  empty_tuple = ()
  ```

<br>

#### Singleton tuple 

A single value followed by a comma.

  ```python
  single_element_tuple = ("Earth",)
  ```

<br>

#### Tuple unpacking

Allows multiple variables to be assigned values from a tuple.
  ```python
  a, b, c, d = planets
  ```

<br>

#### Using the tuple constructor

This is an alternative way to create a tuple.

  ```python
  tuple_from_list = tuple(["Mercury", "Venus", "Earth", "Mars"])
  ```

<br>

---

<br>

## Accessing Tuple Items

<br>

#### Indexing

Just like lists, you can use indexing to access tuple items.

  ```python
  print(planets[1])  # Output: Venus
  ```

<br>

#### Negative Indexing

Access elements from the end.

  ```python
  print(planets[-1])  # Output: Mars
  ```

<br>

#### Slicing

Extract portions of a tuple.

  ```python
  inner_planets = planets[:2]
  print(inner_planets)  # Output: ('Mercury', 'Venus')
  ```

<br>

---

<br>

## Tuple Operations

<br>

#### Concatenation

Combine tuples.

  ```python
  other_planets = ("Jupiter", "Saturn")
  all_planets = planets + other_planets
  ```

<br>

#### Repetition

Repeat tuples using the `*` operator.

  ```python
  repeated_tuple = planets * 2
  ```

<br>

#### Membership

Check if an element exists within a tuple using the `in` keyword.

  ```python
  print("Earth" in planets)  # Output: True
  ```

<br>

#### Length

Get the number of items in a tuple with the `len()` function.

  ```python
  print(len(planets))  # Output: 4
  ```

<br>

---

<br>

## Useful Tuple Methods

<br>

#### `tuple.index(item)`

Return the first occurrence of an item.

  ```python
  position = planets.index("Earth")
  ```

<br>

#### `tuple.count(item)`

Return the number of occurrences of an item.

  ```python
  count_earth = planets.count("Earth")
  ```

<br>

---

<br>

## Nesting

<br>

Tuples can contain other tuples as well as other complex types like lists and dictionaries.

```python
nested_tuple = ("Earth", ("North", "South"))
```

<br>

---

<br>

## Conversion Between List and Tuple

<br>

#### Tuple to List

  ```python
  planet_list = list(planets)
  ```

<br>

#### List to Tuple

  ```python
  planet_tuple = tuple(planet_list)
  ```

<br>

---

<br>

## Advantages of Using Tuples

- **Immutability**: Tuples, being immutable, can be used as keys in dictionaries, while lists can't.
  
- **Safety**: If you have data that doesn't change, putting it in a tuple can prevent accidental modifications.

- **Performance**: Since tuples are static and are allocated once, they can be faster compared to lists for certain operations.

<br>

---

<br>

## **8. Miscellaneous Tips**

- Tuples are often used in function returns when you need to send multiple values.
  
- They are commonly used for structured data, similar to records or structs in other languages.

- Iterating through a tuple is faster than iterating through a list.

<br>

---

<br>