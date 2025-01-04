## 🔢 `for` Loop

The `for` loop is one of the most widely used control structures in programming, used to execute a block of code repeatedly for a specified number of times.

### 📃 Basic Syntax & Structure

A `for` loop is built around four core components: **initialization**, **condition**, **iteration update**, and the **code block** to execute.

**🧱 Basic Structure:**

```csharp
for (<initialization>; <condition>; <iteration_update>)
{
	<code_block>
}
```

**⚙️ Components:**

- **Initialization**: Initializes a new local variable (often called the loop **control variable**) that can only be used within the loop. The value of the variable serves as a starting point and keeps track of the current iteration of the loop.
- **Condition**: Sets the rule for the loop to continue. As long as the condition is `true`, the loop will continue to execute. The expression is evaluated before each iteration of the loop.
- **Iteration Update**: Describes how the control variable is adjusted at the end of each iteration of the loop.
- **Code Block**: Contains the statements (also known as the **loop body**) to be executed repeatedly while the condition is met.

**🔄 Execution Flow:**

The `for` loop follows a straightforward execution process:

1. **Initialization**:
	- Executes only once at the start of the loop, setting the initial value of the control variable.
2. **Condition**:
	- Evaluates before each iteration. If the condition is `true`, the loop executes the code block. If `false`, the loop terminates.
3. **Code Block**:
	- Executes the statements inside the loop. This occurs only if the condition is `true`.
4. **Iteration Update**:
	- Executes after the code block in each iteration, updating the control variable to prepare for the next loop cycle.

This sequence repeats starting from the **Condition** step until the condition evaluates to `false`. At that point, the loop terminates.

#### ✏️ Example: 🖨️ Printing Numbers from `1` to `10`

```csharp
for (int number = 1; number <= 10; number++)
{
	Console.WriteLine(number);
}
```

**📖 Explanation:**

- `int number = 1`: Sets the starting point of the loop.
- `number <= 10`: Ensures the loop continues as long as `number` is equal to or less than `10`.
- `number++`: Increments `number` by `1` after each iteration.
- `Console.WriteLine(number)`: Prints the current value of `number` to the console.

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

1. **First Iteration**:
	- The loop starts with `number` initialized to `1`.
	- The condition `1 <= 10` is evaluated and found to be `true`.
	- The body executes, printing `1` to the console. After executing the body, `number` is incremented to `2`.
1. **Subsequent Iterations**: This process repeats for each subsequent value of `number`.
2. **Final Iteration**: When `number` reaches `11`, the condition `11 <= 10` is evaluated and found to be `false`. The loop terminates, and no further action is taken.

#### ✏️ Example: 🧮 Calculating the Sum of Numbers from `1` to `20`

```csharp
var sum = 0;

for (int number = 1; number <= 20; number++)
{
	// Add the current number to the sum
	sum += number;
}

Console.WriteLine("Sum: " + sum);
```

**📖 Explanation:**

- A variable `sum` is initialized to `0` outside the loop.
- Each iteration adds `number` to `sum`.
- After the loop, the final result is displayed.

**🖨 Output:**

```
Sum: 210
```

#### ✏️ Example: ⚖️ Printing Even Numbers

To print even numbers between `2` and `20`, we can adjust the **initialization** and **iteration update**:

```csharp
for (int number = 2; number <= 20; number += 2)
{
    Console.WriteLine(number);
}
```

**📖 Explanation:**

1. The loop initializes the variable `number` to `2`, setting it as the starting value.
2. The loop iterates as long as `number` is less than or equal to `20`.
3. During each iteration, the current value of `number` is printed to the console. Afterward, `number` is incremented by `2`, ensuring only even numbers are considered.
4. Once `number` exceeds `20`, the loop terminates, and no further action is taken.

**🖨 Output:**

```
2
4
6
8
10
12
14
16
18
20
```

#### ✏️ Example: 🔄 Counting Backwards from `10` to `1`

A `for` loop can count in reverse by decrementing the control variable.

```csharp
for (int number = 10; number >= 1; number--)
{
    Console.WriteLine(number);
}
```

**📖 Explanation:**

1. The loop initializes the variable `number` to `10`, setting it as the starting value.
2. The loop continues as long as `number` is greater than or equal to `1`.
3. During each iteration, the current value of `number` is printed to the console. Afterward, `number` is decremented by `1`, moving towards the stopping condition.
4. Once `number` becomes less than `1`, the loop terminates.

**🖨 Output:**

```
10
9
8
7
6
5
4
3
2
1
```

### 🎓 Summary: Key Takeaways

- The `for` loop is typically used when we know in advance how many times we need to repeat a block of code.
- Ensure the **initialization**, **condition**, and **iteration update** work together logically.
- Experiment with different starting points, conditions, and increments to handle a variety of tasks.