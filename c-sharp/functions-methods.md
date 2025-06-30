# Functions and Methods in C#

![C# Functions](/images/csharpfunctions.png)

## What is a Function/Method?

A function (or method) in C# is a block of code designed to perform a specific task. Functions make your code more modular, reusable, and easier to manage.

### Syntax of a Method

```csharp
returnType MethodName(parameters)
{
    // Method body
    // Code to execute
    return value; // If return type is not void
}
```

- `returnType`: The type of data the method will return (e.g., `int`, `string`, `void` for no return).
- `MethodName`: The name of the method.
- `parameters`: The input data the method needs to perform its task (optional).
- `return`: The output value returned from the method (if any).

## Defining a Simple Method

### Method Without Parameters

```csharp
void SayHello()
{
    Console.WriteLine("Hello, World!"); // This method prints a message
}
```

### Method With Parameters

```csharp
void GreetPerson(string name)
{
    Console.WriteLine($"Hello, {name}!"); // Greets a person by name
}
```

### Method With Return Value

```csharp
int AddNumbers(int num1, int num2)
{
    return num1 + num2; // Adds two numbers and returns the result
}
```

### Calling a Method

You can call a method by its name and passing in the necessary arguments (if any).

```csharp
SayHello(); // Calls the SayHello method

GreetPerson("John"); // Calls the GreetPerson method with "John" as the argument

int result = AddNumbers(5, 3); // Calls the AddNumbers method and stores the result
Console.WriteLine(result); // Prints 8
```

## Method Overloading

In C#, you can create multiple methods with the same name but different parameters (method overloading).

```csharp
int AddNumbers(int num1, int num2)
{
    return num1 + num2;
}

double AddNumbers(double num1, double num2)
{
    return num1 + num2;
}

Console.WriteLine(AddNumbers(5, 3)); // Calls the int version
Console.WriteLine(AddNumbers(5.5, 3.2)); // Calls the double version
```

## Recursion in C\#

A method that calls itself is known as **recursion**. It’s useful for tasks that can be broken down into smaller, similar tasks (like calculating factorials).

### Example: Calculating Factorial Using Recursion

```csharp
int Factorial(int n)
{
    if (n == 0)
        return 1; // Base case: 0! = 1
    else
        return n * Factorial(n - 1); // Recursive call
}

Console.WriteLine(Factorial(5)); // Output: 120 (5! = 5*4*3*2*1)
```

## Explanation:

- **Functions/Methods**: Functions are blocks of code that perform specific tasks. They can be called whenever needed, making your code more modular.

- **Parameters**: Functions can take parameters (inputs) that they use to perform their tasks. These parameters can be of any data type.

- **Return Values**: Methods can return values using the `return` keyword. If no value is returned, the method's return type is `void`.

- **Method Overloading**: Allows defining methods with the same name but different parameter types or numbers, making your code more flexible.

- **Recursion**: A technique where a method calls itself, commonly used for problems that can be divided into smaller similar problems, like computing factorials or Fibonacci numbers.

---
