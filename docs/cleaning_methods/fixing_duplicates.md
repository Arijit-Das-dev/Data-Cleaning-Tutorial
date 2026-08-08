# FIXING DUPLICATE COLUMNS

### Check :

Code :
```python

duplicated_mask = df['column'].duplicated() # Returns duplicates as True in columns
df.loc[duplicated, 'column']                # Returns values which is duplicate
```

### Fix :

Code :
```python

df.drop_duplicates(subset=['column'], inplace=True)  # Drops duplicate rows
```