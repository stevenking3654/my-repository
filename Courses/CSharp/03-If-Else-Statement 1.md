# 🚀 Mastering **If-Else Statements** in C#

The `if-else` statement is a fundamental control structure in programming that lets you execute different code paths based on a condition. It enables your program to **make decisions dynamically** depending on the input or state of variables.

---

### 🔧 **How If-Else Works**

The syntax of an `if-else` statement is as follows:

```csharp
if (condition)
{
    // Code to execute if the condition is TRUE
}
else
{
    // Code to execute if the condition is FALSE
}
```

1. **Condition**:
    
    - Must be a Boolean expression (`true` or `false`).
    - Often uses comparison operators (`==`, `>`, `<`, `>=`, `<=`, `!=`).
2. **Code Execution**:
    
    - The **`if` block** runs when the condition evaluates to `true`.
    - Otherwise, the **`else` block** executes.

---

### 🧑‍💻 **Examples of If-Else Statements**

#### **1️⃣ Basic Pass/Fail Example**

This simple program determines if a student passes or fails based on their score:

```csharp
var studentScore = int.Parse(Console.ReadLine());

if (studentScore >= 50)
{
    Console.WriteLine("Pass!");
}
else
{
    Console.WriteLine("Fail!");
}
```

**Input**:  
`65`  
**Output**:  
`Pass!`

---

#### **2️⃣ Assigning Values with If-Else**

You can use an `if-else` statement to assign values to variables dynamically:

```csharp
var studentScore = int.Parse(Console.ReadLine());
var result = "";

if (studentScore >= 50)
{
    result = "Pass!";
}
else
{
    result = "Fail!";
}

Console.WriteLine(result);
```

**Input**:  
`45`  
**Output**:  
`Fail!`

---

#### **3️⃣ Multiple Conditions with Else-If**

When more than two outcomes are possible, use **`else if`** to check additional conditions:

```csharp
var temperature = int.Parse(Console.ReadLine());

if (temperature > 30)
{
    Console.WriteLine("It's hot outside!");
}
else if (temperature > 20)
{
    Console.WriteLine("It's a pleasant day.");
}
else if (temperature > 10)
{
    Console.WriteLine("It's a bit chilly.");
}
else
{
    Console.WriteLine("It's cold outside!");
}
```

**Input**:  
`15`  
**Output**:  
`It's a bit chilly.`

---

### ✨ **Advanced Examples and Use Cases**

#### **4️⃣ Checking Even or Odd Numbers**

```csharp
var number = int.Parse(Console.ReadLine());

if (number % 2 == 0)
{
    Console.WriteLine($"{number} is even.");
}
else
{
    Console.WriteLine($"{number} is odd.");
}
```

**Input**:  
`7`  
**Output**:  
`7 is odd.`

---

#### **5️⃣ Categorizing Grades**

This program assigns a letter grade based on a numeric score:

```csharp
var score = int.Parse(Console.ReadLine());

if (score >= 90)
{
    Console.WriteLine("Grade: A");
}
else if (score >= 80)
{
    Console.WriteLine("Grade: B");
}
else if (score >= 70)
{
    Console.WriteLine("Grade: C");
}
else if (score >= 60)
{
    Console.WriteLine("Grade: D");
}
else
{
    Console.WriteLine("Grade: F");
}
```

**Input**:  
`85`  
**Output**:  
`Grade: B`

---

#### **6️⃣ Nested If-Else Example**

Sometimes, you need to evaluate multiple related conditions within one another. Here’s an example:

```csharp
var age = int.Parse(Console.ReadLine());
var hasDrivingLicense = Console.ReadLine().ToLower() == "yes";

if (age >= 18)
{
    if (hasDrivingLicense)
    {
        Console.WriteLine("You are eligible to drive.");
    }
    else
    {
        Console.WriteLine("You need a driving license to drive.");
    }
}
else
{
    Console.WriteLine("You are too young to drive.");
}
```

**Input**:

```
18
yes
```

**Output**:  
`You are eligible to drive.`

---

#### **7️⃣ Conditional Logic with Time of Day**

```csharp
var hour = int.Parse(Console.ReadLine());

if (hour < 12)
{
    Console.WriteLine("Good morning!");
}
else if (hour < 18)
{
    Console.WriteLine("Good afternoon!");
}
else
{
    Console.WriteLine("Good evening!");
}
```

**Input**:  
`16`  
**Output**:  
`Good afternoon!`

---

### 🚀 **Pro Tips and Best Practices**

#### **1️⃣ Simplify with Ternary Operator**

For simple conditions, the **ternary operator** can replace `if-else`:

```csharp
var score = int.Parse(Console.ReadLine());
Console.WriteLine(score >= 50 ? "Pass!" : "Fail!");
```

---

#### **2️⃣ Logical Operators**

Combine multiple conditions with logical operators (`&&`, `||`, `!`):

```csharp
var age = int.Parse(Console.ReadLine());
var hasID = Console.ReadLine().ToLower() == "yes";

if (age >= 18 && hasID)
{
    Console.WriteLine("You are allowed to enter.");
}
else
{
    Console.WriteLine("Access denied.");
}
```

---

#### **3️⃣ Avoid Redundant Conditions**

Optimize your conditions to avoid unnecessary checks:

```csharp
// Less efficient
if (score >= 90)
{
    Console.WriteLine("Grade: A");
}
else if (score >= 80 && score < 90)
{
    Console.WriteLine("Grade: B");
}

// Optimized
if (score >= 90)
{
    Console.WriteLine("Grade: A");
}
else if (score >= 80)
{
    Console.WriteLine("Grade: B");
}
```

---

### 🔚 **Conclusion**

The `if-else` statement is a powerful decision-making tool that allows you to build **responsive, logical, and dynamic programs**. Whether it's simple checks or complex nested conditions, mastering this structure lays the foundation for handling real-world scenarios effectively.