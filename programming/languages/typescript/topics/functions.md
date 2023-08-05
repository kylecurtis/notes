
In TypeScript, functions work much like they do in JavaScript, but with the added benefits of static typing and additional syntax for defining them.

<br>

---

<br>

## Declare & Initialize

```typescript
function message(): void {
	console.log("Hello, TypeScript!");
}

message(); // "Hello, TypeScript!"
```

<br>

- `(): void` is where you would annotate the type of the return value(s). In this case, the return is `void` because no return statement is declared.
<br>
- in TypeScript, if a function does not return a value, you should annotate its return type as `void`. The `void` type in TypeScript is used where there is no type at all. It's commonly used as the return type of functions that do not return a value.

<br>

You can also define functions using function expressions, including arrow functions:

```typescript
let message = (): void => {
	console.log("Hello again!");
}
```

<br>

- Note: although `void` is used as a type for a function with no return, JavaScript will still output the return value as `undefined` under the hood.


<br>

```typescript
console.log(message()); // Undefined
```

<br>

---

<br>


## Function Parameters (return)

```typescript
function greet(name: string): string {
	return `Hello, ${name}!`;
}

console.log(greet("TypeScript")); // "Hello, TypeScript!"
```

<br>

- `(name: string)` means that the single input should be of type `string`.
<br>
- `(): string` means that the return value is also a string.

<br>

You can also have multiple parameters of different types:

```typescript
function about(name: string, age: number): string {
  return `Your name is ${name} and your age is ${age}!`;
}

console.log(about("",))
```

<br>

---

<br>

## Optional & Default Parameters

In TypeScript, function parameters are assumed to be required by default. But you can make a parameter optional by appending a `?` to its name:

```typescript
function greet(name?: string): string {
	if (name === undefined) {
		return "Hello, guest";
	} 
	return `Hello, ${name}`;
}

console.log(greet()); // "Hello, guest"
console.log(greet("Jack")); // "Hello, Jack"
```

<br>

You can also specify default values for parameters:

```typescript
function greet(name = "guest"): string {
	return `Hello, ${name}`;
}

console.log(greet("Jill")); // "Hello, Jill"
console.log(greet()); // "Hello, guest"
```

<br>

---

<br>

## Rest Parameters

TypeScript supports rest parameters, which allow you to pass an arbitrary number of arguments as an array:

```typescript
function greetMany(greeting: string, ...names: string[]): string {
	return greeting + ", " + names.join(" and ");
}

let message = greetMany("Hello", "Alice", "Bob", "Charlie"); 
// message is "Hello, Alice and Bob and Charlie"
```