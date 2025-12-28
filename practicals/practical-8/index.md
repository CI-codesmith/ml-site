# Practical 8: PCA for Dimensionality Reduction

## Objective
Reduce data dimensionality while preserving important information.

## Duration
**3-4 hours**

## Prerequisites
- Practicals 1-7 completed

---

## What You'll Learn
- ✅ Understand principal component analysis
- ✅ Implement PCA
- ✅ Determine optimal number of components
- ✅ Visualize reduced data
- ✅ Interpret explained variance

---

## 📋 Tasks

### 1. Apply PCA
```python
from sklearn.decomposition import PCA
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()
X_scaled = scaler.fit_transform(X)

pca = PCA(n_components=2)
X_reduced = pca.fit_transform(X_scaled)
```

### 2. Explained Variance
```python
print(f"Explained variance: {pca.explained_variance_ratio_}")
print(f"Cumulative: {np.cumsum(pca.explained_variance_ratio_)}")

plt.plot(np.cumsum(pca.explained_variance_ratio_))
plt.xlabel('Number of components')
plt.ylabel('Cumulative explained variance')
plt.show()
```

---

## 📊 Learning Outcomes
- [ ] Standardize features
- [ ] Apply PCA transformation
- [ ] Determine component count
- [ ] Visualize PCA results
- [ ] Interpret explained variance

---

[Next: Practical 9 →](../practical-9/) | [← Back to Practicals](../)
