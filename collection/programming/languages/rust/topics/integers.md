<br>

---

<br>

Understanding the integer data types in Rust is crucial since they form the foundation for most numerical operations in various applications. Rust provides several integer types, each with its own range of values and use-cases.

<br>

---

<br>

## Integer Types in Rust

<br>

#### Signed and Unsigned Integers

Integers in Rust are divided into two main categories:

1. **Signed (`i` prefix)**: These can store both positive and negative numbers.
2. **Unsigned (`u` prefix)**: These can store only positive numbers.

<br>

#### Integer Widths

Rust provides both signed and unsigned versions for varying bit-widths: `8`, `16`, `32`, `64`, `128`, and `size` (arch-dependent).

For example:

- **Unsigned**: `u8`, `u16`, `u32`, `u64`, `u128`, `usize`
- **Signed**: `i8`, `i16`, `i32`, `i64`, `i128`, `isize`

<br>

---

<br>

## Integer Limits

<br>

#### u8

- **Min**: `u8::MIN` (0)
- **Max**: `u8::MAX` (255)

```rust
println!("Max u8: {}", u8::MAX);
println!("Min u8: {}", u8::MIN);
```

<br>

#### i8

- **Min**: `i8::MIN` (-128)
- **Max**: `i8::MAX` (127)

```rust
println!("Max i8: {}", i8::MAX);
println!("Min i8: {}", i8::MIN);
```

<br>

#### u16

- **Min**: `u16::MIN` (0)
- **Max**: `u16::MAX` (65,535)

```rust
println!("Max u16: {}", u16::MAX);
println!("Min u16: {}", u16::MIN);
```

<br>

#### i16

- **Min**: `i16::MIN` (-32,768)
- **Max**: `i16::MAX` (32,767)

```rust
println!("Max i16: {}", i16::MAX);
println!("Min i16: {}", i16::MIN);
```

<br>

#### u32

- **Min**: `u32::MIN` (0)
- **Max**: `u32::MAX` (4,294,967,295)

```rust
println!("Max u32: {}", u32::MAX);
println!("Min u32: {}", u32::MIN);
```

<br>

#### i32

- **Min**: `i32::MIN` (-2,147,483,648)
- **Max**: `i32::MAX` (2,147,483,647)

```rust
println!("Max i32: {}", i32::MAX);
println!("Min i32: {}", i32::MIN);
```

<br>

#### u64

- **Min**: `u64::MIN` (0)
- **Max**: `u64::MAX` (18,446,744,073,709,551,615)

```rust
println!("Max u64: {}", u64::MAX);
println!("Min u64: {}", u64::MIN);
```

<br>

#### i64

- **Min**: `i64::MIN` (-9,223,372,036,854,775,808)
- **Max**: `i64::MAX` (9,223,372,036,854,775,807)

```rust
println!("Max i64: {}", i64::MAX);
println!("Min i64: {}", i64::MIN);
```

<br>

#### u128

- **Min**: `u128::MIN` (0)
- **Max**: `u128::MAX` (340,282,366,920,938,463,463,374,607,431,768,211,455)

```rust
println!("Max u128: {}", u128::MAX);
println!("Min u128: {}", u128::MIN);
```

<br>

#### i128

- **Min**: `i128::MIN` (-170,141,183,460,469,231,731,687,303,715,884,105,728)
- **Max**: `i128::MAX` (170,141,183,460,469,231,731,687,303,715,884,105,727)

```rust
println!("Max i128: {}", i128::MAX);
println!("Min i128: {}", i128::MIN);
```

<br>

---

<br>

## Integer Overflow

<br>

In Rust, integer overflow behavior depends on whether you're running in debug mode or release mode.

- **Debug mode**: Overflow will cause your program to panic (crash).
- **Release mode**: Rust will perform "wrapping" arithmetic. For instance, if an `u8` exceeds `255`, it will wrap around to `0`.

<br>

---

<br>

## Integer Literals

<br>

You can represent integer literals in various formats:

- Base 10: `98_222`
- Hex: `0xff`
- Octal: `0o77`
- Binary: `0b1111_0000`
- Byte (`u8` only): `b'A'`

<br>

---

<br>

## Numeric Operations

<br>

Integers support typical arithmetic operations:

```rust
let sum = 5 + 10; // addition
let difference = 95.5 - 4.3; // subtraction
let product = 4 * 30; // multiplication
let quotient = 56.7 / 32.2; // division
let remainder = 43 % 5; // modulo
```

<br>

---

<br>
