---
layout: post  
title:  "Python Loops"  
date:   2018-07-29 18:11:39 +0430  
categories: python\chap1  
---

### for loop, while loop, break and continue 

#### For loop
- `syntax`  
```python
for i in iterable_objects:
 #do something
```

- `range` function
  - **range(a,b)** returns sequences of integers in [a,b)
  - **range(n)** return sequence of integers between [0,n)
  - **range(a,b,d)** return sequence of integers between [a,b) with **d** is the step size

```python
for i in range(1,10)
  print i
```

#### While Loop
```python
while condition :
 # do something
```

#### break
- breakout out of the loop

#### continue
- it ends the current iteration and control goes to the end of the loop body
