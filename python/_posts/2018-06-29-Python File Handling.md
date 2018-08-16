---
layout: post
title: "Python File Handling"
date:  2018-07-30 21:11:39 +0430
categories: python\chap1
---

we can use file handling to write/read data to/from file

#### open a file

```python
f = open(filename , mode)
```
**filename** : a string shows filename along its path  
**mode** : a string shows how a file will be used (writing/reading)

|Modes|Description|
|---|----------|
|r|open a file for `read only`|
|w| open a file for `writing`, new file is created|
|a|open file in `append` mode and write data to end of file|
|wb|open file to `write` in `binary mode`|
|rb|open file to `read` in `binary mode`

**f** : handler object known as `file pointer`

#### close a file
- `close` command
```python
f.close() # f is a file pointer
```

#### writing data to file
```python
f.write("new text\n")
```
- write doesn't add **new line** to file implicitly

#### reading data of a file

|method|Description|
|---|------------|
|read([number])| return specified number of characters from the file, **number** is optional, if ommited entire file will be returned|
|readline()|return next line of file|
|readlines()|read all lines as a list of string|

- when a file is open in readonly mode, by default it is consider every line as the element
```python
f = open("filename","r")
for element in f :
 print element , "*" # it print every line then a *
```
#### binary reading and writing
- to perform binary I/O use a module name `pickle`
- using this module `load' and `dump` methods are used for read and write.
- `pickle.dump("the text",f)` write in f "the text"
- `pickle.load(f)` read a line from f

```python
import pickle
f = open("newFile.dat","wb")
pickle.dump(f,"the first line\n")
pickle.dumb(f,"the second line\n")
f.close()

f = open("newFile.dat","rb")
pickle.load(f) # the first line
pickle.load(f) # the second line
pickle.load(f) #throws `EOFError`
f.close()

```

