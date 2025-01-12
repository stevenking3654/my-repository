## ⚖️ Values Comparison

Value comparison is a foundational aspect of programming, enabling decision-making and logical operations.

### 🔢 Comparing Integer Numbers

Comparing integers is straightforward and can be done using comparison (relational) operators. These operators return boolean values indicating the result of the comparison.

#### ✏️ Example: ⚖️ Comparing Integer Numbers

```csharp
var value1 = 10;
var value2 = 20;

bool areEqual = (value1 == value2); // false
bool isGreater = (value1 > value2); // false
bool isLessOrEqual = (value1 <= value2); // true
```

**Considerations**:

- **Overflow Handling**: Be cautious when comparing integers near their limits (`int.MaxValue` or `int.MinValue`), especially in operations like addition or subtraction.
- **Unsigned Integers**: Use `uint`, `ulong` for unsigned comparisons when dealing with non-negative values only.

### 🔢 Comparing Decimal Numbers

When comparing decimal values, especially those resulting from floating-point arithmetic, it is essential to consider precision issues. Due to how floating-point numbers are represented in memory, two values that are mathematically equal may not be considered equal in a direct comparison. To mitigate this, we use a small value known as **epsilon** to determine if two decimal values are "close enough" to be considered equal. Epsilon represents the smallest difference that can be considered significant for comparison purposes.

```csharp
var epsilon = 0.0001m;
```

#### ✏️ Example: ⚖️ Comparing Decimal Numbers

```csharp
// This might not exactly equal 0.3m due to precision issues
var x = 0.1m + 0.2m;

var y = 0.3m;

bool areEqual = Math.Abs(x - y) < epsilon; // true if x and y are close enough
```

This method ensures that minor discrepancies due to floating-point representation do not affect logical comparisons.

**Steps for Comparison**:

1. Compute the absolute difference between two numbers.
2. Check if the difference is smaller than a predefined `epsilon`.

```csharp
var value1 = 1.000001;
var value2 = 1.000002;

var epsilon = 0.00001;

if (Math.Abs(value1 - value2) < epsilon)
{
    Console.WriteLine("The values are effectively equal.");
}
```

**Considerations**:

- **Choose Epsilon Wisely**: The `epsilon` value should match the precision requirements of your application.
- **Use `decimal` for Higher Precision**: For financial and scientific calculations, use `decimal` instead of `float` or `double`.

### 🔣 Comparing Characters

Characters can be compared directly using the same relational operators used for integers. The underlying representation of characters is based on their Unicode code points, which allows comparisons based on their numerical values.

#### ✏️ Example: ⚖️ Comparing Characters

```csharp
var value1 = 'A';
var value2 = 'B';

bool isEqual = (value1 == value2); // false
bool isGreater = (value1 > value2); // false ('A' has a lower Unicode value than 'B')
```

Characters can also be compared with integers, where the integer represents the Unicode code point of the character. For example, `'A'` is less than `'B'` because `'A'` has a Unicode value of `65`, while `'B'` has `66`.

```csharp
var character = 'A';

if (character == 65)
{
    Console.WriteLine("Character is 'A'.");
}
```

**Considerations**:

- **Character Comparisons**: Understand Unicode values when comparing. Use relational operators for intuitive ordering.
- **Non-English Characters**: Comparisons respect Unicode ordering, which may differ from lexical expectations in some languages.

### 📜 Comparing Strings

Strings are compared lexicographically. Comparison respects case and the Unicode value of each character.

#### ✏️ Example: ⚖️ Comparing Strings

```csharp
var str1 = "apple";
var str2 = "banana";

bool areEqual = (str1 == str2); // false
bool isGreater = (str1.CompareTo(str2) > 0); // false
bool isLess = (str1.CompareTo(str2) < 0); // true
```

#### ✏️ Example: ⚖️ Using String Comparison Methods

Strings can be compared using methods provided by the `String` class.

Some of these methods include:

- `Equals()`: Evaluates if two strings are equal.
- `Compare()`: Compares two strings lexicographically.

```csharp
var str1 = "apple";
var str2 = "banana";

bool areStringsEqual = str1.Equals(str2); // false
int comparisonResult = string.Compare(str1, str2); // negative value since "apple" comes before "banana"
```

```csharp
string str1 = "apple";
string str2 = "banana";

bool areEqual = (str1 == str2); // false
bool isGreater = (str1.CompareTo(str2) > 0); // false
bool isLess = (str1.CompareTo(str2) < 0); // true
```

1. **`==` and `!=` Operators**: Compare strings for exact equality or inequality.
2. **`CompareTo` Method**:
    - Returns `0` if strings are equal.
    - Returns a negative value if the first string precedes the second.
    - Returns a positive value if the first string follows the second.
3. **`Equals` Method**: Compares strings for value equality.

Default string comparison is case-sensitive. Use `StringComparison` options for case-insensitive or culture-specific comparisons.

```csharp
bool areStringsEqualIgnoreCase = string.Equals(str1, str2, StringComparison.OrdinalIgnoreCase);
```

**Considerations**:

- **Normalize Strings**: Normalize strings to a standard form (e.g., lowercase) for consistent comparison.
- **Use StringComparison**: Explicitly specify comparison type to avoid culture-dependent issues.