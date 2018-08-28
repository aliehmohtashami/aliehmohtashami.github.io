---
layout: post
title: "Python *args and **kwargs"
date:  2018-08-1 21:11:39 +0430
categories: python\chap3
---

#### *args
- allow to pass `variable number of argumants` to the function

```python
def sum(a,b): #just two number
	print a+b 

def sum(*args): #variable number of numbers
	s = 0
	for i in args:
		s += i
	print s
```
- name of `*args` is just a convention, any valid identifier can be replaced. **ex. *myargs **

#### **kwargs
- allows to pass variable number of keyword arguments

```python
def my_func(**kwargs):
	for i,j in kwargs.items():
		print i,j

my_func(name="jack",age=12,city="London")

```

- by using *args and **kwargs we can pass elements in iterable variable to a function  
- when using `*args`
  - number of arguments should be the same as number of elements in iterable variable
- when using `**kwargs`
  - Names of arguments in function must match with the name of keys in dictionary.
  - Number of arguments should be same as number of keys in the dictionary

```python
def my_three(a, b, c):
	print(a, b, c)
a = {1,2,3} # a=(1,2,3) or a=[1,2,3]
my_three(*a) #(1, 2, 3)

a = {'a': "one", 'b': "two", 'c': "three" }
my_three(**a) #('one', 'two', 'three')

a = {'a': "one", 'h': "two", 'c': "three" } #my_three() got an unexpected keyword argument 'h'

```