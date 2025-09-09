* Course/Module/Topic: Introduction to Python.   
Issuer: Udacity   
Lesson: data structures in python   
Date: 2025-09-03   
Type: note   
Tags: Python. basics, data structures, built-in functions, operators   
Related Project(s)  
Related journals:  
---------------   

## Overview
Types of data structures: lists, Tuples, Sets, Dictionaries, and Compound Data Structures.       
How to use lists in python: How does zero indexing work and how 'to slice' a part of the list.      
Check if a word in/or not in the list and how to change the value of en element in the list.   
The use of the functions `len()` `max()` `min()` `sorted()` with lists.      
The use of the methods `join` and `append` with lists.   

Operators: Membership and identity.   

## key concepts  
* Many programming languages use <b>zero-based indexing</b>. They start counting with 0.   
* It is possible to start counting from the last element of the list by using a negative number.   
* When using slicing to select a part of a list, remember: The lower index is inclusive, the upper number is exclusive. 
* A list is mutable, whereas a string is not. 

## Definitions/Syntax  
* <b>Data structures</b> are collections of data that group and organise data types together.
  Similar to a file system.

* <b>Lists</b> is a datatype for mutable ordered sequences of elements and can consist of different data types.
* <b>Zero indexing: </b>the index describes how far the element is removed from the start of the list.   
  Element 1 is zero places removed from the start of the list and gets index [0] 

* It is possible to select only a part of the string with slicing [1:4], [ :4], [2: ]
* In a list, you can reassign a new value to an element of that list by writing dwoen the variable[indexnr] = new value  

<b>functions</b>   
`len()` returns how many elements/items there are in the list.   
`max()`    
`min()`   
`sorted()`   

## Examples

Data structure: List
```python
animals = ['sheep', 'frog', 'fish', 'duck', 'monkey']        # variable animals with a list as value
print(animals[0])                                            # print the value at place 0 in the list
print(animals[4])                                            # print the value at place 4 in the list
print(animals[-2])                                           # print the value at place 2 counting backwards from the end.
sheep                                                        # printed result [0]
monkey                                                       # printed result [4]
duck                                                         # printed result [-2]   
```
Using slicing to select part of a list:
```python
random_list = [1, 'Hello', 7.3, False]                      # variable with a random list as value
print(random_list[1:2])                                     # print the element on index 1 stop before index 2 
Hello                                                       # printed result

random_list[:2]                                             # print the elements from the start of the list until index 2  
1, Hello                                                    # printed result  

random_list[1:]                                             # print the elements starting on index place 1 - end of the list
Hello, 7.3, False                                           # printed result  
```
Is a word included/excluded from the list?
```python
string = "This is a sentence"                                 # variable with the string "this is a sentence" as value 
print('example' in string)                                    # Is the word example in the value of the variable string?
false                                                         # printed result.
```
## lesson learned


## external resources 


-------------------
