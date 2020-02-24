# CS Programming Language Cheat Sheet
When learning CS, it is always good practice to refresh yourself on some previously learned concepts.

These are some basic tips and concepts to refresh your memory on some of software engineering's biggest programming languages made simple. Many concepts such as proper syntax, data structures, and algorithms for each language will be covered. Good luck and happy learning!

## PYTHON
- [Basic Python](#basic-python) : Learn basic Python concepts and syntax
- [Python Data Structures](#python-data-structures) : Different kinds of data structures that can be used in Python

## JAVA
- [Basic Java](#basic-java) : Learn basic Java concepts and syntax
- [Java Data Types](#java-data-types) : Learn data types you can cast with Java
- [Java Loops and Conditions](#java-loops-and-conditions) : Learn for and while loops, if/else statements, etc.
- [Java Methods and Classes](#java-methods-and-classes) : Learn how to create methods and use classes and objects.  

## C++  
- [Basic C++](#basic-c) : Learn basic C++ concepts and syntax
- [Loops and Conditions](#loops-and-conditions) : : Learn for and while loops, if/else statements, etc.

### Basic Python
All python files are saved ending in .py 

For example, I can create a file called test.py with the following code:
```python
print('Hellow World')
s = "Hello Again"
print s
```
In order to run the code on the terminal, go to the correct directory and run **python test.py**  
This will result in the following code being printed out on the terminal:  
`Hello World`  
`Hello Again`  

We do not need to specify a type when declaring variables so a variable can contain anything including ints, floats, strings, booleans, and etc. No need to end lines with **;** just write code normally:  
```python
s = "Hello Again"
num = 12
answer = True
```  
Types can include: **bool, int, long, float, str, tuple, list, dict**  

**Strings**: Let us look at Strings in particular and see some useful functions we can use on strings:  
- `len` : allows us to find length of string  
```python
phrase = "Hi"
len(phrase)    # Should return 2
```  
- indexing a string: can index a string using brackets [] (is 0-indexed)  
```python
phrase = "test"
phrase[0]    # Returns 't'
```  
- `.index()` : returns index of where character or string is first located  
```python
phrase = "Hello World"
phrase.index("e")    # Returns 1
phrase.index("World")    # Returns 6
```  
- `.split(separator)` : splits string into a list. Default separator is any whitespace if none is specified
```python
phrase = "Hello World"
phrase.split()    # Returns ['Hello', 'World'] 

```  
- `.replace(old_value, new_value)` : replaces every instance of old_value with new_value within string  
```python
phrase = "Hello World"
phrase.replace("World", "Universe")    # phrase is now "Hello Universe"
```  
- `int("string")` : converts strings to ints 
```python
int("6")    # converts "6" to 6
```  
- [More String Functions](https://www.w3schools.com/python/python_ref_string.asp)  
  
  
**Numbers**: Some useful concepts and functions for number types (including ints and floats)  
- Math operations:  
```python
1 + 2    # Returns 4
1 - 2    # Returns -1
2 * 3    # Returns 6
2 ** 3   # Returns 8
5 / 2    # Returns 2.5
5 // 2   # Returns 2
```  

- `str()` : allows you to convert number type to string
```python
my_num = 5
phrase = str(my_num)    # phrase should now contain '5'
```  
- `abs()` : finds absolute value of number
```python
my_num = -3
print(abs(my_num))    # prints 3
```  
- `pow(num, exponent)` : allows you to calculate num to the power of exponent
```python
my_num = 5
print(pow(my_num, 2))    # prints 25
```  
- `max(num1, num2)` : returns larger value
```python
print(max(4,6))    # returns 6
```  
- `min(num1, num2)` : returns smaller value
```python
print(min(4,6))    # returns 4
```  
- `from math import *` : allows us to use even more functions such as floor(), ceil(), and sqrt()  
- `RANDOM` : allows you to select random int from range  
```python
import random
def roll_dice(num):
  return random.randint(1,num)   # Random from 1 to num-1
  
**User Input**: How to get and use user input from terminal
- `input()` : allows us to have user input information  
```python
name = input("Enter your name: ")    # stores users input in name
print("Hello " + name + "!")
```  

**Functions**: Allow users to create methods that can perform tasks and manipulate input. Indentation is important!
```python  
def say_hi(name, age):
  print("Hello " + name + " you are " + str(age) + " years old.")
  return None    # Python's way of saying null
  
say_hi("Kevin", 22)    # This function prints 'Hello Kevin you are 22 years old.'
```  
**Conditional Statements**: Allows conditions to be made in code
```python
is_true = True
is_false = False
if is_True:
  print('Success')
 elif is_true and is_false:
  print('Skipped')
elif is_true or is_false:
  print('Success')
elif not is_false"
  print('Success')
else:
  print('Skipped')
```  

**Compare Statements**: Allows users to compare values. Comparisons include **>, <, >=, <=, ==, != **  
```python
2>1    # Returns True
1<=1    # Returns True
1!=2    # Returns True

s = "test"
s == 'test'    # Returns True
```  

**While Loops**: Loops while condition is met  
```python
i = 1
while i <= 10:    # Prints i 10 times 
  print(i)
  i += 1
```  
**For Loops**: Loops over collection of items  
```python
colors = ["Red", "Blue", "Green"]
for color in colors:
  print(colors)    # Prints all of the colors

for index in range(5):
  print(index)    # Prints 0,1,2,3,4
  
for index in range(2,5):
  print(index)    # Prints 2,3,4
```  
Users can also do a nested for-loop:  
```python  
numbers = [
  [1,2,3],
  [4,5,6],
  [7,8,9],
  [0]
 ]
 for row in numbers:
  for col in row:
    print(col)
 ```  
**Try-Excpet Blocks** Programs tries code and if error is thrown, we will have an instance for that situation.
```python
try:
 number = int(input("Enter a number: "))    # What if someone inputs a string instead of a number?
 print(number)
except:
 print("Invalid Input")    # Exception will catch every error
  
try:
  value = 10 / 0
  number = int(input("Enter a number: "))   
  print(number)
except ZeroDivisionError:
  print("Invalid Input")    # Exception will catch zero division error 
except ValueError:
  print("Invalid Input")    # Exception will invalid input error  
 ```  
 
 - [List of More Exceptions](https://www.programiz.com/python-programming/exceptions)  
 
**Reading Files** How to read, write, and append to files using Python  
```python  
employee_file = open("employees.txt", "r")    # Make sure file is in correct directory
employee_file.readable()    # Returns True if readable
for employee in employee_file.readlines():
  print(emplyee)
employee_file.close()    # Good practice to close files after using them

employee_file = open("employees.txt", "a")    # APPEND
employee_file.readable()    # Returns True if readable
employee_file.write("\nKevin - Programmer)    # Appends to the end of the file
employee_file.close()    # Good practice to close files after using them

employee_file = open("employees.txt", "w")    # Writes to file (if employees.txt does not exist, it creates file)
                                              # Can create any file: .txt, .html, .css, etc.
employee_file.readable()    # Returns True if readable
employee_file.write("\nKevin - Programmer)    # Overwrites entire file and replaces it with write text
employee_file.close()    # Good practice to close files after using them
```  
**Importing Other Files** : Import other files to get access to their variables and functions
```python
import useful_tools    # Do not need to include the .py for the file
useful_tools.roll_dice(10)    # Use useful_tools methods
```  

**Classes and Objects** : How to create classes and objects and use them effectively
- Let us create a `Student` class in a file called Student.py:  
```python
class Student:
  def __init__(self, name, major, gpa):
    self.name = name
    self.major = major
    self.gpa = gpa
  def on_honor_roll(self):
    if self.gpa >= 3.5:
      return True
     else:
      return False
```  
- Now let's use this class in a new file called app.py:  
```python
from Student import Student    # From the Student file import Student class
student1 = Student('Jim', 'Business', 3.8)    # Creates a Student object
student2 = Student('Pam', 'Art', 2.5)
student2.gpa    # Returns 2.5
student1.on_honor_roll()    # Returns True
```  
**Inheritance**: We can inherit classes in order to not be repeating code across classes
```python
class Chef:
  def make_chicken(self):
    print("Making Chicken")
  def make_special(self):
    print("Making Burger")
    
-----------------------------
 
from Chef import Chef
class ItalianChef(Chef):
 def make_special(self):
   print("Making Pasta")

-----------------------------

from Chef import Chef
from ItalianChef import ItalianChef
myChef = Chef()
myChef.make_special()           # Prints 'Making Burger'
myItalianChef = ItalianChef()
myItalianChef.make_Special()    # Prints 'Making Pasta'
```

### Python Data Structures
**Lists**: 
- Most widely used data structure
- Grow and shrink size as needed
- Sequence type
- Sortable  

<img width="644" alt="list" src="https://user-images.githubusercontent.com/16792195/75100362-6f059380-5581-11ea-9cd6-bb05c265f288.png">     

```python
foods = ['ham', 'eggs', 'beans', 'turkey', 'candy', 'apples']    # Declares a list
print(foods[0])    # Prints ham
print(foods[-1])    # Prints apples
print(foods[1:])    # Prints 'eggs', 'beans', 'turkey', 'candy', 'apples'
print(foods[1:3])    # Prints eggs, beans (includes 1 index and everything up to but not including 3)

numbers = [5,3,4,1,2]
foods.extend(numbers)    # foods becomes ['ham', 'eggs', 'beans', 'turkey', 'candy', 'apples',5,3,4,1,2]  
foods.append('bread')    # foods becomes ['ham', 'eggs', 'beans', 'turkey', 'candy', 'apples', 'bread']  
foods.insert(1, 'bread')    # foods becomes ['ham', 'bread', 'eggs', 'beans', 'turkey', 'candy', 'apples'] 
foods.remove('ham')    # foods becomes ['eggs', 'beans', 'turkey', 'candy', 'apples'] 
foods.clear()    #foods becomes []
foods.pop()    # foods becomes ['ham', 'eggs', 'beans', 'turkey', 'candy']
foods.index('eggs')    # Returns 1
foods.count('ham')    # Returns 1
foods.sort()    # Sorts list in alphabetical / numerical order
numbers.reverse()     # Reverses numbers
more_foods = foods.copy()    # more_foods copies foods
```  
We can also create multi-dimensional lists and access them easily:  
```python
numbers = [
  [1,2,3],
  [4,5,6],
  [7,8,9],
  [0]
 ]
 numbers[0][0]    # Returns 1
 numbers[3]       # Returns [0]
 numbers[3][0]    # Returns 0
```  

**Tuples**: Support all operations that do not mutate the data structure (and have same complexity)
- Immutable (can't add/change
- Useful for fixed data
- Faster than lists
- Sequnce Type
```python
coordinates = (4,5)    # Use () instead of []
coordinates[1]    # Returns 5
coordinates = [(4,5), (1,2)]    # Can make list of tuples  
```  

**Dictionary**: 
- Key/Value Pairs
- Associative array, like Java HashMap
- Unordered  

<img width="644" alt="dict" src="https://user-images.githubusercontent.com/16792195/75100465-8db85a00-5582-11ea-99fc-7e930c5bd1bd.png"><br/>  
```python
months = {
  "Jan":"January,
  "Feb":"February,
  "March":"March",
 }
 
 months["Jan"]    # Returns "January"
 months.get("Jan")    # Returns "January"
 months.get("Dec")    # Returns None
 months.get("Dec", "Not valid")    # Returns default value "Not Valid"
 ```  

 
 **Sets**
 - Store non-duplicate items
 - Very fast access vs Lists
 - Math Set ops (union, intersect)
 - Unordered  
 
 <img width="643" alt="sets" src="https://user-images.githubusercontent.com/16792195/75100452-737e7c00-5582-11ea-9046-8efbd59479cc.png"><br/>  
 
 ```python
 set = {1,2,3,4,1}    # Set is {1,2,3,4}
 ```  
## JAVA
### Basic Java  
- Java works on different platforms (Windows, Mac, Linux, Raspberry Pi, etc.)
- It is one of the most popular programming language in the world
- It is easy to learn and simple to use
- It is open-source and free
- It is secure, fast and powerful
- It has a huge community support (tens of millions of developers)
- Java is an object oriented language which gives a clear structure to programs and allows code to be reused, lowering development costs
- As Java is close to C++ and C#, it makes it easy for programmers to switch to Java or vice versa  

Java is used for:  
- Mobile applications (specially Android apps)
- Desktop applications
- Web applications
- Web servers and application servers
- Games
- Database connection
- And much, much more!  
Every java file ends with .java such as for example `MyClass.java` :  
```java
public class MyClass {
  public static void main(String[] args) {
    System.out.println("Hello World");
  }
}
```  
Every line of code ends with a semicolon **;** and instead of : we use { to begin a clause.  
The name if the java file **MUST MATCH** the class name!  
Every java file must contain the `main()` method:  
```java
public static void main(String[] args)
```  
In order to perform a **comment** in java, we do the following:  
```java
// This is a comment
System.out.println("Hello World");

/* The code below will print the words Hello World
to the screen, and it is amazing */
System.out.println("Hello World");

```  
In order to **run** the program must type in the following:  
- javac MyClass.java    (this will compile the code)
- java MyClass          (this will run the code)  

### Java Data Types  
<img width="809" alt="java_types" src="https://user-images.githubusercontent.com/16792195/75100839-12f23d80-5588-11ea-8225-9b9451028f8a.png"><br/>

```java  
int myNum = 5;
float myFloatNum = 5.99f;
char myLetter = 'D';
boolean myBool = true;
String myText = "Hello";
```  
<img width="686" alt="java_ops" src="https://user-images.githubusercontent.com/16792195/75101678-04f6e980-5595-11ea-822d-72850bc177a7.png"><br/>
<img width="627" alt="java_simple" src="https://user-images.githubusercontent.com/16792195/75101710-cb72ae00-5595-11ea-9817-5641feddbaf1.png"><br/>
<img width="584" alt="java_compare" src="https://user-images.githubusercontent.com/16792195/75101711-cca3db00-5595-11ea-9713-c7798c25c091.png"><br/>
<img width="708" alt="java_logic" src="https://user-images.githubusercontent.com/16792195/75101712-cd3c7180-5595-11ea-9fc5-1ed4c8b98c9e.png"><br/>  
**Strings**: Some useful String Methods  
```java
String txt = "Hello World";
System.out.println(txt.toUpperCase());   // Outputs "HELLO WORLD"
System.out.println(txt.toLowerCase());   // Outputs "hello world"

String txt = "Please locate where 'locate' occurs!";
System.out.println(txt.indexOf("locate")); // Outputs 7

String txt = "It\'s alright.";
```  
**Math**: Couple of math methods users can use  
```java  
Math.max(5, 10);
Math.min(5, 10);
Math.sqrt(64);
Math.abs(-4.7);
Math.random();
```  
- [List of more Java math methods](https://www.w3schools.com/java/java_ref_math.asp)  

### Java Loops and Conditions  
Here are some conditional statements including if, else, and else if:  

```java
int time = 22;
if (time < 10) {
  System.out.println("Good morning.");
} else if (time < 20) {
  System.out.println("Good day.");
} else {
  System.out.println("Good evening.");
}
// Outputs "Good evening."

//--------------------------------------
int time = 20;
if (time < 18) {
  System.out.println("Good day.");
} else {
  System.out.println("Good evening.");
}

int time = 20;
//variable = (condition) ? expressionTrue :  expressionFalse;
String result = (time < 18) ? "Good day." : "Good evening.";     // Simpler way of describing same thing
System.out.println(result);
```  
**Switch Statements** : Use if you want to select one of the many code blocks to be executed  
```java
int day = 4;
switch (day) {
  case 6:
    System.out.println("Today is Saturday");
    break;
  case 7:
    System.out.println("Today is Sunday");
    break;
  default:
    System.out.println("Looking forward to the Weekend");
}
// Outputs "Looking forward to the Weekend"
```  
**While loops** While loops will continue to loop until condition is satisfied  
```java  
int i = 0;
while (i < 5) {
  System.out.println(i);
  i++;
}
```  
The **do/while** loop will always execute the code block once before checking if condition is true, then it will repeat the loop as long as the condition is true.  
```java  
int i = 0;
do {
  System.out.println(i);
  i++;
}
while (i < 5);
```  
**For Loop** Loop through code a certain amount of times.  
```java  
for (int i = 0; i < 5; i++) {
  System.out.println(i);
}

String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
for (String i : cars) {
  System.out.println(i);
}
```  
**Break and Continue** Break breaks out of the loop immediately. Continue breaks one iteration of the loop.  

**Try/Catch Clauses** Catches exceptions within a bracket of executed code  
```java  
import java.io.File;  // Import the File class
import java.io.IOException;  // Import the IOException class to handle errors

public class CreateFile {
  public static void main(String[] args) {
    try {
      File myObj = new File("filename.txt");
      if (myObj.createNewFile()) {
        System.out.println("File created: " + myObj.getName());
      } else {
        System.out.println("File already exists.");
      }
    } catch (IOException e) {
      System.out.println("An error occurred.");
      e.printStackTrace();
    }
  }
}
```  


### Java Methods and Classes
In order to define a mehtod, you need to define a return value (void, int, char, etc.), a name, and parameters:  
```java  
public class MyClass {
  static int myMethod(int x, int y) {
    return x + y;
  }

  public static void main(String[] args) {
    int z = myMethod(5, 3);
    System.out.println(z);
  }
}
// Outputs 8 (5 + 3)
```  
In this example, `static` means that the method belongs to the MyClass class and not an object of the MyClass class.  
**Classes**  

Object-oriented programming has several advantages over procedural programming:
- OOP is faster and easier to execute
- OOP provides a clear structure for the programs
- OOP helps to keep the Java code DRY "Don't Repeat Yourself", and makes the code easier to maintain, modify and debug
- OOP makes it possible to create full reusable applications with less code and shorter development time  
Classes are simple to make and multiple classes can be used at a time (just need to make sure they are in the same directory)  
```java
//MyClass.java
public class MyClass {
  final int x = 5;     //If you don't want the ability to override existing values, declare the attribute as final
}

//OtherClass.java
class OtherClass {
  public static void main(String[] args) {
    MyClass myObj = new MyClass();
    System.out.println(myObj.x);
  }
}

//Just make sure to javac both files before using.
```  
**STATIC AND NON-STATIC METHODS** A clear example of when and how to use static and non-static methods in program.  
```java  
public class MyClass {
  // Static method
  static void myStaticMethod() {
    System.out.println("Static methods can be called without creating objects");
  }

  // Public method
  public void myPublicMethod() {
    System.out.println("Public methods must be called by creating objects");
  }

  // Main method
  public static void main(String[] args) {
    myStaticMethod(); // Call the static method
    // myPublicMethod(); This would compile an error

    MyClass myObj = new MyClass(); // Create an object of MyClass
    myObj.myPublicMethod(); // Call the public method on the object
  }
}  
```  
**Constructors**  How to initialize an object with certain parameters.  
```java  
public class Car {
  int modelYear;
  String modelName;

  public Car(int year, String name) {
    modelYear = year;
    modelName = name;
  }

  public static void main(String[] args) {
    Car myCar = new Car(1969, "Mustang");
    System.out.println(myCar.modelYear + " " + myCar.modelName);
  }
}

// Outputs 1969 Mustang  
```  
**Inheritance** : To inherit from a class, use the `extends` keyword.  
```java  
class Vehicle {
  protected String brand = "Ford";        // Vehicle attribute
  public void honk() {                    // Vehicle method
    System.out.println("Tuut, tuut!");
  }
}

class Car extends Vehicle {
  private String modelName = "Mustang";    // Car attribute
  public static void main(String[] args) {

    // Create a myCar object
    Car myCar = new Car();

    // Call the honk() method (from the Vehicle class) on the myCar object
    myCar.honk();

    // Display the value of the brand attribute (from the Vehicle class) and the value of the modelName from the Car class
    System.out.println(myCar.brand + " " + myCar.modelName);
  }
}  
```  
**SUPER and Proper Inheritance** : If want to inherit from class with constructor already, follow this example:  
```java  
// Animal.java
public class Animal {
	String name;
	String type;
	int age;
	public Animal(String animal_name, String animal_type, int animal_age) {
		name = animal_name;
		type = animal_type;
		age = animal_age;
	}

	public void shout() {
		System.out.println("REEEEE");
	}
	public void cook() {
		System.out.println("I am cooking");
	}
}

//Dog.java
public class Dog extends Animal {
	
	String yell;
	public Dog(String name, String type, int age, String _yell){
		super(name, type, age);    //sets up the Dog.name, Dog.type, and Dog.age
		yell = _yell;
	}
	public void shout() {
		System.out.println("WOOF");
	}
	public void say_name() {
		System.out.println("My name is " + name + " and I love to " + yell);
	}
	public static void main(String[] args) {
		Dog jeff = new Dog("Jeff", "Carnivore", 2, "ARGGGHHHH");
		jeff.shout();
		jeff.say_name();
		jeff.cook();
	}
}  
```  
## C++
### Basic C   
  
Why use C++ :  
- C++ is one of the world's most popular programming languages.
- C++ can be found in today's operating systems, Graphical User Interfaces, and embedded systems.
- C++ is an object-oriented programming language which gives a clear structure to programs and allows code to be reused, lowering development costs.
- C++ is portable and can be used to develop applications that can be adapted to multiple platforms.
- C++ is fun and easy to learn!
- As C++ is close to C# and Java, it makes it easy for programmers to switch to C++ or vice versa  
C++ files are stored using the .cpp end tag. For example myfirstprogrma.cpp.  
Let us look at a simple program and break it down:  
```c++  
#include <iostream>
using namespace std;

int main() {
  cout << "Hello World!";
  return 0;
}

/* This is a multi-
line comment */

//This is a single-line comment
```  
- `#include <iostream>` is a header file library that lets us work with input and output objects such as cout. Header files add functionality to C++ programs.  
- `using namespace std` means that we can use names for objects and variables from the `standard` library.  
- `int main()` is the main function needed to run the program.  
- **EVERY** C++ statment ends with a semicolon **;**  
- Comment can be `//` or `/*   */`  

In C++, there are different **types** of variables including:  
- `int` - stores integers (whole numbers), without decimals, such as 123 or -123
- `double` - stores floating point numbers, with decimals, such as 19.99 or -19.99
- `char` - stores single characters, such as 'a' or 'B'. Char values are surrounded by single quotes
- `string` - stores text, such as "Hello World". String values are surrounded by double quotes
- `bool` - stores values with two states: true or false  
<img width="811" alt="c_types" src="https://user-images.githubusercontent.com/16792195/75122859-dfcaaf80-5656-11ea-996b-0a0ec87d550f.png">

```c++  
int myNum = 5;               // Integer (whole number without decimals)
double myFloatNum = 5.99;    // Floating point number (with decimals)
float myFloatNum = 5.99;     // Floating point number
char myLetter = 'D';         // Character
string myText = "Hello";     // String (text)
bool myBoolean = true;       // Boolean (true or false)
```  
Always declare the variable as **constant** when you have values that are unlikley to change.  
```c++  
const int myNum = 15;  // myNum will always be 15
myNum = 10;  // error: assignment of read-only variable 'myNum'
const int minutesPerHour = 60;
const float PI = 3.14;
```  
**USER INPUT** In order to get user input we need to take advantage of the `cin` function:  
```c++
int x, y;
int sum;
cout << "Type a number: ";
cin >> x;
cout << "Type another number: ";
cin >> y;
sum = x + y;
cout << "Sum is: " << sum;
```  
`cin` considers a space as a terminating character so it can only input and display a single word. In these cases we would need to use the getlin() function to read a line of text:  
```c++  
string fullName;
cout << "Type your full name: ";
getline (cin, fullName);
cout << "Your name is: " << fullName;

// Type your full name: John Doe
// Your name is: John Doe  
```  

**LOGICAL OPERATORS**

<img width="712" alt="andorc" src="https://user-images.githubusercontent.com/16792195/75128987-bec88580-567b-11ea-9463-4fa97918a500.png"><br/>  

**MATH** In order to use certain math functions we need to include a header:  
```c++  
// Include the cmath library
#include <cmath>

cout << sqrt(64);
cout << round(2.6);
cout << log(2);
```  

### Loops and Conditions















