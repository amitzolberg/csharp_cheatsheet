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
csharp
Copy code
string s1 = "Hello";
string s2 = new string(new char[] { 'W', 'o', 'r', 'l', 'd' });
string s3 = s1 + " " + s2;
Console.WriteLine(s3);    // Output: Hello World
Object-Oriented Programming:
```
# Classes
* Class is a blueprint for creating objects.
* Class can have attributes (fields) and operations (methods).
* Class can have a constructor that initializes its attributes.
* Class can have access modifiers such as private, public, protected, internal, etc.
* Class can have an array as an attribute.
* Class can have getter and setter methods to access and modify its attributes.
* ToString method is used to convert an object to a string representation.
* Object is created using the "new" keyword followed by the class name.
* Object's operations can be called using the dot notation.
## Example:
```
csharp
Copy code
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
