---
layout: post
title: "Regression Analysis"
date:  2018-09-03 19:11:39 +0430
categories: python\chap4
---
#### Simplest Form 
- estimate a line which is nearly pass from all observations. **y = ax+b**

#### regression by minimum least square 
-estimating by minimising an error estimate

```python
data.describe() #give 5-number summary and some other features (mean, std)
```

#### Regression Analysis
- define independant variable(s) + constant variable 
- define dependant variable
- compute regression

```python
import statsmodels.api as sm
x = data['independant column']
x = sm.add_constant(x) # add a new column of constants to x
y = data['dependant column']
est = sm.OSL(y,x) #est is a regression object
est.fit() 
est.summary() #give a summary of estimate
est.predict() #give estimation of y
```



