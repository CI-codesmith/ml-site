# Practical 6: K-Means Clustering

## Objective
Apply K-Means clustering to segment data into meaningful groups.

## Duration
**3-4 hours**

## Prerequisites
- Practicals 1-5 completed
- Understanding of unsupervised learning

---

## What You'll Learn
- ✅ Implement K-Means algorithm
- ✅ Determine optimal number of clusters
- ✅ Use elbow method and silhouette analysis
- ✅ Visualize clusters
- ✅ Interpret clustering results

---

## 📋 Tasks

### 1. Perform K-Means Clustering
```python
from sklearn.cluster import KMeans

kmeans = KMeans(n_clusters=3, random_state=42)
clusters = kmeans.fit_predict(X)
```

### 2. Elbow Method
```python
inertias = []
for k in range(1, 11):
    kmeans = KMeans(n_clusters=k)
    kmeans.fit(X)
    inertias.append(kmeans.inertia_)

plt.plot(range(1, 11), inertias)
plt.xlabel('Number of clusters (k)')
plt.ylabel('Inertia')
plt.show()
```

### 3. Silhouette Analysis
```python
from sklearn.metrics import silhouette_score

for k in range(2, 11):
    kmeans = KMeans(n_clusters=k)
    labels = kmeans.fit_predict(X)
    score = silhouette_score(X, labels)
    print(f"k={k}: {score:.4f}")
```

---

## 📊 Learning Outcomes
- [ ] Apply K-Means clustering
- [ ] Find optimal cluster count
- [ ] Evaluate clustering quality
- [ ] Visualize cluster results
- [ ] Interpret cluster characteristics

---

[Next: Practical 7 →](../practical-7/) | [← Back to Practicals](../)
