<br>

---

<br>

## Variables in C++

A variable in C++ is a named space in the memory where a value can be stored and manipulated. Each variable in C++ has a specific type, which determines the size and layout of the variable's memory, the range of values that can be stored within that memory, and the set of operations that can be applied to the variable.

<br>

---

<br>

#### Declaration and Initialization

A variable is declared by stating its type followed by one or more space-separated identifiers. For example:

```cpp
int myVariable;
```

<br>

A variable can be initialized (assigned a value) at the time of declaration:

```cpp
int myVariable = 10;
```

<br>

Or it can be assigned a value later in the code:

```cpp
myVariable = 20;
```

<br>

---

<br>

#### Scope of Variables

The scope of a variable determines the portion of the code where a variable can be accessed. There are three types of scopes in C++:

1. **Local Scope**: Variables declared within a block or a function are local to that block or function. They can't be accessed outside of it.
2. **Global Scope**: Variables declared outside all functions are global variables and can be accessed from any part of the code.
3. **Class Scope**: Variables declared within a class are accessible within the scope of the class.

<br>

---

<br>

#### Variable Naming

Variable names in C++ can consist of letters, digits, and underscores, but must begin with a letter or an underscore. C++ is case-sensitive, so `myVariable`, `myvariable`, and `MYVARIABLE` are all different variables.

<br>

---

<br>

## Constants in C++

A constant in C++ is similar to a variable, but once it is initialized, its value cannot be changed throughout the program. This is useful when you want to declare a variable that remains the same throughout the program.

#### Declaration and Initialization

A constant is declared by using the `const` keyword before the type specification:

```cpp
const int myConstant = 10;
```

<br>

Note that constants must be initialized at the time of declaration. You cannot declare a constant and assign it a value later in the code.

<br>

---

<br>

#### Constant Expressions

A constant expression is an expression that is evaluated at compile time rather than at run time. The `constexpr` keyword is used to declare a constant expression:

```cpp
constexpr int myConstExpr = 10 * 10;
```

<br>

In this case, `myConstExpr` is evaluated at compile time, and anywhere the program uses `myConstExpr`, the compiler will substitute it with the result of the expression (in this case, 100).
