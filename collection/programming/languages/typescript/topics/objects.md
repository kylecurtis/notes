TypeScript, being a superset of JavaScript, provides static types to JavaScript objects, which makes it easier to write robust and error-free code.

<br>

---

<br>

## Object Type Literals

The simplest way to describe an object in TypeScript is by using a type literal. A type literal is similar to an object schema. It describes the shape of an object.

```typescript
let user: {
	name: string,
	age: number
};

user = {
	name: "Dave"
	age: 32
};
```

<br>

You can also write it like this:

```typescript
let user: {
	name: string,
	age: number
} = {
	name: "Dave",
	age: 32
};
```

<br>

You may think that this syntax is ugly and/or confusing, and that is because most of the time, the type definitions in situations like this are often handled with a type alias or an `interface`.  Both will be covered in a later section.

<br>

---

<br>

## Optional Properties

TypeScript allows object properties to be optional, meaning that they may or may not exist in the object. This is denoted by appending a `?` to the property name.

```typescript
let user: {
	name: string,
	age?: number
};

user = {
	name: "Voldemort"
};
```

<br>

---

<br>

## Readonly Properties

TypeScript provides a way to mark a property as read-only. This means that once the object is created, the value of that property can't be changed.

```typescript
let user: {
	readonly name: string,
	age: number
};

user = {
	name: "Jake",
	age: 30
};

user.name = "John"; // Error
```