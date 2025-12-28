# Practical 13: Ensemble Methods Advanced

## Objective
Implement advanced ensemble techniques for high-performance models.

## Duration
**4-5 hours**

## Prerequisites
- Practicals 1-12 completed

---

## What You'll Learn
- ✅ Implement Gradient Boosting
- ✅ Use XGBoost and LightGBM
- ✅ Understand stacking and voting
- ✅ Combine multiple models
- ✅ Achieve state-of-the-art performance

---

## 📋 Tasks

### 1. Gradient Boosting
```python
from sklearn.ensemble import GradientBoostingClassifier

gb = GradientBoostingClassifier(
    n_estimators=100,
    learning_rate=0.1,
    max_depth=5
)
gb.fit(X_train, y_train)
```

### 2. XGBoost
```python
import xgboost as xgb

xgb_model = xgb.XGBClassifier(
    n_estimators=100,
    max_depth=5,
    learning_rate=0.1
)
xgb_model.fit(X_train, y_train)
```

### 3. Stacking
```python
from sklearn.ensemble import StackingClassifier

base_models = [
    ('rf', RandomForestClassifier()),
    ('svm', SVC()),
    ('lr', LogisticRegression())
]

stacking = StackingClassifier(
    estimators=base_models,
    final_estimator=LogisticRegression()
)
stacking.fit(X_train, y_train)
```

---

## 📊 Learning Outcomes
- [ ] Build Gradient Boosting models
- [ ] Use XGBoost effectively
- [ ] Implement stacking ensembles
- [ ] Compare ensemble methods
- [ ] Achieve high performance

---

[Next: Practical 14 →](../practical-14/) | [← Back to Practicals](../)
