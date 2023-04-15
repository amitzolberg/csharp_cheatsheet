[cheat sheet](https://github.com/LabinatorSolutions/csharp-cheat-sheet)

# Strings:
* String is a reference type that represents a sequence of characters.
* String can be created using string literals or by calling the string constructor.
* String is immutable, which means its value cannot be changed once it is created.
* String can be concatenated using the "+" operator.
* String can be compared using the "==" operator or the String.Equals method.
* String can be formatted using the String.Format method or the $"..." syntax.
## Example:
```
string s1 = "Hello";
string s2 = new string(new char[] { 'W', 'o', 'r', 'l', 'd' });
string s3 = s1 + " " + s2;
Console.WriteLine(s3);    // Output: Hello World
```

# Variables
* Variables are used to store data in a program.
* Variables have a type and a name.
* Variable's type specifies the kind of data that can be stored in it.
* Variable's name is used to refer to it in the program.
* Variables can be assigned a value using the "=" operator.
## Example:
```
int age = 30;
string name = "John";
double score = 85.5;
bool isStudent = true;
```
# Input/output instructions
Console.ReadLine and Console.WriteLine methods are used for input/output respectively.
## Example:
```
Console.Write("Enter your name: ");
string name = Console.ReadLine();
Console.WriteLine($"Hello, {name}!");
```
# Conversion (casting)
Conversion can be done implicitly or explicitly using cast operators or Convert methods.
##Example:
```
double x = 1.23;
int y = (int)x;
string s = "123";
int z = int.Parse(s);
```
# Division and remainder
Division is done using the "/" operator and remainder is done using the "%" operator.
## Example:
```
int a = 10;
int b = 3;
int c = a / b;      // integer
```
# For Loops
C# for loops are used to execute a block of code repeatedly. They are particularly useful when you know the number of times you want to execute a block of code.

## Syntax
```
for (initializer; condition; iterator) {
    // code to execute
}
```
* Initializer: This is an expression that is executed once before the loop starts. It is used to initialize the loop control variable.
* Condition: This is an expression that is checked before each iteration of the loop. If the condition is true, the loop continues; otherwise, it ends.
* Iterator: This is an expression that is executed after each iteration of the loop. It is used to update the loop control variable.
## Examples
### Example 1: Counting from 0 to 9
```
for (int i = 0; i < 10; i++) {
    Console.WriteLine(i);
}
```
This code will count from 0 to 9 and print each number on a new line.

### Example 2: Summing up the numbers from 1 to 100
```
int sum = 0;
for (int i = 1; i <= 100; i++) {
    sum += i;
}
Console.WriteLine(sum);
```
This code will sum up the numbers from 1 to 100 and print the result to the console.

### Example 3: Looping through an array
```
int[] numbers = { 1, 2, 3, 4, 5 };
for (int i = 0; i < numbers.Length; i++) {
    Console.WriteLine(numbers[i]);
}
```
This code will loop through the numbers array and print each element to the console.

### Example 4: Nested for loops
```
for (int i = 0; i < 3; i++) {
    for (int j = 0; j < 3; j++) {
        Console.WriteLine($"{i},{j}");
    }
}
```
This code will print all the combinations of the numbers 0, 1, and 2.

# Arrays
In C#, an array is a collection of values of the same type that are stored in a contiguous block of memory. Arrays can be of any type, including value types (e.g. int, double, etc.) and reference types (e.g. string, object, etc.).

## Declaration and Initialization
Arrays can be declared and initialized in several ways:

```
int[] numbers = new int[5];           // declaring an array of 5 integers
double[] prices = { 2.99, 3.99, 4.99 }; // initializing an array of doubles with values
string[] names = new string[] { "John", "Jane", "Bob" }; // initializing an array of strings with values
```
## Accessing Array Elements
Individual elements of an array can be accessed using an index. The index of the first element is 0, and the index of the last element is the length of the array minus one.

```
int[] numbers = { 1, 2, 3, 4, 5 };
Console.WriteLine(numbers[0]);   // Output: 1
Console.WriteLine(numbers[4]);   // Output: 5
```
## Common Operations on Arrays
### Finding the Maximum and Minimum Values
To find the maximum and minimum values in an array, you can loop through the array and keep track of the largest and smallest values seen so far.

```
int[] numbers = { 10, 20, 5, 25, 15 };
int max = numbers[0];
int min = numbers[0];
for (int i = 1; i < numbers.Length; i++) {
    if (numbers[i] > max) {
        max = numbers[i];
    }
    if (numbers[i] < min) {
        min = numbers[i];
    }
}
Console.WriteLine($"Max: {max}, Min: {min}");   // Output: Max: 25, Min: 5
```
### Counting the Occurrences of an Element
To count the number of times a particular element occurs in an array, you can loop through the array and count each occurrence.

```
int[] numbers = { 1, 2, 3, 2, 4, 2, 5 };
int count = 0;
for (int i = 0; i < numbers.Length; i++) {
    if (numbers[i] == 2) {
        count++;
    }
}
Console.WriteLine($"Count: {count}");   // Output: Count: 3
```
### Calculating the Average
To calculate the average of the elements in an array, you can loop through the array and sum up the values, then divide by the number of elements.

```
double[] prices = { 2.99, 3.99, 4.99 };
double sum = 0;
for (int i = 0; i < prices.Length; i++) {
    sum += prices[i];
}
double average = sum / prices.Length;
Console.WriteLine($"Average: {average}");   // Output: Average: 3.99
```
# Object-Oriented Programming:
## Classes
* Class is a blueprint for creating objects.
* Class can have attributes (fields) and operations (methods).
* Class can have a constructor that initializes its attributes.
* Class can have access modifiers such as private, public, protected, internal, etc.
* Class can have an array as an attribute.
* Class can have getter and setter methods to access and modify its attributes.
* ToString method is used to convert an object to a string representation.
* Object is created using the "new" keyword followed by the class name.
* Object's operations can be called using the dot notation.
### Example:
```
public class Person {
    private string name;
    private int age;
    private int[] scores;

    public Person(string name, int age, int[] scores) {
        this.name = name;
        this.age = age;
        this.scores = scores;
    }

    public string Name {
        get { return name; }
        set { name = value; }
    }

    public int Age {
        get { return age; }
        set { age = value; }
    }

    public int[] Scores {
        get { return scores; }
        set { scores = value; }
    }

    public double AverageScore() {
        double sum = 0;
        foreach (int score in scores) {
            sum += score;
        }
        return sum / scores.Length;
    }

    public override string ToString() {
        return $"{name} ({age})";
    }
}

Person john = new Person("John", 30, new int[] { 80, 90, 70 });
Person jane = new Person("Jane", 25, new int[] { 85, 95, 75 });
Console.WriteLine(john.Name);            // Output: John
Console.WriteLine(jane.Age);             // Output: 25
Console.WriteLine(john.AverageScore());  // Output: 80
Console.WriteLine(jane.ToString());      // Output: Jane (25)
```
