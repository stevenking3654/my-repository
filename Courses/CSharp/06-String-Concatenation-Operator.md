## 🔗 String Concatenation Operator

String concatenation is the process of joining multiple strings to form a single, cohesive string.

In C#, the string concatenation operator is represented by the `+` symbol.

When strings are concatenated, the `+` operator sequentially combines them, resulting in the creation of a new string object in memory. In cases where non-string variables are included in the concatenation operation, C# automatically performs a conversion of these variables to string format.

#### ✏️ Example: 🖨️ Printing a Full Name

Consider a situation where we want to display a person's full name by combining their first and last names.

```csharp
string firstName = "Peter";
string lastName = "Smith";

string fullName = firstName + " " + lastName;
Console.WriteLine(fullName); // 👈 Output: "Peter Smith"
```

**Explanation**:

- `firstName + " " + lastName`: The expression `firstName + " " + lastName` combines the two variables with a space character (`" "`) in between, producing the final output of `"Peter Smith"`.
- `string fullName = firstName + " " + lastName`: The variable `fullName` holds the result after the concatenation of `firstName` and `lastName`.

#### ✏️ Example: 👋 Greeting a User

```csharp
string firstName = "Peter";
string lastName = "Smith";

string fullName = firstName + " " + lastName;
string greeting = "Hello, " + fullName + "!";
Console.WriteLine(greeting); // 👈 Output: "Hello, Peter Smith!"
```

**Explanation**:

- `string greeting = "Hello, " + fullName + "!"`: The variable `greeting` holds the result after the concatenation of `"Hello, "`, the value of `fullName`, and an exclamation mark.

#### ✏️ Example: 🌡️ Print Temperature

We can use the plus sign to combine strings with other strings, variables, or even other data types. C# is smart enough to convert non-string values to strings when they're used with the plus operator in a string concatenation operation.

```csharp
int temperature = 30;
string output = "The current temperature is " + temperature + " degrees Celsius.";

// 👇 Output: "The current temperature is 30 degrees Celsius."
Console.WriteLine(output);
```

#### ✏️ Example: 🧨 Formulating an Error Message

String concatenation is frequently employed in generating error/log messages or notifications.

```csharp
string fileName = "data.txt";
string errorMessage = "Error: The file '" + fileName + "' could not be found.";

// 👇 Output: "Error: The file 'data.txt' could not be found."
Console.WriteLine(errorMessage);
```