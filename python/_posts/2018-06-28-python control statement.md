---
layout: post
title:  "Python Control Statement"
date:   2018-07-24 18:11:39 +0430
categories: python\chap1
---

 #### `if-elif-else` Command
 - for every **if** we can have any number of **elif** and one number of **else**

 ```python
 age = input("enter your age:")
 if age<18:
  print "you have no permission to play"
 elif age<50:
  print "you have permission to play"
 else:
   print "you may become tired of playing?"
   answer = input(" are you sure?Y/N")
   if answer.lower() == "y":
     print "welcome"
   elif answer.lower() = "n":
     print "Nice to meet you"
   else :
     print "we have to lock your account, sorry."
 ```

- pay attention to indents