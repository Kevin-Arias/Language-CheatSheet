# CS Programming Language Cheat Sheet
When learning CS, it is always good practice to refresh yourself on some previously learned concepts.

These are some basic tips and concepts to refresh your memory on some of software engineering's biggest programming languages made simple. Many concepts such as proper syntax, data structures, and algorithms for each language will be covered. Good luck and happy learning!

## PYTHON
- [Basic Python](#basic-python) : Learn basic Python concepts and syntax
- [Python Data Structures](#python-data-structures) : Different kinds of data structures that can be used in Python

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
| Operation       | Big O Efficiency         
| --------------- |:-------------:|
| index(item)     | O(1)          |
| store l[i]      | O(1)          |
| len(l)          | O(1)          |
| append(item)    | O(1)          |
| pop()           | O(1)          |
| pop(i)          | O(n)          |
| insert(i, item) | O(n)          |
| remove(x)       | O(n)          |
| contains        | O(n)          |
| reverse()       | O(n)          |
| sort()          | O(nlogn)      |

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

**Tuples**: 
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
```python
months = {
  "Jan":"January,
  "Feb":"February,
  "March":"March",
 }
 
 months["Jan"]    # Returns "January"
 months.get("Jan")    # Returns "January"
 months.get("Dec")    # Returns None
 months.get("Dec", "Not valid")    # Returns default value "Not Valid
 ```  
 
 **Sets**
 - Store non-duplicate items
 - Very fast access vs Lists
 - Math Set ops (union, intersect)
 - Unordered




