# Practical 2: Data Cleaning & Exploratory Data Analysis (EDA)

## Objective
Learn to clean real-world datasets and perform comprehensive exploratory data analysis to understand data characteristics.

## Duration
**3-4 hours**

## Prerequisites
- Practical 1 completed (Python environment set up)
- Basic Python knowledge

---

## What You'll Learn
- ✅ Handle missing values
- ✅ Detect and treat outliers
- ✅ Perform exploratory data analysis
- ✅ Create meaningful visualizations
- ✅ Generate statistical summaries

---

## 📊 Dataset
Use the Iris or Titanic dataset (provided)

---

## 📋 Key Tasks

### 1. Load and Explore Data
```python
import pandas as pd
df = pd.read_csv('dataset.csv')
print(df.head())
print(df.info())
print(df.describe())
```

### 2. Handle Missing Values
```python
# Check for missing values
print(df.isnull().sum())

# Fill missing values
df.fillna(df.mean(), inplace=True)  # For numerical
df.fillna(df.mode()[0], inplace=True)  # For categorical
```

### 3. Detect Outliers
```python
import numpy as np
Q1 = df.quantile(0.25)
Q3 = df.quantile(0.75)
IQR = Q3 - Q1
outliers = ((df < (Q1 - 1.5*IQR)) | (df > (Q3 + 1.5*IQR))).sum()
print(outliers)
```

### 4. Create Visualizations
```python
import matplotlib.pyplot as plt
df.hist(bins=20)
plt.show()

df.plot(kind='box')
plt.show()
```

---

## 📊 Learning Outcomes
- [ ] Load data from CSV/Excel files
- [ ] Understand data structure and types
- [ ] Identify and handle missing values
- [ ] Detect and treat outliers
- [ ] Create effective visualizations
- [ ] Generate statistical insights

---

## 💾 Deliverables
- Cleaned dataset (CSV)
- EDA report with visualizations
- Statistical summary
- Jupyter notebook with complete code

---

[Next: Practical 3 →](../practical-3/) | [← Back to Practicals](../)
