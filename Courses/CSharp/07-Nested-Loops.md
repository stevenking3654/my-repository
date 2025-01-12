## 📦 Nested Loops

## 🔀 Nested Loops

Nested loops are loops inside other loops.

Nested loops are useful when dealing with multidimensional data structures, matrices, tables, or patterns that require layered iteration.

When used within nested loops, the `break` and `continue` statements operate in the innermost loop they refer to.

#### ✏️ Example: Simple Calendar Grid

```csharp
int weeks = 4;
int daysInWeek = 7;

for (int week = 1; week <= weeks; week++)
{
	Console.Write($"Week {week}:");

	for (int day = 1; day <= daysInWeek; day++)
	{
		Console.Write($"Day {day} ");
	}

	Console.WriteLine();
}
```

#### ✏️ Example: Multiplication Table

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

#### ✏️ Example: Displaying a Seating Chart

Suppose you are creating a seating chart for a small venue where rows are numbered and each seat has a letter.

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