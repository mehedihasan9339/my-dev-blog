# Object-Oriented Programming (OOP) in C#

![OOP in C#](/images/csharpoop.jpg)

## What is Object-Oriented Programming (OOP)?

Object-Oriented Programming (OOP) is a programming paradigm that organizes software design around objects and classes, rather than functions and logic. The core concepts of OOP are **encapsulation**, **inheritance**, **polymorphism**, and **abstraction**.

### OOP Principles

#### 1. Encapsulation

Encapsulation is the concept of bundling data (fields) and methods that operate on that data within a single unit, i.e., a class. It helps protect the data by restricting direct access to it from outside the class.

```csharp
class Person
{
    private string name;  // Private field

    // Public method to set the value of name
    public void SetName(string personName)
    {
        name = personName;
    }

    // Public method to get the value of name
    public string GetName()
    {
        return name;
    }
}
```

In this example, we encapsulate the `name` field and control its access via `SetName` and `GetName` methods.

#### 2. Inheritance

Inheritance allows a class to inherit properties and methods from another class. This promotes reusability and is the foundation of the "is-a" relationship.

```csharp
class Animal
{
    public string Name { get; set; }

    public void Speak()
    {
        Console.WriteLine("Animal is speaking");
    }
}

class Dog : Animal
{
    public void Bark()
    {
        Console.WriteLine("Woof! Woof!");
    }
}
```

In this example, the `Dog` class inherits from the `Animal` class and gains access to its properties and methods.

#### 3. Polymorphism

Polymorphism allows objects of different types to be treated as objects of a common base type. It enables a method to have different behaviors based on the object type.

```csharp
class Animal
{
    public virtual void Speak()
    {
        Console.WriteLine("Animal is speaking");
    }
}

class Dog : Animal
{
    public override void Speak()
    {
        Console.WriteLine("Woof! Woof!");
    }
}

class Program
{
    static void Main()
    {
        Animal animal = new Animal();
        Dog dog = new Dog();

        animal.Speak();  // Outputs: Animal is speaking
        dog.Speak();     // Outputs: Woof! Woof!
    }
}
```

Here, both `Animal` and `Dog` have a `Speak` method, but the `Dog` class **overrides** the base class method to provide a different implementation.

#### 4. Abstraction

Abstraction is the concept of hiding complex implementation details and providing a simplified interface for the user. It is often achieved using **abstract classes** or **interfaces**.

```csharp
abstract class Animal
{
    public abstract void Speak();  // Abstract method - no body
}

class Dog : Animal
{
    public override void Speak()
    {
        Console.WriteLine("Woof! Woof!");
    }
}
```

In this example, the `Animal` class is **abstract**, meaning it cannot be instantiated directly. The `Dog` class provides a concrete implementation for the abstract `Speak` method.

---

## Creating and Using Objects

A class is a blueprint for creating objects (instances). You create an object by using the `new` keyword and calling the class constructor.

```csharp
class Person
{
    public string Name;
    public int Age;

    public Person(string name, int age)
    {
        Name = name;
        Age = age;
    }

    public void Introduce()
    {
        Console.WriteLine($"Hello, my name is {Name} and I am {Age} years old.");
    }
}

// Creating an object
Person person1 = new Person("John", 30);
person1.Introduce();  // Outputs: Hello, my name is John and I am 30 years old.
```

Here, `Person` is a class, and `person1` is an object created from that class.

---

## Constructor and Destructor

- **Constructor**: A special method that is called when an object is created. It is used to initialize objects.
- **Destructor**: A method that is called when an object is destroyed. It is used to clean up resources.

```csharp
class Car
{
    public string Model;

    // Constructor
    public Car(string model)
    {
        Model = model;
        Console.WriteLine($"{Model} car created.");
    }

    // Destructor
    ~Car()
    {
        Console.WriteLine($"{Model} car destroyed.");
    }
}
```

---

## Explanation:

- **Encapsulation**: Bundles data and methods into one unit. It protects the data by restricting access to it.
- **Inheritance**: Allows one class to inherit properties and methods from another class. Promotes reusability.
- **Polymorphism**: Allows different classes to have methods with the same name but different implementations.
- **Abstraction**: Hides complex logic and shows only the necessary parts to the user. Achieved through abstract classes and interfaces.

---

By mastering these OOP principles, you can write cleaner, more modular, and more maintainable C# code. OOP is a powerful paradigm that encourages code reuse and flexibility.

---
