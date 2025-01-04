## 🔼 Exponentiation

Exponentiation is the mathematical operation of raising a number (**the base**) to the power of another number (**the exponent**). This operation is used extensively in calculations such as growth rates, scientific computations, and more.

In **C#**, there is no dedicated exponentiation operator, but we can perform this operation using the `Math.Pow` method.

### 🔧 The `Math.Pow` Method

The **`Math.Pow`** method in **C#** allows us to compute exponentiation. It takes two `double` arguments:

1. **The base**: The number to be raised.
2. **The exponent**: The power to which the base is raised.

The method returns the result as a `double`, making it capable of handling fractional and negative exponents as well.

#### ✏️ Example: ⏫ Raising a Number to a Positive Exponent

```csharp
var baseNumber = int.Parse(Console.ReadLine()); // 👈 Input: "2"
var exponent = int.Parse(Console.ReadLine()); // 👈 Input: "5"

var result = Math.Pow(baseNumber, exponent);
Console.WriteLine(result); // 👈 Output: "32"
```

**📖 Explanation**:

- For the input `baseNumber = 2` and `exponent = 5`, the method calculates `2 ^ 5`, resulting in `32`.

#### ✏️ Example: 🔄 Calculating Exponents Using Loops

We can manually calculate the power of a number using a `for` loop:

```csharp
var number = int.Parse(Console.ReadLine()); // 👈 Input: "2"
var power = int.Parse(Console.ReadLine()); // 👈 Input: "5"
var result = 1;

// Multiply the base `power` times
for (int counter = 1; counter <= power; counter++)
{
    result *= number;
}

Console.WriteLine(result); // 👈 Output: "32"
```

**📖 Explanation**:

- The `result` is initialized to `1` because `1` is the multiplicative identity (multiplying by `1` does not change the result).
- The loop multiplies `result` by the base `number` for each iteration, effectively raising it to the power.

#### ✏️ Example: ⏬ Handling Negative Exponents

The `Math.Pow` method also supports negative exponents, returning fractional results.

```csharp
var baseNumber = 2;
var exponent = -2;

var result = Math.Pow(baseNumber, exponent);
Console.WriteLine(result); // 👈 Output: "0.25"
```

**📖 Explanation**:

- For `baseNumber = 2` and `exponent = -2`, the calculation is equivalent to `1 / (2 ^ 2)`, which equals `0.25`.

#### ✏️ Example: 💰 Compound Interest Calculation

Exponentiation is a key part of financial calculations like compound interest, where interest is calculated on both the principal and accumulated interest.

**🧪 Formula**: `A = P * (1 + r / n) ^ (n * t)`

- **A**: The amount of money accumulated after `n` years, including interest.
- **P**: Principal amount (initial investment).
- **r**: Annual interest rate (decimal).
- **n**: Number of times interest is compounded per year.
- **t**: Time in years.

```csharp
var principal = 1000; // Initial investment (P)
var rate = 5 / 100.0; // Annual interest rate as decimal (r)
var timesCompounded = 4; // Quarterly compounding (n)
var years = 10; // Time in years (t)

// Calculate compound interest
var amount = principal * Math.Pow((1 + rate / timesCompounded), timesCompounded * years);
Console.WriteLine($"After {years} years, the total amount is {amount:F2}.");
```

**📖 Explanation**:

- For an initial investment of `1000` with a `5%` annual interest rate, compounded quarterly over `10 years`, the total amount is calculated as: `A = 1000 * (1 + 0.05 / 4) ^ (4 * 10)`.

**Output**:

```
After 10 years, the total amount is 1647.01.
```

### Conclusion

The `Math.Pow` method simplifies working with exponents, providing a concise and efficient way to perform complex calculations like fractional powers, negative exponents, and financial formulas without manually implementing loops or algorithms.