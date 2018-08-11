---
layout : post
title : Lists in Pythons
date:  2018-07-21 19:11:39 +0430
categories: python\chap0
---

### General Features
- another sequence type
- similar to array
- lists are **mutable**
```python
l1 = [1 , 2 , 4 , 7]
l1 = list([1,"jack"]) #[1,'jack']
l3 = list("python") #['p', 'y', 't', 'h','o','n']
l4 = list() #empty list
```
### Common Operations
- element1 `in`/`not in` list1  : true if element1 `is`/`isn't` in list1
- list1`+`list2 : concatente two sequence list1, list2
- list1 `*` number1 : number1 copies of list1
- list1`[i]` : **i th** element in list1
- `len(s)` : length of list1
- `min(s)` : smallest element in sequence
- `max(s)` : largest elemt in sequence
- `sum(s)` : sum of all numbers in list, throw exception on non-numeric lists
- `list slicing` : list[start:end]
- `for loop` 
```python
for i in list:
	 print i
```

### commonly used list methods (built-in)

| Method | goal | return |  
|-----|------|---|  
| `append(object)` | adds element to end of list | none |
| `count(object)` | number of times the object elements appers in list | number |
| `extend(list1)` | append all elements of in list1 to  list  | none |
| `index(object)` | return index of first occurance of element x in list, throw exception in | number |
| `insert(integer,object)` | insert object at position i | none |
| `remove(object)` | remove first occurance of object in list | none |
| `reverse()` | reverse list | none |
| `sort()` | sort list in ascending order | none |
| `pop(i)` | remove element at given position and return it, if parameter i is not specified the last element will be picked | object |

### List Comprehension
- it provides a concise way to create list
  - consists of square brackets containing expression followed by for clause then can have if clauses
  ```python
  list1 = [x-1 for x in range(20) if x % 2 !=0] # [0, 2, 4, 6, 8, 10, 12, 14, 16, 18]
  ```



