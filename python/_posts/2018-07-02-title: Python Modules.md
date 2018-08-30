---
layout: post
title: "Python Modules"
date:  2018-08-01 21:11:39 +0430
categories: python\chap3
---
[Python Math Module](#pmf)  
[Python Random Module](#prm)  
[Python Custom Modules](#pcm)

### Python Math Module
{: #pmm}

- no need to import any module

|Method|Description|
|---|------------|
|round(number[,ndigit])|round number, percision is the second argument|
|pow(a,b)|return **a** rasie to the power of **b**|
|abs(x)|absolute value of x|
|max(x1,x2,...,xN)|largest among supplied arguments|
|min(x1,x2,...,xN)|smallest value among supplied arguments|  

- need to `import math` to use them

|Method|Description|
|---|------------|
|cell(x)|round the number up and returns its nearest integer|
|floor(x)|rounds the number down and returns its nearest integer|
|sqrt(x)|square root of the number|

### Python Random module
{: #prm}
- we should use `import random`
- **random()** function returns a random number between [0,1)
- **randint(a,b)** generate random number between [a,b]

```python
import math , random
for i in range(1,10) :
 number = math.ceil(random.random()*360)
 list.append(number)

list # 10 angel beween 0 , 360
 ```

### Python Custom Modules 
{: #pcm}
- a normal python file
- to store functions, variables, classes, constants, etc.
- help us to recognize related codes

#### creating modules
- create a file with appropriate name
- write needed codes

#### using a module
- `import mymodule`
- `mymodule.myfunc` or `mymodule.myvar`
- to access only a specific function or variable use `from`, in this case no need to specify module name to access variable
```python
from mymodule import myVar
print myvar
```

#### dir() method
- in-built method to find all attributs of the object, as every thing in python is an object we can use dir() to find attributes of a module
- output contains some attributes which are in-built and python provides them to all modules automatically



