## 🎯 Rounding Numbers

### 🎯 Rounding Numbers

Rounding is a common operation where a number is approximated to a specified number of digits, especially when dealing with currency or measurements.

Rounding could be used to present numbers in a more manageable form, especially when dealing with real-world scenarios that require precision.

C# offers multiple methods for rounding, each suited for different needs.

### 🔽 The "Math.Floor" Method

The `Math.Floor` method returns the largest integral value less than or equal to the specified number.

```csharp
var realNumber = double.Parse(Console.ReadLine()); // 👈 Example: "7.8"

var roundedValue = Math.Floor(realNumber);
Console.WriteLine(roundedValue); // 👈 Prints: "7"
```

### 🔼 The "Math.Ceiling" Method

The `Math.Ceiling` method returns the smallest integral value that is greater than or equal to the specified number.

```csharp
var realNumber = double.Parse(Console.ReadLine()); // 👈 Example: "7.24

var roundedValue = Math.Ceiling(realNumber);
Console.WriteLine(roundedValue); // 👈 Prints: "8"
```





// TODO: working with negative numbers






`Math.Floor` and `Math.Ceiling` behave differently for negative numbers. `Math.Floor` moves further away from zero (e.g., `-4.1` to `-5`), while `Math.Ceiling` moves closer to zero (e.g., `-4.1` to `-4`).

The `Math.Round` method rounds a decimal value to the nearest integer or a specified number of fractional digits using the specified rounding convention.

```csharp
var realNumber = double.Parse(Console.ReadLine()); // 👈 Example: "3.14159"

//            Number of fractional digits 👇
var roundedNumber = Math.Round(realNumber, 2);
Console.WriteLine(roundedNumber); // 👈 Prints: "3.14"
```

It can also specify how to handle midpoint values (numbers exactly halfway between two possible rounded values).

```csharp
var realNumber = double.Parse(Console.ReadLine());

var roundedNumber = Math.Round(realNumber, 2, MidpointRounding.AwayFromZero);
Console.WriteLine(roundedNumber);
```

The `Math.Round` method supports two rounding conventions for handling midpoint values:
- Rounding away from zero: This form of rounding is represented by `MidpointRounding.AwayFromZero`;
- Rounding to nearest even, or banker's rounding: This form of rounding is represented by `MidpointRounding.ToEven`.

The `Math.Truncate` method returns the number that remains after any fractional digits have been discarded.

```csharp
var realNumber = double.Parse(Console.ReadLine()); // 👈 Example: "6.8"

var doubleNumber = Math.Truncate(realNumber); // 👈 Data Type: System.Double / double
Console.WriteLine(doubleNumber); // 👈 Prints: "6"
```

We can think of it as casting to an integer.

```csharp
var realNumber = double.Parse(Console.ReadLine()); // 👈 Example: "6.8"

var integerNumber = (int)(realNumber); // 👈 Data Type: System.Int32 / int
Console.WriteLine(integerNumber); // 👈 Prints: "6"
```

#### ✏️ Example: Rounding Numbers in Financial Applications

When dealing with financial transactions, it is common to round amounts to two decimal places.

```csharp
var amount = 123.456;
var roundedAmount = Math.Round(amount, 2);

Console.WriteLine(roundedAmount); // 👈 Prints: "123.46"
```

## 🎯 Rounding Numbers

Rounding is a fundamental mathematical operation that involves approximating a number to a specified number of significant digits (**precision**).

Rounding is essential in various fields, including finance, engineering, and data analysis, where precise numerical representation and manageable formats are often required.

Rounding significantly improves data interpretation and enhances readability.

In C#, multiple methods are available for rounding numbers, each suited for specific requirements and scenarios.

## 🎯 Rounding Numbers

Rounding could be used to present numbers in a more manageable form, especially when dealing with real-world scenarios that require precision.

The `Math.Floor` method returns the largest integral value less than or equal to the specified number.

```csharp
var realNumber = double.Parse(Console.ReadLine()); // 👈 Example: "7.64"

var roundedValue = Math.Floor(realNumber);
Console.WriteLine(roundedValue); // 👈 Prints: "7"
```

The `Math.Ceiling` method returns the smallest integral value that is greater than or equal to the specified number.

```csharp
var realNumber = double.Parse(Console.ReadLine()); // 👈 Example: "7.24

var roundedValue = Math.Ceiling(realNumber);
Console.WriteLine(roundedValue); // 👈 Prints: "8"
```

The `Math.Round` method rounds a decimal value to a specified number of fractional digits using the specified rounding convention.

```csharp
var realNumber = double.Parse(Console.ReadLine());

//                                        👇 Number of fractional digits
var roundedNumber = Math.Round(realNumber, 2, MidpointRounding.AwayFromZero);
Console.WriteLine(roundedNumber);
```

The `Math.Round` method supports two rounding conventions for handling midpoint values:
- Rounding away from zero: This form of rounding is represented by `MidpointRounding.AwayFromZero`;
- Rounding to nearest even, or banker's rounding: This form of rounding is represented by `MidpointRounding.ToEven`.

The `Math.Truncate` method returns the number that remains after any fractional digits have been discarded.

```csharp
var realNumber = double.Parse(Console.ReadLine()); // 👈 Example: "6.8"

var doubleNumber = Math.Truncate(realNumber); // 👈 Data Type: System.Double / double
Console.WriteLine(doubleNumber); // 👈 Prints: "6"
```

```csharp
var realNumber = double.Parse(Console.ReadLine()); // 👈 Example: "6.8"

var integerNumber = (int)(realNumber); // 👈 Data Type: System.Int32 / int
Console.WriteLine(integerNumber); // 👈 Prints: "6"
```









### ✂️ The `Math.Truncate` Method

The `Math.Truncate` method returns the integer part of a number by discarding any fractional digits. It is a way to reduce a floating-point number to its whole number representation without any form of rounding.

#### ✏️ Example: ✂️ Truncating a Floating-Point Number

```csharp
var realNumber = double.Parse(Console.ReadLine()); // 👈 Input: "6.8"

var doubleNumber = Math.Truncate(realNumber);
Console.WriteLine(doubleNumber); // 👈 Output: "6"
```

In C#, both the `Math.Truncate` method and casting to an integer are used to remove the fractional part of a floating-point number, but they differ in the data type of the final result.

```csharp
var realNumber = double.Parse(Console.ReadLine()); // 👈 Input: "6.8"

var integerNumber = (int)(realNumber);
Console.WriteLine(integerNumber); // 👈 Output: "6"
```

Casting a floating-point number to an integer directly converts it to an `int`, resulting in a loss of any fractional part and changing the data type.

The `Math.Truncate` method returns a `double` (or `decimal` if used with decimal types), preserving the original data type while discarding fractions.

### 🔽 The `Math.Floor` Method

The `Math.Floor` method always rounds a floating-point number down to the nearest integer less than or equal to the given value. This method is particularly useful when we need to ensure values do not exceed their truncated result.

#### ✏️ Example: 🔽 Rounding Down a Floating-Point Number

```csharp
var realNumber = double.Parse(Console.ReadLine()); // 👈 Input: "7.8"

var roundedValue = Math.Floor(realNumber);
Console.WriteLine(roundedValue); // 👈 Output: "7"
```

### 🔼 The `Math.Ceiling` Method

The `Math.Ceiling` method rounds a floating-point number up to the smallest integer greater than or equal to the given value. This method is ideal for cases where overestimation is preferable.

#### ✏️ Example: 🔼 Rounding Up a Floating-Point Number

```csharp
var realNumber = double.Parse(Console.ReadLine()); // 👈 Input: "7.24"

var roundedValue = Math.Ceiling(realNumber);
Console.WriteLine(roundedValue); // 👈 Output: "8"
```

### 🔄 The `Math.Round` Method

The `Math.Round` method rounds a decimal value to the nearest integer or to a specified number of fractional digits according to defined rounding conventions. This method is highly configurable.

#### ✏️ Example: 🔄 Rounding a Floating-Point Number

```csharp
var realNumber = double.Parse(Console.ReadLine()); // 👈 Input: "3.14159"

//            Number of fractional digits 👇
var roundedNumber = Math.Round(realNumber, 2);
Console.WriteLine(roundedNumber); // 👈 Output: "3.14"
```

#### ✏️ Example: 📜 Rounding Conventions

The `Math.Round` method can also specify how to handle midpoint values (numbers exactly halfway between two possible rounded values, e.g. `0.5`).

By default, the `Math.Round` method uses the "banker's rounding" (to the nearest even number) for midpoint values. This behavior can be customized:

```csharp
var realNumber = double.Parse(Console.ReadLine()); // 👈 Input: "2.5"

var roundedNumber = Math.Round(realNumber, 0, MidpointRounding.AwayFromZero);
Console.WriteLine(roundedNumber); // 👈 Output: "3"
```

The `Math.Round` method supports two rounding conventions for handling midpoint values:

- **MidpointRounding.AwayFromZero:** Rounds midpoint values (e.g., `0.5`) away from zero.
- **MidpointRounding.ToEven (default):** Rounds midpoint values to the nearest even number.

### ⚖️ Rounding Negative Numbers

`Math.Floor` and `Math.Ceiling` behave differently for negative numbers.

Specifically, `Math.Floor` moves further away from zero (e.g., `-4.1` becomes `-5`), while `Math.Ceiling` moves closer to zero (e.g., `-4.1` becomes `-4`).