# Practical 7: Hierarchical Clustering

## Objective
Understand and apply hierarchical clustering with dendrogram visualization.

## Duration
**3-4 hours**

## Prerequisites
- Practicals 1-6 completed

---

## What You'll Learn
- ✅ Understand linkage methods
- ✅ Perform agglomerative clustering
- ✅ Create and interpret dendrograms
- ✅ Cut dendrograms at optimal height
- ✅ Compare with K-Means

---

## 📋 Tasks

### 1. Hierarchical Clustering
```python
from scipy.cluster.hierarchy import dendrogram, linkage
from sklearn.cluster import AgglomerativeClustering

Z = linkage(X, method='ward')
labels = AgglomerativeClustering(n_clusters=3).fit_predict(X)
```

### 2. Dendrogram Visualization
```python
dendrogram(Z)
plt.xlabel('Sample index')
plt.ylabel('Distance')
plt.show()
```

---

## 📊 Learning Outcomes
- [ ] Apply hierarchical clustering
- [ ] Compare linkage methods
- [ ] Interpret dendrograms
- [ ] Cut dendrograms effectively
- [ ] Compare hierarchical vs K-Means

---

[Next: Practical 8 →](../practical-8/) | [← Back to Practicals](../)
