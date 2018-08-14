---
layout: post
title:  "Python Functions"
date:   2018-07-24 18:11:39 +0430
categories: python\chap1
---
[General Features](#general-features)  
[Global Variable vs Local Variable](#gvvlv)  
[Function Argument](#fa)  
[Returning Multiple Values From Functions](#rmvff)  


### General Features
- reusable piece of code  
- ```python
def function_name(arg1,...,argN):  
    # statement 
    #return output1 , ... , outputN 
```
- **return** statement is optional and return some values as output and exits the function 

```python
def findMax(a,b):
 if a>b:
  print a
 elif a==b:
  print "equal"
 else:
  print b

findMax(12,17) #17
```
### Global Variable vs Local Variable
{: #gvvlv}
#### Global Variable
- not bound to any function
- can access from inside of any function

#### Local variable
- declared inside a function
- to bind a local variable in the global scope using `global` keyword before name of variable (same name) inside functions
- every change in the function affect global variable
```python
t = 15
print t #15
def increment_global()
 global t
 t +=1
 print t #16
print t #16
```

### Function Arguments
{: #fa}
#### Argument with Default Values
  - we can assigne a dfault value to a function parameter using **assignment** operator
  - non-default arguments should come **before** default arguments  

  ```python
  def inturoduce(name , g = 'm'):
   print name , "gender:" , g

  introduce("jack") #Ali gender: "m"
  introduce("lili" , f) #lili gender:"f"
  ```
#### ways to pass arguments to methods
- `positional argument`  
  - arguments are passed by their order  
- `Keyword Argument`  
  - arguments are passed using **name=value** pairs

```python
introduce(g="f",name="Mary") #Mary gender:"f"
```
- we can mix position and keyword argument

### Returning Multiple Values From Functions
{: #rmvff}
- using **return** statement by separating values with **comma**
- Multiple values are returned as **tuples**  

```python
 def minmax(a,b):
  if a>b :
   return b,a
  else:
   return a,b

minmax(6,2) # (2,6)
```




