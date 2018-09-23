---
layout: post
title: "Serries in pandas "
date:   2018-08-21 18:11:39 +0430
categories: python\chap4
---

### Serries in pandas
should install and import `pandas` module
- pip install pandas
- sudo apt-get install python-pandas

series can be produced in several ways
- from scaler values
- from collections
  - list, dictionary, tuples, arrays(defined in `numpy` module)

```python
import pandas, numpy
paS = pandas.Series([1,2,3],index=['a','b','c'])

dic = {'name':'ali','gpa':'12.5'}
paD = pandas.Series(dic)

lis = [2,4,5]
paL = pandas.Series(lis)

tup = ('t1','t2','t3')
paT = pandas.Series(tup)

arr = numpy.random.randn(5)
paA = pandas.Series(arr)

print paS,"\n",paD,"\n",paL,"\n",paT,"\n",paA , paS[0]
```

Access to an element in series
- using `[]` : series[index]

---
### Import data from files

```python
import pandas as ps
csv_data = ps.read_csv('customer.csv')
xls_data = ps.read_excel('customer.xlsx',sheetname='Sheet2') #second parameter is optional if several sheets are available
```
---

### Export data to files
```python
csv_data.to_csv('new_file.csv')#create csv file while adding an index column to it
csv_data.to_csv('new_file.csv',index = False)#create csv file without adding index column to it
csv_data.to_excel('new_file.xlsx',index = False)#create excel file without adding index column
```   
---
### get data of a column
- #### by column name  
  - get a `single` column 
    - **data['name']**
    - **data.name** as each column is an attribute   
<br>
  - get `multiple` column, input argumant is a list of column
    - **data[['name','city']]**   
<br>
- #### by column index
  - `no matter` if we want a single/multiple column(s), input argumant is always a list 
    - **data[[1]] or data[[1,2]]**   

---

### get data of a row
  - **data[l:u]** : return (u-l-1) rows start from l
  - #### using `ix`
    - **data.ix[i]** : return **i**th row 
    - **data.ix[l:u]** : return (u-l) rows start from l

---

### get data of special row and column
- **data.ix[r,c]**
- **data.ix[r1:r2,c1:c2]**  

---

### define a condition 
- **data.ix[data.age>20]**
- `isin` : **data.ix[data.name.isin['jack','jim']]**

### useful methods
- data.head(n) : **n th** start from first 
- data.tail(n) : **n th** start from end
- len(data) : length of data
