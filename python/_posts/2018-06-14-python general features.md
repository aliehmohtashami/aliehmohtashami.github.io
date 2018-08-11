---
layout: post
title: "Python General Features"
date:  2018-07-19 18:11:39 +0430
categories: python\chap0
---

[DataTypes,Commands,Function,Operators](#dcfo)

# Python General Features
- a **general purpose** language  
- has **elegant syntax** 
- **readable** codes  
- Python is **dynamically typed**.i.e. no need to declare varaiable types  
- it is **strongly typed**.i.e.not supports autamatic conversion
- python is **an interpreted** language.no need to define data structures and small utility functions  
- no need to **semi-colon**  
- an **interpreted language**   
- codes are very **small but effective**  

### python in ubuntu
- in **ubuntu** 14.04 , 16.04 is installed by default

### running a python program
- from a **.py** file: python somefile.py
- from command  

### getting help  
- help(class_name)  
- help(class_name.method_name)  


### variables
- name of locations to store references of objects . these objects are stored in memory
- they follow naming convention of most of program languages

### comments
- comments are detected using `#` character  

### simultanious assignment
- **Example.** var1 , var2 , var3 = val1 , val2 , val3  
- all variables initialized **simultanously**  
- this is useful in swapping (**x , t = t , x**)  

```python
x , t = 10 , 15
print(x,t) #(10,15)
x , t = t , x
print(x,t) #(15,10)
```
# DataTypes, Commands, Function, Operators
{: #dcfo}  

### datatypes
- `Number`
  - int  
  - float  
  - complex: `2+3j`  

- `List` :[]
- `String` : ""
- `Tuple` : ()
- `Dictionary` : {}
- `boolean`
  - two values include **True , False**.    
  - **empty/zero** datatypes are declared as False  
    - 0,0.0,zero,[],(),"",{},None  

### print command
- `print("","","")`
- every `comma` in output replaced by a `space` character

### input command
- `input("message")` : string

### useful functions
- `int(string)` : convert string to int
- `eval()`
- `type(a)` : return datatype of a
- `id(a))` : return memory address of a

### operators
- `//` : float devision
- `/` : integer devision
- `%` : remainder
- `**` : exponentiation  

### using modules in python
- many modules with predefined methods are available in python (`re` for regular expression , `math` for matematics)
- to use them we should use import word 
  -  `import module1,module2`  
  -  calling a method in them : `module1.method1`  


### general tips
- **every thing** is an **object** even basic types

## Operator Precedence  
- it is like many other programming languages

