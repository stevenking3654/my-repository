## 🧠 Logical Operators

**Logical operators** are fundamental components in programming that allow developers to combine **multiple conditions** (boolean expressions and/or boolean variables).

Logical operators enable complex decision-making processes and enhance the control flow within applications.

The primary logical operators in C# include:

- **Logical AND**: `&&`
- **Logical OR**: `||`
- **Logical NOT**: `!`

### 🤝 The Logical `&&` Operator

The logical `AND` operator (`&&`) returns `true` only if **all** operands are `true`. If any operand is `false`, the result is `false`. This operator is used in scenarios where multiple conditions must be satisfied simultaneously.

| A     | B     | A && B |
|-------|-------|--------|
| true  | true  | true   |
| true  | false | false  |
| false | true  | false  |
| false | false | false  |

#### ✏️ Example: 💳 Eligibility for Driving

Imagine a system that determines whether a person can drive. Two conditions must be met:

1. They must possess a valid driver's license (`hasLicense`).
2. They must have access to a vehicle (`hasCar`).

```csharp
bool hasLicense = true; 
bool hasCar = false;

//     👇 Both conditions must be true
bool canDrive = hasLicense && hasCar;
Console.WriteLine(canDrive); // 👈 Output: "False"
```

**Explanation**:

- `hasLicense`: Indicates whether the user has a valid driver's license.
- `hasCar`: Indicates whether the user owns a car.
- `bool canDrive = hasLicense && hasCar`: The variable `canDrive` evaluates to `true` only if both `hasLicense` and `hasCar` are `true`.

#### ✏️ Example: ✈️ Airport Check-In

Consider a system at an airport that checks if passengers meet boarding requirements:

1. A valid ticket (`hasTicket`).
2. Passing security clearance (`isCleared`).

```csharp
bool hasTicket = true;
bool isCleared = true;

bool canBoard = hasTicket && isCleared;
Console.WriteLine(canBoard); // 👈 Output: "True"
```

If either condition is unmet, the passenger cannot board the flight.

### ⚖️ The Logical `||` Operator

The logical `OR` operator (`||`) returns `true` when **at least one** of its operands is evaluated to `true`. This operator is particularly useful when any one of multiple conditions must be satisfied.

| A     | B     | A || B |
|-------|-------|--------|
| true  | true  | true   |
| true  | false | true   |
| false | true  | true   |
| false | false | false  |

#### ✏️ Example: ☁️ Planning Outdoor Activities

Suppose we want to decide whether to go outside. The conditions are:

1. The weather is sunny (`isSunny`).
2. The temperature is warm (`isWarm`).

```csharp
bool isSunny = true; 
bool isWarm = false;

//     👇 At least one condition must be true
bool goOutside = isSunny || isWarm;
Console.WriteLine(goOutside); // 👈 Output: "True"
```

**Explanation**:

- `isSunny`: Indicates whether the weather is sunny.
- `isWarm`: Indicates whether the temperature is warm.
- `bool goOutside = isSunny || isWarm`: The variable `goOutside` evaluates to `true` if either `isSunny` or `isWarm` is `true`.

#### ✏️ Example: 🛒 Online Shopping Discounts

Consider a discount applied if:

1. The user has a coupon (`hasCoupon`).
2. The user is a loyalty program member (`isLoyalCustomer`).

```csharp
bool hasCoupon = false;
bool isLoyalCustomer = true;

bool getsDiscount = hasCoupon || isLoyalCustomer;
Console.WriteLine(getsDiscount); // 👈 Output: "True"
```

Even without a coupon, being a loyal customer is enough to qualify for the discount.

### ⛔ The Logical `!` Operator

The logical `NOT` operator (`!`) inverts/negates the value of its operand, flipping a boolean expression from `true` to `false`, or vice versa.

| A     | !A    |
|-------|-------|
| true  | false |
| false | true  |

#### ✏️ Example: ⌨️ Detecting User Inactivity

Consider a system that triggers an alert if the user is inactive.

```csharp
bool isUserActive = true;

Console.WriteLine(!isUserActive); // 👈 Output: "False"
```

**Explanation**:

- `bool isUserActive = true;`: The variable `isUserActive` indicates that the user is currently active.
- `!isUserActive`: The `!` operator negates the value of `isUserActive`.

#### ✏️ Example: 🕒 Late Night Access Control

A program might restrict access during late hours. For instance, access is denied if the current time is **not** during regular hours (`isRegularHours`).

```csharp
bool isRegularHours = false;

bool accessDenied = !isRegularHours;
Console.WriteLine(accessDenied); // 👈 Output: "True"
```