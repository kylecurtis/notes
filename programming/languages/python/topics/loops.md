Python provides various constructs to perform looping. In Python, there are mainly two types of loops: `for` and `while`.

<br>

---

<br>

## For Loop

The `for` loop in Python is used to iterate over a sequence (list, tuple, string) or other iterable objects. Iterating over a sequence is called traversal.

```python
# Iterating over a list
for item in ["Apple", "Orange", "Blueberry"]:
    print(item)
```

<br>

#### The range() function

We can generate a sequence of numbers using the `range()` function. `range(10)` will generate numbers from 0 to 9 (10 numbers).

```python
# Printing numbers from 0 to 9
for i in range(10):
    print(i)
```

<br>

The `range()` function can also be called with two arguments where the first argument is the start index and the second argument is the end index. The function will generate numbers from the start index up to but not including the end index.

```python
# Printing numbers from 5 to 9
for i in range(5, 10):
    print(i)
```

<br>

You can also provide a third argument, which is the step size or the difference between each number in the sequence.

```python
# Printing even numbers between 2 and 10
for i in range(2, 11, 2):
    print(i)
```

In this example, `range(2, 11, 2)` generates numbers starting from 2 up to but not including 11, and the difference between each number is 2, meaning it will generate the sequence [2, 4, 6, 8, 10].

<br>

---

<br>

#### For/Else

A `for` loop can have an optional `else` block as well. The `else` part is executed if the items in the sequence used in the `for` loop exhausts.

```python
digits = [0, 1, 5]
for i in digits:
    print(i)
else:
    print("No items left.")
```

<br>

---

<br>

## Nested Loops

A nested loop is a loop inside a loop. The inner loop will be executed one time for each iteration of the outer loop.

```python
for i in range(1, 6):
    for j in range(i):
        print(i, end=' ')
    print()
```

<br>

---

<br>

## Iterable

In Python, an iterable is an object capable of returning its members one at a time. Examples of iterables include all sequence types (such as list, str, and tuple) and some non-sequence types like dict and file and objects of any classes you define with an `__iter__()` or `__getitem__()` method.

```python
my_tuple = ("apple", "banana", "cherry")
my_iter = iter(my_tuple)

print(next(my_iter))  # Output: "apple"
print(next(my_iter))  # Output: "banana"
print(next(my_iter))  # Output: "cherry"
```

<br>

---

<br>

## While Loop

The `while` loop in Python is used to iterate over a block of code as long as the test expression (condition) is true.

```python
# Printing numbers less than 5
n = 1
while n < 5:
    print(n)
    n += 1
```

<br>

#### While/Else

Similar to the `for` loop, the `while` loop can also have an optional `else` statement. The `else` statement will be executed if the loop has exhausted iterating the list.

```python
n = 1
while n < 5:
    print(n)
    n += 1
else:
    print("No items left.")
```

<br>

#### Break

You can also break a while loop using the `break` keyword:

```python
while True:
	command = input(">")
	if command.lower() == "quit":
		break
	else:
		# continue loop...
```

<br>

---

<br>

## Infinite Loop

If the condition of `while` is always True, we get an infinite loop.

```python
# An infinite loop
while True:
    num = int(input("Enter an integer: "))
    print("The double of", num, "is", 2 * num)
```

<br>

Note: To break out of an infinite loop in a console, you can press `Ctrl+C`. In a Jupyter notebook, you can interrupt the kernel.