---
layout: post
title: "Python Lambda Function"
date:  2018-08-6 21:11:39 +0430
categories: python\chap3
---
#### Lambda Functions(Anonymous Functions)
- function with no name using a facility
- small functions usually not more than a line
- arbitrary number of arguments like normal functions
- no return statement is needed

#### Create a lambda function
- `lambda` arg1`,`arg2,...`,`argN:`expression`


```python
def multiply(a,b):
	return a*b
#convert multiply function to lambda

r = lambda(a,b):a*b
print r(12,3)#36
```
- no need to assigne lambda function to a variable
```python
print (lambda a,b:a*b)(3,4) #12
```
