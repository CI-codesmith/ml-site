# Practical 4: Classification with Logistic Regression

## Objective
Build binary and multi-class classification models using logistic regression.

## Duration
**3-4 hours**

## Prerequisites
- Practicals 1-3 completed
- Understanding of classification

---

## What You'll Learn
- ✅ Implement logistic regression
- ✅ Handle binary and multi-class classification
- ✅ Create confusion matrices
- ✅ Calculate precision, recall, F1-score
- ✅ Plot ROC curves

---

## 📋 Tasks

### 1. Build Classification Model
```python
from sklearn.linear_model import LogisticRegression

model = LogisticRegression(max_iter=1000)
model.fit(X_train, y_train)
y_pred = model.predict(X_test)
```

### 2. Evaluate Classification
```python
from sklearn.metrics import confusion_matrix, classification_report, roc_auc_score

cm = confusion_matrix(y_test, y_pred)
print(classification_report(y_test, y_pred))

auc = roc_auc_score(y_test, model.predict_proba(X_test)[:, 1])
print(f"AUC Score: {auc:.4f}")
```

---

## 📊 Learning Outcomes
- [ ] Build logistic regression classifier
- [ ] Generate confusion matrix
- [ ] Calculate classification metrics
- [ ] Plot ROC curves
- [ ] Interpret results

---

[Next: Practical 5 →](../practical-5/) | [← Back to Practicals](../)
