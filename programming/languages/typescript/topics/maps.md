  
The `Map` object in TypeScript, like in JavaScript, holds key-value pairs and remembers the original insertion order of the keys. This data structure is useful when we need to keep the original insertion order of the keys and want to store data in key-value pairs. The keys of a Map can be of any type: functions, objects, or any primitive types.

<br>

---

<br>

## Using Maps

```typescript
let myMap = new Map();

// Specify types
let myMap = new Map<number, string>([
	[1, "one"],
	[2, "two"]
]);
```

<br>

---

<br>

## Adding Values to Maps

You can add values to the map using the `set` method:

```typescript
myMap.set(3, "three");
myMap.set(4, "four");
```

<br>

---

<br>

## Getting Values from Maps

You can get a value from a map using the `get` method:

```typescript
console.log(myMap.get(1)); // "one" 
console.log(myMap.get(2)); // "two" 
```

<br>

---

<br>

## Checking If Key Exists

You can check if a key exists in a map using the `has` method:

```typescript
console.log(myMap.has(1)); // true
console.log(myMap.has(10)); // false
```

<br>

---

<br>

## Removing A Value

You can remove a value from a map using the `delete` method:

```typescript
myMap.delete(1); // Removes the key-value pair with key 1
```

<br>

---

<br>

## Getting The Size of Map

You can get the number of key-value pairs in a map using the `size` property:

```typescript
console.log(myMap.size); // 3
```

<br>

---

<br>

## Clearing A Map

You can clear the map (i.e., remove all key-value pairs) using the `clear` method:

```typescript
myMap.clear();
```

<br>

---

<br>

## Iterating Over A Map

<br>

#### For of

You can iterate over the keys and values in a map using a `for...of` loop:

```typescript
for (let [key, value] of myMap) {
    console.log(key, value);
}
```

<br>

#### For each

Alternatively, you can use the `forEach` method:

```typescript
myMap.forEach((value, key) => {
    console.log(key, value);
});
```