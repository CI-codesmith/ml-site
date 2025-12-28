# Quick Start Guide

Get up and running with your first ML program in 30 minutes.

---

## Minute 1-5: Prepare Your Environment

```bash
# Activate virtual environment
conda activate ml_env

# Create a new directory
mkdir my_first_ml_project
cd my_first_ml_project

# Create Jupyter notebook
jupyter notebook
```

---

## Minute 6-15: Load and Explore Data

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

# Load sample dataset
from sklearn.datasets import load_iris
iris = load_iris()
df = pd.DataFrame(iris.data, columns=iris.feature_names)
df['target'] = iris.target

# Quick exploration
print(df.head())
print(df.describe())
print(df.shape)

# Visualization
df.hist(figsize=(10, 8))
plt.show()
```

---

## Minute 16-25: Build Your First Model

```python
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import accuracy_score, classification_report

# Prepare data
X = df.drop('target', axis=1)
y = df['target']
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Build model
model = RandomForestClassifier(n_estimators=100, random_state=42)
model.fit(X_train, y_train)

# Make predictions
y_pred = model.predict(X_test)

# Evaluate
accuracy = accuracy_score(y_test, y_pred)
print(f"Accuracy: {accuracy:.2%}")
print(classification_report(y_test, y_pred))
```

---

## Minute 26-30: Interpret Results

```python
# Feature importance
feature_importance = model.feature_importances_
for name, importance in zip(iris.feature_names, feature_importance):
    print(f"{name}: {importance:.4f}")

# Make single prediction
sample = [[5.1, 3.5, 1.4, 0.2]]
prediction = model.predict(sample)
probability = model.predict_proba(sample)
print(f"Prediction: {prediction}")
print(f"Confidence: {probability}")
```

---

## What You've Learned

✅ Load a dataset  
✅ Explore data with pandas  
✅ Build a classification model  
✅ Evaluate model performance  
✅ Make predictions  

---

## Next Steps

1. **[Practical 1](../practicals/practical-1/)** - Environment setup (detailed)
2. **[Unit 1](../units/unit-1/)** - Learn theory
3. **[Practical 2](../practicals/practical-2/)** - Data cleaning

---

## Common Next Questions

**Q: How do I use my own data?**
```python
df = pd.read_csv('my_data.csv')
# Then follow the same steps
```

**Q: How do I save my model?**
```python
import pickle
with open('my_model.pkl', 'wb') as f:
    pickle.dump(model, f)
```

**Q: How do I use different algorithms?**
Check [Unit 2](../units/unit-2/) for logistic regression, SVM, decision trees, etc.

---

[← Back to Resources](index.md)
