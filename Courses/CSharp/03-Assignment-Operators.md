## 🏗️ Assignment Operators

Assignment operators allow us to assign and modify the values stored in variables. Assignment operators include:

The most basic assignment operator (`=`) assigns the value on the right to the variable on the left.

```csharp
int x = 10; // 👈 Assigns the value `10` to the variable `x`
```

Normally, we would read these statements from left to right.

```csharp
int x = 5 + 5; // 👈 The expression needs to be calculated first
```

```csharp
int count = 5;
int total = count; // 👈 Assigns the value of `count` to the variable `total`

Console.WriteLine(count); // 👈 Prints: "5"
Console.WriteLine(total); // 👈 Prints: "5"
```

Compound assignment operators (`+=`, `-=`, `*=`, `/=`, `%=`) combine the assignment with another operation.

```csharp
int number = 5;

number += 3; // 👈 Equivalent to: `number = number + 3`

Console.WriteLine(number); // 👈 Prints: "8"
```

The difference between `number + 3` and `number += 3` is that in the second scenario the value of number is updated.

The form `x operand= y` is equivalent to `x = x operand y`.

Compound assignment operators serve as shortcuts.

```csharp
int x = 5;

x += 3; // x = 5 + 3;
Console.WriteLine(x); // 👈 Prints: "8"

x -= 2; // x = 8 - 2;
Console.WriteLine(x); // 👈 Prints: "6"

x *= 4; // x = 6 * 4;
Console.WriteLine(x); // 👈 Prints: "24"

x /= 6; // x = 24 / 6;
Console.WriteLine(x); // 👈 Prints: "4"

x %= 2; // x = 4 % 2;
Console.WriteLine(x); // 👈 Prints: "0"
```

Cascade assignments allow us to assign the same value to multiple variables (chained assignment).

```csharp
int a, b;

a = b = 7; // 👈 Both a and b are assigned the value 7

Console.WriteLine(a); // 👈 Prints: "7"
Console.WriteLine(b); // 👈 Prints: "7"
```

The statement `b = 7` assigns the value `7` to variable `b`. The statement `a = b` assigned the value of `b` (which is `7`) to variable `a`.


## 🏗️ Assignment Operators

Assignment operators allow us to assign and modify the values stored in variables. Assignment operators include:

The most basic assignment operator (`=`) assigns the value on the right to the variable on the left.

```csharp
int x = 10; // 👈 Assigns the value `10` to the variable `x`
```

Normally, we would read these statements from left to right.

```csharp
int x = 5 + 5; // 👈 The expression needs to be calculated first
```

```csharp
int count = 5;
int total = count; // 👈 Assigns the value of `count` to the variable `total`

Console.WriteLine(count); // 👈 Prints: "5"
Console.WriteLine(total); // 👈 Prints: "5"
```

Compound assignment operators (`+=`, `-=`, `*=`, `/=`, `%=`) combine the assignment with another operation.

```csharp
int number = 5;

number += 3; // 👈 Equivalent to: `number = number + 3`

Console.WriteLine(number); // 👈 Prints: "8"
```

The difference between `number + 3` and `number += 3` is that in the second scenario the value of number is updated.

The form `x operand= y` is equivalent to `x = x operand y`.

Compound assignment operators serve as shortcuts.

```csharp
int x = 5;

x += 3; // x = 5 + 3;
Console.WriteLine(x); // 👈 Prints: "8"

x -= 2; // x = 8 - 2;
Console.WriteLine(x); // 👈 Prints: "6"

x *= 4; // x = 6 * 4;
Console.WriteLine(x); // 👈 Prints: "24"

x /= 6; // x = 24 / 6;
Console.WriteLine(x); // 👈 Prints: "4"

x %= 2; // x = 4 % 2;
Console.WriteLine(x); // 👈 Prints: "0"
```

Cascade assignments allow us to assign the same value to multiple variables (chained assignment).

```csharp
int a, b;

a = b = 7; // 👈 Both a and b are assigned the value 7

Console.WriteLine(a); // 👈 Prints: "7"
Console.WriteLine(b); // 👈 Prints: "7"
```

The statement `b = 7` assigns the value `7` to variable `b`. The statement `a = b` assigned the value of `b` (which is `7`) to variable `a`.