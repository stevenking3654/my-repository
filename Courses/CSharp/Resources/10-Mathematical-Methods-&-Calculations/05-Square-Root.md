9## 🌱 Square Root

In mathematics, the **square root** of a number is a value that, when multiplied by itself, equals the original number.

In mathematics, the square root of `x` is denoted by `√x`.

### 🔧 The `Math.Sqrt` Method

In **C#**, the `Math.Sqrt()` method is used to calculate the square root of a number.  
It accepts a single `double` argument and returns the square root as a floating-point value.

#### ✏️ Example: 🌱 Basic Square Root Calculation

```csharp
var number = int.Parse(Console.ReadLine()); // 👈 Input: "9"

var squareRoot = Math.Sqrt(number);
Console.WriteLine(squareRoot); // 👈 Output: "3"
```

**📖 Explanation**:

- `Math.Sqrt(number)`: Returns `3.0` (`3 * 3 = 9`). For an input of `9`, the method calculates `√9`, which is `3.0`.

#### ✏️ Example: 🚧 Handling Edge Cases

The square root of a negative number is not defined in the set of real numbers. In **C#**, attempting to calculate it with `Math.Sqrt` will return `NaN` (**Not a Number**). 

```csharp
var zero = 0;
var negativeNumber = -9;

Console.WriteLine(Math.Sqrt(zero)); // 👈 Output: "0"
Console.WriteLine(Math.Sqrt(negativeNumber)); // 👈 Output: "NaN"
```

**📖 Explanation**:

- `Math.Sqrt(zero)` returns `0` because `√0 = 0`.
- `Math.Sqrt(negativeNumber)` returns `NaN` as the square root of negative numbers is undefined in real numbers.

#### ✏️ Example: 🔢 Non-Perfect Squares

For numbers that are not perfect squares, `Math.Sqrt` returns a floating-point approximation of the square root.

```csharp
var number = 20;

var squareRoot = Math.Sqrt(number);
Console.WriteLine(squareRoot); // 👈 Output: "4.47"
```

**📖 Explanation**:

- The square root of `20` is approximately `4.47`.

#### ✏️ Example: 📐 Pythagoras' Theorem

The square root is essential for calculating the hypotenuse of a right triangle using **Pythagoras' Theorem**.

```csharp
var a = 3;
var b = 4;
var c = Math.Sqrt(Math.Pow(a, 2) + Math.Pow(b, 2));

Console.WriteLine($"Hypotenuse: {c}."); // 👈 Output: "5"
```

**📖 Explanation**:

- The square root is applied to the sum of the squares of the two sides (`3^2 + 4^2 = 25`), resulting in `√25 = 5`.

#### ✏️ Example: 📏 Calculating Distance Between Two Points

To find the distance between two points `(x₁, y₁)` and `(x₂, y₂)`, subtract the coordinates of one point from the other, square each difference, add the results together, and then take the square root of that sum.

```csharp
// Coordinates of the first point
var x1 = 1;
var y1 = 2;

// Coordinates of the second point
var x2 = 4;
var y2 = 6;

var distance = Math.Sqrt(Math.Pow(x2 - x1, 2) + Math.Pow(y2 - y1, 2));
Console.WriteLine($"The distance between the points is: {distance}");
```

**Explanation**:

- Subtract the coordinates to find the differences, square them, sum the squares, and then take the square root to find the distance.

**Output**:

```
The distance between the points is: 5
```

### Conclusion

The `Math.Sqrt` method is versatile and essential for mathematical calculations involving roots. It simplifies complex computations like hypotenuse length, geometric distances, and real-world applications where precision is key.