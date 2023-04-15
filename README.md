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

