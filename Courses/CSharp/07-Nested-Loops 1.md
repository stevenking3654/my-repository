# 🚀 Mastering **Nested Loops** in C#

Nested loops are an essential programming construct where one loop is placed inside another. They are invaluable for working with **multidimensional data structures**, creating **tables**, processing **grids**, or generating **patterns** that require layered iteration.

---

### 🔧 **How Nested Loops Work**

A nested loop involves:

- An **outer loop**: Iterates over a primary range or collection.
- An **inner loop**: Executes fully for each iteration of the outer loop.

#### **Key Points**:

1. **Execution Order**:
    
    - The outer loop runs once, then the inner loop completes all its iterations.
    - Afterward, the outer loop advances to its next iteration, and the inner loop starts again.
2. **Scope of Control Statements**:
    
    - The `break` and `continue` statements apply to the **innermost loop** by default.

---

### 🧑‍💻 **Examples of Nested Loops**

#### **1️⃣ Simple Calendar Grid**

Let's build a calendar with weeks and days:

```csharp
int weeks = 4;
int daysInWeek = 7;

for (int week = 1; week <= weeks; week++)
{
    Console.Write($"Week {week}: ");

    for (int day = 1; day <= daysInWeek; day++)
    {
        Console.Write($"Day {day} ");
    }

    Console.WriteLine();
}
```

**Explanation**:

- The **outer loop** iterates through the weeks (`week`).
- The **inner loop** iterates through the days of each week (`day`).

**Output**:

```
Week 1: Day 1 Day 2 Day 3 Day 4 Day 5 Day 6 Day 7 
Week 2: Day 1 Day 2 Day 3 Day 4 Day 5 Day 6 Day 7 
Week 3: Day 1 Day 2 Day 3 Day 4 Day 5 Day 6 Day 7 
Week 4: Day 1 Day 2 Day 3 Day 4 Day 5 Day 6 Day 7 
```

---

#### **2️⃣ Multiplication Table**

A multiplication table is a classic example of nested loops:

```csharp
int number = 5;

for (int n = 1; n <= number; n++)
{
    for (int m = 1; m <= number; m++)
    {
        Console.Write($"{n} * {m} = {n * m}\t");
    }

    Console.WriteLine();
}
```

**Explanation**:

- The **outer loop** iterates over the rows (`n`).
- The **inner loop** calculates the product for each column in the row (`m`).

**Output**:

```
1 * 1 = 1	1 * 2 = 2	1 * 3 = 3	1 * 4 = 4	1 * 5 = 5	
2 * 1 = 2	2 * 2 = 4	2 * 3 = 6	2 * 4 = 8	2 * 5 = 10	
3 * 1 = 3	3 * 2 = 6	3 * 3 = 9	3 * 4 = 12	3 * 5 = 15	
4 * 1 = 4	4 * 2 = 8	4 * 3 = 12	4 * 4 = 16	4 * 5 = 20	
5 * 1 = 5	5 * 2 = 10	5 * 3 = 15	5 * 4 = 20	5 * 5 = 25	
```

---

#### **3️⃣ Seating Chart Example**

Imagine creating a seating chart for a small venue where:

- Rows are numbered.
- Seats in each row are labeled with letters (`A`, `B`, `C`, ...).

```csharp
int rows = int.Parse(Console.ReadLine());
int seatsPerRow = int.Parse(Console.ReadLine());

for (int row = 1; row <= rows; row++)
{
    for (char seat = 'A'; seat < 'A' + seatsPerRow; seat++)
    {
        Console.Write($"{row}{seat} ");
    }

    Console.WriteLine();
}
```

**How It Works**:

- The **outer loop** iterates through row numbers (`row`).
- The **inner loop** generates seat labels (`seat`), starting from `'A'` and advancing based on the number of seats per row.

**Input**:

```
3
4
```

**Output**:

```
1A 1B 1C 1D 
2A 2B 2C 2D 
3A 3B 3C 3D 
```

---

### 🔄 **Common Applications of Nested Loops**

1. **Grids and Tables**:  
    Used for creating and processing tabular or matrix-like data.
    
2. **Patterns and Shapes**:  
    Example: Generating a pyramid or triangle pattern.
    
    ```csharp
    int rows = 5;
    
    for (int i = 1; i <= rows; i++)
    {
        for (int j = 1; j <= i; j++)
        {
            Console.Write("*");
        }
        Console.WriteLine();
    }
    ```
    
    **Output**:
    
    ```
    *
    **
    ***
    ****
    *****
    ```
    
3. **Multidimensional Arrays**:  
    Processing rows and columns in 2D arrays.
    
    ```csharp
    int[,] matrix = { { 1, 2 }, { 3, 4 }, { 5, 6 } };
    
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
        {
            Console.Write($"{matrix[i, j]} ");
        }
        Console.WriteLine();
    }
    ```
    
    **Output**:
    
    ```
    1 2 
    3 4 
    5 6 
    ```
    

---

### 🚩 **Important Notes and Best Practices**

1. **Avoid Infinite Loops**:  
    Ensure loop termination conditions are correctly defined.  
    Example of a potential issue:
    
    ```csharp
    for (int i = 0; i < 5; i++)
    {
        for (int j = 0; ; j++) // ❌ Missing termination
        {
            Console.WriteLine(j);
        }
    }
    ```
    
2. **Optimize Performance**:  
    Nested loops can increase computational complexity. Avoid unnecessary nesting.
    
3. **Use Meaningful Variable Names**:  
    In nested loops, variables like `i`, `j`, `k` are common but not always descriptive. Use meaningful names when possible (`row`, `column`, `week`, etc.).
    
4. **Break Out of Nested Loops**:  
    Use the `break` statement to exit a loop when a specific condition is met:
    
    ```csharp
    for (int i = 1; i <= 10; i++)
    {
        for (int j = 1; j <= 10; j++)
        {
            if (i * j == 25)
            {
                Console.WriteLine($"Found a match: {i} * {j} = 25");
                break; // Exits the inner loop
            }
        }
    }
    ```
    

---

### 🔚 **Conclusion**

Nested loops are a cornerstone of structured programming, enabling you to handle complex tasks like iterating through grids, generating patterns, or working with multidimensional data. By mastering nested loops and understanding their nuances, you'll unlock new levels of problem-solving efficiency in C#.