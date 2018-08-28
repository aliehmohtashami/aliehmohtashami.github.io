---
layout: post
title: "Python inheritance and polymorfism"
date:  2018-08-1 21:11:39 +0430
categories: python\chap2
---
### inheritance
- allow programmers to create a general class
- access data field and methods **which are not private**, while having our owns
- class X extends class Y, `X` is `subclass or derved class` and `Y` is `super class or base class`
- **class child(parent):**

```python

class Vehicle(object):# in python 2 (object) is necessary but in python 3 it is considered as default
	def __init__(self,name,color):
		self.__name = name
		self.__color = color

	def getColor(self):
		return self.__color

	def setColor(self,color):
		self.__color = color

	def getName(self):
		return self.__name

class car(Vehicle):
	def __init__(self,name,color,model):
#		Vehicle.__init__(self,name,color)
#		super().__init__(name,color) #python 3
		super(car,self).__init__(name,color) 
		self.__model=model

	def getDescription(self):
		return self.getName()+" "+self.__model+" in color " + self.getColor()


c = car("BMW","Blue","GM23")
print c.getDescription()
print c.getName()
```
#### Multiple Inheritance
- python has supports multiple inheritance
- **class child(parent1 , parent2)**

#### Overriding methods
- subclasses should have a method with exact signature to override it

#### isinctance function
- weather an object is an instance of the class or not  
**isinstance(object,class_type)**
```python
isinstance(2 , int) # true
```







