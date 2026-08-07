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

special_chars = "!@#$%^&*()+-=[]{}|;':\",./<>?`~\\"

for chars in special_chars:
    df.columns = df.columns.str.replace(chars, "")  # Removes special characters

df.columns = df.columns.str.strip()                 # Removes spaces
df.columns = df.columns.str.lower()                 # Converts to lower case
df.columns = df.columns.str.replace(r'[0-9]', "")   # Removes digits
```