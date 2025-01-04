## ⚖️ Maximum & Minimum Values

### 🔢 The `Math.Min` & `Math.Max` Methods

In C#, `Math.Min` and `Math.Max` are two useful static methods provided by the `System.Math` class, which allows us to easily compare two values and return the smaller or larger one, respectively.

- `Math.Min(a, b)`: This method returns the smaller of two specified numbers.
- `Math.Max(a, b)`: This method returns the larger of two specified numbers.

These methods are often used in mathematical operations, such as finding boundaries, comparing values, or determining limits.

Both methods can be used with various numeric types, such as `int`, `float`, `double`, and `decimal`, providing flexibility for different types of numerical comparisons.

`Math.Min` and `Math.Max` are particularly useful for comparisons, limiting ranges, or performing boundary checks.

#### ✏️ Example: ⚖️ Finding the Minimum and Maximum Values

```csharp
var firstNumber = 5;
var secondNumber = 15;

// Returns the smaller of 5 and 15
var minNumber = Math.Min(firstNumber, secondNumber);
Console.WriteLine($"The minimum value is: {minNumber}"); // 👈 Prints: "5"

// Returns the larger of 5 and 15
var maxNumber = Math.Max(firstNumber, secondNumber);
Console.WriteLine($"The maximum value is: {maxNumber}"); // 👈 Prints: "5"
```

**Explanation**:

- `Math.Min(firstNumber, secondNumber)` evaluates to `5`, since `5` is smaller than `15`.
- `Math.Max(firstNumber, secondNumber)` evaluates to `15`, since `15` is larger than `5`.

**Output**:

```
The minimum value is: 5
The maximum value is: 15
```

Ensure the data types of the two arguments match or are compatible. If the data types differ, we need to cast one to match the other.

#### ✏️ Example: 🔄 Comparing Values in a Range

This is a way to ensure a value stays within a given range (between `minRange` and `maxRange`).

```csharp
var minRange = 5;
var maxRange = 50;
var value = 30;

var clampedValue = Math.Min(Math.Max(value, minRange), maxRange);

Console.WriteLine($"The clamped value is: {clampedValue}");
```

**Explanation**:

- `Math.Max(value, minRange)`: Ensures that the value is not smaller than the minimum range (`5`). In this case, `30` is larger than `5`, so it remains unchanged.
- `Math.Min(..., maxRange)`: Ensures that the value is not greater than the maximum range (`50`). Since `30` is less than `50`, it remains unchanged.

**Output**:

```
The clamped value is: 30
```

### 🛠️ Why Use the `Math.Min` & `Math.Max` Methods?

The most straightforward and recommended approach to find the minimum or maximum of two numbers is by using the `Math.Min` or `Math.Max` methods. These methods provide a simple, clear line of code that directly expresses your intent.

```csharp
var firstPrice = double.Parse(Console.ReadLine());
var secondPrice = double.Parse(Console.ReadLine());

var highestPrice = Math.Max(firstPrice, secondPrice);
Console.WriteLine(highestPrice);
```

We can achieve the same result using conditional statements.

```csharp
var firstPrice = double.Parse(Console.ReadLine());
var secondPrice = double.Parse(Console.ReadLine());

var highestPrice = 0.0;

//             👇 We could use ">=" too
if (firstPrice > secondPrice)
{
	highestPrice = firstPrice;
}
else
{
	highestPrice = secondPrice;
}

Console.WriteLine(highestPrice);
```

This method uses conditional statements to compare the prices. While it's clear and easy to understand, it requires more lines of code compared to `Math.Max`, adding around 8 extra lines.

We can also achieve the same result using the conditional (ternary) operator (`?:`).

```csharp
var firstPrice = double.Parse(Console.ReadLine());
var secondPrice = double.Parse(Console.ReadLine());

//                           👇 We could use ">=" too
var highestPrice = firstPrice > secondPrice ? firstPrice : secondPrice;
Console.WriteLine(highestPrice);
```

The conditional (ternary) operator provides a compact comparison, making the code less verbose. However, it can be less readable for those not familiar with this operator.