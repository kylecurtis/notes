<br>

---

<br>

## <u>General Variable Rules</u>

- Can only start with a letter (or underscore in some cases).
- Can only contain letters, digits or underscores.
- Should be descriptive and meaningful names.
- Use consistent naming conventions for maintainability.

<br>

## <u>Naming Conventions</u>

- **camelCase**: Each word is capitalized, except for the first.
- **PascalCase**: Each word is capitalized (recommended for functions).
- **snake_case**: Each word is separated by underscores (recommended).
- **SCREAMING_SNAKE_CASE**: Used for enums and constants (recommended).

<br>

```c
#include <stdio.h>      // Standard Input/Ouput
#include <stdlib.h>     // Standard Library (Used for return EXIT_SUCCESS)

int main(void) {
	// Variable (int)
	// Variables are mutable by default
	int num_of_bits = 32;

	// Const (int)
	// Constants are immutable and cannot change
	const int BITS_PER_BYTE = 8;

	return EXIT_SUCCESS;
}
```