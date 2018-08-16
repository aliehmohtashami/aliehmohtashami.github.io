---
layout: post
title: "Python Modules"
date:  2018-07-29 21:11:39 +0430
categories: python\chap1
---
[Python Math Module](#pmf)  
[Python Random Module](#prm)

#### Python Math Module
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

#### Python Random module
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



