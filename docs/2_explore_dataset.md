# Explore dataset

## Things to explore -

- Dataset Shape
- Dataset Information
- Data Types
- Summary Statistics
- Missing Values
- Duplicate Records
- Unique Values

### 1. Dataset shape :
       
- Returns number of rows and columns.

Code:
```python
rows = df.shape[0]
columns = df.shape[1]
```

### 2. Dataset information :

- Returns informations of the dataset. such as data types of columns, how many null values are present, number of rows and columns etc.

Code:
```python
info = df.info()
```

### 3. Data type :

- Returns the data type of a whole dataset or a specific column.
- Data types = Object, int64, float64 etc..

Code:
```
print(df.dtypes)            # Whole dataframe's data type
print(df[columns].dtypes)   # Specific column's data type
```