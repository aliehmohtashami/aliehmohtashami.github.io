---
layout: post
title: "Python Generators"
date:  2018-08-4 21:11:39 +0430
categories: python\chap3
---

#### Generators
- **functions** used to create iterators  
- the only difference is about using `yield` keyword
- this keyword returns value for each iteration of the for loop

```python
def my_range(start,stop,step = 5): #we are trying to clone built-in range function
	if start>stop:
		raise ValueError()
	i = start
	while i<=stop:
		yield i
		i += step

for m in my_range(0,20):
	print m #0,5,10,15,20

```

