# 🧹 Data Cleaning Methods

---

## 📌 Things To Be Done

### 1. Import Required Libraries

- Import Pandas
- Import NumPy
- Import Matplotlib (Optional)
- Import Seaborn (Optional)

---

### 2. Load the Dataset

- Read the CSV file
- Handle encoding issues (if any)
- Display the first five rows

---

### 3. Explore the Dataset

- Dataset Shape
- Dataset Information
- Data Types
- Summary Statistics
- Missing Values
- Duplicate Records
- Unique Values

---

## 🧹 Data Cleaning

### 4. Cleaning column names

Remove unnecessary columns from the dataset.

---

### 5. Rename Columns

Rename columns to improve readability and consistency.

---

### 5. Remove Duplicate Records

Identify and remove duplicate rows.

---

### 6. Handle Missing Values (NaN)

## 6. Handle Missing Values (NaN)

### Step 1: Analyze Missing Values
- Count missing values in each column.
- Calculate the missing percentage.
- If missing percentage **≥ 50%**, drop the column.

### Step 2: Handle Numeric Columns
- **Symmetric distribution (Mean ≈ Median)** → Fill with **Mean**.
- **Skewed distribution / Outliers present (Mean ≠ Median)** → Fill with **Median**.

### Step 3: Handle Categorical Columns
- **Missing < 5–10%** → Fill with **Mode (Most Frequent Value)**.
- **Missing ≥ 5–10%**
  - If the column is **important**, keep missing values for further analysis.
  - Otherwise, replace missing values with **"Unknown"**.

### How to Identify Outliers or Skewness?
- Compare the **Mean** and **Median**.
- **Small difference** → Likely symmetric → Use **Mean**.
- **Large difference** → Likely skewed / contains outliers → Use **Median**.


### 7. Clean Individual Columns

- Remove extra spaces
- Fix inconsistent values
- Convert data types
- Standardize text

---

### 8. Data Transformation

- Feature Engineering
- Encoding
- Scaling
- Normalization
- Date Conversion

---

### 9. Final Dataset Verification

- Check Missing Values
- Check Duplicate Records
- Verify Data Types

---

### 10. Save the Cleaned Dataset

Export the cleaned dataset as a CSV file.

```python
df.to_csv("cleaned_data.csv", index=False)
```