---
layout: post
title: "Python Recursive Function"
date:  2018-08-5 21:11:39 +0430
categories: python\chap3
---
#### Recursive Functions
- similar to loops, but some times it makes for sense to use rucursion than loop
- every loop can be converted to recursion

```python
def fact(n):
	if n==1:
		return 1
	else:
		return n*fact(n-1)

print fact(2000) #runtime error

```
- in python default recursion depth is 1000. it means python stop calling recursive function after 1000 calls. to change this behaviour use this code:

```python
import sys
sys.setrecursionlimit(3000)

def fact(n):
	if n==1:
		return 1
	else:
		return n*fact(n-1)

print fact(2000) #return 2000!
```