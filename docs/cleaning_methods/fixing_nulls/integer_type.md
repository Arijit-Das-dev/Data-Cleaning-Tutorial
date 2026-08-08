# INTEGER TYPE COLUMNS 
 
- Type - int64

## For Integer type column
We have to follow some steps to fix null values.

### Steps -

**Step 1 :**
- Check how many null values are present.
- Calculate percentage of null values.

**Step 2:**
- If null percentage >= 50 %, drop that column if it is not important.
- Else :
    - Get mean (average)
    - Get median

        - Get their difference (mean - median) or (median - mean)
        - If mean and median is approximately same then use mean.
        - Else :
            - Check for outliers (Use box plots)
            - If outliers present then use median
            - Else use mean
---

Code :
```python
import numpy as np

total_nulls = df.isnull().sum()         # Total null values from each columns
nulls_pct = (total_nulls/len(df))*100   # Missing percentage among each columns

# If nulls_pct >= 50 then drop that column if it is not important
df.drop(columns=[columns], inplace = True)  # Drop columns

# If it is important
mean = df['column'].mean()      # Get mean
median = df['column'].median()  # Get median

differnce = abs(mean - median)  # Get difference
```

### If difference approximately same use mean
```python
df['column'] = df['column'].replace(np.nan, df['column'].mean())
```

### If difference is too much
```python
import seaborn as sns

# use boxplot for detecting outliers
sns.boxplot(
    data=df['column'],
    palette="Set3",
    linewidth=2,
    width=0.6,
    showfliers=True,
    fliersize=5
)
```

### If no outliers
```python
df['column'] = df['column'].replace(np.nan, df['column'].mean())
```

### If outliers
```python
df['column']= df['column'].replace(np.nan, df['column'].median())
```