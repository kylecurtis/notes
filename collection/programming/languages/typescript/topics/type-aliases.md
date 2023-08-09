Type aliases in TypeScript are a way to create new names for existing types. You can use type aliases to avoid repeating complex types and to improve code readability. They are created using the `type` keyword.

<br>

---

<br>

## Primitive Type Alias

```typescript
type Year = number;
let current_year: Year = 2023;
```

<br>

In this example, `Year` is now an alias for the `number` type. You can use `Year` wherever you would use `number`.

<br>

---

<br>

## Complex Type Alias

```typescript
type Player = {
	name: string,
	level: number,
	next_lvl_xp: BigInt,
	beat_game: bool 
};
	
let player_1: Player = {
	name: "Player 1",
	level: 1,
	next_lvl_xp: 1000n,
	beat_game: false
};
```

<br>

---

<br>

## Union Type Alias

Type aliases can also be used with union types:

```typescript
type StringOrNumber = string | number;

let input: StringOrNumber = "Hello"; // Valid
input = 10; // Also Valid
```

<br>

---

<br>

## 