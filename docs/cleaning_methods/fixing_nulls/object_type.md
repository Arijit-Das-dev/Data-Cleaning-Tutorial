# OBJECT TYPE COLUMNS

- Type - Object

## For object type columns
We have to follow some steps to fix null values.

**Step 1 :**
- Check how many null values are present.
- Calculate percentage of null values.

**Step 2:**
- If null percentage >= 50 %, drop that column if it is not important.
- Else :
    - If null percentage <= 10%,
        - Fill with most frequent values
    - Else :
        - Identify why this column is so many null values
        - If it has a valid reason of having nulls then fill it with 'unknown'.
---

### Check for null values
Code :
```python
import numpy as np

total_nulls = df.isnull().sum()         # Total null values from each columns
nulls_pct = (total_nulls/len(df))*100   # Missing percentage among each columns

# If nulls_pct >= 50 then drop that column if it is not important
df.drop(columns=[columns], inplace = True)  # Drop columns
```

```python
# If null_pct <= 10%
df['column'] = df['column'].replace(np.nan, df['column'].mode()) 
 ```

 ```python
 # If null_pct >= 10 %
 df['column'] = df['column'].replace(np.nan, 'unknown')
 ```