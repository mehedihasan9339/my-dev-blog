# Control Flow in C#

![C# Control Flow](/images/csharpcontrolflow.jpg)

## Conditional Statements

### `if` Statement - Basic Condition

```csharp
int number = 10;
if (number > 5)
{
    Console.WriteLine("The number is greater than 5.");
} // Executes if the condition is true
```

### `else` Statement - Alternative Action

```csharp
int number = 3;
if (number > 5)
{
    Console.WriteLine("The number is greater than 5.");
}
else
{
    Console.WriteLine("The number is 5 or less.");
} // Executes if the condition is false
```

### `else if` Statement - Multiple Conditions

```csharp
int number = 7;
if (number > 10)
{
    Console.WriteLine("The number is greater than 10.");
}
else if (number > 5)
{
    Console.WriteLine("The number is between 6 and 10.");
}
else
{
    Console.WriteLine("The number is 5 or less.");
} // Checks multiple conditions in sequence
```

### `switch` Statement - Multiple Choices

```csharp
int dayOfWeek = 3;
switch (dayOfWeek)
{
    case 1:
        Console.WriteLine("Monday");
        break;
    case 2:
        Console.WriteLine("Tuesday");
        break;
    case 3:
        Console.WriteLine("Wednesday");
        break;
    default:
        Console.WriteLine("Invalid day");
        break;
} // Matches value with multiple cases
```

## Loops

### `for` Loop - Repeating an Action

```csharp
for (int i = 0; i < 5; i++)
{
    Console.WriteLine($"Iteration {i}");
} // Loops a set number of times
```

### `while` Loop - Loops as Long as Condition is True

```csharp
int counter = 0;
while (counter < 5)
{
    Console.WriteLine($"Counter: {counter}");
    counter++;
} // Loops while the condition is true
```

### `foreach` Loop - Looping Through a Collection

```csharp
string[] fruits = { "Apple", "Banana", "Cherry" };
foreach (var fruit in fruits)
{
    Console.WriteLine(fruit); // Loops through each element in the collection
}
```

### `break` Statement - Exit Loop Early

```csharp
for (int i = 0; i < 10; i++)
{
    if (i == 5)
    {
        break; // Exits the loop when i is 5
    }
    Console.WriteLine(i);
}
```

### `continue` Statement - Skip the Current Iteration

```csharp
for (int i = 0; i < 5; i++)
{
    if (i == 3)
    {
        continue; // Skips the iteration when i is 3
    }
    Console.WriteLine(i);
}
```

## Explanation:

- **Conditional Statements**: Used to make decisions based on certain conditions. Includes `if`, `else`, `else if`, and `switch`.

  - `if`: Executes code when a condition is true.
  - `else`: Executes code when the `if` condition is false.
  - `else if`: Checks another condition if the `if` condition is false.
  - `switch`: Compares a variable with multiple possible values.

- **Loops**: Used to repeat a block of code multiple times.

  - `for`: Repeats a block of code for a specific number of iterations.
  - `while`: Repeats a block of code as long as the condition remains true.
  - `foreach`: Loops through each element of a collection (e.g., array, list).

- **Control Flow Modifiers**:

  - `break`: Exits the loop or switch statement prematurely.
  - `continue`: Skips the current iteration of a loop and moves to the next one.

Control flow statements are crucial for making decisions and repeating actions based on conditions. Mastering these will help you create dynamic, flexible programs.

---
