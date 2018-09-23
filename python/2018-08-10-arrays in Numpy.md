---
layout: post
title: "Arrays in numpy "
date:   2018-08-20 18:11:39 +0430
categories: python\chap5
---


|method name|inputs|description|
|------|------------|----|
|a.shape|-|dimension of a|
|a.reshape(d1,d2,...,dN)|integer numbers|reshape the array with given dimensions, d1*d2*...*dN = number of elements|
|a.T|-|transpose of a|
|a.ravel()|void|convert n-dimensional array to a vector|
|numpy.vstack((a1,a2,...,aN)|N array with same number of columns|join arrays on their columns(result have same column number)|
|numpy.vstack((a1,a2,...,aN)|N array with same number of rows|join arrays on their rows(result have same row number)|
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