
<br>

---

<br>

A Python list is an ordered collection of items, which can be of heterogeneous types. They are mutable, which means the items can be changed after the list creation. Furthermore, lists can contain duplicate values.

<br>

---

<br>

## Creating Lists

<br>

####  Using Square Brackets: 

Lists can be defined using square brackets `[]` with items separated by commas.
  ```python
  planets = ["Mercury", "Venus", "Earth", "Mars"]
  ```

<br>

#### Using the List Constructor: 

Lists can also be created using the `list()` constructor.
  ```python
  space_objects = list(("star", "galaxy", "comet"))
  ```

<br>

#### Reversing a List:

```python
celestial_bodies = ["Sun", "Moon", "Jupiter", "Mars"]
reversed_bodies = list(reversed(celestial_bodies))

print(reversed_bodies)  # Output: ["Mars", "Jupiter", "Moon", "Sun"]
```

<br>

#### Generating from Another List:

```python
numbers = [1, 2, 3, 4, 5]
squares = list(x ** 2 for x in numbers)

print(squares)  # Output: [1, 4, 9, 16, 25]
```

<br>

#### Filtering Elements:

```python
numbers = [1, 2, 3, 4, 5, 6]
even_numbers = list(x for x in numbers if x % 2 == 0)

print(even_numbers)  # Output: [2, 4, 6]
```

<br>

---

<br>

## Exploring List Properties

<br>

#### Determining List Length

  ```python
  constellations = ["Orion", "Big Dipper", "Cassiopeia"]
  print(len(constellations))  # Output: 3
  ```

<br>

#### Accessing List Items

  ```python
  constellations = ["Orion", "Big Dipper", "Cassiopeia"]
  
  print(constellations[0])  # Output: Orion
  print(constellations[-1])  # Output: Cassiopeia
  ```

<br>

#### Finding Minimum & Maximum

  ```python
  numbers = [10, 25, 3, 47, 5]
  
  print(max(numbers))  # Output: 47
  print(min(numbers))  # Output: 3
  ```

<br>

#### Computing Sum

  ```python
  distances = [100, 200, 300, 400]
  print(sum(distances))  # Output: 1000
  ```

<br>

---

<br>

## Manipulating Lists

<br>

#### Unpacking Lists

  ```python
  stars = ["Sirius", "Polaris", "Betelgeuse"]
  star1, star2, star3 = stars
  print(star1)  # Output: Sirius
  ```

<br>

#### Iterating Through Lists

  ```python
  for planet in planets:
      print(planet)
  ```

<br>

#### Checking List Membership

  ```python
  print("Earth" in planets)  # Output: True
  ```

<br>

---

<br>

## Advanced List Operations

<br>

#### Using Lambda Functions

  ```python
  planets = ["Mercury", "Venus", "Earth", "Jupiter"]
  planets.sort(key=lambda x: len(x))
  print(planets)  # Output: ['Venus', 'Earth', 'Mercury', 'Jupiter']
  ```

#### Map and Filter Functions

  ```python
  moons = [1, 2, 3, 4]
  moon_squares = list(map(lambda x: x**2, moons))
  print(moon_squares)  # Output: [1, 4, 9, 16]
  
  odd_moons = list(filter(lambda x: x%2 != 0, moons))
  print(odd_moons)  # Output: [1, 3]
  ```

#### List Comprehensions

  ```python
  moon_cubes = [x**3 for x in moons]
  print(moon_cubes)  # Output: [1, 8, 27, 64]
  ```

#### Zipping Lists

  ```python
  bodies = ['Earth', 'Mars', 'Venus']
  distances = [93, 142, 67]
  zipped_data = list(zip(bodies, distances))
  print(zipped_data)  # Output: [('Earth', 93), ('Mars', 142), ('Venus', 67)]
  ```

<br>

---

<br>

Remember, lists are fundamental and versatile in Python. Mastery over lists and their methods is crucial for efficiently handling collections of data.

<br>

---

<br>

## Common List Methods

<br>

#### append()

Adds an element at the end of the list.

```python
fruits = ['apple', 'banana', 'cherry']
fruits.append("orange")
print(fruits)  # Output: ['apple', 'banana', 'cherry', 'orange']
```

<br>

#### clear()

Removes all the elements from the list.

```python
fruits = ['apple', 'banana', 'cherry']
fruits.clear()
print(fruits)  # Output: []
```

<br>

#### copy()

Returns a copy of the list.

```python
fruits1 = ['apple', 'banana', 'cherry']
fruits2 = fruits1.copy()
print(fruits2)  # Output: ['apple', 'banana', 'cherry']
```

<br>

#### count()

Returns the number of elements with the specified value.

```python
numbers = [1, 2, 3, 2, 2, 4, 5, 6]
print(numbers.count(2))  # Output: 3
```

<br>

#### extend()

Add the elements of a list (or any iterable), to the end of the current list.

```python
fruits1 = ['apple', 'banana', 'cherry']
fruits2 = ['orange', 'mango', 'grape']
fruits1.extend(fruits2)
print(fruits1)  # Output: ['apple', 'banana', 'cherry', 'orange', 'mango', 'grape']
```

<br>

#### index()

Returns the index of the first element with the specified value.

```python
numbers = [1, 2, 3, 2, 2, 4, 5, 6]
print(numbers.index(2))  # Output: 1
```

<br>

#### insert()

Adds an element at the specified position.

```python
fruits = ['apple', 'banana', 'cherry']
fruits.insert(1, "orange")
print(fruits)  # Output: ['apple', 'orange', 'banana', 'cherry']
```

<br>

#### pop()

Removes the element at the specified position.

```python
fruits = ['apple', 'banana', 'cherry']
fruits.pop(1)
print(fruits)  # Output: ['apple', 'cherry']
```

<br>

#### remove()

Removes the first item with the specified value.

```python
fruits = ['apple', 'banana', 'cherry']
fruits.remove('banana')
print(fruits)  # Output: ['apple', 'cherry']
```

<br>

#### reverse()

Reverses the order of the list.

```python
fruits = ['apple', 'banana', 'cherry']
fruits.reverse()
print(fruits)  # Output: ['cherry', 'banana', 'apple']
```