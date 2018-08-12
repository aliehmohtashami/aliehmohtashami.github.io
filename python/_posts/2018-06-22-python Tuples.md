---
layout : post
title : Tuples in Pythons
date:  2018-07-22 19:11:39 +0430
categories: python\chap0
---

### General Features
- tuples are similar to lists, **except that** when it is created it cannot add, delete, replace, reorder
- they are **immutable**

#### Creating Tuples
```python
t1 = (1,2,3) #(1,2,3)
t2 = tuple([11,23,33]) #(11,23,33)
t3 = () #empty tuple
```
#### Iterating Through Tuples
```python
for i in t:
	 print i
```
#### Slicing Tuples
- tuple[`start`:`end`]

#### checking operator
- `in` and `not in` operator 
 -  check existence of item in tuple
 ```python
 t = (1 ,2 , 3, 4)
 2 in t  #true
 ```

