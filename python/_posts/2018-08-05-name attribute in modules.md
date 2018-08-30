---
layout: post
title: "if __name__== '__main__'"
date:  2018-08-6 21:11:39 +0430
categories: python\chap3
---
- every module in python has an attribute called `__name__`
- when the module run as main program this attribute set to **__main__**
- else it set to **moduleName**

```python
#file one.py

def hello():
	print "value of name is module one is :",__name__
	if __name__=="__main__":
		print "one is the main module" 
	else:
		print "one isn't main module"
hello()


##################################
#file two.py

import one

#################################
python one.py
#value of name is module one is : __main__
#one is the main module

python two.py
#value of name is module one is : person
#one isn't main module
```
