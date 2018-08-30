---
layout: post
title: "Python Regular Expression"
date:  2018-08-5 21:11:39 +0430
categories: python\chap3
---
### Regular Expression 
- widely used for `pattern matching`
- python has built in support for RE, to use them import module `re`

#### Basic patterns in regular expression

|---|-------------------|------|
|SYMBOL|DESCRIPTION|equivalent pattern|
|.|any character except new line|
|\w|any word character. (**alphanumeric and underscore**) |[a-zA-Z0-9_]|
|\W|non word characters|[^a-zA-Z0-9_]|
|\d|single digit|[0-9]|
|\D|not digit single characters|[^0-9]|
|\s|any white spaces character (**\n,\t,space**)|[ \t\n\r\f\v]|
|\S|single non white spaces|[^ \t\n\r\f\v]|
|[abc]|single character matches a,b or c|
|[^abc]|single character other than a,b,c|
|[a-z]|a single character in a to z|
|[a-zA-Z]|single character in range a to z or A to Z|
|[0-9]|single charcter in range 0 to 9|
|^|match start at the beginning of string|
|$|match start at the end of string|
|+|greedy match (one or more of the preceding character)|
|*|zero or more preceding character|
|?|zero or one preceding character|
|\||or|

#### Group Capturing
- extract parts from matching string
- can be created using `parantesis`
- if the match is successfull `match.group(1)` returns the first parantesis match


#### re.search
- used to find the **first match** for the pattern in the string
- **re.search(pattern , string, flags[optional])**
- output is a `match object` on success or `None` on failure, math object has `group` method which contains the matching text  
- pattern should be specified using `raw strings`, prepending string with `r`. in raw string all special character loose their special meaning. \n is just a backslash followed by n.


#### re.match
- similar to re.search() but it begins looking for match at the beginning of the string

#### findall()
- used to find all matches in the string (returns a list)
- **findall(pattern,string,flags[optional])

```python
import re
def validateEmail(s): #first charachter can't be numeric, @,. should exists and TLD should be more than 2 characters, maybe a SLD is exists
	match = re.match(r'([a-zA-Z_])(\w*)@([a-zA-Z]+)[.](\w\w+|\w\w+[.]?\w+)$',s)
	if match:
		print match.group(1,2,3,4)
	else:
		print "no match"


validateEmail("-jack1990t@gmail.com") #no match
validateEmail("jack1990t@gmail.com")
validateEmail("jack1990t@gmail.com.")#no match
validateEmail("jack1990t@gmail.en")
validateEmail("jack1990t@gmail.c") #TLD not match 
validateEmail("jack1990t@gmail.co.uk")
validateEmail("jack1990t.com")#no match

```
- in above example character `$` garranties `last character` is an alphanumeric. check the result without it !

#### flags
- optinal parameters use to modify behavior of pattern matching

|flag|description|
|---|--------|
|re.IGNORECASE|ignores uppercase and lowercase|
|re.DOTALL|allow (.) to match newline, by default it doesn't|
|re.MULTILINE|allows ^ and $ match start and end of each line|


