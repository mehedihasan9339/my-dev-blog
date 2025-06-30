# C# Data Types

![C# Logo](/images/csharpdatatypes.png)

## Value Types

### `int` - Integer (Whole Number)

```csharp
int age = 25;  // Stores a whole number
```

### `double` - Floating Point Number (Decimal)

```csharp
double temperature = 36.6;  // Stores a decimal number
```

### `float` - Less Precise Decimal Number

```csharp
float pi = 3.14f;  // Stores a decimal number, with less precision than double
```

### `char` - Single Character

```csharp
char grade = 'A';  // Stores a single character
```

### `bool` - Boolean (True/False)

```csharp
bool isLearningCSharp = true;  // Stores either true or false
```

### `byte` - Small Integer (0 to 255)

```csharp
byte smallNumber = 100;  // Stores small whole numbers (0 to 255)
```

### `decimal` - Precise Decimal (Used for Money)

```csharp
decimal price = 19.99m;  // Stores a precise decimal value
```

## Reference Types

### `string` - Text (Sequence of Characters)

```csharp
string name = "John";  // Stores a sequence of characters (text)
```

### `object` - Can Hold Any Data Type

```csharp
object anything = 123;  // Can store any data type, including numbers and text
```

## Nullable Types

### Nullable `int`

```csharp
int? age = null;  // Nullable type can hold null as a value
```

### Nullable `bool`

```csharp
bool? isAvailable = null;  // Nullable type can hold null
```

## Type Conversion

### Implicit Conversion (Smaller to Larger)

```csharp
int num1 = 5;
double num2 = num1;  // Implicit conversion from int to double
```

### Explicit Conversion (Larger to Smaller)

```csharp
double pi = 3.14;
int roundedPi = (int)pi;  // Explicit conversion (double to int), truncates decimal part
```

### Explanation:

- **Value Types**: Store the actual data. These include `int`, `double`, `float`, `char`, `bool`, `byte`, and `decimal`.
- **Reference Types**: Store references to the data in memory. These include `string` and `object`.
- **Nullable Types**: Allow value types to hold a `null` value.
- **Type Conversion**: Demonstrates how data types are converted between each other, both implicitly and explicitly.
