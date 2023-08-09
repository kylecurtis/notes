----

## <u>Integer Basics</u>

- Integers are signed and unsigned whole numbers that do not contain decimals.
- Signed:   Contains a negative sign (-20, -32, etc.).
- Unsigned: Contains only positive numbers (20, 32, etc.).

<br>


**Using Integers**
```c
int main(void) {
	int negative_num = -100;            // Signed
    unsigned int positive_num = 32U;    // Unsigned

	printf("Negative number: %d\n", negative_num);
    printf("Positive number: %u\n", positive_num);
}
```

<br>

--- 
 
<br> 

## Short Int

- 16-bit / 2-byte integer.
- Signed by default, unless prefixed with `unsigned`.


| Type | Format ID | Size | Min | Max |
| :--- | :---: | :---: | :---: | :---: |
| Signed Short | %hd | 2 bytes | SHRT_MIN | SHRT_MAX |
| Unsigned Short | %hu | 2 bytes | 0 | USHRT_MAX |

<br>

**Using Short**
```c
short short_num = -10;
printf("Short num: %hd\n", short_num);

unsigned short ushort_num = 10;
printf("Ushort num: %hu\n", ushort_num);
```

<br>

**Short MIN/MAX**
```c
// UNSIGNED SHORT INT
 printf("UShort min: 0\n"); // 0
 printf("UShort max: %hu\n", USHRT_MAX);

 // SIGNED SHORT INT
 printf("Short min: %hd\n", SHRT_MIN);
 printf("Short max: %hd\n", SCHAR_MAX);
```

<br>

---

<br>


## Int

- 32-bit / 4-byte integer.
- Signed by default, unless prefixed with `unsigned`.

| Type | Format ID | Size | Min | Max |
| :--- | :---: | :---: | :---: | :---: |
| Signed Int | %d | 4 bytes | INT_MIN | INT_MAX |
| Unsigned Int | %u | 4 bytes | 0 | UINT_MAX | 

<br>

**Using Int**
```c
// SIGNED INT
int int_num = -100;
printf("Int num: %d\n", int_num);

// UNSIGNED INT 
unsigned int uint_num = 100;
printf("UInt num: %u\n", uint_num);
```

<br>

**Int MIN/MAX**
```c
// UNSIGNED INT
printf("UInt min: 0\n"); // 0
printf("UInt max: %u\n", UINT_MAX);

// SIGNED INT
printf("Int min: %d\n", INT_MIN);
printf("Int max: %d\n", INT_MAX);
```


<br>

---

<br>

| Type | Format ID | Size | Min | Max |
| :---: | :---: | :---: | :---: | :---: |

| Type | Format ID | Size | Min | Max |
| :---: | :---: | :---: | :---: | :---: |