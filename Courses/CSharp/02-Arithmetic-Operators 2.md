## 🔢 Arithmetic Operators

Arithmetic operators in C# allow ус to perform basic mathematical operations such as addition, subtraction, multiplication, division, and more. These operators are fundamental for manipulating numeric data types like `int`, `double`, `float`, etc.

### 📃 List of Arithmetic Operators

|Operator|Symbol|Description|Example|
|---|---|---|---|
|**Addition**|`+`|Adds two values together.|`10 + 5 = 15`|
|**Subtraction**|`-`|Subtracts the right operand from the left operand.|`10 - 5 = 5`|
|**Multiplication**|`*`|Multiplies two values.|`10 * 5 = 50`|
|**Division**|`/`|Divides the left operand by the right operand (integer division truncates remainder).|`10 / 2 = 5`|
|**Remainder (Modulo)**|`%`|Returns the remainder of a division operation.|`13 % 5 = 3`|
|**Increment**|`++`|Increases the value of a variable by 1.|`x++` or `++x`|
|**Decrement**|`--`|Decreases the value of a variable by 1.|`x--` or `--x`|

#### ✏️ Example: Arithmetic Operators

```csharp
int x = 10;
int y = 5;

Console.WriteLine(x + y); // 👈 Output: "15"
Console.WriteLine(x - y); // 👈 Output: "5"
Console.WriteLine(x * y); // 👈 Output: "50"
Console.WriteLine(x / y); // 👈 Output: "2"
Console.WriteLine(x % y); // 👈 Output: "0"

x++;
y--;

Console.WriteLine(x); // 👈 Output: "11"
Console.WriteLine(y); // 👈 Output: "4"
```