---
layout: post
title:  "General Concepts"
date:   2018-07-15 18:11:39 +0430
categories: dm\chap1
---

- [Problem Statement](#problem-statement)
- [General Concepts](#general-concepts)
  - [Attribute Types](#attribute-types)

## Problem Statement
 - data are noisy and big in volume, so they should be cleaned in pre-processing
 - in pre-processing we should make data ready for mining 
 - to do this first we should know our data


## General Concepts
  - `data objects`
     - are entities, consists of some attributes
     - instance, object, sample, example, data point are another names
 
  
  - `attribute` 
     - is a data field
     - feature in machine learning, variable in statistic, dimension in data warehouse

  - `observation` 
    - an observed value for a given attribute

  - `feature vector` or attribute vector 
    - set of observation to describe an object 

## Attribute Types 
  - [First Classification](#first-classification)
  - [Second Classification](#another-classification-based-on-machine-learning)

  
# First Classification
 -`nominal`(categorical)
  - relating to names
  - symbols or name of things
  - no order
  - enumuration in computer science
  - not quantitave (however they may be integers)
  - mode can be used as their central tendency  
  - qualitative attribute
  - **example** single, married, divorced, widowed for marital-status

-`ordinal`
 - an attribute with possible values that have a meaningful order or ranking
 - magnitude between successive values are not known
 - median, mean can be used as central tendency
 - qualitative attribute
 - **example** the size of a cup in a cafe. (small, medium, large, they are like nominal values, but have some orders with no knowledge about much of difference)


-`binary`
 - a nominal attribute with two categories
 - **0** means attribute is absent and **1** means it is present
 - Boolean in computer sciences with true and false values
 - qualitative attribute
 - **example** attribute smoker for a patient
  - can be symmetric or asymmetric
    - `symmetric binary attribute`
	  - if both states are equally valuable (male or female)
    - `asymmetric`
	  - the outcomes of the states are not equally important 
	  - **by convension** the most important outcome (usually the rarest one) is 1. (HIV positive)

-`numeric`
 - quantitative attribute
 - measurable
 - can be intervel-scaled or ratio-scaled
   - `interval-scaled`
     - are measured on a scale of equal-size units
     - have order and allow us to quantify the difference between values
     - they have no true zero point, so cannot say a value as being a multiple of another
     - **example** we **can't** say 10 Celsius is warmer than 5 Celsius **two times**.
   - `ratio-scaled`
     - a numeric attribute with an inherent zero point, so scale can be computed
     - **example** years of experiences

# Another Classification based on machine learning
- discrete
  - have a finit or countably infinite(set of values are infinit but can be mapped to natural numbers) set of values (smoker, cup size, marital-status)
- continous
  - isnt discrete
  - numeric attribute is another term (however can be confused because numerics are integers or real, but continious are real)