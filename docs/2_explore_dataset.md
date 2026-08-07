# Explore dataset

## Things to explore -

- Dataset Shape
- Dataset Information
- Data Types
- Summary Statistics
- Missing Values
- Duplicate Records
- Unique records

---

### 1. Dataset shape :
       
- Returns number of rows and columns.

Code:
```python

rows = df.shape[0]      # Returns number of rows
columns = df.shape[1]   # Returns number of columns
```
---

### 2. Dataset information :

- Returns informations of the dataset. such as data types of columns, how many null values are present, number of rows and columns etc.

Code:
```python

info = df.info()    # information of the dataset
```
---

### 3. Data type :

- Returns the data type of a whole dataset or a specific column.
- Data types = Object, int64, float64 etc..

Code:
```python

print(df.dtypes)            # Whole dataframe's data type
print(df[columns].dtypes)   # Specific column's data type
```
---

### 4. Summary statistics :

- Returns number of rows , minimum value, maximum value, mean, standard daviation, total , Q1(0.25) Q3(0.75) percentile.

Code:
```python

stats = df.describe()       # Summary statistics
```
---

### 5. Missing values :

- Returns missing values in each columns.

Code:
```python

total_missing_values = df.isnull().sum()                              # Returns total missing values in each column
missing_pct = (total_missing_values/total_missing_values.sum())*100   # Returns percentage of missing values in each columns
```
---

### 6. Duplicate values :

- Returns total duplicate values in each columns.

Code:
```python

duplicated = df['column'].duplicated()                  # This returns True and False in specific column (True = Duplicates, False = Unique)

print("Total duplicate values : ", duplicated.sum())    # This returns total number of duplicate values
df.loc[duplicated, 'column']                            # This returns duplicated values in specific column
```
---

### 7. Unique values :

- Returns unique values in each columns.

Code:
```python

unqiue = df['column'].unique()                          # This returns unqiue values in specific column
print("Total unique values : ", df['column'].nunique()) # This returns total number of unique values
```