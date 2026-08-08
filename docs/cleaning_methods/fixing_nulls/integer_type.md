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