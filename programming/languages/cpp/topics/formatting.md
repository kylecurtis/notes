C++ provides several ways to format data for output. The `<iomanip>` library is a powerful tool that provides functions to manipulate the output of data in various ways.

<br>

---

<br>

## Including the `<iomanip>` Library

To use the functions provided by the `<iomanip>` library, you need to include it at the beginning of your code:

```cpp
#include <iomanip>
```

<br>

---

<br>

## Setting Precision

The `setprecision` function sets the number of digits displayed for floating-point numbers:

```cpp
#include <iostream>
#include <iomanip>

int main() {
    double pi = 3.14159;
    std::cout << std::setprecision(3) << pi << "\n"; // prints 3.14
    return 0;
}
```

In this example, `setprecision(3)` sets the precision of `pi` to 3 digits.

<br>

---

<br>

## Fixed and Scientific Notation

The `fixed` and `scientific` manipulators change the way floating-point numbers are displayed:

- **`fixed`**: Displays the number in fixed-point notation. The number of digits after the decimal point is determined by the precision.
<br>
- **`scientific`**: Displays the number in scientific notation. The number of digits after the decimal point is determined by the precision.

<br>

```cpp
#include <iostream>
#include <iomanip>

int main() {
    double pi = 3.14159;
    std::cout << std::fixed << std::setprecision(3) << pi << "\n"; // prints 3.142
    std::cout << std::scientific << pi << "\n"; // prints 3.142e+00
    return 0;
}
```

<br>

---

<br>

## Setting Field Width

The `setw` function sets the width of the field in which the next number or string is printed. If the number or string is shorter than the field width, it is padded with spaces:

```cpp
#include <iostream>
#include <iomanip>

int main() {
    int a = 42;
    std::cout << std::setw(5) << a << "\n"; // prints "   42"
    return 0;
}
```

<br>

---

<br>

## Setting Fill Character

The `setfill` function changes the character used for padding when the field width is larger than the number or string being printed:

```cpp
#include <iostream>
#include <iomanip>

int main() {
    int a = 42;
    std::cout << std::setw(5) << std::setfill('0') << a << "\n"; // prints "00042"
    return 0;
}
```

<br>

---

<br>

## Aligning Output

The `left`, `right`, and `internal` manipulators set the alignment of the output:

- **`left`**: Aligns the output to the left of the field.
<br>
- **`right`**: Aligns the output to the right of the field. This is the default alignment.
<br>
- **`internal`**: Aligns the output to the right of the field, but aligns the sign and any base indicator to the left of the field.

<br>

```cpp
#include <iostream>
#include <iomanip>

int main() {
    int a = 42;
    std::cout << std::setw(5) << std::left << a << "\n"; // prints "42   "
    std::cout << std::setw(5) << std::right << a << "\n"; // prints "   42"
    return 0;
}
```

Remember, the `<iomanip>` library provides many more functions for more complex formatting. These are just a few examples of the most commonly used functions.