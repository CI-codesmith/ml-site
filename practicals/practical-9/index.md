# Practical 9: Support Vector Machines (SVM)

## Objective
Build high-performance classification models using Support Vector Machines.

## Duration
**3-4 hours**

## Prerequisites
- Practicals 1-8 completed
- Understanding of classification

---

## What You'll Learn
- ✅ Understand SVM theory
- ✅ Implement SVM classifier
- ✅ Handle different kernels
- ✅ Tune hyperparameters
- ✅ Visualize decision boundaries

---

## 📋 Tasks

### 1. Build SVM Classifier
```python
from sklearn.svm import SVC

svm = SVC(kernel='rbf', C=1.0, gamma='scale')
svm.fit(X_train, y_train)
```

### 2. Hyperparameter Tuning
```python
from sklearn.model_selection import GridSearchCV

param_grid = {
    'C': [0.1, 1, 10],
    'kernel': ['linear', 'rbf', 'poly'],
    'gamma': ['scale', 'auto']
}

grid = GridSearchCV(SVC(), param_grid, cv=5)
grid.fit(X_train, y_train)
print(f"Best params: {grid.best_params_}")
```

---

## 📊 Learning Outcomes
- [ ] Implement SVM classifiers
- [ ] Understand different kernels
- [ ] Tune C and gamma parameters
- [ ] Evaluate SVM performance
- [ ] Visualize decision boundaries

---

[Next: Practical 10 →](../practical-10/) | [← Back to Practicals](../)
