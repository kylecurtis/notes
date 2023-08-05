Operators are special symbols in Python that carry out arithmetic or logical computation. The value that the operator operates on is called the operand.

<br>

---

<br>

## Arithmetic Operators

Arithmetic operators are used with numeric values to perform common mathematical operations:

```python
# Addition
print(1 + 1)  # Output: 2

# Subtraction
print(2 - 1)  # Output: 1

# Multiplication
print(2 * 2)  # Output: 4

# Division
print(10 / 2)  # Output: 5.0

# Modulus
print(10 % 3)  # Output: 1

# Exponent
print(2 ** 3)  # Output: 8

# Floor division
print(10 // 3)  # Output: 3
```

<br>

---

<br>

## Comparison Operators

Comparison operators are used to compare values. It either returns `True` or `False` according to the condition.

```python
# Equal to
print(2 == 2)  # Output: True

# Not equal to
print(2 != 2)  # Output: False

# Greater than
print(3 > 2)  # Output: True

# Less than
print(2 < 3)  # Output: True

# Greater than or equal to
print(3 >= 2)  # Output: True

# Less than or equal to
print(2 <= 3)  # Output: True
```

<br>

---

<br>

## Logical Operators

Logical operators are the `and`, `or`, `not` operators.

```python
# and operator - True if both the operands are true
x, y = True, False
print(x and y)  # Output: False

# or operator - True if either of the operands is true
print(x or y)  # Output: True

# not operator - True if operand is false
print(not x)  # Output: False
```

<br>

---

<br>

## Assignment Operators

Assignment operators are used in Python to assign values to variables.

```python
a = 10  # Assign value 10 to a
a += 10  # Add AND: Add right side to left side and assign to left side (equivalent to a = a + 10)
a -= 10  # Subtract AND (equivalent to a = a - 10)
a *= 10  # Multiply AND (equivalent to a = a * 10)
a /= 10  # Divide AND (equivalent to a = a / 10)
```

<br>

---

<br>

## Identity Operators

`is` and `is not` are the identity operators in Python. They are used to check if two values (or variables) are located on the same part of the memory.

```python
a = 5
b = 5
print(a is b)  # Output: True
```

<br>

---

<br>

## Bitwise Operators

Bitwise operators act on operands as if they were strings of binary digits. They operate bit by bit, hence the name.

```python
a = 10  # binary: 1010
b = 4   # binary: 0100

# bitwise AND
print(a & b)  # Output: 0 (binary: 0000)

# bitwise OR
print(a | b)  # Output: 14 (binary: 1110)

# bitwise NOT
print(~a)  # Output: -11 (binary: -(1011))
```

<br>

---

<br>

## Ternary Operators

Ternary operators evaluate something based on a condition being true or not. It is a shortcut for the `if` statement.

```python
x, y = 10, 20

# If condition is true, then x otherwise y
print(x if x < y else y)  # Output: 10
```

<br>

---

<br>

## Chaining Comparison Operators

An interesting feature of Python is the ability to chain multiple comparisons to perform a more complex test.

```python
x = 10

# check if x is greater than 5 AND less than 15
print(5 < x < 15)  # Output: True
```