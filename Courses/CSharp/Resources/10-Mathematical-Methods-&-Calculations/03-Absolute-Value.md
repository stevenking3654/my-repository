## 📏 Absolute Value

In mathematics, the **absolute value** (or **modulus**) of a number represents its distance from zero on the number line, ignoring its direction. It is always non-negative, regardless of whether the input number is positive or negative.

The absolute value of a number `x` is written as `|x|` and defined as:

- If `x >= 0`, then `|x| = x` (the number itself).
- If `x < 0`, then `|x| = -x` (the negation of the number).

In essence, the absolute value "flips" negative numbers to positive while leaving positive numbers and zero unchanged. This concept is particularly useful in measuring distances, differences, or values where the sign does not matter.

### 🔧 The `Math.Abs` Method

In **C#**, the `Math.Abs` method is used to compute the absolute value of numbers. It is part of the `System` namespace and supports various numeric types like `int`, `double`, `float`, `long`, and `decimal`.

#### ✏️ Example: 📏 Basic Absolute Value Calculation

```csharp
var x = int.Parse(Console.ReadLine()); // 👈 Input: "-5"

var absoluteValue = Math.Abs(x);
Console.WriteLine(absoluteValue); // 👈 Output: "5"
```

**📖 Explanation**:

- For the input `-5`, the `Math.Abs` method returns `5` because the absolute value disregards the sign of the number.

#### ✏️ Example: 🧮 Calculating Absolute Value Using a Conditional Operator

The absolute value can also be calculated manually using the conditional operator (`?:`).

```csharp
var x = int.Parse(Console.ReadLine()); // 👈 Input: "-5"

// If x >= 0, return x; otherwise, return -x
var absoluteValue = x >= 0 ? x : -x;
Console.WriteLine(absoluteValue); // 👈 Output: "5"
```

**📖 Explanation**:

- If `x` is greater than or equal to `0`, it is returned as-is.  
- Otherwise, the negation of `x` is returned.

#### ✏️ Example: 🔢 Check if a Number is Positive

We can use `Math.Abs` to verify if a number is non-negative.

```csharp
var x = int.Parse(Console.ReadLine()); // 👈 Input: "5"

// If x equals its absolute value, it is positive or zero
var isPositive = x == Math.Abs(x);

Console.WriteLine(isPositive); // 👈 Output: "True"
```

**📖 Explanation**:

- For positive numbers and `0`, `x` is equal to `Math.Abs(x)`, so `isPositive` is `true`.  
- For negative numbers, `Math.Abs(x)` returns the negated value, so `isPositive` is `false`.

#### ✏️ Example: 🌡️ Calculating Temperature Difference

The `Math.Abs` method is particularly useful for finding the absolute difference between two values, such as temperatures.

```csharp
var firstDayTemperature = -5;
var secondDayTemperature = 10;

// Calculate the absolute difference between two temperatures
var difference = Math.Abs(firstDayTemperature - secondDayTemperature);
Console.WriteLine("Temperature difference: " + difference); // 👈 Output: "15"
```

**📖 Explanation**:

- `firstDayTemperature - secondDayTemperature` gives the difference between the two temperatures (`-5 - 10 = -15`).  
- `Math.Abs` ensures the result is non-negative, returning `15`.

### 🎉 Conclusion

The `Math.Abs` method simplifies working with values where the sign is irrelevant, such as distances, differences, or comparisons.