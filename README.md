# CS Programming Language Cheat Sheet
When learning CS, it is always good practice to refresh yourself on some previously learned concepts.

These are some basic tips and concepts to refresh your memory on some of software engineering's biggest programming languages made simple. Many concepts such as proper syntax, data structures, and algorithms for each language will be covered. Good luck and happy learning!

## PYTHON
- [Basic Python](#basic-python) : Learn basic Python concepts and syntax

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

We do not need to specify a type when declaring variables so a variable can contain anything including ints, doubles, strings, booleans, and etc. No need to end lines with **;** just write code normally:  
```python
s = "Hello Again"
num = 12
answer = True
```  
Let us look at Strings in particular and see some useful functions we can use on strings:  
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
- `.replace(old_value, new_value)` : replaces every instance of old_value with new_value within string  
```python
phrase = "Hello World"
phrase.replace("World", "Universe")    # phrase is now "Hello Universe"
```  


