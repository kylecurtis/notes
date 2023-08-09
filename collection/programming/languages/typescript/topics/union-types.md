Union types are a powerful way in TypeScript to describe values that can be one of several types. We use the vertical bar (`|`) to separate each type, hence the name "union type".

<br>

---

<br>

## Basic Usage

```typescript
let myVar: string | number | boolean;

myVar = "Hello"; // Valid
myVar = 32; // Valid
myVar = true; // Valid
```

<br>

---

<br>

## Narrowing

Narrowing in TypeScript refers to the process of refining the type of a variable, making it more specific based on certain conditions or checks. When dealing with union types, narrowing can be particularly useful.

```typescript
type StringOrNumber = string | number;

function process(input: StringOrNumber) {
	if (typeof input === "string") {
		// Input can now use string methods
		console.log(input.toUpperCase()); 
	} else {
		// Input can now use number methods
		console.log(input.toFixed(2));
	}
}

process("hello"); // HELLO
process(42); // 42.00
```