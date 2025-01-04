## ✅ The `if` Statement

The `if` statement is one of the simplest yet most powerful tools in programming. It allows your program to make decisions by executing specific blocks of code based on whether a condition is `true` or `false`.

### 📃 Basic Syntax & Structure

At its core, the `if` statement is a decision-making structure. It evaluates a **condition** (a Boolean expression) and determines whether to execute a block of code.

**🧱 Basic Structure:**

```csharp
if (<condition>)
{
    <code_block>
}
```

**⚙️ Components:**

- **`if` keyword**: Marks the beginning of the conditional statement.
- **Condition**: Enclosed in parentheses `()`, this is the logical test that returns `true` or `false`.
- **Code Block**: Enclosed in `{}`, this block executes only when the condition is `true`.

The `<condition>` component can be replaced with:

- **A Boolean literal**: A direct value of `true` or `false`.
	- Example: `if (true)` will always execute the code block.
- **A Boolean variable**: A variable that holds a `true` or `false` value.
	- Example: `if (isAuthenticated)` will execute the code block if `isAuthenticated` is `true`.
- **A Boolean expression**: Any logical operation or combination of conditions that evaluates to `true` or `false`.
	- Example: `if (isAuthenticated && hasActiveMembership)` checks if both `isAuthenticated` and `hasActiveMembership` are `true`.
	- Example: `if (isMember || isPromotionApplied)` checks if either `isMember` or `isPromotionApplied` is `true`.

**🔄 Execution Flow:**

The `if` statement follows a straightforward execution process:

1. **Condition Evaluation**:
	- The program evaluates the condition inside the parentheses `()`. This condition must be a Boolean expression that returns `true` or `false`.
2. **Code Block Execution**:
	- If the condition evaluates to `true`, the code block enclosed in `{}` is executed.
	- If the condition evaluates to `false`, the code block is skipped, and the program continues executing the statements that follow the `if` statement.

#### ✏️ Example: 💯 Checking a Student's Score

```csharp
var passingScore = 50;
var studentScore = 90;

if (studentScore >= passingScore)
{
	Console.WriteLine("You passed the exam!"); 
}
```

**📖 Explanation:**

- The condition `studentScore >= passingScore` is evaluated. Since `90 >= 50` is `true`, the message `"You passed the exam!"` is displayed.

#### ✏️ Example: ✅ Validating Voting Eligibility

```csharp
Console.WriteLine("Enter your age:");

var userAge = int.Parse(Console.ReadLine());
var minimumVotingAge = 18;

if (userAge >= minimumVotingAge)
{
    Console.WriteLine("You are eligible to vote.");
}
```

**⚙️ How It Works?**

1. The program takes the user’s input (`userAge`).
2. It checks whether `userAge` is greater than or equal to `minimumVotingAge`.
3. If `true`, it outputs: "You are eligible to vote."

#### ✏️ Example: 🍔 Planning a Picnic

```csharp
var temperature = 25;
var isSunny = true;

if (temperature > 20 && isSunny)
{
    Console.WriteLine("It's a great day for a picnic!");
}
```

**📖 Explanation:**

- `temperature > 20`: Checks if it’s warm enough.
- `isSunny`: Ensures the weather is sunny.
- Both conditions must be `true` for the message to display, thanks to the `&&` operator.

### 📑 Formatting Conditional Statements

Good formatting improves readability and helps prevent bugs. Here are some key considerations:

**📌 Standard Formatting:**

```csharp
if (userAge >= minimumAgeForAccess)
{
    Console.WriteLine("You're eligible for access!");
}
```

This is the recommended format for clarity.

**📌 Omitting Curly Braces:**

We can write a single statement without `{}`. While valid, it’s less robust.

```csharp
if (userAge >= minimumAgeForAccess)
    Console.WriteLine("You're eligible for access!");
```

**📌 Single-Line Statement:**

It’s also possible to write the entire statement on one line. Use this sparingly for very simple conditions.

```csharp
if (userAge >= minimumAgeForAccess) Console.WriteLine("You're eligible for access!");
```

### 🚧 The Curly Braces Trap

Consider this code:

```csharp
var userAge = int.Parse(Console.ReadLine()); // Input: "12"
var minimumAgeForAccess = 21;

if (userAge >= minimumAgeForAccess)
    Console.WriteLine("You're eligible for access!");
    Console.WriteLine("You are older than 18 years old.");
```

**⚙️ What Happens?**

If `userAge` is `12`, the output will be:

```
You are older than 18 years old.
```

Why? The second `Console.WriteLine()` is **not** part of the `if` block because it lacks `{}`. The `if` statement only applies to the first statement following it.

**💡 Solution: Always Use Curly Braces**

```csharp
if (userAge >= minimumAgeForAccess)
{
    Console.WriteLine("You're eligible for access!");
    Console.WriteLine("You are older than 18 years old.");
}
```

This ensures that both statements are executed only if the condition is `true`.

### 🎓 Summary: Key Takeaways

The `if` statement is the foundation of conditional logic in C#. Understanding its syntax, execution flow, and formatting ensures you can write clean, reliable code.