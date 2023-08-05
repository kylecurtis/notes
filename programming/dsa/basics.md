## Big-O Time Complexity

- O(N) -> Algorithm will grow linearly based on input.

<br>

---

<br>

#### What is the Big-O for this function?

```typescript
function str_loop(n: string): number {
	let sum: number = 0;
	for (let i = 0; i < n.length; ++i) {
		sum += n.charCodeAt(i);
	}
	return sum;
}
```

<br>

- This function is O($n$).
<br>
- To find the Big O, look out for loops (where does it loop over the input).

<br>

---

<br>

#### What is the Big-O for this function?

```typescript
function str_loop(n: string): number {
	let sum: number = 0;
	for (let i = 0; i < n.length; ++i) {
		sum += n.charCodeAt(i);
	}
	
	for (let i = 0; i < n.length; ++i) {
		sum += n.charCodeAt(i);
	}
	
	return sum;
}
```

<br>

- This function is also O($n$).
<br>
- Constants get dropped. 
<br>
- Since there are 2 loops -> O($2n$), the constant is dropped leaving O($n$).

<br>

---

<br>

#### What is the Big-O for this function?

```typescript
function str_loop(n: string): number {
	let sum = 0;
	for (let i = 0; i < n.length; ++i) {
		const charCode = n.charCodeAt(i);
		if (charCode === 69) {
			return sum; // Capital "E"
		}
		sum += charCode;
	}

	return sum;
}
```

<br>

- This function is O($n$).
<br>
- Consider worst case. Any string with "E" in it will terminate early (unless "E" is the last item).

<br>

---

<br>

#### What is the Big-O for this function?

```typescript
function str_loop(n: string): number {
	let sum: number = 0;
	for (let i = 0; i < n.length; ++i) {
		for (let j = 0; j < n.lenth; ++j) {
			sum += charCode;
		}
	}
	return sum;
}
```

- This function is O($n^2$)

<br>

---

<br>

#### What is the Big-O for this function?

```typescript
function str_loop(n: string): number {
	let sum: number = 0;
	for (let i = 0; i < n.length; ++i) {
		for (let j = 0; j < n.lenth; ++j) {
			for (let k = 0; k < n.length; ++k) {
				sum += charCode;
			}	
		}
	}
	return sum;
}
```

- This function is O($n^3$)

<br>

---

<br>

#### O(n log n)

- Quicksort algorithm (explained here <- Turn into link).

<br>

---

<br>

#### O(log n)

- Binary Search Trees

<br>

---

<br>

## Big O Chart

![big-o-chart](big-o-chart.png)


<br>

---

<br>

## Important Concepts

<br>

1. Growth is with respect to the input.
<br>
2. Constants are usually dropped.
<br>
3. Worst case is *usually* the way we measure.


















