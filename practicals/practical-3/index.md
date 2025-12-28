# Practical 3: Linear Regression

## Objective
Build, train, and evaluate linear regression models for predicting continuous values.

## Duration
**3-4 hours**

## Prerequisites
- Practicals 1-2 completed
- Understanding of supervised learning

---

## What You'll Learn
- ✅ Implement linear regression from scratch
- ✅ Use Scikit-learn for regression
- ✅ Evaluate model performance
- ✅ Interpret coefficients
- ✅ Visualize regression results

---

## 📋 Tasks

### 1. Build Simple Linear Regression
```python
from sklearn.linear_model import LinearRegression
from sklearn.model_selection import train_test_split

X = data[['feature1', 'feature2']].values
y = data['target'].values

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)

model = LinearRegression()
model.fit(X_train, y_train)
```

### 2. Evaluate Model
```python
from sklearn.metrics import mean_squared_error, r2_score

y_pred = model.predict(X_test)
mse = mean_squared_error(y_test, y_pred)
rmse = np.sqrt(mse)
r2 = r2_score(y_test, y_pred)

print(f"MSE: {mse:.4f}")
print(f"RMSE: {rmse:.4f}")
print(f"R² Score: {r2:.4f}")
```

---

## 📊 Learning Outcomes
- [ ] Understand linear regression theory
- [ ] Implement regression model
- [ ] Split data properly
- [ ] Evaluate using MSE, RMSE, R²
- [ ] Visualize predictions vs actual
- [ ] Interpret model coefficients

---

[Next: Practical 4 →](../practical-4/) | [← Back to Practicals](../)
