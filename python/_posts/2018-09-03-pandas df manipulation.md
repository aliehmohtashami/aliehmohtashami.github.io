---
layout: post
title: "Pandas Dataframe Manipulation"
date:  2018-09-03 19:11:39 +0430
categories: python\chap4
---
[Rename a column header](#rename)  
[Rearrange columns of data](#rearrangement)  
[Working with indexes](#indices)  
[Delete row and columns](#delete)  
[Insert row and columns](#insert)  

### Rename a column header
{: #rename}

```python
data.rename(columns={old_name:new_name})
```

### Rearrange columns of data
{: #rearrangement}
- get previous arrangement of columns to a list
- change the list order 
- assign new list as the columns of data

```python
list_of_col = data.columns.tolist()
list_of_col = list_of_col[::-1] #convert column list
data[list_of_col]
```
### Working with indexes
{: #indices}
#### create index
- by default python gives an index to a data frame
- this index is not involved in data columns
- we can search on this index by its value
- index should be unique (not must be), if it is not unique, some additional works you will have in future searches
- you can check uniquness of data column using `verify_integrity = True`

```python
data = data.set_index(column_name)
#data = data.set_index(column_name , verify_integrity = True) if you want to check uniqueness
```

#### Search on index
```python
data.ix[value] #search on a index
```
#### reset index
- when resetting an index, previous index has been added to data columns
- we can prevent it using `drop=True` in reset_index parameters
```python
data = data.reset_index(); 
#data = data.reset_index(drop=True); if we want to remove it 
```

### Delete row and columns
{: #delete}
- data.drop([list],option)
- drop a list of columns/rows by checking the `option`, `0` means column, `1` means row
- dropping a row by a condition is similar to selecting some rows (no drop)

```python
data = data.drop(['column'],0)#0 for columns
data = data.drop([1],1)#1 for rows
data = data(data['age']<50) # remove records with age older than 50
```
### Insert row or column
{: #insert}
#### Insert a column
```python
data.insert(posiotion, new_name,list of values)
```
#### Insert a row
- create the record (a dictionary)
- find record position (i) and set i as index
- split data to [0,i) [i,n]
- concat first part of data, new record and second part of data
- reindex it

```python
import pandas as ps
line = ps.DataFrame(new_row,index=[i]); # set record index to i
temp = ps.concat([data[:i],line,data[i:]]) #concat data parts
temp = temp.reset_index(drop=True)
```
