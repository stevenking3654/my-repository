## 📚 `do-while` Loop

The `do-while` loop is a unique control structure in programming, ensuring that the loop body executes **at least once**, regardless of whether the condition is `true` or `false` at the beginning. This makes it particularly useful in scenarios where the initial execution of the code block is required before condition validation.

Unlike a `while` loop, which evaluates the condition **before** executing the loop body, the `do-while` loop evaluates the condition **after** the loop's first execution. This distinct behavior makes the `do-while` loop a go-to solution for tasks like user prompts, input validation, and repetitive actions where one iteration is mandatory.

### 📃 Basic Syntax & Structure

A `do-while` loop in C# is constructed as follows:

**🧱 Basic Structure:**

```csharp
do
{
	<code_block>
} while (<condition>);
```

**⚙️ Components:**

- **Code Block**: The statements inside the loop that are executed at least once.
- **Condition**: Sets the rule for the loop to continue. As long as the condition is `true`, the loop will continue to execute. The expression is evaluated after each iteration of the loop.

**🔄 Execution Flow:**

The `do-while` loop follows a straightforward execution process:

1. **First Iteration**:
	- The loop executes the code block once, without checking the condition.
2. **Condition Evaluation**:
	- After the first iteration, the condition is evaluated.

The loop will repeat this process until the condition evaluates to `false`.

#### ✏️ Example: 🔐 Password Prompt

A classic use case for `do-while` loops is implementing a password prompt that ensures the user gets at least one chance to input their password.

```csharp
var password = "secret";
string userInput;

do
{
    Console.WriteLine("Enter password:");
    userInput = Console.ReadLine();
} while (userInput != password);

Console.WriteLine("Access Granted!");
```

**📖 Explanation:**

- The loop ensures that the user is prompted at least once for the password.
- The condition checks whether the entered password matches `"secret"`.
- After the correct password is provided, the loop terminates and prints `"Access Granted!"`.

**🖨 Input & Output:**

```
Enter password:
wrongPass
Enter password:
password123
Enter password:
secret
Access Granted!
```

#### ✏️ Example: 📝 Quiz Question

In this scenario, the user is asked to answer a quiz question, and the loop ensures they are prompted again if they provide an incorrect answer.

```csharp
string answer;

do
{
	Console.WriteLine("What is the capital of France?");
	answer = Console.ReadLine();
} while (answer.ToLower() != "paris");

Console.WriteLine("Correct! Moving on to the next question.");
```

**📖 Explanation:**

- The `ToLower()` method ensures case-insensitive comparison, accepting inputs like `"Paris"` or `"paris"`.
- Incorrect answers prompt the question again until the correct answer is provided.

**🖨 Input & Output:**

```
What is the capital of France?
london
What is the capital of France?
berlin
What is the capital of France?
paris
Correct! Moving on to the next question.
```

#### ✏️ Example: 🎂 Age Validation

This example ensures the user enters a valid age within a specified range (e.g., 18–65 years).

```csharp
int minAge = 18;
int maxAge = 65;
int age;

do
{
	Console.WriteLine("Please enter your age:");
	age = int.Parse(Console.ReadLine());
} while (age < minAge || age > maxAge);

Console.WriteLine("Age accepted. Welcome!");
```

**📖 Explanation:**

- The loop ensures the user enters an age between `18` and `65`.
- If the entered age is outside this range, the user will be prompted again.
- Once a valid age is entered, the loop ends, and `"Age accepted. Welcome!"` is displayed.

**🖨 Input & Output:**

```
Please enter your age:
17
Please enter your age:
70
Please enter your age:
25
Age accepted. Welcome!
```

### 🎓 Summary: Key Takeaways

- The do-while loop is ideal for scenarios where the code block must execute at least once before checking the condition.
- Make sure the code block runs first, followed by the condition check to determine if the loop continues.
- Utilize do-while loops when you want to ensure that user input or certain operations are performed before any validation occurs.