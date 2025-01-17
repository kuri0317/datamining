
|  | Data types | Description | Examples | Descriptive statistics allowed | Domain |
| ---- | ---- | ---- | ---- | ---- | ---- |
| Categorical | nominal | set of labels Operators: =, != | zip code, fiscal code | mode,entropy,contingency,correlation | Discrete |
|  | ordinal | is possible to order operators to exist <,<<,>,>> | non numerical quality evaluations | media percentiles rank correlations | Discrite |
| Numerical | interval | possible to add or subtract data +,- | calendar dates | average standard deviations | Continous |
|  | ratio | univocal definition of 0 allowing all mathematical operations | temperatures | geometric mean harmonic mean percentage variation | Continous |


## INTERVAL DATA

- used in statistical research
- examples:
	- Temperature
	- Scores
	- Time
	- IQ test

## ALLOWED TRANSFORMATIONS

| data type | transformation                                                     |
| --------- | ------------------------------------------------------------------ |
| nominal   | any one to one correspondence                                      |
| ordinal   | Any order preserving transformation (any monotonic function)       |
| interval  | linear functions                                                   |
| radio     | any mathematical function, standardization,variation in percentage |

- this transformation those not change the meaning of the attribute, they are used to standardize data format.

## ASYMMETRIC ATTRIBUTES

- attributes where only presence is relevant (non null value)
	- example exams 

## GENERAL PRO TIPS
### Dimensionality
 - the difference between having a small or a large (hundreds, thousands, . . . ) of attribute is also qualitative see the curse of dimensionality, later
### Sparsity
- when there are many zeros or nulls
	- Beware the nulls in disguise
		- a widespread bad habit is to store zero or some special value when a piece information is not available
### Resolution
- has a great influence on the results
- the analysis of too detailed data can be affected by noise
- the analysis of too general data can hide interesting patterns



## DATA QUALITY

- data from source layer are often dirty and full of outliers due to noise (*example web crawler activity mixed with human activity on websites*)
- there can be missing values due to data not being collected 
- there can be duplicated values

### DETECT OUTLIERS WITH DESCRIPTIVE STATISTICS

#### IQR interQuartile range

```
IQR = Q3 - Q1`
lower-boundary = Q1-IQR * 1.5
upper-boundary = Q3-IQR * 1.5

with Q1 first quartile Q3 third quartile 
```

the outliers are values outside the boundaries

### HANDLING MISSING VALUES

| strategy                                              | comment                                   |
| ----------------------------------------------------- | ----------------------------------------- |
| ignoring the values that are missing                  | extreme, not a generic good idea          |
| insert all possible values weighted with probabilities | used in probabilistic learning, expensive |
| estimate the missing values| default choise|

### DUPLICATED DATA

- major issue when dealing with data merging from different sources