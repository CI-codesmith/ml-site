# Practical 12: Neural Networks Basics

## Objective
Build and train artificial neural networks using TensorFlow/Keras.

## Duration
**4-5 hours**

## Prerequisites
- Practicals 1-11 completed
- Understanding of deep learning basics

---

## What You'll Learn
- ✅ Build neural networks with Keras
- ✅ Understand activation functions
- ✅ Implement forward and backward propagation
- ✅ Train and evaluate neural networks
- ✅ Visualize network architecture

---

## 📋 Tasks

### 1. Build Sequential Model
```python
import tensorflow as tf
from tensorflow import keras

model = keras.Sequential([
    keras.layers.Dense(128, activation='relu', input_shape=(10,)),
    keras.layers.Dropout(0.2),
    keras.layers.Dense(64, activation='relu'),
    keras.layers.Dense(1, activation='sigmoid')
])

model.compile(
    optimizer='adam',
    loss='binary_crossentropy',
    metrics=['accuracy']
)
```

### 2. Train Model
```python
history = model.fit(
    X_train, y_train,
    epochs=20,
    batch_size=32,
    validation_split=0.2
)
```

### 3. Evaluate
```python
loss, accuracy = model.evaluate(X_test, y_test)
print(f"Test accuracy: {accuracy:.4f}")

predictions = model.predict(X_test)
```

---

## 📊 Learning Outcomes
- [ ] Design neural network architecture
- [ ] Understand layers and activation functions
- [ ] Train deep learning models
- [ ] Handle overfitting with dropout
- [ ] Evaluate neural networks

---

[Next: Practical 13 →](../practical-13/) | [← Back to Practicals](../)
