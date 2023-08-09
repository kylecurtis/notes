Sets are a unique collection of items, which means every item can only occur once in a set.

<br>

---

<br>

## Creating A Set

```typescript
let numSet: Set<number> = new Set(); // Number set
let strSet: Set<string> = new Set(); // String set
// etc...
```

<br>

---

<br>

## Modifying Sets

<br>

#### Add

You can add values to the set using the `add` method:

```typescript
numSet.add(1);

// Chaining methods
numSet.add(2).add(3).add(4).add(5);
```

<br>

#### Has

You can check if a value exists in a set using the `has` method:

```typescript
numSet.has(1); // true
numSet.has(100); // false
```

<br>

#### Size

You can get the number of values in a set using the `size` property:

```typescript
numSet.size; // 5
```

<br>

#### Delete

You can remove a value from a set using the `delete` method:

```typescript
numSet.delete(5);
```

<br>

#### Clear

You can clear the set (i.e., remove all values) using the `clear` method:

```typescript
numSet.clear();
```

<br>

---

<br>

## Iterating Over Sets

<br>

#### For/of

```typescript
for (let value of numSet) {
	console.log(value);
}
```

<br>

#### forEach

```typescript
numSet.forEach(value => {
	console.log(value);
});
```

<br>

---

<br>

## Converting Set to Array

If you need to convert a set to an array, you can use the `Array.from` function or the spread operator (`...`):

```typescript
let numArray: number[] = Array.from(numSet);

// or
let numArray2: number[] = [...numSet];
```