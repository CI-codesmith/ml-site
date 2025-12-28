# Practical 5: Decision Trees & Random Forest

## Objective
Build tree-based classification models and understand ensemble methods.

## Duration
**3-4 hours**

## Prerequisites
- Practicals 1-4 completed

---

## What You'll Learn
- ✅ Understand decision tree construction
- ✅ Implement random forests
- ✅ Handle overfitting with ensemble methods
- ✅ Feature importance analysis
- ✅ Visualize decision trees

---

## 📋 Tasks

### 1. Build Decision Tree
```python
from sklearn.tree import DecisionTreeClassifier

dt = DecisionTreeClassifier(max_depth=5)
dt.fit(X_train, y_train)
```

### 2. Build Random Forest
```python
from sklearn.ensemble import RandomForestClassifier

rf = RandomForestClassifier(n_estimators=100, max_depth=10)
rf.fit(X_train, y_train)
y_pred = rf.predict(X_test)
```

### 3. Feature Importance
```python
importances = rf.feature_importances_
for name, importance in zip(feature_names, importances):
    print(f"{name}: {importance:.4f}")
```

---

## 📊 Learning Outcomes
- [ ] Understand decision tree splitting
- [ ] Build random forest ensemble
- [ ] Compare single tree vs forest performance
- [ ] Analyze feature importance
- [ ] Visualize trees

---

[Next: Practical 6 →](../practical-6/) | [← Back to Practicals](../)
