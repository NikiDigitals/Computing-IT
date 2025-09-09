* Course/Module/Topic: Udacity Introduction to Python  
Lesson: Data Types and Operators  
Date: 2025-09-01  
Type: note  
Tags: Python, basics, Data Types, Operators  
Related Project(s)  
Related journals: [Udacity-Pyhon Data Types and Operations](https://github.com/NikiDigitals/Computing-IT/tree/main/journals/udacity-python-datatypes-and-operators.md)
---------------

## Overview
In this section, I learned how to use various operators and apply them to calculations.
How to use and name variables correctly in Python.
The various assignment operators and their usage in code. 

## key concepts
* Operators: The use of operators in Python: PEMDAS: Parentheses, Exponents, Multiplication/Division, Addition/Subtraction.
* Variable: You can assign a variable to a value, which will then store the value. After that, you can change the value inside the variable.  
* When naming a variable, there are some rules in Python:
1. Only use ordinary letters, numbers and underscores in your variable names.
2. You can’t use reserved words or built-in identifiers as a variable name
3. When naming, use all lowercase letters and underscores to separate words. This is called snake case.
* With an assignment operator, I can perform a calculation using the current value of the variable, perform the calculation on that and store it as a new value of the variable. 

## whitespaces & good readable coding.
<i>see the Python's style guide 'PEP8' </i>
* When calling a function like `print`, add the `(` directly after without a whitespace.
* Don't write long lines of code; try to stay between 79 and 99 characters per line.

## Definitions/Syntax
`print()` is a built-in function that displays input values as text in the output.  
`print(type()) ` is a built-in function that will return the data type of the value within the brackets.  

<b>Arithmetic operators:</b>  
` + ` addition  
` - ` subtraction     
` * ` multiplication     
` / ` division  
` % ` mod (the remainder after dividing)  
` ** ` Exponentiation   
` // `  Divides and rounds down to the nearest integer

 <b>Assignment operators:</b>  
 ` = `  x = 2   
 ` += `  x = x + 2  
 ` -= ` x = x - 2  
 ` *= ` x = x * 2

<b>Datatypes</b>   
* Int: whole numbers   
* float: Real number with decimal.   
* Calculating with an integer and a float results in a float
* Be aware! Python uses approximations for a float
* bool: a boolean datatype can have true or false as a value.

<b>Comparison operaters</b>  
`<` less than  
`>` greater than  
`<=` less than or equal to  
`>=` greater than or equal to  
`==` equal to  
`!=` not equal to  

<b>Logical operarors</b>  
`And` evaluates if both sides are true  
`or` evaluates if at least one side is true  
`not` inverts a boolean datatype.  

## Examples
Use the print()
```python
print("Hello World")
Hello World                    # printed result.  
```
Use the type function:

```python
print(type(4)) 
<class 'int'>                  # printed result 
 ```
Use the operators:

``` python
x = 5 + 3
print(x)
8                               # printed result
```

Use of variables and assignment operators:

```python  
rain = 2e6                 # The amount of rain (in cubic metres)
volume_watertank = 4.5e8     # The current volume of a water water tank (in cubic metres)
rain *= .9                 # decrease the rainvariable by 10% 
volume_watertank += rain   # add the raivariable to the volume_watertank variable
volume_watertank *= 1.15       # increase volume_watertank by 15% 
volume_watertank *= .91        # decrease volume by 9% 
volume_watertank -= 1.2e5      # substract 1.2e5 cubic metres from volume_watertank
```
Changing a float and int:

```python
print(int(48.6))               # changing a float into a int
48                             # printed result

print(float(3200 + 400))       # print the result as a float
3600.0                         # printed result
```

Using a Boolean with operator:
```python
age = 5
is_teen = age > 12 and age < 18 
print(is_teen)                       
false                           # printed result

age = 5
not_teen = not (age > 12 and age < 18)
print(not_teen)
true                            # printed result of reversed.  
```

## lesson learned
- Learned how to use the operators and make simple calculations using Python.
- LEarned how to assign a variable name to a value and how to change the value of that variable. 

## external resources: 
[bitwise operators](https://wiki.python.org/moin/BitwiseOperators)   
[order of operations in Math](https://en.wikipedia.org/wiki/Order_of_operations)   
[Python reserved words](https://docs.python.org/3/reference/lexical_analysis.html#keywords)   
[PEP8 styleguide](https://peps.python.org/pep-0008/)
[Guide on Errors and Exceptions](https://docs.python.org/3/tutorial/errors.html)

