---
layout: post
title: "Python Exception Handling"
date:  2018-08-1 21:11:39 +0430
categories: python\chap2
---
- handle errors gracefully and do something meaningful
- **try .. except .. else .. finally ..**

```python
try:
	#do something
except <Exception Type1>:
	#handle exception

except <Exception Type2>:
	#handle exception
except: #exception type is ommited to handle unhandled exceptions

else: #optional, excecuted when no exception occures
	#process else

finally: #optional, always run
	# process finally
```
**steps**
- first statement between try and except is executed
- if no error occurs, except block is ignored
- when an error occured, if exception type matches exception name the code in except clause is executed
- `else` block is executed when no exception is raised
- finally block is executed always
- an `except` with no exception type is used to handle all exceptions 

#### raising an exception
- `raise` keyword is used to raise an exception from our own methods

```python
def classifyAge(age):
	if age<0:
		raise ValueError("enter a positive number for age")
	elif age<18:
		print "teenager"
	elif age<45:
		print "young"
	elif age<70:
		print "middle age"
	else:
		print "old"

classifyAge(-90) #line 3, in classifyAge raise ValueError()
classifyAge(35) #young
```
#### Exception Objects

```python
try:
	classifyAge(-90)
except ValueError as vx:
	print vx #enter a positive number for age
```
#### Custom Exception Class
- most of exception in pyton extends from `BaseException` class
- we can use any of these classes in this image
![exceptionHierarchy](/assets/python/exceptionHierarchy.png){: .center-image }

