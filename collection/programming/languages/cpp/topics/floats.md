Floating-point numbers are used to represent real numbers (numbers with fractional parts) in C++. They are represented using the IEEE 754 standard, which allows them to accommodate decimal points.

<br>

---

<br>

#### Floating-Point Types

C++ provides three types of floating-point numbers:

- **`float`**: The smallest floating-point type. It typically requires 4 bytes of memory.
<br>
- **`double`**: A floating-point type that is twice as large as `float`. It typically requires 8 bytes of memory.
<br>
- **`long double`**: A floating-point type that is at least as large as `double`. Its size is compiler-dependent.

<br>

---

<br>

## Floating Point Limits

The exact size and range of these types can be found using the `sizeof` function and the `limits` library:

```cpp
#include <iostream>
#include <cfloat>

int main() {
    std::cout << "Size of float: " << sizeof(float) << " bytes\n";
    std::cout << "Range of float: " << FLT_MIN << " to " << FLT_MAX << "\n";

    std::cout << "Size of double: " << sizeof(double) << " bytes\n";
    std::cout << "Range of double: " << DBL_MIN << " to " << DBL_MAX << "\n";

    std::cout << "Size of long double: " << sizeof(long double) << " bytes\n";
    std::cout << "Range of long double: " << LDBL_MIN << " to " << LDBL_MAX << "\n";

    return 0;
}
```

<br>

---

<br>

## Floating-Point Literals

Floating-point literals are numbers used directly in the code. They can be written in decimal or exponential format:

- **Decimal**: The default format. Example: `double dec = 3.14;`
- **Exponential**: Written with an `e` or `E`, followed by an integer that represents the exponent of 10. Example: `double exp = 3.14e-2;` // 3.14 * 10^-2 = 0.0314

<br>

---

<br>

## Precision of Floating-Point Numbers

Floating-point numbers have limited precision, and operations on them can produce rounding errors. For example:

```cpp
double a = 0.1;
double b = 0.2;
double c = a + b; // c is not exactly 0.3
```

In this example, `c` is not exactly `0.3` due to rounding errors. This is a fundamental limitation of floating-point numbers and is not specific to C++.

<br>

---

<br>

## Division By Zero

Division by zero with floating-point numbers does not cause an error as it does with integers. Instead, it produces special values:

- **Positive infinity (`inf`)**: Produced by dividing a positive number by zero.
<br>
- **Negative infinity (`-inf`)**: Produced by dividing a negative number by zero.
<br>
- **Not a number (`nan`)**: Produced by dividing zero by zero or subtracting infinity from infinity.

```cpp
double pos = 1.0 / 0.0; // inf
double neg = -1.0 / 0.0; // -inf
double nan = 0.0 / 0.0; // nan
```

In these examples, `pos` is positive infinity, `neg` is negative infinity, and `nan` is not a number.

Remember, while floating-point numbers are powerful tools for representing real numbers, they have limitations and can produce rounding errors. Always be aware of these limitations when working with floating-point numbers.