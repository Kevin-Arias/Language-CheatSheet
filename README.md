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
- [Loops and Conditions](#loops-and-conditions) : Learn for and while loops, if/else statements, etc.
- [Methods and Classes](#methods-and-classes) : Learn how to create methods and classes and objects.  

## Data Structures  
- [Arrays](#arrays)  
    - [Python Array Implementations](#python-array-implementations)  
    - [Java Array Implementation](#java-array-implementation)  
    - [C++ Array Implementation](#c-array-implementation)  
- [Linked Lists](#linked-lists)  
    - [Python Linked List Implementation](#python-linked-list-implementation)  
    - [Java Linked List Implementation](#java-linked-list-implementation)  
    - [C++ Linked List Implementation](#c-linked-list-implementation)   
- [Queues](#queues)  
    - [Python Queue Implementation](#python-queue-implementation)  
    - [Java Queue Implementation](#java-queue-implementation)  
    - [C++ Queue Implementation](#c-queue-implementation)   
- [Hash Tables](#hash-tables)  
    - [Python Hash Table Implementation](#python-hash-table-implementation)
    - [Java Hash Table Implementation](#java-hash-table-implementation)  
    - [C++ Hash Table Implementation](#c-hash-table-implementation)  
- [Sets](#sets)  
    - [Python Set Implementation](#python-set-implementation)
    - [Java Set Implementation](#java-set-implementation)  
    - [C++ Set Implementation](#c-set-implementation)  
- [Trees](#trees)  
    - [Python Tree Implementation](#python-tree-implementation)
    - [Java Tree Implementation](#java-tree-implementation)  
    - [C++ Tree Implementation](#c-tree-implementation)  
    
## Algorithms

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
**If/Else/Else If Conditional Statements**  
```c++  
int time = 22;
if (time < 10) {
  cout << "Good morning.";
} else if (time < 20) {
  cout << "Good day.";
} else {
  cout << "Good evening.";
}
// Outputs "Good evening."

//variable = (condition) ? expressionTrue : expressionFalse;
int time = 20;
string result = (time < 18) ? "Good day." : "Good evening.";
cout << result;
```  

** Switch Statements ** : Switch expression is evaluated once, then value is compared with each case. If match then case code is executed.  
```c++  
int day = 4;
switch (day) {
  case 6:
    cout << "Today is Saturday";
    break;
  case 7:
    cout << "Today is Sunday";
    break;
  default:
    cout << "Looking forward to the Weekend";
}
// Outputs "Looking forward to the Weekend"
```  
**While Loop**
```c++ 
int i = 0;
while (i < 5) {
  cout << i << "\n";
  i++;
}
```  
**For Loop**  
```c++  
for (int i = 0; i < 5; i++) {
  cout << i << "\n";
}
```  
**REFERENCES AND POINTERS**  
A reference variable is a "reference" to an existing variable, and is created with the `&` operator. It can also be used to get the memory address of a variable:  
```c++
string food = "Pizza";
string &meal = food;

cout << food << "\n";  // Outputs Pizza
cout << meal << "\n";  // Outputs Pizza
cout << &food; // Outputs 0x6dfed4

```  
A pointer is a variable that stores the memory address as its value.  
```c++  
string food = "Pizza";  // A food variable of type string
string* ptr = &food;    // A pointer variable, with the name ptr, that stores the address of food

// Output the value of food (Pizza)
cout << food << "\n";

// Output the memory address of food (0x6dfed4)
cout << &food << "\n";

// Output the memory address of food with the pointer (0x6dfed4)
cout << ptr << "\n";  

// Dereference: Output the value of food with the pointer (Pizza)
cout << *ptr << "\n";

// Change the value of the pointer
*ptr = "Hamburger";

// Output the new value of the pointer (Hamburger)
cout << *ptr << "\n";

// Output the new value of the food variable (Hamburger)
cout << food << "\n";

//There are various ways to declare a pointer variable:
string* mystring; // Preferred
string *mystring;
string * mystring;
```  
### Methods and Classes  
In C++, functions are evaluated from top to bottom so need to make sure that the sequence of functions are correct.  
```c++  
int myFunction(int x, int y) {
  return x + y;
}

int main() {
  cout << myFunction(5, 3);
  return 0;
}

// Outputs 8 (5 + 3)  
```  
You can also pass by reference so that the inputs can be altered:  
```c++  
void swapNums(int &x, int &y) {
  int z = x;
  x = y;
  y = z;
}

int main() {
  int firstNum = 10;
  int secondNum = 20;

  cout << "Before swap: " << "\n";
  cout << firstNum << secondNum << "\n";

  // Call the function, which will change the values of firstNum and secondNum
  swapNums(firstNum, secondNum);

  cout << "After swap: " << "\n";
  cout << firstNum << secondNum << "\n";

  return 0;
}  
```  
**Classes and OOP**  
```c++  
class Car {        // The class
  public:          // Access specifier
    string brand;  // Attribute
    string model;  // Attribute
    int year;      // Attribute
    Car(string x, string y, int z) { // Constructor with parameters
      brand = x;
      model = y;
      year = z;
    }
    void myMethod() {  // Method/function defined inside the class
      cout << "Hello World!";
    }
};

int main() {
  // Create Car objects and call the constructor with different values
  Car carObj1("BMW", "X5", 1999);
  Car carObj2("Ford", "Mustang", 1969);

  // Print values
  cout << carObj1.brand << " " << carObj1.model << " " << carObj1.year << "\n";
  cout << carObj2.brand << " " << carObj2.model << " " << carObj2.year << "\n";
  return 0;
}  
```  
Public and private access specifiers allow you to access and not access certain attributes. By **default** if otherwise not specified, all members of a class are private.  

```c++  
class MyClass {
  public:    // Public access specifier
    int x;   // Public attribute
  private:   // Private access specifier
    int y;   // Private attribute
};

int main() {
  MyClass myObj;
  myObj.x = 25;  // Allowed (public)
  myObj.y = 50;  // Not allowed (private)
  return 0;
}
```  
Just like every other one of these languages, we can perform inheritance:  
```c++  
// Base class (parent)
class MyClass {
  public:
    void myFunction() {
      cout << "Some content in parent class." ;
    }
};

// Derived class (child)
class MyChild: public MyClass {
};

// Derived class (grandchild)
class MyGrandChild: public MyChild {
};

int main() {
  MyGrandChild myObj;
  myObj.myFunction();
  return 0;
}  
```  

## DATA STRUCTURES  
### Arrays  
**Definition**  
- Stores data elements based on sequential, mostcommonly 0 based, index.
- Based on tuples 
- One of the most commonly used data structures  

**What You Need to Know**  

- Optimal for indexing
- Bad for searching, inserting, and deleting (except if it at end)
- If dynamic, good for appending at end
- Linear arrays, or one dimensional arrays, are the most basic.
    - Are static in size, meaning that they are declared with a fixed size.
- Dynamic arrays are like one dimensional arrays, but have reserved space for additional elements.
    - If a dynamic array is full, it copies its contents to a larger array.
- Multi dimensional arrays nested arrays that allow for multiple dimensions such as an array of arrays providing a 2 dimensional spacial representation via x, y coordinates.  

Action | Static Array | Dynamic Array
--- | --- | ---
Access | O(1) | O(1)
Search | O(n) | O(n)
Insertion | N/A | O(n)
Appending | N/A | O(1)
Deletion | N/A | O(n)  

### Python Array Implementations  
In Python, I lists and arrays are pretty similar in functionality. Lists can hold different types whereas arrays can hold only one type, so I would say to just use lists instead. Lists can also mutate all values at once such as multiplication.
**Implementation**  
```python  
l = [1,2,3,"Test", True, 'b', 10.25]  

# Multi-Dimensional Lists
l = [[1,2],[True, 'b'], [3,4]]
```  
**Methods**  

Operation | Example 
--- | --- 
Index | l[i] 
Store | l[i] = 0
Length | len(l)
Append | l.append(5) 
Pop | l.pop() or l.pop(i)  
Slice | l[a:b] 
Delete | del l[i]
Remove | l.remove(item)
Reverse | l.reverse()
Sort | l.sort()
Multiply | k * l  

### Java Array Implementation

In java, there are Arrays and ArrayLists. Arrays are static whereas as ArrayLists are dynamic and allow for resizing. Most of the time I would prefer to use ArrayLists if there is no definite amount of elements we need to use.  

**Implementation**  
```java  
int[] arr = new int[10] 
int[][] arr = new int[10][20]

ArrayList<Integer> arrL = new ArrayList<Integer>();
```  

**Methods**  

Array:  

Operation | Example 
--- | --- 
Index | l[i] 
Store | l[i] = 0
Length | l.length
Sort | Arrays.sort(l)
Find Index of Element | Arrays.binarySeach(l,element)
Copy | Arrays.copyOf(l, l.length)
Equal | Arrays.equals(l1, l2)  

ArrayList:  

Operation | Example | Runtime
--- | --- | ---
Add | l.add(element) or l.add(i, element) | O(1) if adding to end
Clear | l.clear() | 
Contains | l.contains(element) | O(n)
For Each | l.forEach((n)->System.out.println(n)) | O(n)
Get | l.get(i) | O(1)
Index Of | l.indexOf(element) | 
Empty | l.isEmpty() | 
Remove | l.remove(i) or l.remove(element) | O(n)
Replace | l.set(i, element) | 
Size | l.size() | 
Sort | Collections.sort(l) |     


### C Array Implementation  

In C++, arrays do exist but I think people tend to use vectors more since they are more dynamic and allow for easy appending and removing of elements.  

**Implementation**  
```c++  
vector<int> g1;
for (int i = 1; i <= 5; i++) 
	g1.push_back(i);
	
vector<int> v(n, element)  //Make vector with n elements that are the same  
```  

**Methods**  

Operation | Definition | Runtime
--- | --- | ---
v[i] |         Return (or set) the I'th element.        |                O(1)
v.at(i) |      Return (or set) the I'th element, with bounds checking. | O(1)
v.size() |     Return current number of elements.                      | O(1)
v.empty() |    Return true if vector is empty.                         | O(1)
v.begin()  |   Return random access iterator to start.                 | O(1)
v.end() |      Return random access iterator to end.                   | O(1)
v.front() |    Return the first element.                               | O(1)
v.back()  |    Return the last element.                                | O(1)
v.capacity() | Return maximum number of elements.                      | O(1)
v.push_back(value) |        Add value to end.                                             |   O(1) (amortized)
v.insert(iterator, value) | Insert value at the position indexed by iterator.              |  O(n)
v.pop_back()    |           Remove value from end.                                          | O(1)
v.assign(begin, end) |      Clear the container and copy in the elements from begin to end. | O(n)
v.erase(iterator)   |       Erase value indexed by iterator.                                | O(n)
v.erase(begin, end)  |      Erase the elements from begin to end.                           | O(n)   


### Linked Lists  

**Definition**  
- Stores data with nodes that point to other nodes.  
    - Nodes, at its most basic holds one data element and one reference to another node.
    - A linked list chains nodes together by pointing one node's reference towards another node.  

**What You Need to Know**  
- Designed to optimize insertion and deletion.
- Slow at indexing and searching
- Doubly Linked List has nodes that also reference the previous node.
- Circularly Linked List is linked list whose tail, references to the head.  

Action | Singly Linked | Doubly Linked
--- | --- | ---
Search | O(n) | O(n)
Insert at Head | O(1) | O(1)
Insert at Tail | O(1) | O(1)
Remove at Head | O(1) | O(1)
Remove at Tail | O(n) | O(1)
Remove in Middle | O(n) | O(n)  

### Python Linked List Implementation  
We will be covering how to implement both singly and doubly linked lists and how to implement adding and removing elements since they are the most used methods for Linked Lists.  

```python  
# Singly Linked List  
class Node(object):
	"""docstring for Node"""
	def __init__(self, data = None):
		self.data = data
		self.next_node = None


class LinkedList(object):
	"""docstring for LinkedList"""
	def __init__(self, head = None, tail = None):
		self.head = head
		self.tail = tail

	def add(self, data):
		temp = Node(data)
		if (self.head == None):
			self.head = temp
			self.tail = temp
		else:
			self.tail.next_node = temp
			self.tail = self.tail.next_node

	def pop(self):
		if (self.head == None):
			return
		elif self.head.next_node == None:
			self.head = None;
		else:
			prev = self.head
			current = prev.next_node
			while current.next_node != None:
				prev = current
				current = current.next_node
			self.tail = prev
			self.tail.next_node = None
			


	def print_vals(self):
		current = self.head
		if current == None:
			print("No Values in Linkede List yet")
			return
		while current.next_node != None:
			print(current.data)
			current = current.next_node

		print(current.data)  
		
```  

### Java Linked List Implementation  
```java
// Singly Linked List 

public class LinkedList {
	Node head;
	Node tail;
	public LinkedList() {
		head = null;
		tail = null;
	}
	public void add(int value) {
		Node temp = new Node(value);
		if (head == null) {
			head = temp;
			tail = temp;
		} else {
			tail.next = temp;
			tail = tail.next;
		}
	}
	public void pop() {
		if (head == null) {
			return;
		}
		else if (head.next == null){
			head = null;
			return;
		} else {
			Node prev = head;
			Node current = prev.next;
			while (current.next != null) {
				prev = current;
				current = current.next;
			}
			tail = prev;
			tail.next = null;
		}
	}
	public void print_vals() {
		if (head == null) {
			return;
		}
		Node current = head;
		while (current.next != null) {
			System.out.println(current.data);
			current = current.next;
		}
		System.out.println(current.data);
	}
	public static void main(String[] args) {
		
	}
}

class Node {
	int data;
	Node next;
	public Node(int value) {
		data = value;
		next = null;
	}
}
```  

### C Linked List Implementation  
```c++  
#include <iostream>
using namespace std;

struct node
{
	int data;
	struct node* next;

};

class linked_list { 
public:
	node* head, *tail;
	linked_list() {
		head = NULL;
		tail = NULL;
	}
	void add(int n) {
		node* temp = new node;
		temp->data = n;
		temp->next = NULL;
		if (head == NULL) {
			head = temp;
			tail = temp;
		} else {
			tail->next = temp;
			tail = tail->next;
		}
	}
	void pop() {
		if (head == NULL) {
			return;
		}
		else if (head->next == NULL) {
			head = NULL;
			return;
		} else {
			node* prev = head;
			node* current = prev->next;
			while (current->next != NULL) {
				prev = current;
				current = current->next;
			}
			tail = prev;
			tail->next = NULL;
		}
	}
	void printall() {
		node* temp = head;
		if (head == NULL) {
			return;
		} else {
			while (temp->next != NULL) {
				cout << temp->data << "\n";
				temp = temp->next;
			}
			cout << temp->data << "\n";
		}
	}
};
```  

### Stacks  

**Definition**  
- Linear data structure that stores items in a Last-In First-Out.  
- A new element is added at one end and an element is removed from that end only.
    

**What You Need to Know**  
- Designed to optimize insertion and deletion.
- Slow at indexing and searching
- Does not offer constant time access to ith element.
- Does allow constant time adds and removes because it doesn't require shifting elements around.

Action | Stack Runtime
--- | --- 
Pushing | O(1) 
Popping | O(1)
Peeking | O(1) 
Searching | O(n)
Size | O(1) 
Empty | O(1)  

**Python Stack Implementation**  
There are a couple of ways to implement a stack in python but the best way is probably the simplest way by using something we are already familiar with: lists. 

```python  
stack = [] 
  
# append() function to push 
# element in the stack 
stack.append('a') 
stack.append('b') 
stack.append('c') 

  
print('Initial stack') 
print(stack) 
  
# pop() fucntion to pop 
# element from stack in  
# LIFO order 
print('\nElements poped from stack:') 
print(stack.pop()) 
print(stack.pop()) 
print(stack.pop()) 
  
print('\nStack after elements are popped:') 
if not stack:
	print("EMPTY")
print(len(stack)) 
```  

### Java Stack Implementation
  
For Java, there is already a stack implementation so we just use that. Have to make sure to import java.util.*  

```java  
import java.util.*;

Stack<Integer> stack = new Stack<Integer>();

// Push Element onto stack  
stack.push(1);

// Pop element from stack
int top = stack.pop();

// Peek at top element
stack.peek();

// Search the stack
int index = stack.search(1);

// Returns true if empty
stack.empty();

// Returns size of stack
stack.size();
```  

### C Stack Implementation  

For C++ there is already a stack implementation built in but you have to make sure to `#include <stack>`.  

```c++  
#include <iostream>
#include <stack> 
using namespace std;

int main(int argc, char const *argv[])
{
	stack<int> s;
	s.push(10);    // Push to stack O(1)
	s.push(11);
	s.push(12);
	s.pop();       // Pop from stack O(1)
	cout << s.size() << "\n";     // Find SIZE of stack O(1)
	cout << s.empty() << "\n";    // Determine whether stack is empty O(1)
	cout << s.top() << "\n";      // C++ version of peek()  O(1)
	return 0;
}  
```  


### Queues  

**Definition**  
- Linear data structure that stores items in a First-In First-Out.  
- With a queue the least recently added item is removed first.
    

**What You Need to Know**  
- Designed to optimize insertion and deletion.
- Slow at indexing and searching
- Does not offer constant time access to ith element.
- Does allow constant time adds and removes because it doesn't require shifting elements around.

Action | Queue Runtime
--- | --- 
Enqueue | O(1) 
Dequeue | O(1)
Peeking | O(1) 
Contains | O(n)
Removal | O(n) 
Is Empty | O(1)  

### Python Queue Implementation  
For Python, we can do something similar to that of the stack. We can use Python's built in `list` in order to implement the queue:  

```python  
queue = [] 
  
# Adding elements to the queue 
queue.append('a') 
queue.append('b') 
queue.append('c') 
  
print("Initial queue") 
print(queue) 
  
# Removing elements from the queue 
print("\nElements dequeued from queue") 
print(queue.pop(0)) 
print(queue.pop(0)) 
print(queue.pop(0)) 
  
print("\nQueue after removing elements") 
print(queue) 
```  


### Java Queue Implementation  
```java  
import java.util.LinkedList; 
import java.util.Queue; 
public class QueueExample 
{ 
  public static void main(String[] args) 
  { 
    Queue<Integer> q = new LinkedList<Integer>(); 
  
    // Adds elements {0, 1, 2, 3, 4} to queue 
    for (int i=0; i<5; i++) 
     q.add(i); 
  
    // Display contents of the queue. 
    System.out.println("Elements of queue-"+q); 
  
    // To remove the head of queue. 
    int removedele = q.remove(); 
    System.out.println("removed element-" + removedele); 
  
    System.out.println(q); 
  
    // To view the head of queue 
    int head = q.peek(); 
    System.out.println("head of queue-" + head); 
  
    // Rest all methods of collection interface, 
    // Like size and contains can be used with this 
    // implementation. 
    int size = q.size(); 
    System.out.println("Size of queue-" + size); 
    q.remove();
    q.remove();
    q.remove();
    q.remove();
    if (q.isEmpty()) {
    	System.out.println("SUCCESS");
    }
  } 
} 
```  

### C Queue Implementation  

There is a built in queue implementation in C++ so we can use that for execution:  

```c++  
#include <iostream> 
#include <queue> 
  
using namespace std; 
  
void showq(queue <int> gq) 
{ 
    queue <int> g = gq; 
    while (!g.empty()) 
    { 
        cout << '\t' << g.front(); 
        g.pop(); 
    } 
    cout << '\n'; 
} 
  
int main() 
{ 
    queue <int> gquiz; 
    gquiz.push(10); 
    gquiz.push(20); 
    gquiz.push(30); 
  
    cout << "The queue gquiz is : "; 
    showq(gquiz); 
  
    cout << "\ngquiz.size() : " << gquiz.size(); 
    cout << "\ngquiz.front() : " << gquiz.front(); 
    cout << "\ngquiz.back() : " << gquiz.back(); 
  
    cout << "\ngquiz.pop() : "; 
    gquiz.pop(); 
    showq(gquiz); 
  
    return 0; 
} 
```   

### Hash Tables  

**Definition**  
- Stores data with key value pairs.
- Hash functions accept a key and return an output unique only to that specific key.
    - This is known as hashing, which is the concept that an input and an output have a one-to-one correspondence to map information.
    - Hash functions return a unique address in memory for that data.

**What You Need to Know**  
- Designed to optimize searching, insertion, and deletion.
- Hash collisions are when a hash function returns the same output for two distinct inputs.
    - All hash functions have this problem.
    - This is often accommodated for by having the hash tables use linked list look up 
- Hashes are important for associative arrays and database indexing.

Action | Average Runtime | Worst Runtime
--- | --- | ---
Insertion | O(1) | O(n)
Deletion | O(1) | O(n)
Search | O(1) | O(n)  

### Python Hash Table Implementation    
For python, the best way to keep a key-value type data structure and keep a good runtime is by using the built-in dictionary:  
```python  
d = dict()
d['k'] = 'v'
d['key'] = 'value'
d[4] = 2  
```  
<img width="644" alt="dict" src="https://user-images.githubusercontent.com/16792195/75100465-8db85a00-5582-11ea-99fc-7e930c5bd1bd.png"><br/>  

### Java Hash Table Implementation  
For java, we use the built-in Hashtable from java.util :  
```java  
import java.util.*;

public class hashtable {

	public static void main(String[] args) {
		Hashtable<Integer, String> h = new Hashtable<Integer, String>();
		
		String s1 = "pollinating sandboxes";
		String s2 = "amusement & hemophilias";
		h.put(s1.hashCode(), s1);
		h.put(s2.hashCode(), s2);
		System.out.println(h);
	}
}

```  

![java_hashtable](https://user-images.githubusercontent.com/16792195/75707477-cab3d900-5c73-11ea-8805-78e16e702910.png)</br>  

### C Hash Table Implementation  

In C++, we can use an unordered_map because it is implemented using Hash Table. The average cost of search, insert, and delete from hash table are O(1).  

```c++
#include <iostream>
#include <unordered_map>
using namespace std;

int main() {
	unordered_map<string, double> umap;

	umap["pi"] = 3.14;
	umap["root4"] = 2.0;

	umap.insert(make_pair("e", 2.718));

	unordered_map<string, double>:: iterator itr; 

	for (itr = umap.begin(); itr != umap.end(); itr++) 
    { 
        // itr works as a pointer to pair<string, double> 
        // type itr->first stores the key part  and 
        // itr->second stroes the value part 
        cout << itr->first << "  " << itr->second << endl; 
     } 
     cout << umap.size() << "\n";

     if (!umap.empty()) {
     	cout << "SUCCESS!\n";
     }
     return 0;
}
```  


<img width="404" alt="unordered_map" src="https://user-images.githubusercontent.com/16792195/75712220-75c89080-5c7c-11ea-8204-3d6128fb7066.png"> </br>   

### Sets  

**Definition**  
- Stores data like lists/arrays
- Set guarantees that there is no duplicate object in it.

**What You Need to Know**  
- Designed to optimize insertion, deletion, checking size, and checking for containment
- Since no duplicates allowed, great for unioning and only having unique values
- Values are not ordered so not good for indexing or popping

Action | Average Runtime 
--- | --- 
Insertion | O(1) 
Deletion | O(1)
Containment | O(1) 
Length | O(1)  
Union | O(1)  

### Python Set Implementation  

For python, adding a set is almost no different than creating a list:  

```python  
thisset = {"apple", "banana", "cherry"}

for x in thisset:
  print(x)
  
print("banana" in thisset)

thisset.add("orange")

thisset.update(["orange", "mango", "grapes"])

thisset.remove("banana")

print(len(thisset))
```


<img width="667" alt="set_python" src="https://user-images.githubusercontent.com/16792195/75718614-1cfef500-5c88-11ea-888b-0c276fc9b99e.png"> </br>  

### Java Set Implementation  

In java, we use the HashSet in order to satisfy all of our set needs and operations:  

```java
import java.util.*;

public class set {
	public static void main(String[] args) {
		Set<Integer> s = new HashSet<Integer>();
		s.add(1);
		s.add(2);
		if (s.contains(1)) {
			System.out.println("Success");
		}
		for (int i : s) {
			System.out.println(i);
		}
	}
}
```  

<img width="955" alt="set_java" src="https://user-images.githubusercontent.com/16792195/75719611-e629de80-5c89-11ea-85bd-f1f5abe44321.png"> </br>  

### C Set Implementation  

In C++ we use an already built-in version of the set and use it as follows:  

```c++  
#include <iostream> 
#include <set> 
#include <iterator> 
  
using namespace std; 
  
int main() 
{ 
    // empty set container 
    set <int, greater <int> > gquiz1;         
  
    // insert elements in random order 
    gquiz1.insert(40); 
    gquiz1.insert(30); 
    gquiz1.insert(60); 
    gquiz1.insert(20); 
    gquiz1.insert(50); 
    gquiz1.insert(50); // only one 50 will be added to the set 
    gquiz1.insert(10); 
  
    // printing set gquiz1 
    set <int, greater <int> > :: iterator itr; 
    cout << "\nThe set gquiz1 is : "; 
    for (itr = gquiz1.begin(); itr != gquiz1.end(); ++itr) 
    { 
        cout << '\t' << *itr; 
    } 
    cout << endl; 
  
    // assigning the elements from gquiz1 to gquiz2 
    set <int> gquiz2(gquiz1.begin(), gquiz1.end()); 
  
    // print all elements of the set gquiz2 
    cout << "\nThe set gquiz2 after assign from gquiz1 is : "; 
    for (itr = gquiz2.begin(); itr != gquiz2.end(); ++itr) 
    { 
        cout << '\t' << *itr; 
    } 
    cout << endl; 
  
    // remove all elements up to 30 in gquiz2 
    cout << "\ngquiz2 after removal of elements less than 30 : "; 
    gquiz2.erase(gquiz2.begin(), gquiz2.find(30)); 
    for (itr = gquiz2.begin(); itr != gquiz2.end(); ++itr) 
    { 
        cout << '\t' << *itr; 
    } 
  
    // remove element with value 50 in gquiz2 
    int num; 
    num = gquiz2.erase (50); 
    cout << "\ngquiz2.erase(50) : "; 
    cout << num << " removed \t" ; 
    for (itr = gquiz2.begin(); itr != gquiz2.end(); ++itr) 
    { 
        cout << '\t' << *itr; 
    } 
  
    cout << endl; 
  
    //lower bound and upper bound for set gquiz1 
    cout << "gquiz1.lower_bound(40) : "
         << *gquiz1.lower_bound(40) << endl; 
    cout << "gquiz1.upper_bound(40) : "
         << *gquiz1.upper_bound(40) << endl; 
  
    //lower bound and upper bound for set gquiz2 
    cout << "gquiz2.lower_bound(40) : "
         << *gquiz2.lower_bound(40) << endl; 
    cout << "gquiz2.upper_bound(40) : "
         << *gquiz2.upper_bound(40) << endl; 
  
    return 0; 
  
} 
```  
<img width="618" alt="set_c" src="https://user-images.githubusercontent.com/16792195/75720877-1ffbe480-5c8c-11ea-8965-9fd170b716a7.png"></br>  

### Trees  

**Definition**  
- Undirected graph which satisfies the following definitions:
    - An acyclic connected graph
    - A connected graph with N nodes and N-1 edges
    - A graph in which any two vertices are connected by exactly **one** path

**What You Need to Know**  
- **Binary Tree** is a tree with no more than two children per node
- **Binary Search Tree** is a binary tree that has all left subtrees hold smaller values than root node and all right subtrees hold 


Action | Average Runtime | Worst Runtime
--- | --- | ---
Insertion | O(log(n)) | O(n)
Delete | O(log(n)) | O(n)
Remove | O(log(n)) | O(n)
Search | O(log(n)) | O(n)

### Python Tree Implementation  
```python
class Node:

	def __init__(self, data):
		self.left = None
		self.right = None
		self.data = data

	def insert(self, data):
		if self.data:
			if data < self.data:
				if self.left is None:
					self.left = Node(data)
				else:
					self.left.insert(data)
			elif data > self.data:
				if self.right is None:
					self.right = Node(data) 
				else:
					self.right.insert(data)
		else:
			self.data = data
	
	def PrintTree(self):
		if self.left:
			self.left.PrintTree()
		print(self.data)
		if self.right:
			self.right.PrintTree()



root = Node(12)
root.insert(6)
root.insert(14)
root.insert(3)
root.PrintTree()
```  

### Java Tree Implementation  
```java
class BinarySearchTree {

	class Node {
		int data;
		Node left, right;

		public Node(int item) {
			data = item;
			left = right = null;
		}
	}

	Node root;

	BinarySearchTree() {
		root = null;
	}

	void insert(int data) {
		root = insertRec(root, data);
	}
	
	Node insertRec(Node root, int data) {
		/* If the tree is empty, return a new node */
        if (root == null) { 
            root = new Node(data); 
            return root; 
        } 
  
        /* Otherwise, recur down the tree */
        if (data < root.data) 
            root.left = insertRec(root.left, data); 
        else if (data > root.data) 
            root.right = insertRec(root.right, data); 
  
        /* return the (unchanged) node pointer */
        return root; 
	}

	// A utility function to do inorder traversal of BST 
    void inorderRec(Node root) { 
        if (root != null) { 
            inorderRec(root.left); 
            System.out.println(root.data); 
            inorderRec(root.right); 
        } 
    } 

    public static void main(String[] args) {
    	BinarySearchTree tree = new BinarySearchTree(); 
  
        /* Let us create following BST 
              50 
           /     \ 
          30      70 
         /  \    /  \ 
       20   40  60   80 */
        tree.insert(50); 
        tree.insert(30); 
        tree.insert(20); 
        tree.insert(40); 
        tree.insert(70); 
        tree.insert(60); 
        tree.insert(80); 
  
        // print inorder traversal of the BST 
        tree.inorderRec(tree.root); 
    }
}
```  

### C Tree Implementation
```c++
#include <iostream>
using namespace std;

class BST {
	class Node
	{
	public:
		int data;
		Node* left;
		Node* right;
		Node(int value) {
			data = value;
			left = right = NULL;
		}
		
	};
	public:
		Node* root;
		BST() {
			root = NULL;
		}
		void insert(int data) {
			root = insertRec(root, data);
		}
		Node* insertRec(Node* root, int data) {
			if (root == NULL) {
				root = new Node(data);
			}

			if (data < root->data) {
				root->left = insertRec(root->left, data);
			}
			else if (data > root->data) {
				root->right = insertRec(root->right, data);
			}
			return root;
		}
		void inorderRec(Node* root) {
			if (root != NULL) {
				inorderRec(root->left);
				cout << root->data << "\n";
				inorderRec(root->right);
			}
		}

};
int main(int argc, char const *argv[])
{
	BST tree;

	/* Let us create following BST 
          50 
       /     \ 
      30      70 
     /  \    /  \ 
   20   40  60   80 */
    tree.insert(50); 
    tree.insert(30); 
    tree.insert(20); 
    tree.insert(40); 
    tree.insert(70); 
    tree.insert(60); 
    tree.insert(80); 

    // print inorder traversal of the BST 
    tree.inorderRec(tree.root);
	return 0;
}
```  

## Algorithms  

## Divide and Conquer Algorithms  

### <a id="selection-sort"></a>Selection Sort
#### Definition
- A comparison based sorting algorithm.
  - Starts with the cursor on the left, iterating left to right
  - Compares the left side to the right, looking for the smallest known item
    - If the left is smaller than the item to the right it continues iterating
    - If the left is bigger than the item to the right, the item on the right becomes the known smallest number
    - Once it has checked all items, it moves the known smallest to the cursor and advances the cursor to the right and starts over
  - As the algorithm processes the data set, it builds a fully sorted left side of the data until the entire data set is sorted
- Changes the array in place.

#### What you need to know
- Inefficient for large data sets.
- Very simple to implement.

#### Time Complexity
- Best Case Sort: Merge Sort: `O(n^2)`
- Average Case Sort: Merge Sort: `O(n^2)`
- Worst Case Sort: Merge Sort: `O(n^2)`

#### Space Complexity
- Worst Case: `O(1)`

#### Visualization
![#](https://upload.wikimedia.org/wikipedia/commons/9/94/Selection-Sort-Animation.gif)

[(source: Wikipedia, _Insertion Sort_)](https://en.wikipedia.org/wiki/Selection_sort)

### <a id="insertion-sort"></a>Insertion Sort
#### Definition
- A comparison based sorting algorithm.
  - Iterates left to right comparing the current cursor to the previous item.
  - If the cursor is smaller than the item on the left it swaps positions and the cursor compares itself again to the left hand side until it is put in its sorted position.
  - As the algorithm processes the data set, the left side becomes increasingly sorted until it is fully sorted.
- Changes the array in place.

#### What you need to know
- Inefficient for large data sets, but can be faster for than other algorithms for small ones.
- Although it has an `O(n^2)`, in practice it slightly less since its comparison scheme only requires checking place if its smaller than its neighbor.

#### Time Complexity
- Best Case Sort: Merge Sort: `O(n)`
- Average Case Sort: Merge Sort: `O(n^2)`
- Worst Case Sort: Merge Sort: `O(n^2)`

#### Space Complexity
- Worst Case: `O(n)`

#### Visualization
![#](https://upload.wikimedia.org/wikipedia/commons/0/0f/Insertion-sort-example-300px.gif)

[(source: Wikipedia, _Insertion Sort_)](https://en.wikipedia.org/wiki/Insertion_sort)

### <a id="merge-sort"></a>Merge Sort
#### Definition
- A divide and conquer algorithm.
  - Recursively divides entire array by half into subsets until the subset is one, the base case.
  - Once the base case is reached results are returned and sorted ascending left to right.
  - Recursive calls are returned and the sorts double in size until the entire array is sorted.

#### What you need to know
- This is one of the fundamental sorting algorithms.
- Know that it divides all the data into as small possible sets then compares them.

#### Time Complexity
- Worst Case: `O(n log n)`
- Average Case: `O(n log n)`
- Best Case: `O(n)`

#### Space Complexity
- Worst Case: `O(1)`

#### Visualization
![#](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e6/Merge_sort_algorithm_diagram.svg/400px-Merge_sort_algorithm_diagram.svg.png)

[(source: Wikipedia, _Merge Sort_)](https://en.wikipedia.org/wiki/Merge_sort)

### <a id="quick-sort"></a>Quicksort
#### Definition
- A divide and conquer algorithm
  - Partitions entire data set in half by selecting a random pivot element and putting all smaller elements to the left of the element and larger ones to the right.
  - It repeats this process on the left side until it is comparing only two elements at which point the left side is sorted.
  - When the left side is finished sorting it performs the same operation on the right side.
- Computer architecture favors the quicksort process.
- Changes the array in place.

#### What you need to know
- While it has the same Big O as (or worse in some cases) many other sorting algorithms it is often faster in practice than many other sorting algorithms, such as merge sort.

#### Time Complexity
- Worst Case: `O(n^2)`
- Average Case: `O(n log n)`
- Best Case: `O(n log n)`

#### Space Complexity
- Worst Case: `O(log n)`

#### Visualization
![#](https://upload.wikimedia.org/wikipedia/commons/6/6a/Sorting_quicksort_anim.gif)

[(source: Wikipedia, _Quicksort_)](https://en.wikipedia.org/wiki/Quicksort)

#### Merge Sort Vs. Quicksort
- Quicksort is likely faster in practice, but merge sort is faster on paper.
- Merge Sort divides the set into the smallest possible groups immediately then reconstructs the incrementally as it sorts the groupings.
- Quicksort continually partitions the data set by a pivot, until the set is recursively sorted.  

#### Binary Search  
- Binary Search allows us to find a key *k* in a large file containing keys *z*[0,1,...,n-1] in sorted order, we first compare k with *z*[n/2], and depending on the result we recurse either on the first half of the file *z*[0,..., n/2-1], or on the second half *z*[n/2,...,n-1]
- The runtime of this algorithm is O(log n)  

#### Medians  
- The median of a list of numbers is its 50th percentile.
- Sorting values and then finding the median takes O(n log n) time and that is just too slow.
- We can use the Selection algorithm to find the k largest item where k is size/2

<img width="804" alt="median" src="https://user-images.githubusercontent.com/16792195/76030757-2dfb7080-5eeb-11ea-8401-e62251b5366b.png"> </br>  

## Graphs  
- Graph is a data structure that consists of the following:  
    - A finite set of vertices
    - A finite set of ordered pairs of the form (u,v) called an edge.
- Graphs are used to represent many real-life apllications such as networks
- There are a few ways of representing graphs but the two most commonly used are adjacency lists and adjacency matrix:
    - Adjacency Matrix Pros and Cons:
    - Representation is easier to implement and follow, removing an edge takes constant time, and determining whether two vertices are connected or not takes constant time. But it consumes more space.
    - Adjacency List Pros and Cons:
    - It saves space but determing whether two vertices are connected or not can take longer in comparison.  

### Python Graph Implementation  

```python  
def add_vertex(v):
	global graph
	global size
	if v in graph:
		print(v + " already exists")
	else:
		size += 1
		graph[v] = []

def add_edge(v1, v2, e):
	global graph

	if v1 not in graph:
		print(v1 + " not in graph")
	elif v2 not in graph:
		print(v2 + " not in graph")
	else:
		temp = [v2, e]
		graph[v1].append(temp)

def print_graph():
	global graph
	for vertex in graph:
		for edges in graph[vertex]:
			print(vertex,"->", edges[0], "edge weight: ", edges[1])

graph = dict()
size = 0
add_vertex(1)
add_vertex(2)
add_vertex(3)
add_vertex(4)

add_edge(1, 2, 1)
add_edge(1, 3, 1)
add_edge(2, 3, 3)
add_edge(3, 4, 4)
add_edge(4, 1, 5)
print_graph()

print("Internal representation: ", graph)
```  

### Java Graph Implementation  
```java  
import java.util.LinkedList;
import java.util.*;

public class graph {
	class Node {
		int next;
		int weight;
		public Node(int connected, int edge_weight) {
			next = connected;
			weight = edge_weight;
		}
	}

	int size;
	Hashtable<Integer, LinkedList<Node>> gr;

	public graph() {
		size = 0;
		gr = new Hashtable<Integer, LinkedList<Node>>();
	}

	void add_vertex(int v) {
		size += 1;
		LinkedList<Node> temp = new LinkedList<Node>();
		gr.put(v, temp);
	}

	void add_edge(int v1, int v2, int e) {
		Node n = new Node(v2, e);
		LinkedList<Node> temp = gr.get(v1);
		temp.add(n);
	}

	void print_graph() {
		Set<Integer> keys = gr.keySet();
		for (int vertex : keys) {
			for (Node n : gr.get(vertex)) {
				
				System.out.println(String.valueOf(vertex) + " -> " + 
					String.valueOf(n.next) + " edge weight: " + String.valueOf(n.weight));
			}
		}
	}
	public static void main(String[] args) {
		graph g = new graph();
		g.add_vertex(1);
		g.add_vertex(2);
		g.add_vertex(3);
		g.add_vertex(4);

		g.add_edge(1, 2, 1);
		g.add_edge(1, 3, 1);
		g.add_edge(2, 3, 3);
		g.add_edge(3, 4, 4);
		g.add_edge(4, 1, 5);
		g.print_graph();
		
	}

}
```







 






	

