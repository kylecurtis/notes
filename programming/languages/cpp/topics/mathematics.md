
C++ provides a rich set of mathematical operations that can be used for calculations. These include basic arithmetic operations, comparison operations, and a variety of functions provided in the `<cmath>` library.

<br>

---

<br>

## Basic Arithmetic Operations

C++ supports the following basic arithmetic operations:

- **Addition (`+`)**: Adds two numbers. Example: `a + b`
<br>
- **Subtraction (`-`)**: Subtracts the second number from the first. Example: `a - b`
<br>
- **Multiplication (`*`)**: Multiplies two numbers. Example: `a * b`
<br>
- **Division (`/`)**: Divides the first number by the second. Example: `a / b`
<br>
- **Modulus (`%`)**: Returns the remainder of the division of the first number by the second. Example: `a % b`

<br>

```cpp
int a = 10;
int b = 3;

int sum = a + b; // 13
int difference = a - b; // 7
int product = a * b; // 30
int quotient = a / b; // 3
int remainder = a % b; // 1
```

<br>

---

<br>

## Order of Operations

The order of operations in C++ follows the standard mathematical rules known as BIDMAS or PEMDAS:

- **Brackets/parentheses**: Operations enclosed in brackets are performed first.
<br>
- **Indices/Exponents**: Powers and square roots, etc.
<br>
- **Division and Multiplication**: These have the same precedence and are performed from left to right.
<br>
- **Addition and Subtraction**: These also have the same precedence and are performed from left to right.

<br>

For example:

```cpp
int a = 10;
int b = 2;
int c = 3;

int result = a + b * c; // result is 16, not 36
```

<br>

In the above example, multiplication is performed before addition due to the order of operations.

<br>

---

<br>

## Comparison Operations

C++ supports the following comparison operations:

- **Equal to (`==`)**: Returns true if the two numbers are equal. Example: `a == b`
<br>
- **Not equal to (`!=`)**: Returns true if the two numbers are not equal. Example: `a != b`
<br>
- **Greater than (`>`)**: Returns true if the first number is greater than the second. Example: `a > b`
<br>
- **Less than (`<`)**: Returns true if the first number is less than the second. Example: `a < b`
<br>
- **Greater than or equal to (`>=`)**: Returns true if the first number is greater than or equal to the second. Example: `a >= b`
<br>
- **Less than or equal to (`<=`)**: Returns true if the first number is less than or equal to the second. Example: `a <= b`

<br>

```cpp
int a = 10;
int b = 3;

bool isEqual = a == b; // false
bool isNotEqual = a != b; // true
bool isGreaterThan = a > b; // true
bool isLessThan = a < b; // false
bool isGreaterThanOrEqual = a >= b; // true
bool isLessThanOrEqual = a <= b; // false
```

<br>

---

<br>

## The `<cmath>` Library in C++

The `<cmath>` library in C++ provides a wide range of mathematical functions. To use these functions, you need to include the `<cmath>` library at the beginning of your code:

```cpp
#include <cmath>
```

<br>

#### Common `<cmath>` Functions

Here are some common functions provided by the `<cmath>` library:

- **`pow(base, exponent)`**: Raises the base to the power of the exponent. Example: `pow(2, 3)` returns 8.
<br>
- **`sqrt(number)`**: Returns the square root of the number. Example: `sqrt(9)` returns 3.
<br>
- **`cbrt(number)`**: Returns the cube root of the number. Example: `cbrt(27)` returns 3.
<br>
- **`abs(number)`**: Returns the absolute value of the number. Example: `abs(-10)` returns 10.
<br>
- **`ceil(number)`**: Rounds the number up to the nearest integer. Example: `ceil(9.2)` returns 10.
<br>
- **`floor(number)`**: Rounds the number down to the nearest integer. Example: `floor(9.8)` returns 9.
<br>
- **`round(number)`**: Rounds the number to the nearest integer. Example: `round(9.5)` returns 10.
<br>
- **`log(number)`**: Returns the natural logarithm (base e) of the number. Example: `log(1)` returns 0.
<br>
- **`log10(number)`**: Returns the base-10 logarithm of the number. Example: `log10(100)` returns 2.
<br>
- **`sin(angle)`**, **`cos(angle)`**, **`tan(angle)`**: Returns the sine, cosine, and tangent of the angle (in radians), respectively.
<br>

```cpp
double base = 2.0;
double exponent = 3.0;
double result = pow(base, exponent); // 8.0

double number = 9.0;
double root = sqrt(number); // 3.0

number = -10;
int absolute = abs(number); // 10

double decimal = 9.2;
double ceiling = ceil(decimal); // 10.0

decimal = 9.8;
double floored = floor(decimal); // 9.0

double angle = 3.14159265 / 2; // pi/2 radians
double sine = sin(angle); // 1.0
```

Remember, these are just a few of the mathematical operations and functions available in C++. The `<cmath>` library provides many more functions for more complex mathematical calculations.