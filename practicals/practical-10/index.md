# Practical 10: Model Comparison & Selection

## Objective
Compare multiple algorithms and select the best model for a given problem.

## Duration
**4-5 hours**

## Prerequisites
- Practicals 1-9 completed

---

## What You'll Learn
- ✅ Compare multiple algorithms
- ✅ Use cross-validation properly
- ✅ Create comparison metrics
- ✅ Visualize performance comparisons
- ✅ Make informed model selection

---

## 📋 Tasks

### 1. Compare Multiple Models
```python
from sklearn.linear_model import LogisticRegression
from sklearn.tree import DecisionTreeClassifier
from sklearn.ensemble import RandomForestClassifier
from sklearn.svm import SVC

models = {
    'Logistic Regression': LogisticRegression(),
    'Decision Tree': DecisionTreeClassifier(),
    'Random Forest': RandomForestClassifier(),
    'SVM': SVC()
}

results = {}
for name, model in models.items():
    model.fit(X_train, y_train)
    score = model.score(X_test, y_test)
    results[name] = score
    print(f"{name}: {score:.4f}")
```

### 2. Cross-Validation
```python
from sklearn.model_selection import cross_val_score

for name, model in models.items():
    scores = cross_val_score(model, X, y, cv=5)
    print(f"{name}: {scores.mean():.4f} (+/- {scores.std():.4f})")
```

---

## 📊 Learning Outcomes
- [ ] Compare multiple algorithms fairly
- [ ] Use proper cross-validation
- [ ] Create comparison visualizations
- [ ] Make data-driven model selection
- [ ] Document comparison results

---

[Next: Practical 11 →](../practical-11/) | [← Back to Practicals](../)
