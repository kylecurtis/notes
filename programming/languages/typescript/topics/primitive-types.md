---
tags: Number, BigInt, String, Boolean
---

<br>

---

<br>

## Number

Used for numeric values. In TypeScript, all numbers are floating point values. TypeScript supports decimal, hexadecimal, binary and octal literals.

```typescript
let small_num: number = -123;

// Larger numbers can be seperated by underscores 
// similar to commas for readability.
let large_num: number = 100_000;

// Numbers can be represented in various ways:
let decimal: number = 6.0; // Decimal
let hex: number = 0xf00d; // Hexadecimal
let binary: number = 0b1010; // Binary
let octal: number = 0o744; // Octal
```

<br>

## Number Methods

<br>

#### toString

arg: (radix)

Converts a number to a string and returns the string.

```typescript
let num = 15;
console.log(num.toString()); // 15
console.log(num.toString(2)); // 1111 - binary representation
```

<br>

#### toFixed

arg: (digits)

Formats a number using fixed-point notation.

```typescript
let num = 10.578;
console.log(num.toFixed(2)); // 10.58
```

<br>

#### toExponential

arg: (fractionDigits)

Returns a string representing the number in exponential notation.

```typescript
let num = 76.3;
console.log(num.toExponential(4)); // 7.6300e+1
```

<br>

#### toPrecision

arg: (precision)

Returns a string representing a Number object in fixed-point or exponential notation rounded to precision significant digits.

```typescript
let num = 13.3714;
console.log(num.toPrecision(3)); // 13.4
```

<br>

#### valueOf

Returns the primitive value of a Number object.

```typescript
let num = new Number(10);
console.log(num.valueOf()); // 10
```

<br>

#### parseFloat

arg: (string)

Parses a string argument and returns a floating point number.

```typescript
console.log(Number.parseFloat("10.33")); // 10.33
```

<br>

#### parseInt

arg: (string, radix)

Parses a string argument and returns an integer of the specified radix or base.

```typescript
console.log(Number.parseInt("10", 10)); // 10
```

<br>

#### isFinite

arg: (number)

Determines whether the passed value is a finite number.

```typescript
console.log(Number.isFinite(10)); // true
console.log(Number.isFinite(Infinity)); // false
```

<br>

#### isInteger

arg: (number)

Determines whether the passed value is an integer.

```typescript
console.log(Number.isInteger(10)); // true
console.log(Number.isInteger(10.5)); // false
```

<br>

#### isNaN

arg: (number)

Determines whether the passed value is NaN and its type is Number.

```typescript
console.log(Number.isNaN(NaN)); // true
console.log(Number.isNaN(10)); // false
```

<br>

#### isSafeInteger

arg: (number)

Determines whether the provided value is a number that is a safe integer.

```typescript
console.log(Number.isSafeInteger(10)); // true
console.log(Number.isSafeInteger(Math.pow(2, 53))); // false
```

<br>

---

<br>

## BigInt

Bigint is used to represent whole numbers larger than $2^{53} - 1$, which is the largest number JavaScript can reliably represent with the `Number` primitive and represented by the `Number.MAX_SAFE_INTEGER` constant.

```typescript
let huge_num: bigint = 123_456_789n; // Don't forget the n suffix
```

<br>

## BigInt Methods

<br>

#### Considerations

Unlike `Number`, `BigInt` does not have methods like `toFixed`, `toExponential`, `toPrecision`, `parseFloat`, `parseInt`, `isFinite`, `isInteger`, `isNaN`, `isSafeInteger` because BigInt deals with integers only and is not intended to replace the Number type but complement it.

<br>

---

<br>

## String

Represents a sequence of characters, which can be defined using either single quotes (`'`), double quotes (`"`), or backticks (```). Backticks are used to define template expressions.

```typescript
let message: string = "Hello, TypeScript!";
```

<br>

## String Methods

<br>

#### charAt

arg: (index)

Returns the character at the specified index.

```typescript
let str = "Hello, world!";
console.log(str.charAt(1)); // "e"
```

<br>

#### concat

arg: (...strings)

Concatenates the string arguments to the calling string and returns a new string.

```typescript
let str1 = "Hello";
let str2 = ", world!";
console.log(str1.concat(str2)); // "Hello, world!"
```

<br>

#### indexOf

arg: (searchValue, fromIndex)

Returns the index within the calling String object of the first occurrence of the specified value, starting the search at `fromIndex`. Returns -1 if the value is not found.

```typescript
let str = "Hello, world!";
console.log(str.indexOf("world")); // 7
console.log(str.indexOf("world", 10)); // -1
```

<br>

#### lastIndexOf

arg: (searchValue, fromIndex)

Returns the index within the calling String object of the last occurrence of the specified value, searching backwards from `fromIndex`. Returns -1 if the value is not found.

```typescript
let str = "Hello, world, world!";
console.log(str.lastIndexOf("world")); // 15
```

<br>

#### replace

arg: (regex|substr, newSubStr|function)

Returns a new string with some or all matches of a pattern replaced by a replacement.

```typescript
let str = "Hello, world!";
console.log(str.replace("world", "TypeScript")); // "Hello, TypeScript!"
```

<br>

#### slice

arg: (beginIndex, endIndex)

Extracts a section of the string and returns it as a new string, without modifying the original string.

```typescript
let str = "Hello, world!";
console.log(str.slice(7, 12)); // "world"
```

<br>

#### split

arg: (separator, limit)

Splits a String object into an array of strings by separating the string into substrings, using a specified separator string to determine where to make each split.

```typescript
let str = "Hello, world!";
console.log(str.split(' ')); // ["Hello,", "world"!]
```

<br>

####  substr

arg: (start, length)

Returns the characters in a string beginning at the specified location through the specified number of characters.

```typescript
let str = "Hello, world!";
console.log(str.substr(7, 5)); // "world"
```

<br>

#### toLowerCase

Returns the calling string value converted to lowercase.

```typescript
let str = "Hello, World!";
console.log(str.toLowerCase()); // "hello, world!"
```

<br>

#### toUpperCase

Returns the calling string value converted to uppercase.

```typescript
let str = "Hello, World!";
console.log(str.toUpperCase()); // "HELLO, WORLD!"
```


<br>

#### trim

Trims whitespace from both ends of the string.

```typescript
let str = "   Hello, world!   ";
console.log(str.trim()); // "Hello, world!"
```

<br>

#### charCodeAt

arg: (index)

Returns a number that is the Unicode value of the character at the given index.

```typescript
let str = "Hello, world!";
console.log(str.charCodeAt(1)); // 101
```

<br>

#### includes

arg: (searchString, position)

Determines whether one string may be found within another string, returning `true` or `false` as appropriate.

```typescript
let str = "Hello, world!";
console.log(str.includes("world")); // true
```

<br>

#### startsWith

arg: (searchString, position)

Determines whether a string begins with the characters of a specified string, returning `true` or `false` as appropriate.

```typescript
let str = "Hello, world!";
console.log(str.startsWith("Hello")); // true
```

<br>

#### endsWith

arg: (searchString, length)

Determines whether a string ends with the characters of a specified string, returning `true` or `false` as appropriate.

```typescript
let str = "Hello, world!";
console.log(str.endsWith("!")); // true
```

<br>

#### repeat

arg: (count)

Constructs and returns a new string which contains the specified number of copies of the string on which it was called, concatenated together.

```typescript
let str = "Hello, world!";
console.log(str.repeat(2)); // "Hello, world!Hello, world!"
```

<br>

#### padStart

arg: (targetLength, padString)

Pads the current string from the start with a given string and returns a new string of a given length.

```typescript
let str = "5";
console.log(str.padStart(4, "0")); // "0005"
```

<br>

#### padEnd

arg: (targetLength, padString)

Pads the current string from the end with a given string and returns a new string of a given length.

```typescript
let str = "5";
console.log(str.padEnd(4, "0")); // "5000"
```

<br>

---

<br>

## Boolean

Represents a logical entity and can have two values: `true` or `false`

```typescript
let is_true: bool = true;
let is_false: bool = false;
```

<br>

---

<br>