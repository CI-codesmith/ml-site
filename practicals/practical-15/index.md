# Practical 15: Real-World Project - Part 2 (Deployment)

## Objective
Complete the real-world ML project by building, evaluating, and deploying the final model.

**Part 2 focuses on model building, evaluation, and production deployment.**

## Duration
**5-6 hours**

## Prerequisites
- Practical 14 completed
- Clean, preprocessed dataset ready

---

## 📋 Tasks for Part 2

### 1. Model Building & Comparison
```python
# Build multiple models
models = {
    'Random Forest': RandomForestClassifier(),
    'Gradient Boosting': GradientBoostingClassifier(),
    'XGBoost': xgb.XGBClassifier(),
    'Neural Network': keras.Sequential([...])
}

# Train and evaluate
best_score = 0
best_model = None

for name, model in models.items():
    model.fit(X_train, y_train)
    score = model.score(X_test, y_test)
    print(f"{name}: {score:.4f}")
    
    if score > best_score:
        best_score = score
        best_model = model
```

### 2. Model Evaluation
```python
# Comprehensive evaluation
from sklearn.metrics import classification_report, confusion_matrix

y_pred = best_model.predict(X_test)
print(classification_report(y_test, y_pred))
print(confusion_matrix(y_test, y_pred))

# Cross-validation
cv_scores = cross_val_score(best_model, X, y, cv=5)
print(f"CV Score: {cv_scores.mean():.4f}")
```

### 3. Save Model
```python
import pickle

# Save model
with open('best_model.pkl', 'wb') as f:
    pickle.dump(best_model, f)

# Load model
with open('best_model.pkl', 'rb') as f:
    loaded_model = pickle.load(f)
```

### 4. Create API (Flask)
```python
from flask import Flask, request, jsonify
import pickle

app = Flask(__name__)

# Load model
with open('best_model.pkl', 'rb') as f:
    model = pickle.load(f)

@app.route('/predict', methods=['POST'])
def predict():
    data = request.json
    features = [data['feature1'], data['feature2'], ...]
    prediction = model.predict([features])
    return jsonify({'prediction': int(prediction[0])})

if __name__ == '__main__':
    app.run(debug=True)
```

### 5. Deploy to Cloud (Optional)
```bash
# Using Heroku
heroku login
heroku create your-app-name
git push heroku main
```

---

## 📊 Deliverables for Part 2
- [ ] Trained and saved model
- [ ] Complete evaluation report
- [ ] Flask API code
- [ ] Deployment instructions
- [ ] Project documentation

---

## 📊 Final Project Components
- [ ] Data collection & preprocessing (Part 1)
- [ ] Model building & evaluation (Part 2)
- [ ] Complete documentation
- [ ] Working API or deployment
- [ ] Performance metrics and results
- [ ] Ethical considerations addressed
- [ ] Future improvements documented

---

## 🏆 Course Completion

After completing Practical 15, you have:
✅ Mastered ML fundamentals and advanced techniques  
✅ Completed 15 hands-on practical labs  
✅ Built a production-ready ML system  
✅ Deployed models to real environments  
✅ Applied ethical ML principles  

---

## 📝 Final Assessment

- [ ] All 15 practicals completed
- [ ] Weekly Tests 1-5 passed
- [ ] Class Tests 1-2 passed
- [ ] Preliminary Exam completed
- [ ] Real-world project deployed

---

**Congratulations on completing the Machine Learning course!**

[← Back to Practicals](../) | [← Home](../../)
