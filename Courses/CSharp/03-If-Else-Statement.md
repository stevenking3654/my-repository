## If-Else Statement

IF-ELSE statements enable our programs to take one path if a condition is true and another if it's false. They feature the familiar `if` keyword, a condition in parentheses, a block of code for the true scenario, followed by the `else` keyword and another block of code for the false scenario.

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

```csharp
var studentScore = int.Parse(Console.ReadLine());
var output = "";

if (studentScore >= 50)
{
	output = "Pass!";
}
else
{
	output = "Fail!";
}

Console.WriteLine(output);
```