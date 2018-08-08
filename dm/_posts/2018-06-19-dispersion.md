---
layout: post
title: "Measuring The Dispersion Of Data"
date:   2018-07-17 18:11:39 +0430
categories: dm\chap1
---

[Range,Quartile,Interquartile](#one)  
[Five-Number Summary,Boxplots,Outliers](#two)  
[Variance and standard deviation](#variance-and-standard-deviation)  
[Graphic displays of basic description](#graphic-displays-of-basic-description)

# Range,Quartile,Interquartile
{: one}

 `Range`
 - difference between max and min

 `Quantile`
 - **points** taken at regular intervals of data distribution  
- `q-quantile` : divide dataset to q equal parts  
- `100-quantiles` are referred as **percentiles**  
- `2-quantiles` corresponds to median  
- `4-quantiles` corresponds to **quartile**  
	  - $$Q_{1}$$: the first quartile, the 25th persentile (cuts off lowest 25% of the data)  
	  - $$Q_{2}$$: the **median**  
	  - $$Q_{3}$$: the third quartile, the 75th persentile (cuts of highest 25% of data)  

`Interquartile range`
- spread that gives the range of middle half of data

$$IQR = Q_{3} - Q_{1}$$  

- a common rule of thumb for identifying suspected outlier:   
	single out values at falling least **1.5*IQR** above the third quantile or below the first quantile

---

# Five-Number Summary,Boxplots,Outliers
{: #two }

  `Five-number Summary`  
	- min, median, Q1, Q3 , max   (to know head and tail of data)

`Boxplots`
- popular way of visualizing a distribution  
- incorporates the five number summary  
- length of the box is the interquantile  
- median, max and min will be three horizontal line (the last two called **whiskers**)  
- when moderate number of observation, we can plot potential outliers individually, to do this, extend whiskers to the most extreme data occuring **1.5*IQR** of the quartile and plot remining observations individually  
- Boxplot can be computed in **O(nlogn)** time  
![boxplot_img](/assets/dm/boxplot.png){: .center-image }

---

# Variance and standard deviation 

`Variance` $$(\sigma^2)$$
 - indicate how spread out a data distribution  
 - low value show data are close to mean  

   $$variance = mean(x^2)-(mean(x))^2$$

`Standard Deviation` $$(\sigma)$$
- root of variance
- `basic properties`  
  - measures spread about the mean, so only should be considered when mean is chosen as the measure of center  
  - always greater than zero, except when all values are equal  
  - an observation is unlikely to be more than several standard deviations away from the mean.  
   - `chebyshev inequality`  
        - at least $$(1-\frac{1}{k^{2}})$$ percent of data are no more than $$k*\sigma$$

 $$p(x<=k\sigma)>=1-\frac{1}{k^{2}}$$

---

# Graphic Displays Of Basic Description

‍‍`quantile plot`  
- simple and effective to show all data (univariate)  
- plots quantile information  
- for every x there is a f(x) which show f(x)% of data are less than x  
![quantile_img](/assets/dm/Quantile.png){: .center-image }



`quantile-quantile`  
- q-q plot graphs the quantile of one univariate distribution against another
- it can show shift between two distribution  
![quantile_quantile_img](/assets/dm/Q_Q.png){: .center-image }



`histogram`
- a bar chart
- vertical axis is frequency of x value
- the range of values is partitioned to disjoint consecutive subranges
- **subranges** : buckets or bins
- range od buckets : **width**  
![histogram_img](/assets/dm/histogram.png){: .center-image }


`scatter`
- to determine if there is a relationship between two numeric attribute
- each pair of values treated as a pair of coordination in algebra
- useful to check possibility of correlation on bivariate data  
![scatter_img](/assets/dm/scatter.png){: .center-image }







