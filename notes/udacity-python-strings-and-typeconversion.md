* Course/Module/Topic: Udacity Introduction to Python  
Lesson: Data Types and Operators   
Date: 2025-09-02  
Type: note  
Tags: Python, basics, strings, bool, methods 
Related Project(s)  
Related journals: [Udacity-python-strings-and-typeconversion](https://github.com/NikiDigitals/Computing-IT/blob/main/journals/udacity-python-strings-and-typeconversion.md)   
---------------

## Overview
This section covers the datatypes of booleans, combined with operators, Strings, and the use of Methods.


## key concepts  
`Str` is a datatype used for an ordered sequence of characters (eg letters, symbols, spaces, numbers)   
* It is used by enclosing the sequence with single ' or double " quotes, between brackets.  
* A variable can have a string as a value, just like with numbers.  

<b>A method</b> is a function that "belongs" to its object.
* In Python, a method behaves similarly to a function; the difference is that methods are specific to the data type for a particular variable
* There are built-in methods available for all strings, integers, etc.
* All the values between the parentheses() when using a function or a method are called <b>arguments</b>.
* When using a method, the first argument is always the object it "belongs" to.
* An essential and often used method is `format()` Especially combined with the `print()` function it is a great value.  

<b>F-string, or "Formatted String Literals"</b>, is a method of string formatting introduced in Python 3.6.   
It optimises and simplifies the process of including variables within a string.   
* When using expressions within a f-string, you can use complex expressions within the {}.
* Python will evaluate the expressions and replace them with their results.

<b>The .split method</b> returns a data container called a list that contains the words from the input string.
*  <b>The sep argument</b> stands for "separator". It can be used to identify how the string should be split up
   (e.g., whitespace characters like space, tab, return, newline; specific punctuation (e.g., comma, dashes)).
   If the <b>sep argument</B> is not provided, the default separator is whitespace.
* <b>maxsplit argument</b> provides the maximum number of splits.
  The argument gives maxsplit + 1 number of elements in the new list, with the remaining string being returned as the last element in the list.
  
## Definitions/Syntax  
* When using a quote as a sting value, use single and double quotes: '"This is a Quote"'  
* When using a ' inside the string use an  `\`: '"I think you\'re a programmer"'
* `len` is a built-in function that counts the length of a string.  

<b>Operations combined with strings</b>  
`+` combines strings   
`*` repeats strings  

<b>String methods</b>   
  
`capitalize()` `casefold()` `center()` `count()` `encode()` `endswitch()` `expandtabs()` `find()`   
`format()` `format_map()` `index()` `isalnum()` `isalpha()` `isdecimal()` `isdigit()` `isidentifier()`   
`islower()` `isnumeric()` `isprintable()` `isspace()` `istitle()` `isupper()` `join()` `ijust()`   

* f-string formatting
* The split method: `string.split(sep, maxsplit)`

## Examples

Assign strings to a variable:

```python
first_name = 'Simon'                            
print(first_name)
Simon                                              # printed result.  

quote1 = '"I Think you\'re a writer"'
print(quote1)
I think you're a writer                            # printed result.      
```
Stings and operators:

```python
first_name'Simon'
last_name'Eck'
print(first_name + ' ' + last_name)                # combine 2 strings and ad a space inbetween.
Simon Eck                                          # printed result.  

call = 'Hey'
print(call * 5)
HeyHeyHeyHeyHey                                    # printed result. 
```
Count the length of a string.
```python
Programming_length = len('programming')
print(programming_length)
11                                                  # printed result is the number of characters.  
```

Use of methods
```python
print("simon eck".title())                                      #.title formats the string object into a title 
Simon Eck                                                       # printed results with upper cases.

print("one fish, two fish, big fish, small fish".count(fish))   #.count, count the number of times the argument is in the string  
4                                                               # printed result.
```

Using the method `format()
```python
print("James is {} years old".format(23))                       # the argument 23 in the method format() is printed on the place of the {}  
James is 23 years old                                           # printed result  

animal = cat                                                    # assigned variable    
color = black                                                   # assigned variable 
print("Do you have a {}{}?".format(color,animal))               # method uses argumented values as input for the {}{} in the string 
Do you have a black cat?                                        # printed result    

jane_string = "Jane loves {} and {}"                            
print(jane_string.format("dogs", "cats"))                       # the method uses the argumens in the string. 
Jane loves dogs and cats                                        # printed result
```

f-string formats
```python

name = "John"
print(f"Hello, {name}")
Hello, John
```
Using Expressions within the f-string. 
```python
a = 5
b = 3
print(f"The sum of {a} and {b} is {a+b}")
The sum of 5 and 3 is 8
```

split method
``` python
new_str = "The cow jumped over the moon."
new_str.split()
['The', 'cow', 'jumped', 'over', 'the', 'moon.']

new_str.split(' ', 3)
['The', 'cow', 'jumped', 'over the moon.']
```
## lesson learned
* I learned about strings and the different ways I can use them in Python.
* I learned about booleans and how to combine them with operators effectively,
* I learned about methods. What they are and how they can be used on a string.
* I learned a bit more about the methods .format, f-string and .split since they are particulary useful for coding in python

## external resources 
[read more](https://docs.python.org/3.6/library/string.html#format-string-syntax) about he method .format() syntax   
[read more](https://docs.python.org/3/library/stdtypes.html#string-methods) about strings and string methods

-------------------
 journals: [python-datatypes-and-operators](https://github.com/NikiDigitals/Computing-IT/blob/main/journals/udacity-python-datatypes-and-operators.md)     
 notes: [python-datatypes-and-operators.](https://github.com/NikiDigitals/Computing-IT/blob/main/notes/udacity-python-datatypes-and-operators.md)    
