---
layout: post
title: "Data Visualization"
date:  2018-09-03 19:11:39 +0430
categories: python\chap4
---
### Visualize Data Value
- using `matplotlab` we can draw several plots types

#### series plot
- large sample size
- discover pattern behavior over time
- ex. stock price over time
```python
datacolumn.plot()#by default a series plot
```

#### bar plot
- small smaple size
- discover pattern behavior
- compare different observation
- ex. annual revenue
```python
datacolumn.plot.bar()
```


### Visualize Data Distribution

#### histogram plot
- compare frequency of differnet observations
- small sample size
```python
dataframe.plot.hist() # several attributes draw on one graph and the bigger cover the other
dataframe.plot.hist(alpha=0.25) #alpha is for transparency
dataframe.plot.hist(stacked = true)  # more frequent feature doesn't cover the other
```

#### boxplot
- statistical data visaualize
- minimun, 1st quartile, median, 3rd quartile,maximum (5 number summary)
- `Nth-quartile` is a value `N/4` data are lower than it
```python
dataframe.plot.box()
```

### Visualize Data Concentration
#### Scatter Plot
- needs two dimension
- small sample size
```python
df.plot.scatter(x='first-var',y='second-var',s=df.score) #set size of point based on s
```

#### Heat Map (Hexagon Beaning plot)
- large data size
- color intensity of an area dependes on data concentration
```python
df.plot.hexbin(x='first-var',y='second-var',gridsize=25) #the deeper the color, the more concentration
```


### Visualize Data Composition

#### Pie Plot  
- compare data on a fixed point
-ex. annual revenue of several supplies
```python
df.ix[0].plot.pie() # a row
df.myColumn.plot.pie() #a column
```


#### Area Plot
- data composition change over time
- ex.  stock price of different supplies
```python
df.plot.area();
```




