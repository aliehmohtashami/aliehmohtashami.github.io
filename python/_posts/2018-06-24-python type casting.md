---
layout: post
title:  "Data Conversion(Type casting)"
date:   2018-07-24 18:11:39 +0430
categories: python\chap0
---


| input data type | output data type | function name |
|---|---|---|
|int|float|float(i)|  
|float|int|int(f)|
|string|int|int(s)|
|int|number|str(i)|  

- when converting string to int, a **valueError** will be thrown if this convertion cannot be done
  - int("12a") #error  


#### round(number,ndigit)
- round a float number using defined digits
 ```python
 f = 23.497
 round(f,2) #23.5
 ```

