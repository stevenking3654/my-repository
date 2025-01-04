## 🔄 Repetitive Actions

In both real life and programming, repetitive tasks are common. By using loops, we can automate these tasks efficiently and eliminate the monotony of performing them manually.

### 📅 Real-Life Examples of Repetition

In our daily lives, we often repeat actions, sometimes with slight variations:

- **Morning Routines**: Waking up, brushing teeth, and having breakfast are recurring daily tasks.
- **Exercise**: Workouts often involve repeating specific activities, such as completing multiple sets of push-ups or running laps.
- **Reading**: Turning pages to read through a book is a repetitive action we perform to absorb its content.

Humans might grow bored or make errors when repeating tasks, but computers excel at performing repetitive actions swiftly and with precision.

### 🎵 Repetition in Code

Consider the song *Around the World* by Daft Punk, which famously repeats its lyrics. Using a loop, we can mimic this repetition in C#:

```csharp
for (int lineCounter = 1; lineCounter <= 24; lineCounter++)
{
    Console.WriteLine("Around the World, Around the World");
}
```

**🖨️ Output:**

```plaintext
Around the World, Around the World
Around the World, Around the World
...
Around the World, Around the World
```

This code demonstrates how loops allow us to automate tasks that would otherwise require manual repetition. The loop ensures the lyrics are printed 24 times without writing the `Console.WriteLine` statement repeatedly.

### 🔄 The Concept of Loops in Programming

A **loop** is a programming construct used to execute a block of code repeatedly, as long as a specified condition evaluates to `true`.

**🔑 Key Terminology:**

- **Iteration**: A single pass through the loop’s code block. Each execution of the loop is an iteration.
- **Loop Types**:
	- **Count-Based**: Actions repeated a fixed number of times.
	- **Condition-Based**: Actions repeated until a specific condition is met.

Loops simplify code, making it concise and easier to maintain. Instead of manually duplicating code, loops handle repetition efficiently.

### 🚀 Types of Loops in C#

C# offers several loop structures, each suited for different scenarios:

#### 1. `for` Loop

Used when the number of iterations is predetermined. Executes a block of code a specified number of times.

```csharp
var pagesCount = 273;

for (int pageCounter = 1; pageCounter <= pagesCount; pageCounter++)
{
    Console.WriteLine($"Reading page {pageCounter}");
}
```

**📖 Explanation:**

- The loop runs from `1` to `273`, incrementing `pageCounter` on each iteration.
- For each iteration, the message "Reading page {pageCounter}" is displayed, simulating reading each page of a book.

#### 2. `while` Loop

Executes a block of code repeatedly as long as a specified condition remains `true`.

```csharp
var success = tryToAchieveGoal();

while (!success)
{
    Console.WriteLine("Trying again...");
    success = tryToAchieveGoal();
}
```

**📖 Explanation:**

- The loop continues until `tryToAchieveGoal()` returns `true`.
- On each iteration, the program prints "Trying again..." and attempts the goal again.

#### 3. `do-while` Loop

Similar to the `while` loop, but ensures the loop body executes at least once before checking the condition.

```csharp
var attempts = 0;
var isPasswordCorrect;

do
{
    Console.WriteLine("Enter your password:");
    isPasswordCorrect = checkPassword(Console.ReadLine());
    attempts++;
} while (!isPasswordCorrect && attempts < 3);
```

**📖 Explanation:**

- The user is prompted to enter a password, and `checkPassword` validates it.
- The loop guarantees at least one password check, even if the condition is initially `false`.

#### 4. `foreach` Loop

Specially designed for iterating over collections like arrays or lists.

```csharp
var shoppingList = new string[] { "Milk", "Bread", "Eggs" };

foreach (var item in shoppingList)
{
    Console.WriteLine($"Don't forget: {item}");
}
```

**📖 Explanation:**

- Each item in the `shoppingList` array is processed in sequence.
- The program prints "Don't forget: {item}" for every item, reminding the user of each list entry.

### 🎓 **Summary: Key Takeaways**

**Loops** as constructs that allow code to run a block of statements multiple times based on specified conditions, thereby reducing redundancy and improving code efficiency.