# Task-1
Simple data cleaning project using Python and Pandas. Handled missing values, removed duplicates, standardized formats, and exported a cleaned dataset. Part of my Data Analyst Internship Task 1.
````markdown
#  Task 1 – Data Cleaning Project (Amazon Dataset)

##  About the Project

This project is a part of my **Data Analyst Internship Task 1**.  
The task was to clean a raw dataset using Python and Pandas in Jupyter Notebook.

I worked on the `amazon.csv` file and cleaned it step-by-step to make it ready for analysis.

---

## Steps I Performed 

### 1. Imported Libraries
I started by importing the necessary Python library — **Pandas** — which is used for data handling.

```python
import pandas as pd
````

---

### 2. Loaded the Dataset

I read the dataset using `read_csv()` to see the raw data.

```python
df = pd.read_csv('amazon.csv')
```

---

### 3. Checked the Data

I used `.head()` to look at the first few rows and understand how the data looks.

```python
df.head()
```

---

### 4. Checked for Missing Values

I used `.isnull().sum()` to find any missing or blank values in the dataset.

```python
df.isnull().sum()
```

Then I removed all rows that had missing values:

```python
df = df.dropna()
```

---

### 5. Removed Duplicate Rows

I used `.drop_duplicates()` to remove any repeated rows.

```python
df = df.drop_duplicates()
```


### 6. Cleaned the Column Names

I made all column names lowercase and replaced spaces with underscores `_` to make them easy to use.

```python
df.columns = df.columns.str.lower().str.strip().str.replace(' ', '_')
```

### Exported the Cleaned Data

Finally, I saved the cleaned dataset to a new file:

```python
df.to_csv('amazon_cleaned.csv', index=False)
```

## What I Learned

* How to clean raw data step-by-step using Pandas
* How to deal with missing and duplicate values
* How to make column names and data more consistent
* How to prepare a dataset for analysis

---

## Tools Used

* Python
* Jupyter Notebook
* Pandas Library
