<br>

---

<br>

## Creating Arrays

```typescript
// Number Array
let num_array: number[] = [1, 2, 3, 4];

// BigInt Array
let bigint_array: bigint[] = [100n, 200n, 300n, 400n];

// String Array
let str_array: string[] = ["North", "East", "South", "West"];

// Boolean Array
let bool_array: bool[] = [true, false];

// etc...
```

<br>

---

<br>

## Generic Array Type

The generic array type syntax uses the `Array<>` construct with the type inside the angle brackets.

```typescript
let arr: Array<number> = [1, 2, 3];
```

<br>

The two styles of declaration are equivalent, and which one you use is largely a matter of personal preference. However, generic array type syntax can be more flexible in certain situations. For example, if you have a more complex type or a union type, using the generic syntax can be easier or clearer.

```typescript
let arr: Array<number | string> = [1, "2", 3];
```

<br>

---

<br>

## Common Array Methods

<br>

```typescript
// These arrays will be used throughout this section.
let array_1: number[] = [1, 2, 3, 4];
let array_2: number[] = [5, 6, 7, 8];
```

<br>

#### push()

Adds one or more elements to the end of an array.

```typescript
array_1.push(10); // [1, 2, 3, 4, 10]
```

<br>

#### pop()

Removes the last element from an array.

```typescript
array_1.pop(); // [1, 2, 3, 4]
```

<br>

#### shift()

Removes the first element from an array.

```typescript
array_1.shift(); // [2, 3, 4]
```

<br>

#### unshift()

Adds one or more elements to the beginning of an array.

```typescript
array_1.unshift(1); // [1, 2, 3, 4]
```

<br>

#### concat()

Used to merge two or more arrays and returns a new array.

```typescript
let array_3: number[] = array_1.concat(array_2);
// [1, 2, 3, 4, 5, 6, 7, 8];
```

<br>

#### join()

Joins all elements of an array into a string.

```typescript
array_1.join(""); "1234"
```

<br>

#### slice()

Returns a shallow copy of a portion of an array.

```typescript
array_1.slice(1, 4); // [2, 3]
```

<br>

#### splice()

Changes the contents of an array by removing or replacing existing elements and/or adding new elements in place.

The `splice()` method takes three types of parameters:

1. `start`: The index at which to start changing the array.
2. `deleteCount` (optional): The number of elements in the array to remove from `start`. If `deleteCount` is omitted or if its value is greater than `array.length - start`, then all of the elements from `start` to the end of the array will be deleted.
3. `items` (optional): The elements to add to the array, beginning from `start`. If you don't specify any elements, `splice()` will only remove elements from the array.

<br>

```typescript
array_1.splice(2, 1, 8); // [1, 2, 8, 4]
```

<br>

- `2` is the `start` parameter. So, the operation will start from the third element in the array (since array indexing is zero-based).
- `1` is the `deleteCount` parameter. It means one element should be removed from the start index. So, the third element in the array (3) is removed.
- `8` is the `items` parameter. It is the new element that is added to the array at the start index. So, 8 is added at the third position in the array.

<br>

#### sort()

Used to sort the elements of an array in place and returns the array. Be careful with this method, because by default it sorts elements as strings.

```typescript
let random: number[] = [5, 3, 2, 4, 1];
random.sort(); // [1, 2, 3, 4, 5]
```

<br>

#### reverse()

Used to reverse the order of the elements in an array in place (the first array element becomes the last and the last becomes the first).

```typescript
random.reverse(); // [5, 4, 3, 2, 1]
```

<br>

#### map()

Creates a new array with the results of calling a provided function on every element in the array.

```typescript
array_1.map(x => x * x); // [1, 4, 9, 16, 25]
```

<br>

#### filter()

Creates a new array with all elements that pass the test implemented by the provided function.

```typescript
let even_numbers: number[] = array_1.filter(x => x % 2 == 0);
// [2, 4]
```

<br>

#### reduce()

Applies a function against an accumulator and each element in the array (from left to right) to reduce it to a single value.

```typescript
array_1.reduce((a, b) => a + b, 0); // 15

// This function takes 2 numbers (the first number and the number after), and adds them together. This happens through the entire array, adding all elements together in order from start to end.
```

<br>

#### forEach()

Executes a provided function once for each array element.

```typescript
array_1.forEach(x => console.log(x));

// 1
// 2
// 3
// 4
// 5
```

<br>

#### indexOf()

Returns the first (least) index of an element within the array equal to the specified value, or -1 if none is found. It starts the search at the specified index, or at the beginning if no index is specified.

```typescript
array_1.indexOf(3); // 2
array_1.indexOf(10); // -1 (not found in array)
```

<br>

---

<br>

## Iterating Over Arrays

<br>

#### For

This is one of the most common ways of iterating over an array:

```typescript
let arr: number[] = [1, 2, 3, 4, 5];

for (let i: number = 0; i < arr.length; i++) {
	console.log(arr[i]);
}
```

<br>

#### For of

This is a simpler way of iterating over an array:

```typescript
let arr: number[] = [1, 2, 3, 4, 5];

for (let value of arr) {
	console.log(value);
}
```

<br>

#### forEach

This method takes a callback function as an argument and applies it to each element of the array:

```typescript
let arr: number[] = [1, 2, 3, 4, 5];

arr.forEach(value => {
	console.log(value);
});
```

<br>

#### Map

This method also takes a callback function as an argument and applies it to each element of the array, but it returns a new array containing the results:

```typescript
let arr: number[] = [1, 2, 3, 4, 5];
let newArr: number[] = arr.map(value => value * 2);

console.log(newArr); // [2, 4, 6, 8, 10]
```

<br>

#### Reduce

This method takes a callback function and applies it to each element of the array to reduce the array to a single output value:

```typescript
let arr: number[] = [1, 2, 3, 4, 5];
let sum: number = arr.reduce((total, value) => total + value);

console.log(sum); // 15
```