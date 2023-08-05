A list in Python is an ordered collection of items which can be of different types. Lists are mutable (i.e., their elements can be changed), and they allow duplicate values.

<br>

---

<br>

## Creating Lists

<br>

#### Using Square Brackets

Lists are defined by enclosing a comma-separated sequence of items in square brackets `[]`.

```python
planets = ["Mercury", "Venus", "Earth", "Mars"]
```

<br>

#### Using List Constructors

You can also create a list with the built-in `list()` constructor.

```python
numbers = list(("one", "two", "three"))
```

<br>

When you're using the `list()` constructor, you can  perform actions such as reversing another list or iterating through another list. The key is to provide an iterable object to the `list()` constructor. Here are a few examples:

#### Reversing Another List

Python's `reversed()` function returns a reversed iterator of a sequence (like a list). You can pass this to the `list()` constructor to get a new list with the elements in reversed order.

```python
original_list = [1, 2, 3, 4, 5]
reversed_list = list(reversed(original_list))
print(reversed_list)  # Output: [5, 4, 3, 2, 1]
```

<br>

#### Iterating Through Another List

If you want to perform some action on each element of a list and create a new list with the results, you can use a generator expression. A generator expression is similar to a list comprehension, but instead of creating a new list in memory, it creates a generator object that can be iterated over on-the-fly. This can be more memory-efficient when dealing with large lists.

Here's an example where we create a new list with the squares of the numbers in the original list:

```python
original_list = [1, 2, 3, 4, 5]
squares = list(x ** 2 for x in original_list)
print(squares)  # Output: [1, 4, 9, 16, 25]
```

<br>

#### Filtering Elements From Another List

You can use a generator expression with an `if` condition to filter elements from another list. Here's an example where we create a new list with only the even numbers from the original list:

```python
original_list = [1, 2, 3, 4, 5, 6]
evens = list(x for x in original_list if x % 2 == 0)
print(evens)  # Output: [2, 4, 6]
```

<br>

---

<br>

## Get The Length of A List

The `len()` function returns the number of items in a list. This can be useful when you want to determine the list's size, like when looping over the list or allocating resources based on the number of items in the list.

```python
my_list = [1, 2, 3, 4, 5]
print(len(my_list))  # Output: 5
```

<br>

---

<br>

## Accessing List Items

You can access the list items by referring to the index number.

```python
print(fruits[0])  # Output: apple
```

<br>

Negative indexing means accessing from the end. -1 refers to the last item, -2 refers to the second last item, and so on.

```python
print(fruits[-1])  # Output: cherry
```

<br>

---

<br>

## Get Min & Max List Element

The `max()` and `min()` functions return the largest and smallest elements in a list, respectively. These functions can be helpful in finding the range of numeric data in a list.

```python
my_list = [1, 2, 3, 4, 5]
print(max(my_list))  # Output: 5
print(min(my_list))  # Output: 1
```

<br>

---

<br>

## Sum Of List

The `sum()` function returns the sum of all elements in a list. It can only be applied to lists containing numbers (integers or floats). This can be useful for quickly adding up all numbers in a list without having to write a loop.

```python
my_list = [1, 2, 3, 4, 5]
print(sum(my_list))  # Output: 15
```

<br>

---

<br>

## Unpacking Lists

Unpacking is an operation that consists in splitting an iterable (like a list) into variables.

```python
fruits = ["apple", "banana", "cherry"]
x, y, z = fruits
print(x)  # Output: apple
print(y)  # Output: banana
print(z)  # Output: cherry
```

<br>

---

<br>

## Looping Over Lists

You can loop through the list items by using a `for` loop.

```python
for fruit in fruits:
    print(fruit)
```

<br>

---

<br>

## List Membership Testing

You can check whether a value exists in a list with the `in` keyword. The `in` operator returns `True` if the value is found in the list and `False` otherwise.

```python
my_list = ["apple", "banana", "cherry"]
print("apple" in my_list)  # Output: True
print("orange" in my_list)  # Output: False
```

<br>

---

<br>

## Lambda Functions with Lists

Lambda function is a small anonymous function that is defined using the `lambda` keyword.

```python
fruits = ["apple", "banana", "cherry", "orange"]
fruits.sort(key = lambda x: len(x))
print(fruits)  # Output: ['apple', 'cherry', 'banana', 'orange']
```

<br>

---

<br>

## Map Function with Lists

The `map()` function applies a function to all items in an input list.

```python
numbers = [1, 2, 3, 4]
squares = list(map(lambda x: x**2, numbers))
print(squares)  # Output: [1, 4, 9, 16]
```

<br>

---

<br>

## Filter Function with Lists

The `filter()` function constructs a list from elements of another list for which a function returns true.

```python
numbers = [1, 2, 3, 4, 5, 6]
even_numbers = list(filter(lambda x: x%2 == 0, numbers))
print(even_numbers)  # Output: [2, 4, 6]
```

<br>

---

<br>

## List Comprehensions

List comprehension provides a concise way to create lists. It consists of brackets containing an expression followed by a `for` statement, then zero or more `for` or `if` clauses.

```python
squares = [x**2 for x in numbers]
print(squares)  # Output: [1, 4, 9, 16, 25, 36]
```

<br>

---

<br>

## Zip Function with Lists

The `zip()` function takes in iterables as arguments and returns an iterator that generates tuples based on these iterables.

```python
list1 = ['apple', 'banana', 'cherry']
list2 = [1, 2, 3]
zipped = list(zip(list1, list2))
print(zipped)  # Output: [('apple', 1), ('banana', 2), ('cherry', 3)]
```

Remember, lists are a versatile Python data structure to group together other values. Mastering the use of lists and list methods can greatly increase your efficiency when dealing with collections of data.

<br>

---

<br>

## List Manipulation

<br>

#### List Slicing

Slicing allows you to get a subset of elements from a list. Slicing is performed by using the `:` operator inside the square brackets. You can specify where to start and end the slicing, and even specify a step.

The syntax is `my_list[start:stop:step]`.

- `start`: The index where the slice starts. If omitted, it defaults to 0.
- `stop`: The index where the slice stops. This index is not included in the slice. If omitted, it defaults to `len(my_list)`.
- `step`: How many items to skip between items in the slice. If omitted, it defaults to 1.

```python
my_list = [0, 1, 2, 3, 4, 5]
print(my_list[2:5])  # Output: [2, 3, 4]
```

<br>

#### List Replication

You can repeat elements in a list by using the multiplication operator. This operator replicates the list for the specified number of times.

```python
my_list = ["a", "b", "c"]
print(my_list * 3)  # Output: ['a', 'b', 'c', 'a', 'b', 'c', 'a', 'b', 'c']
```

<br>

#### List Membership Testing

You can check whether a value exists in a list with the `in` keyword. The `in` operator returns `True` if the value is found in the list and `False` otherwise.

```python
my_list = ["apple", "banana", "cherry"]
print("apple" in my_list)  # Output: True
print("orange" in my_list)  # Output: False
```


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