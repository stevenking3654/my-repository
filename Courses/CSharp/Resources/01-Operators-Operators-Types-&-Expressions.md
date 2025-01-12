## 🔣 Operators, Operator Types & Expressions

Operators are symbols that perform operations on one or more operands (values, variables, or expressions). In C#, operators allow us to manipulate data, make comparisons, and perform calculations.

### 🔍 Classification of Operators

#### 🛠️ Based on Their Functionality

C# operators are grouped into different types based on their functionality.

|Operator Type|Description|
|---|---|---|
|**Arithmetic Operators**|Perform mathematical operations like addition, subtraction, multiplication, and division.|`+`, `-`, `*`, `/`, `%`|
|**Assignment Operators**|Assign values to variables.|`=`, `+=`, `-=`, `*=`, `/=`|
|**Comparison Operators**|Compare two values or expressions, returning `true` or `false`.|`==`, `!=`, `<`, `>`, `<=`, `>=`|
|**Logical Operators**|Combine or negate boolean expressions.|`&&`, `|
|**Bitwise Operators**|Perform bit-level operations on integers.|`&`, `|
|**String Concatenation**|Combine strings into one.|`+`|

#### 🔢 Based on the Number of Operands

Operators are classified based on how many operands they operate on:

|Type|Description|Example|
|---|---|---|
|**Unary**|Operate on a single operand.|`-x` (negation), `!x` (logical NOT), `x++` (post-increment)|
|**Binary**|Operate on two operands.|`x + y`, `x * y`, `x && y`|
|**Ternary**|Operate on three operands.|`condition ? result1 : result2`|

#### 📌 Based on Position

Operators can be classified based on their position relative to operands:

|Type|Description|Example|
|---|---|---|
|**Prefix**|The operator appears before the operand.|`++x` (increment before use), `-x` (negation)|
|**Infix**|The operator appears between two operands.|`x + y`, `x < y`|
|**Postfix**|The operator appears after the operand.|`x++` (increment after use)|

### 🧮 What Are Expressions?

An **expression** is a combination of operators, operands, and literals that evaluates to a single value. Expressions are the building blocks of programming logic, allowing you to:

- Perform calculations.
- Make comparisons.
- Execute conditional logic.

**📚 Example of Expression:**

```csharp
int result = (5 + 3) * 2;
```

**📖 Explanation:**

- `5 + 3` is a sub-expression that evaluates to `8`.
- `8 * 2` evaluates to `16`.
- The overall expression assigns `16` to the variable `result`.

#### ⚙ Components of an Expression:

- **Operators**: Symbols that define the operation (e.g., `+`, `*`).
- **Operands**: Variables, literals, or expressions (e.g., `5`, `3`).
- **Literals**: Fixed values in code (e.g., `5`, `"Hello"`).

#### 🔢 Data Type of Expressions:

The data type of an expression depends on the data types of its operands and the operation being performed. For example:

- `int + int` produces an `int`.
- `int / double` produces a `double`.

### 🔄 Associativity

**Associativity** defines the direction in which operators of the same precedence are evaluated. It can be:

- **Left-to-Right (Left Associative):** Evaluation happens from left to right.  
    Example: `5 - 3 - 1` is evaluated as `(5 - 3) - 1`.
- **Right-to-Left (Right Associative):** Evaluation happens from right to left.  
    Example: `x = y = 5` is evaluated as `x = (y = 5)`.

### 🎓 Summary: Key Takeaways

- Operators enable manipulation and computation in code.
- Expressions combine operators, operands, and literals to produce results.
- Understanding associativity ensures correct interpretation of complex expressions.