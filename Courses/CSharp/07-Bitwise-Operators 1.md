## 🔬 Bitwise Operators

Bitwise operators provide a way to perform operations at the binary level. They work directly with the binary representation of numbers. Bitwise operators include:

- Bitwise `AND`: `&`
- Bitwise `OR`: `|`
- Bitwise `XOR`: `^`
- Bitwise `NOT`: `~`
- Bitwise Left Shift: `<<`
- Bitwise Right Shift: `>>`

The bitwise `AND` operator (`&`) performs a bitwise `AND` operation between the corresponding bits of two integers.

```csharp
int a = 5; // Binary: 0101
int b = 3; // Binary: 0011

Console.WriteLine(a & b); // 👈 Prints: "1" (Binary: 0001)
// 0 & 0 = 0
// 1 & 0 = 0
// 0 & 1 = 0
// 1 & 1 = 1
```

The bitwise `OR` operator (`|`) performs a bitwise `OR` operation between the corresponding bits of two integers.

```csharp
int x = 9; // Binary: 1001
int y = 6; // Binary: 0110

Console.WriteLine(x | y); // 👈 Prints: "15" (Binary: 1111)
// 1 | 0 = 1
// 0 | 1 = 1
// 0 | 1 = 1
// 1 | 0 = 1
```

The `XOR` operator (`^`) performs a bitwise exclusive `OR` operation. It sets a bit to `1` if the corresponding bits are different.

```csharp
int m = 12; // Binary: 1100
int n = 7; // Binary: 0111

Console.WriteLine(m ^ n); // 👈 Prints: "11" (Binary: 1011)
// 1 ^ 0 = 1
// 1 ^ 1 = 0
// 0 ^ 1 = 1
// 0 ^ 1 = 1
```

The `NOT` operator (`~`) is a unary operator that performs a bitwise `NOT` operation. It flips the bits, turning zeroes into ones and vice versa. Keep in mind that the `NOT` operator also flips the sign.

```csharp
int p = 10; // Binary: 1010

Console.WriteLine(~p); // 👈 Prints:: "-11" (Binary: 0101)
```

The `Left Shirt` operator (`<<`) shifts the bits of the left operand to the left by a specified number of positions.

```csharp
int number = 5; // Binary: 0101

int leftShift = number << 2;
Console.WriteLine(leftShift); // 👈 Prints: 20 (Binary: 101000)
```

Logically, we can interpret the result of applying the left shift operator as multiplication by 2.

The `Right Shift` operator (`>>`) shifts the bits of the left operand to the right by a specified number of positions.

```csharp
int number = 5; // Binary: 0101

int rightShift = number >> 1;
Console.WriteLine(rightShift); // 👈 Prints: 2 (Binary: 0010)
```

Logically, we can interpret the result of applying the right shift operator as multiplication by 2.

Bitwise operators are useful in low-level programming, such as working with device drivers, network protocols, or when optimizing code for performance.