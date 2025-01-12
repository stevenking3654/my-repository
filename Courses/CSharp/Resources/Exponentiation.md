### ⏫ The "Math.Pow" Method

The `Math.Pow` method returns the specified number raised to the specified power.

The method accepts two `double` arguments: the `base` and the `exponent`, and returns the result as a `double`.

```csharp
var baseNumber = int.Parse(Console.ReadLine()); // 👈 Example: "2"
var exponent = int.Parse(Console.ReadLine()); // 👈 Example: "5"

var result = Math.Pow(baseNumber, exponent);
Console.WriteLine(result); // 👈 Prints: "32"
```

In this example, `Math.Pow(2, 5)` calculates `2 ^ 5`, which is `32`.

The same result can be calculated using loops.

```csharp
var number = int.Parse(Console.ReadLine()); // 👈 Example: "2"
var power = int.Parse(Console.ReadLine()); // 👈 Example: "5"

var result = 1;

for (int counter = 1; counter <= power; counter++)
{
	result *= number;
}

Console.WriteLine(result); // 👈 Prints: "32"
```

Initially, the `result` variable is set to `1`, because the number `1` is neutral in this operation. A product can be multiplied by `1` N times with no change in the final result.

We have the same case when summing numbers. The neutral number is `0`.

The `Math.Pow` method can handle negative exponents as well, resulting in fractions or decimals.

```csharp
var baseNumber = 2;
var exponent = -2;

var result = Math.Pow(baseNumber, exponent);
Console.WriteLine(result); // 👈 Prints: "0.25"
```

In this example, `Math.Pow(2, -2)` calculates `2 ^ (-2)`, which is `0.25`.

## ✨ Exponentiation

In mathematics, exponentiation is the process of raising a number to a specific power.

The `Math.Pow` method returns a specified number raised to the specified power.

```csharp
var baseNumber = int.Parse(Console.ReadLine()); // 👈 Example: "2"
var exponent = int.Parse(Console.ReadLine()); // 👈 Example: "5"

var result = Math.Pow(baseNumber, exponent);
Console.WriteLine(result); // 👈 Prints: "32"
```

The same result can be calculated using loops.

```csharp
var number = int.Parse(Console.ReadLine()); // 👈 Example: "2"
var power = int.Parse(Console.ReadLine()); // 👈 Example: "5"
var result = 1;

for (int counter = 1; counter <= power; counter++)
{
	result *= number;
}

Console.WriteLine(result); // 👈 Prints: "32"
```

The `Math.Pow` method can handle negative exponents, resulting in fractions or decimals.

Calculating the compound interest for a given amount of time:

```csharp
var principal = 1000;
var rate = 0.05;
var years = 3;

var compoundInterest = principal * Math.Pow(1 + rate, years);
Console.WriteLine("After " + years + " years, the compound interest is: " + compoundInterest + ".");
```