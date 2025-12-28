# Practical 1: Python Foundations & Environment Setup

## Objective
Set up a complete machine learning environment and verify that all necessary tools are installed and working correctly.

## Duration
**2-3 hours** (including downloads and installation)

## Prerequisites
- Computer with Windows, macOS, or Linux
- Internet connection
- Administrator access (for software installation)

---

## What You'll Learn
- ✅ Install Python and Anaconda
- ✅ Set up virtual environments
- ✅ Install essential ML libraries (NumPy, Pandas, Scikit-learn)
- ✅ Configure Jupyter Notebook
- ✅ Verify installation with test programs

---

## 📋 Lab Guide

### Step 1: Install Python
1. Download Python 3.10+ from [python.org](https://www.python.org/downloads/)
2. Run the installer
3. **Important:** Check "Add Python to PATH"
4. Verify: Open terminal and run `python --version`

### Step 2: Install Anaconda (Recommended)
1. Download Anaconda from [anaconda.com](https://www.anaconda.com/download)
2. Run the installer
3. Follow the installation wizard
4. Verify: Run `conda --version` in terminal

### Step 3: Create Virtual Environment
```bash
conda create -n ml_env python=3.10
conda activate ml_env
```

### Step 4: Install Essential Libraries
```bash
conda install numpy pandas scikit-learn matplotlib seaborn jupyter
# OR using pip:
pip install numpy pandas scikit-learn matplotlib seaborn jupyter
```

### Step 5: Test Installation
```bash
python test_installation.py
```

---

## 💻 Sample Code

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

# NumPy test
arr = np.array([1, 2, 3, 4, 5])
print(f"NumPy array: {arr}")
print(f"Mean: {arr.mean()}")

# Pandas test
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})
print("\nPandas DataFrame:")
print(df)

# Matplotlib test
plt.plot([1, 2, 3, 4], [1, 4, 2, 3])
plt.title("Test Plot")
plt.xlabel("X-axis")
plt.ylabel("Y-axis")
plt.savefig("test_plot.png")
print("\nPlot saved as test_plot.png")
```

---

## 📝 Jupyter Notebook

Launch Jupyter Notebook:
```bash
jupyter notebook
```

Then access it at `http://localhost:8888`

---

## 📊 Learning Outcomes
- [ ] Python installed and working
- [ ] Virtual environment created
- [ ] All libraries imported successfully
- [ ] First NumPy, Pandas, and Matplotlib operations completed
- [ ] Jupyter Notebook launched and working

---

## 🔗 Resources
- [Installation Guide](../../resources/installation-guide.md)
- [Quick Start Guide](../../resources/quick-start.md)
- [Python Basics](../../resources/python-basics.md)

---

## 📥 Submission
- [ ] Screenshot of `python --version` output
- [ ] Output of test_installation.py
- [ ] First Jupyter notebook with above code

---

[Next: Practical 2 →](../practical-2/) | [Back to Practicals](../)
