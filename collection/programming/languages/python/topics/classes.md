<br>

---

<br>

Object-Oriented Programming (OOP) is a programming paradigm that uses objects and classes. Python supports OOP, enabling you to create custom data types and structures. This guide delves deep into Python classes, covering everything you need to master them.

<br>

---

<br>


## Creating Classes

<br>

Classes define a blueprint for objects. Here's a basic class definition:

```python
class MyClass:
    pass
```

<br>

To create an object (or instance) of the class:

```python
obj = MyClass()
```

<br>

---

<br>

## Constructors: `__init__`

<br>

A constructor is a special method that gets called when you create an instance of the class:

```python
class MyClass:
    def __init__(self):
        print("Instance created!")

obj = MyClass()  # Outputs: "Instance created!"
```

<br>

You can pass arguments to the constructor:

```python
class MyClass:
    def __init__(self, name):
        self.name = name

obj = MyClass("Jack")
```

<br>

---

<br>

## Class vs. Instance Attributes

<br>

#### Class Attributes

Shared by all instances of the class.

```python
class MyClass:
    class_attr = "I'm a class attribute!"

print(MyClass.class_attr)  # Outputs: "I'm a class attribute!"
```

<br>

#### Instance Attributes

Unique to each instance and are defined using `self`.

```python
class MyClass:
    def __init__(self, name):
        self.name = name

obj = MyClass("Jack")
print(obj.name)  # Outputs: "Jack"
```

<br>

---

<br>

## Class vs. Instance Methods

<br>

#### Instance Methods 

Take `self` as the first parameter.

```python
class MyClass:
    def instance_method(self):
        return "instance method"

obj = MyClass()
print(obj.instance_method())
```

<br>

#### Class Methods

Take a reference to the class (`cls`) as the first parameter and are defined with the `@classmethod` decorator.

```python
class MyClass:
    @classmethod
    def class_method(cls):
        return "class method"

print(MyClass.class_method())
```

<br>

#### Static Methods

Don’t take `self` or `cls` and are defined with the `@staticmethod` decorator.

```python
class MyClass:
    @staticmethod
    def static_method():
        return "static method"

print(MyClass.static_method())
```

<br>

---

<br>

## Magic Methods

<br>

Also known as dunder (double underscore) methods, they allow you to define custom behaviors for built-in operations. Examples:

- `__str__`: Returns a string representation of the object.
- `__len__`: Allows you to use `len(obj)` to get the length of the object.
- `__add__`: Enables the use of the `+` operator with the object.

<br>

---

<br>

## Comparing Objects

<br>

By default, comparing objects checks their memory addresses. But you can customize this with magic methods:

- `__eq__`: Define behavior for equality (`==`)
- `__lt__`: Define behavior for less than (`<`)
- `__le__`: Define behavior for less than or equal (`<=`)
- And others...

<br>

---

<br>

## Performing Arithmetic Operations

You can make your objects support arithmetic operations:

- `__add__`: Define behavior for addition (`+`)
- `__sub__`: Define behavior for subtraction (`-`)
- And others...

<br>

---

<br>

## Custom Containers

To make your class behave like a container (like lists or dictionaries), you can implement methods like `__len__`, `__getitem__`, `__setitem__`, and others.

<br>

---

<br>

## Private Members

In Python, there's no strict way to make attributes or methods private. However, prefixing them with `_` or `__` is a convention to indicate they're meant to be private or protected.

<br>

---

<br>

## Properties

Use the `@property` decorator to define methods that act like getters for an attribute. You can also define setters:

```python
class MyClass:
    def __init__(self, x):
        self._x = x

    @property
    def x(self):
        return self._x

    @x.setter
    def x(self, value):
        self._x = value
```

<br>

---

<br>

## Inheritance

Inheritance allows a class (`child`) to inherit attributes and methods from another class (`parent`):

```python
class Parent:
    def greet(self):
        return "Hello from Parent"

class Child(Parent):
    pass

obj = Child()
print(obj.greet())  # Outputs: "Hello from Parent"
```

<br>

---

<br>

## Object Class

All classes in Python inherit from the `object` class, either directly or indirectly.


<br>

---

<br>

## Method Overriding

You can provide a different implementation of a method in the child class:

```python
class Parent:
    def greet(self):
        return "Hello from Parent"

class Child(Parent):
    def greet(self):
        return "Hello from Child"
```

<br>

---

<br>

## Multi-level Inheritance

A class can inherit from a child class, leading to multi-level inheritance:

```python
class Grandparent:
    pass

class Parent(Grandparent):
    pass

class Child(Parent):
    pass
```

<br>

---

<br>

## Multiple Inheritance

A class can inherit from more than one class:

```python
class Mother:
    pass

class Father:
    pass

class Child(Mother, Father):
    pass
```

<br>

---

<br>

## Abstract Base Classes

You can define classes that can't be instantiated and act as a blueprint for other classes. Such classes can have abstract methods that child classes must implement:

```python
from abc import ABC, abstractmethod

class MyAbstractClass(ABC):
    @abstractmethod
    def my_abstract_method(self):
        pass
```

<br>

---

<br>

## Polymorphism

Polymorphism allows objects of different classes to be treated as objects of a common superclass.


<br>

---

<br>

## Duck Typing

"If it looks like a duck and quacks like a duck, it's a duck." Python uses duck typing, meaning the type of an object is determined by its behavior (methods and properties), not its class.

<br>

---

<br>

## Extending Built-in Types

You can extend built-in types like `list`, `dict`, and others:

```python
class MyList(list):
    def my_method(self):
        pass
```

<br>

---

<br>

## Data Classes (Python 3.7+)

`dataclasses` provide a decorator and functions to create classes that are primarily used to store data. These classes can automatically provide special methods like `__init__` and `__repr__`:

```python
from dataclasses import dataclass

@dataclass
class Point:
    x: int
    y: int
```


<br>

---

<br>

Mastering classes in Python provides a strong foundation for OOP, making your code more modular, reusable, and maintainable. Practice and real-world applications will cement your understanding of these concepts.