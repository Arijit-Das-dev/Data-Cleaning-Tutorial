# FIXING OUTLIERS

- We have to follow some steps to fix outliers.
- IQR method is the best way to fix outliers

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