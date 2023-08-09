Tuples are a special type in TypeScript that allow you to specify an array where the type of a fixed number of elements is known, but does not have to be the same for each element. This can be very useful for representing things like pairs of values, or parameter lists for functions, or even more complex data structures.

<br>

---

<br>


## Creating Tuples

```typescript
// Tuple example (X/Y coordinates)
let coordinate: [number, number] = [10, 20];
```

<br>

 You can also use a tuple to store an array of values, however, enums are better for constant values.
 
```typescript
let zip_codes: [number, string][] = [
	[33162, "Miami"],
	[60606, "Chicago"],
	[10007, "New York City"],
	[97210, "Portland"]
];
```

<br>

---

<br>

## Accessing Tuple Elements

```typescript
console.log(coordinate[0]); // 10
console.log(coordinate[1]); // 20

console.log(zip_codes[0][0]); // 33162
console.log(zip_codes[0][1]); // "Miami"
```

<br>

---

<br>

## Optional Elements

```typescript
let full_coordinates: [number, number, number?] = [10, 20]; 

// Third element is optional, but can be added.
let full_coordinates = [10, 20, 0];
```

<br>

---

<br>

## Considerations

In TypeScript, you can use some of the common array methods with tuples, but there are limitations due to the fact that tuples have a fixed number of elements of specific types.

The `push()` method, for example, can be problematic. You'll get a TypeScript error. That's because the tuple is expected to have exactly two elements: a number and a string. By pushing another element onto the tuple, you're making it have three elements, which is not allowed.

However, some array methods can be used safely with tuples. These are generally the methods that don't change the length of the array, such as `indexOf()`, `join()`, and `toString()`.

These methods work because they don't attempt to change the structure of the tuple. They just read the existing elements and do something with them. If you try to use a method that changes the length or types of the elements, such as `push()`, `pop()`, `shift()`, `unshift()`, or `splice()`, TypeScript will prevent it.