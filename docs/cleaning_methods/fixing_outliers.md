# FIXING OUTLIERS

- We have to follow some steps to fix outliers.
- IQR method is the best way to fix outliers
- IQR (Inter Quartile Range) provides a range which gives a position of middle 50% of the data. 

## Steps
#### Step 1 :
- Get the (Q1) 25 percentile,
- Get the (Q2) 75 percentile,

#### Step 2 :
- Get the IQR,

```
IQR = Q3 - Q1
```

#### Step 3 :
- Get the upper and lower limit,

```
upper = Q3 + IQR * 1.5
lower = Q1 - IQR * 1.5
```
---

## Check for outliers

Code :

```python
Q1 = df['column'].quantile(0.25)    # 25th quantile
Q3 = df['column'].quantile(0.75)    # 75th quantile

IQR = Q3 - Q1   # IQR

upper_limit = Q3 + (IQR * 1.5)      # upper limit
lower_limit = Q1 - (IQR * 1.5)      # lower limit

# Check for outliers
df[df['column'] > upper_limit]      # values which is greater than upper limit are outliers
df[df['column'] < lower_limit]      # values which is lesser than lower limit are outliers
```

## Fix

Code :

```python

df[df['column'] > upper_limit] = upper_limit    # values which is greater than upper limit are replacing with that upper limit
df[df['column'] < lower_limit] = lower_limit    # values which is lesser than lower limit are replacing with lower limit

# fixed

df[df['column'] > upper_limit]  # will show 0 rows
df[df['column'] < lower_limit]  # will show 0 rows
```