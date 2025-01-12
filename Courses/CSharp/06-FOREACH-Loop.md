## Foreach Loop
## 🔍 `foreach` Loop

It simplifies the code by handling index management automatically.
### 📃 Basic Syntax & Structure

It is especially useful when we don't need to worry about the index/position of each element and is often simpler than the `for` loop when working with collections.

#### ✏️ Example: Iterating Over an Array of Names

```csharp
string[] names = { "Alice", "Bob", "Charlie" };

foreach (string name in names)
{
	Console.WriteLine($"Hello {name}!");
}
```

In this example, we declare an array of strings. The `foreach` loop iterates over each element in the collection.

We declare a variable `name` of type `string`. During each iteration of the loop, this variable will hold the current element from the `names` array.

It simplifies the process of looping through arrays and collections without needing to manage a position/index manually.

#### ✏️ Example: Monitoring Critical Temperature Thresholds

Suppose we are monitoring the temperature of a machine and need to shut down if it exceeds a critical level.

```csharp
double[] temperatures = { 25.5, 34.5, 80.5, 43, 36.8, 56.4, 64.2 };
double criticalTemperature = 60.0;

foreach (double temperature in temperatures)
{
    if (temperature > criticalTemperature)
    {
        Console.WriteLine($"⚠️ Critical temperature reached: {temperature}°C. Shutting down system.");
        break;
    }
    Console.WriteLine($"Temperature is safe: {temperature}°C");
}
```

In this example, the loop exits immediately once a temperature exceeds the critical threshold.

#### ✏️ Example: Skipping Negative Reviews in an Analysis

Imagine we are analyzing customer reviews and want to ignore reviews with negative scores.

```csharp
int[] reviewScores = { 5, 3, -1, 4, -2, 5 };
int totalScore = 0;
int validReviews = 0;

foreach (int score in reviewScores)
{
	// Skip negative reviews
    if (score < 0)
    {
	    continue;
    }

    totalScore += score;
    validReviews++;
}

double averageScore = (double)totalScore / validReviews;
Console.WriteLine($"📊 Average positive review score: {averageScore:F2}");
```