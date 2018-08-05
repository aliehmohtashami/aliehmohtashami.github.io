---
layout: default
title: Basic Statistical Measurement
categories: dm\chap1
---
[Basic Statistical Description](#basic-statistical-description)  
 - [Median](#median)  
 - [Mean](#mean)  
 - [Mode](#mode)  
 - [Midrange](#midrange)  

# Basic Statistical Description
- can be used to identify properties of the data
- highlight which data is outlier or noise
- central tendency measure
- gives the location of center of distribution
- if we plot a data set of observation where would most of value falls

---
## Median
 - it is good for skewed data
 - middle value in a set of **ordered** data values
 - it sparate lower half and higher half  
    
    **example**  : 2 , 6 ,`9`,16, 35 

 - can be used for **ordinal** and **numeric** data
 - if the set size is **even** median won't be unique, if dataset is numerice **by convention** the average of the two used, otherwise it is the two middlemost values and any value between

 - when there is a large number of observation, computing median is extensive
 - we can approximate this value, using data frequency in some interval. let interval that contains the median frequency be the **median interval**			using this formula we can approximate median

$$medain = L_{m}+\frac{\frac{N}{2}-({\displaystyle\sum freq})_l}{freq_{median}}width$$

 - numerator shows number of observations of lower half in median interval 
 - width is ($$U_{m}-L_{m}$$) and N is number of observations

---
## Mean
- average of data  
- it is very sensitive to outlier values

$$mean = \frac{\displaystyle\sum_{i=1}^{n} x_{i}}{n}$$  

 **Weighted Mean**
- if observation have weights  

$$mean = \frac{\displaystyle\sum_{i=1}^{n} w_{i}x_{i}}{\displaystyle\sum_{i=1}^n w_{i}}$$  


 **Trimmed Mean**
 - to conquer on sensitivity of mean to outliers, trimmed mean can be used
 - compute mean after chopping values of low and high extream (by a small threshold to not loose valuable data)

---
## Mode
- value that occurs most frequently
- we can have more than one mode
- so we have datasets called unimodel(one mode), bimodel(two modes) and trimodel(three modes) and generally multimodel.
- for numeric data that are moderately skewed we have $$mean - mode = 3 *(mean - median)$$ 
- **example**:   `2`,3,`2`,5,7,3,`2` 

---
## Midrange
 - the average of minimum and maximum value

  $$midrange = \frac{value_{max}+value_{min}}{2}$$

