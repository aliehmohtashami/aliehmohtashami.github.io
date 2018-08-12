---
layout : post
title : Dictionatries in Pythons
date:  2018-07-21 19:11:39 +0430
categories: python\chap0
---
[General Features](#general-features)  
[Functions and Operators](#fao)  
[Dictionary Methods](#dm)  


### General Features
- stores `key-value` pairs
- `assosiative array` or `hash` on another languages
- They are **mutable**  

#### Creating Dictionary
- can be created using `{}`
- each object is in form **key:value**
- if more than one object is available they should be separated by **comma**
- each key should be unique
- key should be of hashable types

```python
developers = {
'java':'Jack Hill',
'python':'Lorrance Green'	
}

empty_dic = {} # empty dictionary
print developers['java'] # 'Jack Hill'
```
### Functions and Operators
{: #fao}

#### Deleting Item   
- command **del dic_name['key']**
- if key not found, a **KeyError** exception will be thrown   

```python
del developers['java']
```

#### Looping Over Dictionaries
```python
for key in developers :
  print key ,":",developers[key]
```

#### Operators
- `in` , `not in` : return true when an element **is/is not** in dictionary
```python
'java' not in developers ##true (has deleted before)
```
- `len(dic_name)` : return ***number of items*** in dictionary
- `Comparison Operator`
  - **==** , **!=**
  - sequence of items in dictionaries are not important

### Dictionary Methods
{: #dm}

|Method Name|output type|Description|
|-----|---------------------|
|popitem()|String|return a random item and remove it from dictionary|
|clear()|none|delete all items from dictionary|
|keys()|list|returns all keys in dictionary as list|
|values|list|returns all values in dictionary as list|
|get(key)|string|return value of a key, if key not found **None** will return (instead of exception)|
|pop(key)|string|remove item from dictionary, if key not found an **exception** will be thrown






