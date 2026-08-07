# Fixing individual columns

### Identify errors in each column names :

- Detect special characters.
- Detect numbers.
- Detect spaces
- Detect data types
- Detect lower case format
- Detect letters
- Detect only digits

### Check :

Code :
```python

special_chars = df['column'].astype(str).str.contains(r'[^A-Za-z0-9\s]', na=False) # Detect special characters
numbers = df['column'].astype(str).str.contains(r'[0-9]', na=False)                # Detect numbers
spaces = df['column'].astype(str).str.contains(r' ', na=False)                     # Detect spaces
data_type = df['column'].dtypes                                                    # Detect data types
lower_case = df['column'].str.lower()                                              # Detect lower case
letters = df['column'].astype(str).str.contains(r'[A-Za-z]', na=False)             # Detect only letters
digits = df['column'].astype(str).str.fullmatch(r'\d+', na=False)                  # Detect only digits
```

### Fix :

Code :
```python

df['column'] = df['column'].str.replace(r"[^A-Za-z0-9]", "", regex = True) # Removes special characters
df['column'] = df['column'].str.replace(r"[0-9]", "", regex = True)        # Removes digits
df['column'] = df['column'].str.strip()                                    # Removes trailing spaces
df['column'] = df['column'].astype(str).astype(int)                        # Converts data type
df['column'] = df['column'].str.lower()                                    # Converts to lower case
df['column'] = df['column'].str.replace(r'[A-Za-z]', "", regex = True)     # Removes letters
```