---
layout: post
title: "Arrays in numpy "
date:   2018-08-20 18:11:39 +0430
categories: python\chap5
---
[Create Array](#create)  
[Methods on array](#method)  
[Generate Statistics](#stat)  
[Iterating over array](#iter)  
[Splitting array](#split)  
[Basic operation on array](#oper)  
[Print array](#print)  

### Create Array
{: #create}

```python
import numpy as np
a = np.arange(12) # [0,11)
a = np.arange(first,last,step) # by default first=0 and step=1
a = np.linspace(first,last,element number) #split space between first , last to have element number, last is included in elements
a = np.zeros((d1,d2,...,dN)) #all zeros
a = np.ones((d1,d2,...,dN)) #all one
a = np.empty((d1,d2,...,dN)) #empty array (python creates a random array)
a = np.array([3,7,11]) # array from list
a = np.array((3,7,11)) # array from tuple 
```

### Methods on array
{: #method}

|method name|inputs|description|
|------|------------|----|
|a.shape|-|dimension of a|
|a.ndim|-|dimension number of a|
|a.size|-|number of elements in a|
|a.reshape(d1,d2,...,dN)|integer numbers|reshape the array with given dimensions, d1*d2*...*dN = number of elements|
|a.T|-|transpose of a|
|a.ravel()|void|convert n-dimensional array to a vector|
|numpy.vstack((a1,a2,...,aN)|N array with same number of columns|join arrays on their columns(result have same column number)|
|numpy.hstack((a1,a2,...,aN)|N array with same number of rows|join arrays on their rows(result have same row number)|
|numpy.vsplit(a,n)|array a , n integer|split array a to n segments vertically|
|numpy.hsplit(a,n)|array a , n integer|split array a to n segments horizontally |


```python
import numpy as np
a = np.arange(12)
a = a.reshape(3,4)
b = np.arange(12,20).reshape(2,4)
c = np.vstack((a,b))#different from (b,a)
d = np.vsplit(c,2)
```

### Print array
{: #print}
```python
print a #python 2 
print(a) #python 3
```
- if a is large, python doesn't print all elements. instead it prints some and dots for the others. to print all we can use this command
```python
np.set_printoptions(threshold = np.inf)#np.inf means infinity
```python


### Basic operation on array
{: #oper}
- we can do any basic operation on array `A` and the result is a new array with equal size of `A` by applying basic operation on each element of `A`


### Splitting array
{: #split}
```python
a[1:6] # from 2nd element to 6th (a[1] to a[5])
a[:3] # a[0],a[1],a[2]

```

### Iterating over array
{: #iter}
```python
for i in a:
	print i
```
### Generate Statistics
{: #stat}
```python
import numpy as np
print a.sum()
print a.min()
print a.max()
print np.average(a)
print np.std(a) #standard deviation

# if we want to generate statistic on a single dimension
print a.sum(axis=0)
print a.min(axis=0)
print a.max(axis=0)
print np.average(a,axis=0)
print np.std(a.axis=0) 
```
