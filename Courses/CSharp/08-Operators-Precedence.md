## 🎩 Operators Precedence

When multiple operators are used in an expression, the order in which they are evaluated can impact the result.

Operators precedence is the set of rules that dictate the order in which operators are evaluated in an expression.

Basic arithmetic operators follow the standard rules. Multiplication and division take precedence over addition and subtraction.

Operators with higher precedence are evaluated before those with lower precedence. If operators have the same precedence, their evaluation order depends on their associativity, which can be left-to-right or right-to-left.

|Operator|Description|Associativity|Example
|-|-|-|-|
|()|Parentheses|Left-to-right|(true && false)|
|!|Logical NOT|Right-to-left|!true|
|* / %|Multiplication, Division, Modulus|Left-to-right|10 * 2 / 5|
|+ -|Addition, Subtraction|Left-to-right|5 + 3 - 2|
|< <= > >=|Comparison Operators|Left-to-right|10 > 5|
|== !=|Equality Operators|Left-to-right|5 == 5|
|&&|Logical AND|Left-to-right|true && false|
|\|\||Logical OR|Left-to-right|true \|\| false|
|=|Assignment Operator|Right-to-left|x = 10|

Comparison operators have higher precedence than logical operators.

```csharp
var x = 8;
var y = 5;
var z = 10;

Console.WriteLine(x > y && x < z); // 👈 Evaluated as `true && true => true`
```








## 🎩 Operators Precedence

When multiple operators are used in an expression, the order in which they are evaluated can impact the result.

Operators precedence is the set of rules that dictate the order in which operators are evaluated in an expression.

Basic arithmetic operators follow the standard rules. Multiplication and division take precedence over addition and subtraction.

Operators with higher precedence are evaluated before those with lower precedence. If operators have the same precedence, their evaluation order depends on their associativity, which can be left-to-right or right-to-left.

|Operator|Description|Associativity|Example
|-|-|-|-|
|()|Parentheses|Left-to-right|(true && false)|
|!|Logical NOT|Right-to-left|!true|
|* / %|Multiplication, Division, Modulus|Left-to-right|10 * 2 / 5|
|+ -|Addition, Subtraction|Left-to-right|5 + 3 - 2|
|< <= > >=|Comparison Operators|Left-to-right|10 > 5|
|== !=|Equality Operators|Left-to-right|5 == 5|
|&&|Logical AND|Left-to-right|true && false|
|\|\||Logical OR|Left-to-right|true \|\| false|
|=|Assignment Operator|Right-to-left|x = 10|

Comparison operators have higher precedence than logical operators.

```csharp
var x = 8;
var y = 5;
var z = 10;

Console.WriteLine(x > y && x < z); // 👈 Evaluated as `true && true => true`
```
