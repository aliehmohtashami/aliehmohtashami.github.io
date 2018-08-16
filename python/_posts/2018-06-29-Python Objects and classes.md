---
layout: post
title: "Python Objects and classes"
date:  2018-08-1 21:11:39 +0430
categories: python\chap2
---

- python is object oriented languages
- every thing is an object, primitive types, modules, functions and so on
- object oriented programming use objects to create programs, these objects stores data and behaviors

[Classes in Python](#cip)  
[Overloading Operator in Python](#ooip)

#### Classes in Python
{: #cip}
- needed `class` keyword, class name followed by a `colon`
- every class in python have `initializer` method (it is a constructor and executes every time an object is created)
- initializer method signature is defined by
```python
 def __init__(self,arg2,...argN)
 ```

 `self`
  - in python all methods should have `self` as their **first parameter**
  - it refers to the object which invoke the method
  - on creating a new object the self parameter in __init__ set to reference of the created object automatically
  - when a method is called, there is no need to pass anything to self parameter.
  - To have `private` attribute or method we can use `__` before name of them

```python
class Student:
 def __init__(self , name , age):
  self.__name = name
  self.age = age
 

 def sayHello(self)  :
  print "hello" , self.__name

p1 = Student("John","12")
p1.sayHello() #hello John
print p1.age # 12
print p1.__name #Student instance has no attribute __name
```
#### Overloading Operator in Python
{: #ooip}
- defining methods for operators
- we can overload many operators using their relevant function

|Operator|Function|Description|
|---|------------|---------|
|+| \__add\__(self , other)|Addition|
|-|\__sub\__(self , other)|Subtraction|
|*|\__mul\__(self , other)|Mulriplication|
|%|\__mod\__(self , other)|Remainder|
|/|\__truediv\__(self,other)|Devision|
|<|\__lt\__(self , other)|less than|
|<=|\__le\__(self , other)|less than or equal|
|==|\__eq\__(self , other)|equal to|
|!=|\__ne\__(self , other)|not equal to|
|>|\__gt\__(self , other)|greater than|
|>=|\__ge\__(self , other)|greather than or equal to|
|[index]|\__getitem\__(self,index)|index operator|
|in|\__contains\__(self,value)|check membership|
|ln|\__len\__(self)|the number of elements|
|str|\__str\__(self)|string representation|

```python
class Student:
 def __init__(self , name , age):
  self.__name = name
  self.__age = age
 
 def __gt__(self,other):
 	return self.__age>other.__age

 def __lt__(self,other):
 	return self.__age<other.__age

 def sayHello(self)  :
  print "hello" , self.__name


p1 = Student("Wohn",12)
p2 = Student("Marry",15)
print p1<p2 #true
print p1>p2 #false
```

