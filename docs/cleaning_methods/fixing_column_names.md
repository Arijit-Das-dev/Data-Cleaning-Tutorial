# FIXING COLUMN NAMES

### Identify errors in each column names :
- Check for special characters
- Check for spaces
- Check for digits
- Check for lower case format

### Check :
```python

print(df.columns[df.columns.str.contains(r'[^A-Za-z0-9\s]')]) # Checks special characters except letters and numbers
print(df.columns[df.columns != df.columns.str.strip()])       # Checks for spaces
print(df.columns[df.columns.str.contains(r'[0-9]')])          # Checks for digits
print(df.columns[df.columns != df.columns.str.lower()])       # Checks if a column contains lower case format or not
```

### Fix :
```python

df.columns = (
    df.columns
    .str.lower()
    .str.strip()
    .str.replace(' ', '_')
    .str.replace(r'[^A-Za-z_]', '', regex = True)
)
```

```python
# Renaming column names
df.columns = df.columns.rename(
    {
        "columnn":"column"
    }
)
```