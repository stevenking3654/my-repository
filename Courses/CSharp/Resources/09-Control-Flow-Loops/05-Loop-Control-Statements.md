## 🔧 Loop Control Statements

Loop control statements are programming constructs that manage the flow of execution within loops. They include:

- `break`: Exits a loop immediately.
- `continue`: Skips the current iteration and proceeds to the next.
- `return` (in some cases): Exits both the loop and the enclosing function.

Imagine you are a manager overseeing a factory line. A conveyor belt (your loop) keeps delivering items for quality checks. Loop control statements are like tools you can use:
- `break` is like hitting the emergency stop button.
- `continue` is like skipping a defective item to process the next one.
- `return` is like abandoning the conveyor line altogether.

### ✋ The `break` Statement

The `break` statement allows the program to stop iterating as soon as the desired condition is met.

#### ✏️ Example: 🔍 Find the First Number Divisible by `7`

This example demonstrates how to use the `break` statement to exit a loop as soon as a number divisible by `7` is found between `100` and `200`.

```csharp
for (int number = 100; number <= 200; number++)
{
    // Check if the number is divisible by 7
    if (number % 7 == 0)
    {
        // Print the found number
        Console.WriteLine($"Found the first number divisible by 7: {number}");
        // Exit the loop
        break;
    }
}
```

##### 📖 Explanation:

1. **Condition Check**:  
   The condition `number % 7 == 0` determines if a number is divisible by `7` (remainder is `0`).

2. **Printing the Result**:  
   When the condition is true, the program prints the first number divisible by `7`.

3. **Exiting the Loop**:  
   The `break` statement is executed immediately after the condition is met, halting the loop and preventing further iterations.

##### 🔍 Output:

```
Found the first number divisible by 7: 7
```

### ⏭️ The `continue` Statement

The `continue` statement is useful when we want to bypass certain iterations based on a condition.

#### ✏️ Example: 🔄 Print Only Odd Numbers Using `continue`

This example demonstrates how to use the `continue` statement to skip over even numbers and print only the odd numbers from `1` to `10`.

```csharp
for (int number = 1; number <= 10; number++)
{
    // Check if the number is even
    if (number % 2 == 0)
    {
        // Skip the rest of this iteration
        continue;
    }

    // Print the odd number
    Console.WriteLine(number);
}
```

##### 📖 Explanation:

1. **Condition Check**:  
   The expression `number % 2 == 0` determines if a number is even (remainder is `0` when divided by `2`).

2. **Skipping Even Numbers**:  
   When the condition is true, the `continue` statement is executed. This skips the rest of the current iteration and moves to the next number in the loop.

3. **Printing Odd Numbers**:  
   Only odd numbers (numbers not divisible by `2`) bypass the `if` condition and are printed to the console.

##### 🔍 Output:

```
1
3
5
7
9
```

### 🔚 The `return` Statement

The `return` statement allows us to exit a method immediately, which can be useful for breaking out of a loop early when a specific condition is met.

#### ✏️ Example: ⛔ Exiting a Loop Early with `return`

This example demonstrates how to use the `return` statement to exit a loop and a method early when a condition is met.

```csharp
var number = 4;

if (number <= 1)
{
	Console.WriteLine($"{number} is not a prime number.");
	return; // Exit early if the number is not prime
}

for (int divisor = 2; divisor < number; divisor++)
{
	if (number % divisor == 0)
	{
		Console.WriteLine($"{number} is not a prime number.");
		return; // Exit early when a divisor is found
	}
}

// If no divisors are found, the number is prime
Console.WriteLine($"{number} is a prime number.");
```

### 📖 Explanation:

1. **Checking if the Number is Prime**:
   - If `number <= 1`, it's not a prime number, and the program exits immediately using `return`.

2. **Looping Through Divisors**:
   - A `for` loop checks numbers from `2` to `number - 1`.
   - If any divisor divides the number evenly (`number % i == 0`), the program identifies the number as not prime and exits early with `return`.

3. **Final Check**:
   - If no divisors are found, the program prints that the number is prime.

### 🔍 Input & Output:

For `number = 4`:

```
4 is not a prime number.
```

For `number = 5`:

```
5 is a prime number.
```

|Input|Output|
|-|-|
|4|4 is not a prime number.|