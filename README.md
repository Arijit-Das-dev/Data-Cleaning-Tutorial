# 🧹 Data Cleaning Techniques using Python

<div align="center">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/numpy/numpy-original.svg"
       width="90"
       title="NumPy">

  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/pandas/pandas-original.svg"
       width="90"
       title="Pandas">

  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/matplotlib/matplotlib-original.svg"
       width="90"
       title="Matplotlib">

  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/seaborn/seaborn-original.svg"
       width="90"
       title="Seaborn">

  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/scikitlearn/scikitlearn-original.svg"
       width="90"
       title="Scikit-learn">
</div>

---

# 📌 About This Repository

Welcome to the **Data Cleaning Techniques** repository.

This repository is a comprehensive collection of **real-world data cleaning methods** used in Data Analysis and Data Science projects.

Data cleaning is one of the most important phases of the data analysis pipeline. Poor-quality data often leads to inaccurate insights and unreliable machine learning models. This repository demonstrates practical techniques to transform messy datasets into clean, consistent, and analysis-ready data.

Whether you're a beginner learning Pandas or an aspiring Data Analyst preparing for projects and interviews, this repository serves as a practical reference guide.

---

# 🎯 Repository Goals

This repository aims to:

- Learn industry-standard data cleaning practices.
- Handle messy real-world datasets.
- Build reusable data preprocessing techniques.
- Improve data quality before visualization or machine learning.
- Create a personal reference for future projects.
- Help beginners understand data cleaning step by step.

---

# 📚 Topics Covered

The repository includes techniques for:

## ✅ Data Exploration

- Understanding the dataset
- Inspecting rows and columns
- Checking data types
- Summary statistics
- Memory usage
- Detecting missing values

---

## 🗑️ Removing Unnecessary Data

- Dropping redundant columns
- Removing irrelevant features
- Removing duplicate rows
- Removing duplicate columns

---

## 📝 Column Standardization

- Renaming columns
- Formatting column names
- Converting to lowercase
- Replacing spaces with underscores

Example:

```python
df.columns = df.columns.str.lower().str.replace(" ", "_")
```

---

## 🔍 Handling Missing Values

Techniques covered include:

- Detecting null values
- Drop missing values
- Fill using Mean
- Fill using Median
- Fill using Mode
- Forward Fill (ffill)
- Backward Fill (bfill)
- Custom replacement values

---

## 🔢 Data Type Conversion

Examples include:

- String → Integer
- String → Float
- Object → Datetime
- Integer → Category
- Boolean Conversion

---

## 🧼 String Cleaning

Cleaning text data by:

- Removing leading/trailing spaces
- Removing special characters
- Removing extra spaces
- Converting to lowercase
- Converting to uppercase
- Correcting inconsistent text formatting

Example:

```python
df["city"] = df["city"].str.strip().str.lower()
```

---

## ✨ Handling Special Characters

Removing unwanted symbols such as:

```
@
#
$
%
&
*
(
)
!
?
```

Using:

```python
str.replace()
regex
```

---

## 📆 Date Cleaning

- Converting to datetime
- Formatting dates
- Extracting:

- Year
- Month
- Day
- Weekday

---

## 🔄 Handling Duplicates

- Detect duplicates
- Remove duplicates
- Keep first occurrence
- Keep last occurrence

---

## 📊 Outlier Detection

Methods include:

- IQR Method
- Z-Score Method
- Box Plot Analysis

---

## 📈 Numerical Data Cleaning

Handling:

- Negative values
- Invalid ranges
- Impossible values
- Incorrect measurements

---

## 🏷️ Categorical Data Cleaning

Handling:

- Inconsistent categories
- Wrong spellings
- Unknown values
- Rare categories

Example:

```
Kolkata
Kolkataa
kolkata
KOLKATA
```

↓

```
Kolkata
```

---

## 🔍 Data Validation

Checking for:

- Invalid emails
- Invalid phone numbers
- Impossible ages
- Duplicate IDs
- Invalid categories

---

## ⚡ Feature Engineering

Basic preprocessing including:

- Splitting columns
- Combining columns
- Creating new features
- Encoding categorical variables

---

## 📦 Exporting Clean Data

Saving cleaned datasets as:

- CSV
- Excel
- Parquet

---

# 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Regular Expressions (Regex)
- Jupyter Notebook

---

# 📂 Repository Structure

```
Data-Cleaning-Tutorial/
│
├── datasets/
│
├── notebooks/
│   ├── Data Cleaning.ipynb
│
├── images/
│
├── README.md
│
└── requirements.txt
```

---

# 🚀 Why Data Cleaning Matters

Data cleaning helps to:

- Improve data quality
- Increase analysis accuracy
- Reduce errors
- Prepare data for Machine Learning
- Produce reliable business insights
- Save time during analysis

---

# 👨‍💻 Who Can Use This Repository?

This repository is useful for:

- Beginners in Python
- Data Analysis learners
- Data Science students
- Machine Learning enthusiasts
- College students
- Interview preparation
- Kaggle practitioners

---

# 🤝 Contributions

Contributions are always welcome.

If you have better techniques, optimization ideas, or additional cleaning methods, feel free to:

- Fork the repository
- Create a new branch
- Commit your changes
- Submit a Pull Request

---

# ⭐ Support

If you found this repository useful, consider giving it a ⭐ on GitHub.

Your support motivates further improvements and more educational content.

---

# 📖 Future Updates

Planned additions include:

- Advanced Missing Value Imputation
- Text Cleaning using NLP
- Fuzzy Matching
- Spell Correction
- Duplicate Detection using Similarity Scores
- Data Validation Rules
- Feature Scaling
- Encoding Techniques
- Automated Data Cleaning Pipelines
- End-to-End Data Preprocessing Projects

---

# 📄 License

This project is licensed under the MIT License.

---

<p align="center">
Made with ❤️ using Python & Pandas
</p>
