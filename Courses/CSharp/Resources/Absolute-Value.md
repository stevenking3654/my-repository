## 📏 Absolute Value

In mathematics, the absolute value or modulus of a real number is the non-negative value of the number without regard to its sign.

It is denoted by `|x|`, where `x` is a real number.

The `Math.Abs` method returns the non-negative value of `x`.

```csharp
var x = int.Parse(Console.ReadLine()); // 👈 Example: "-5"

var absoluteValue = Math.Abs(x);
Console.WriteLine(absoluteValue); // 👈 Prints: "5"
```

The absolute value of a number measures the distance of the number from zero along the real number line, regardless of its direction, and is always a positive value.

Normally, we would use such functions when working with the value itself, regardless of its sign.

The same result can be calculated using the conditional operator (`?:`).

```csharp
var x = int.Parse(Console.ReadLine()); // 👈 Example: "-5"

//                               👇 -(-5) = 5
var absoluteValue = x >= 0 ? x : -x;
Console.WriteLine(absoluteValue); // 👈 Prints: "5"
```




## 🌱 Square Root

### 🌱 Square Root



### 📦 The "Math.Sqrt" Method



```csharp
var number = int.Parse(Console.ReadLine()); // Example: "9"

var squareRoot = Math.Sqrt(number);
Console.WriteLine(squareRoot); // 👈 Prints: "3"
```

In this example, `Math.Sqrt(9.0)` returns `3.0` because `3 * 3 = 9`.

The method accepts a single `double` as an argument and returns the square root of that number as a `double`. If we are working with other numeric types, we might need to cast them to `double` before calling `Math.Sqrt`.

```csharp
var number = 20;

var squareRoot = Math.Sqrt(number);

// 👇 Prints: "The square root of 20 is approximately 4.47."
Console.WriteLine($"The square root of {number} is approximately {squareRoot:F2}.");
```

The `:F2` formatting specifier limits the output to two decimal places.

While square roots of negative numbers are not real in the realm of real numbers, C# handles them using the `NaN` (Not a Number) value.

```csharp
var number = -4;

var squareRoot = Math.Sqrt(number);
Console.WriteLine(squareRoot); // 👈 Prints: "NaN"
```

#### ✏️ Example: Pythagoras' Theorem

```csharp
var a = 3;
var b = 4;

var c = Math.Sqrt(Math.Pow(a, 2) + Math.Pow(b, 2));
Console.WriteLine($"The hypotenuse is {c}."); // 👈 Prints: "5"
```

In this example, we use the `Math.Pow` and `Math.Sqrt` methods to calculate the length of the hypotenuse of a right-angled triangle.

#### ✏️ Example: Calculating the Distance Between Points

Calculating the distance between two points with coordinates `(x1, y1)` and `(x2, y2)`.

We can calculate the distance between two points with coordinates `(x1, y1)` and `(x2, y2)` using the `Math.Sqrt` and the `Math.Pow` methods.

```csharp
var x1 = 1;
var y1 = 2;

var x2 = 4;
var y2 = 6;

var distance = Math.Sqrt(Math.Pow(x2 - x1, 2) + Math.Pow(y2 - y1, 2));
Console.WriteLine($"The distance between the points is: {distance}");
```



## 📏 Absolute Value

### 📏 Absolute Value

In mathematics, the absolute value or `modulus` of a real number is the non-negative value of the number without regard to its sign.

It is denoted by `|x|`, where `x` is a real number.

The absolute value of a number measures the distance of the number from zero along the real number line, regardless of its direction, and is always a positive value.

### 🔧 The "Math.Abs" Method

The `Math.Abs` method returns the non-negative value of `x`.

```csharp
var x = int.Parse(Console.ReadLine()); // 👈 Example: "-5"

var absoluteValue = Math.Abs(x);
Console.WriteLine(absoluteValue); // 👈 Prints: "5"
```

Normally, we would use such calculations when working with the value itself, regardless of its sign. For example, calculating the length (the non-negative difference) between two numbers.

The same result could be calculated using the conditional operator (?:).

```csharp
var x = int.Parse(Console.ReadLine()); // 👈 Example: "-5"

//                               👇 -(-5) = 5
var absoluteValue = x >= 0 ? x : -x;
Console.WriteLine(absoluteValue); // 👈 Prints: "5"
```

#### ✏️ Example: Positive Or Negative Number

We can use the `Math.Abs` method to determine whether a number is positive or not.

```csharp
var x = int.Parse(Console.ReadLine()); // 👈 Example: "5"

//                 👇 "Is 5 equal to |5|?"
var isPositive = x == Math.Abs(x);

Console.WriteLine(isPositive); // 👈 Example: "True"
```

In this example, the expression `x == Math.Abs(x)` returns `true` if and only if `x` is non-negative.