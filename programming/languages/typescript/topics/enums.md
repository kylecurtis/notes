Enums or Enumerations in TypeScript are a way of giving friendly names to a set of numeric values. They are particularly useful when you want to work with a specific set of related values, for example, days of the week, directions on a compass, or roles in a system.

<br>

---

<br>

## Creating Enums

The first member of an enum is assigned `0` by default, but can be any value.

```typescript
const enum DaysOfWeek {
	Monday,    // 0
	Tuesday,   // 1
	Wednesday, // 2
	Thursday,  // 3
	Friday,    // 4
	Saturday,  // 5
	Sunday     // 6
}
```

<br> 

You can also assign non-numeric values to enums, however, all the members must have a declared value assigned. For example:

```typescript
const enum Directions {
	North = "N",
	NorthEast = "NE",
	East = "E",
	SouthEast = "SE",
	South = "S",
	SouthWest = "SW",
	West = "W",
	NorthWest = "NW"
}
```

<br>

---

<br>

## Accessing Enum Members

```typescript
console.log(Directions.North); // "N"

// You can also access via numeric value
console.log(Directions[1]); // "NE"
```

<br>

---

<br>

