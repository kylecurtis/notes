
In C++, numbers are primarily represented using integer and floating-point data types. This section will focus on integers, which are whole numbers that can be either positive or negative.

<br>

---

<br>

## Integer Types

C++ provides several types of integers, which differ in size and whether they can represent both positive and negative numbers (signed) or only non-negative numbers (unsigned).

<br>

- **`int`**: The most commonly used integer type. Its size is platform-dependent, but it is usually 4 bytes (32 bits) on most modern systems.
<br>
- **`short int` or `short`**: A smaller integer type that uses less memory but has a smaller range. It is at least 2 bytes (16 bits).
<br>
- **`long int` or `long`**: A larger integer type that uses more memory but has a larger range. It is at least 4 bytes (32 bits).
<br>
- **`long long int` or `long long`**: An even larger integer type. It is at least 8 bytes (64 bits).
<br>
- **`unsigned int`, `unsigned short`, `unsigned long`, `unsigned long long`**: These are the unsigned versions of the above types. They can only represent non-negative numbers.

<br>

---

<br>

## Integer Table

| Type | Size (bytes) | Minimum Value | Maximum Value |
| --- | --- | --- | --- |
| `int` | `sizeof(int)` | `INT_MIN` | `INT_MAX` |
| `short` | `sizeof(short)` | `SHRT_MIN` | `SHRT_MAX` |
| `long` | `sizeof(long)` | `LONG_MIN` | `LONG_MAX` |
| `long long` | `sizeof(long long)` | `LLONG_MIN` | `LLONG_MAX` |
| `unsigned int` | `sizeof(unsigned int)` | `0` | `UINT_MAX` |
| `unsigned short` | `sizeof(unsigned short)` | `0` | `USHRT_MAX` |
| `unsigned long` | `sizeof(unsigned long)` | `0` | `ULONG_MAX` |
| `unsigned long long` | `sizeof(unsigned long long)` | `0` | `ULLONG_MAX` |

<br>

---

<br>

## Integer Sizes

You can replace `sizeof(type)` with the actual size in bytes on your system, and `INT_MIN`, `INT_MAX`, etc., with the actual minimum and maximum values on your system. These values can be obtained using the `sizeof` function and the `limits` library, as shown in the previous example.



The exact size and range of these types can be found using the `sizeof` function and the `limits` library:

```cpp
#include <iostream>
#include <climits>

int main() {
    std::cout << "Size of int: " << sizeof(int) << " bytes\n";
    std::cout << "Range of int: " << INT_MIN << " to " << INT_MAX << "\n";

    std::cout << "Size of short: " << sizeof(short) << " bytes\n";
    std::cout << "Range of short: " << SHRT_MIN << " to " << SHRT_MAX << "\n";

    std::cout << "Size of long: " << sizeof(long) << " bytes\n";
    std::cout << "Range of long: " << LONG_MIN << " to " << LONG_MAX << "\n";

    std::cout << "Size of long long: " << sizeof(long long) << " bytes\n";
    std::cout << "Range of long long: " << LLONG_MIN << " to " << LLONG_MAX << "\n";

    std::cout << "Size of unsigned int: " << sizeof(unsigned int) << " bytes\n";
    std::cout << "Range of unsigned int: 0 to " << UINT_MAX << "\n";

    return 0;
}
```

<br>

---

<br>

## Integer Literals

Integer literals are numbers used directly in the code. They can be written in decimal (base 10), octal (base 8), or hexadecimal (base 16) format:

- **Decimal**: The default format. Example: `int dec = 42;`
<br>
- **Octal**: Preceded by a `0`. Example: `int oct = 052;` // 52 in octal is 42 in decimal
<br>
- **Hexadecimal**: Preceded by `0x` or `0X`. Example: `int hex = 0x2A;` // 2A in hexadecimal is 42 in decimal

<br>

---

<br>

## Integer Overflow

Integer overflow occurs when an integer is increased beyond its maximum value or decreased beyond its minimum value. The result is undefined behavior, which often leads to bugs. For example:

```cpp
#include <iostream>
#include <climits>

int main() {
    int x = INT_MAX;
    x = x + 1; // overflow
    std::cout << x << "\n"; // prints INT_MIN
    return 0;
}
```