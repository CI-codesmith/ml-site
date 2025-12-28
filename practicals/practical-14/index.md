# Practical 14: Real-World Project - Part 1 (Data & Preprocessing)

## Objective
Work on a complete real-world machine learning project from data collection to deployment.

**Part 1 focuses on data gathering, cleaning, and preprocessing.**

## Duration
**5-6 hours**

## Prerequisites
- Practicals 1-13 completed
- All ML concepts understood

---

## Project Options

Choose one of these real-world problems:

### Option 1: Customer Churn Prediction
- Predict which customers will leave
- Prepare customer behavior data
- Handle imbalanced classes

### Option 2: House Price Prediction
- Predict house prices based on features
- Clean real estate data
- Handle missing values and outliers

### Option 3: Disease Diagnosis
- Predict disease presence from medical data
- Handle sensitive health information
- Address ethical concerns

### Option 4: Sentiment Analysis
- Classify text sentiment
- Preprocess text data
- Handle NLP-specific challenges

---

## 📋 Tasks for Part 1

### 1. Data Collection & Understanding
```python
# Load data
df = pd.read_csv('your_dataset.csv')

# Explore
print(df.head())
print(df.info())
print(df.describe())
print(df.isnull().sum())
```

### 2. Data Cleaning
```python
# Handle missing values
df.dropna(subset=['critical_column'], inplace=True)
df.fillna(df.median(), inplace=True)

# Remove duplicates
df.drop_duplicates(inplace=True)

# Handle outliers
Q1 = df.quantile(0.25)
Q3 = df.quantile(0.75)
# ... outlier removal code
```

### 3. Feature Engineering
```python
# Create new features
df['new_feature'] = df['col1'] * df['col2']

# Encode categorical variables
df = pd.get_dummies(df, columns=['category_col'])

# Normalize features
from sklearn.preprocessing import StandardScaler
scaler = StandardScaler()
df_scaled = scaler.fit_transform(df)
```

### 4. Data Visualization & Analysis
```python
# Visualizations
df.hist(figsize=(15, 10))
plt.show()

# Correlation matrix
import seaborn as sns
sns.heatmap(df.corr(), annot=True)
plt.show()
```

---

## 📊 Deliverables for Part 1
- [ ] Cleaned dataset (CSV)
- [ ] Data exploration report with visualizations
- [ ] Feature engineering documentation
- [ ] Jupyter notebook with all code
- [ ] Summary of data characteristics

---

## 📊 Learning Outcomes
- [ ] Collect and load real-world data
- [ ] Perform comprehensive EDA
- [ ] Clean and preprocess data
- [ ] Engineer meaningful features
- [ ] Document data preparation process

---

[Next: Practical 15 →](../practical-15/) | [← Back to Practicals](../)
