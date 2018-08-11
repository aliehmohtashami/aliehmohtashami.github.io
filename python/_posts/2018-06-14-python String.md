---
layout: post
title: "Strings in Python"
date:  2018-07-19 19:11:39 +0430
categories: python\chap0
---
## General Concepts

[Slicing Strings](#slicing-strings)  
[String Functions](#string-functions)  
[String Operators](#string-operators)  
[Iterating Strings](#iterating-strings) 
[String Inbuilt Methods](#string-inbuilt-methods)


- contiguous series of charcters delimited by single or double quotes
- no seperate datatype for characters  
- in python strings are **immutable**  
```python
 str1 ="hello"  
 str2 = "hello"  
 print(id(str1)==id(str2)) #result will be true  
```
  
### Slicing Strings
- `s[start:end]`  
- `start` and `end` are optional, if ommited, the default values will be **zero** snd **last index of string**  
 - negative values for `end` computes from last index of string 
 ```python
 str = "python"
 str[:2] #pyt
 str[3:-1] #ho
 ```

### String Functions
- `ord()` : returns ASCII code of character
- `chr()` : returns character represented by a ASCII number
- `len()` : return string length
- `max()` : return character with maximum ASCII code
- `min()` : return character with minimum ASCII code

### String Operators
#### Membership Operators
- `in` , `not in` :check existing a string in another string  

#### Comparison Operators
-  they compare strings character by character using their ASCII codes
```python
"ab"<="abc" # true
```

### Iterating Strings
```python
for i in s:
 print(i,"") #by adding a second parameter we change the default assumption of writing each string in new line
```

### String Inbuilt Methods 
[Testing Functions](#testing-functions)    
[Searching for Substrings](#searching-for-substrings)    
[Converting Strings](#converting-strings)  

#### Testing Functions
- `isalnum`: return true when all characters are **alphabetical or numeric**   
- `isalpha` : return true when all characters are **alphabetical**  
- `isdigit` :return true when all characters are **digits** 
- `isidentifier` : return true if string is a **valid identifier** 
- `islower` : return true when all characters are in **lowercase** 
- `isupper` : return true when all characters are in **uppercase** 
- `isspace` : return true when string is an **empty string** 

#### Searching for Substrings
- `endswith(some_str)`,`startswith(some_str)` return a **boolean** represents if string **end with or start with** some_str
- `count(some_str)` return an **int** as number of occurances of substring
- `find(s1)`  returns **int** represents **lowest index** from where s1 started
- `rfind(s1)` returns **int** represents **highest index** from where s1 started  

```python
str_parent = "python development is similar to other developments"
str_parent.find("development") #7  
str_parent.rfind("development") #39  
str_parent.count("development") #2  
```
#### Converting Strings
- `capitalize` : return a copy of string with **capitalizing first charachter and convert other letters to lower case**
- `lower`  
 - return a copy of string with **converting every letter to lower case**
- `upper` : return a copy of string with **converting every letter to upper case**
- `title` : return a copy of string with **converting first letter of every word to upper case and others to lower case**
- `swapcase` : **swap** case of every character
- `replace(old_str,new_str)` : **replace** old_str with new_str
```python
str = "1st self-study course of Python "
str.capitalize() # 1st self-study course of python
str.upper() #1ST SELF-STUDY COURCE OF PYTHON
str.lower() #1st self-study cource of python
str.title() #1St Self-Study Cource Of Python ('-' operate like a word splitter)
str.swapcase() #'1ST SELF-STUDY COURCE OF pYTHON'
```



