<br>

---

<br>

Understanding variables is fundamental in Rust due to the language's strong focus on safety and performance. In Rust, variables are immutable by default, which means once you set their value, you cannot change it. This immutability by default leads to more predictable code. 

<br>

---

<br>

## Variable Declaration

<br>

To declare a variable in Rust, you use the `let` keyword.

```rust
let x = 5;
```

<br>

In this case, `x` is an immutable variable bound to the value `5`. If you try to reassign a value to `x`, you'll get a compiler error.

<br>

---

<br>

## Mutable Variables

<br>

If you need to change the value of a variable after its declaration, you can use the `mut` keyword.

```rust
let mut y = 5;
y = 6; // This is fine because y is mutable
```

<br>

By using `mut`, you're explicitly signaling to the reader that this variable's value can change.

<br>

---

<br>

## Benefits of Immutability

<br>

#### Predictability
Immutable variables make the code more predictable since you're assured they won't change once set.

<br>

#### Concurrency
Immutable variables can be safely accessed by multiple threads without the need for locks or other synchronization mechanisms.

<br>

---

<br>

## When to Use Mutable Variables

<br>

While immutability is a strength of Rust, there are situations where mutable variables are necessary:

#### Changing State
Some operations, like collecting items in a vector, require a mutable reference to change the state.

<br>

#### Performance
In certain scenarios, mutating an existing variable is faster than creating a new one.

<br>

---

<br>

## Shadowing

<br>

Rust offers a unique feature called shadowing. It allows you to declare a new variable with the same name as a previous variable, effectively "shadowing" the original one.

```rust
let x = 5;
let x = x + 1; // x is now 6
let x = x * 2; // x is now 12
```

<br>

Here, we're not making the original `x` mutable. Instead, we're creating a new variable `x` that shadows the original one. Each time, it's a new immutable variable.

<br>

---

<br>

## Why Shadowing is Useful

<br>

#### Type Changes
Shadowing allows changing the type of a variable:

```rust
let spaces = "   ";
let spaces = spaces.len();
```

<br>

The first `spaces` is a `&str`, and the second one is `usize`.

<br>

#### Avoiding Mutability
By using shadowing, you can perform a series of transformations on an immutable variable without making it mutable.

<br>

---

<br>

## Constants

<br>

In addition to variables, Rust has constants that are always immutable. You declare them with the `const` keyword.

```rust
const MAX_POINTS: u32 = 100_000;
```

<br>

---

<br>

## Differences between Constants and Variables

<br>

#### Fixed Value
Constants must always have a value at compile time, and you cannot assign a runtime-computed value to them.

<br>

#### Type Annotations
Constants require type annotations.

<br>

#### Global Scope
Constants can be declared in any scope, including the global scope.

<br>

---

<br>

## Data Types in Variables

<br>

When declaring variables, Rust usually infers the type of the variable based on the value and how it's used. However, you can provide type annotations if needed.

```rust
let guess: u32 = "42".parse().expect("Not a number!");
```

In this case, `guess` is explicitly set to be of type `u32`.

<br>

---

<br>