## 🔁 `while` Loop

The `while` loop is a fundamental control flow statement, enabling a set of instructions to be executed repeatedly as long as a specified condition evaluates to `true`.

### 📃 Basic Syntax & Structure

A `while` loop is structured around two fundamental components: the **condition** that determines whether the loop continues to execute and the **code block** (inside `{ }`) that contains the instructions to be executed as long as the condition remains `true`.

**🧱 Basic Structure:**

```csharp
while (<condition>)
{
	<code_block>
}
```

**⚙️ Components:**

- **Condition**: Defines the rule for the loop to continue executing. The loop runs as long as this condition evaluates to `true`. The condition is evaluated before each iteration.
- **Code Block**: Contains the statements inside the curly braces `{}` (also known as the **loop body**) that are executed repeatedly while the condition remains `true`. This process continues until the condition evaluates to `false`, at which point the loop terminates.

**🔄 Execution Flow:**

The `while` loop follows a clear execution process:

1. **Condition**:
	- Evaluates before each iteration. If the condition is `true`, the loop executes the code block. If `false`, the loop terminates.
2. **Code Block**:
	- Executes the statements inside the loop. This occurs only if the condition is `true`.
3. **Iteration Update**:
	- While not a formal part of the while loop structure, this step involves updating any variables that affect the condition to ensure progress toward termination.

This sequence repeats starting from the **Condition** step until the condition evaluates to `false`. At that point, the loop terminates.

#### ✏️ Example: 🖨️ Printing a Sequence of Numbers

```csharp
var number = 1;

while (number <= 10)
{
    Console.WriteLine(number);
    number++;
}
```

**📖 Explanation:**

- `var number = 1`: Initializes the starting point of the loop.
- `number <= 10`: Ensures the loop continues as long as `number` is equal to or less than `10`.
- `Console.WriteLine(number)`: Prints the current value of `number` to the console.
- `number++`: Increments `number` by `1` after each iteration.

**🖨 Output:**

```
1
2
3
4
5
6
7
8
9
10
```

**🔄 Execution Flow:**

1. **Variable Initialization**: A variable `number` is created and set to `1`.
2. **First Iteration**:
	- The condition `1 <= 10` is evaluated and found to be `true`.
	- The body executes, printing `1` to the console. The `number` variable is incremented to `2`.
3. **Subsequent Iterations**: The process repeats for each subsequent value of `number`.
4. **Final Iteration**:
	- When `number` reaches `11`, the condition `11 <= 10` is evaluated and found to be `false`.
	- The loop terminates, and no further action is taken.

#### ✏️ Example: 🧮 Calculating the Sum of Numbers from `1` to `20`

```csharp
var sum = 0;
var number = 1;

while (number <= 20)
{
	// Add the current number to the sum
	sum += number;
	number++;
}

Console.WriteLine("Sum: " + sum);
```

**📖 Explanation:**

- We initialize `sum = 0` outside the loop to store the cumulative sum.
- We initialize `number = 1` outside the loop to store the starting value.
- The loop adds the value of `number` to `sum` and increments `number` by `1`.
- When `number > 20`, the loop finishes, and the final `sum` is printed.

**🖨 Output:**

```
Sum: 210
```

#### ✏️ Example: ⏳ Counting Down

```csharp
var countdown = 10;

while (countdown > 0)
{
	Console.WriteLine($"Countdown: {countdown}");

	// Decrease the value by 1
	countdown--;
}
```

**📖 Explanation:**

- The loop continues as long as `countdown > 0`.
- The `countdown` variable is decremented by `1` after each iteration (`countdown--`).

**🖨 Output:**

```
Countdown: 10
Countdown: 9
Countdown: 8
Countdown: 7
Countdown: 6
Countdown: 5
Countdown: 4
Countdown: 3
Countdown: 2
Countdown: 1
```

#### ✏️ Example: 📚 Generating Fibonacci Numbers

This example generates the first `10` Fibonacci numbers using a `while` loop.

```csharp
var count = 1;
var firstNumber = 0;
var secondNumber = 1;

while (count <= 10)
{
	Console.WriteLine(firstNumber);

	var nextNumber = firstNumber + secondNumber;
	firstNumber = secondNumber;
	secondNumber = nextNumber;

	count++;
}
```

**📖 Explanation:**

1. **Initialization**:
	- `count = 1`: Tracks the number of Fibonacci numbers generated.
	- `firstNumber = 0` and `secondNumber = 1`: The first two Fibonacci numbers.
1. **Condition**: The loop runs until `count > 10`.
2. **Code Block**:
	- Prints `firstNumber`.
	- Calculates the next Fibonacci number (`nextNumber = firstNumber + secondNumber`).
	- Updates `firstNumber` and `secondNumber` for the next iteration.
	- Increments `count`.

**🖨 Output:**

```
0
1
1
2
3
5
8
13
21
34
```

### 🎓 Summary: Key Takeaways

- Use a `while` loop when the number of iterations is **unknown** but depends on a condition.  
- Always ensure the loop condition becomes `false` at some point to prevent infinite loops.  
- Experiment with `while` loops to handle dynamic scenarios like user input, calculations, and real-time processing.