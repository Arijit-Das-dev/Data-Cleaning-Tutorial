# FIXING COLUMN NAMES

### Identify errors in each column names

- Check for special characters
- Check for spaces
- Check for digits
- Check for lower case format

### Fix
```python

print(df.columns[df.columns == r'[^A-Za-z0-9]'])        # Checks special characters except letters and numbers
print(df.columns[df.columns == r' '])                   # Checks for spaces
print(df.columns[df.columns == r'[0-9]'])               # Checks for digits
print(df.columns[df.columns != df.columns.str.lower()]) # Checks if a column contains lower case format or not
```