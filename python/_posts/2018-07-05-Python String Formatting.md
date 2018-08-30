---
layout: post
title: "Python String Formatting"
date:  2018-08-6 21:11:39 +0430
categories: python\chap3
---
#### format method
- allow to format strings in any way you want
- template.format(p1,p2,...,k1=v1,k2=v2)
- `template` contains format codes
- format method replace value for each format code


#### for numbers we can use some specific format codes
|format code|description|
|---|--------|
|d|integers|
|f|floating point numbers
|b|binary numbers|
|o|octal numbers|
|s|string|
|e|floating point in exponential format|

```python
'in {0}, {1} born in {2}'.format('1956','Steve Jobs','USA')

```