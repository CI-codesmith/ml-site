# Installation & Environment Setup

## System Requirements

- **Python:** 3.8 or higher
- **RAM:** 4GB minimum (8GB recommended)
- **Disk Space:** 5GB free space
- **OS:** Windows, macOS, or Linux

---

## Step 1: Install Python

### macOS
```bash
# Using Homebrew
brew install python3
```

### Windows
1. Download from [python.org](https://www.python.org/downloads/)
2. Run installer
3. ✅ Check "Add Python to PATH"
4. Click "Install Now"

### Linux
```bash
# Ubuntu/Debian
sudo apt-get update
sudo apt-get install python3 python3-pip

# Fedora
sudo dnf install python3 python3-pip
```

**Verify installation:**
```bash
python --version
pip --version
```

---

## Step 2: Install Anaconda (Recommended)

Anaconda includes Python and all essential data science libraries.

1. Download from [anaconda.com](https://www.anaconda.com/download)
2. Run installer
3. Follow prompts
4. Verify: `conda --version`

---

## Step 3: Create Virtual Environment

### Using Anaconda
```bash
# Create environment
conda create -n ml_env python=3.10

# Activate
conda activate ml_env
```

### Using venv (Python native)
```bash
# Create environment
python -m venv ml_env

# Activate
# On macOS/Linux:
source ml_env/bin/activate
# On Windows:
ml_env\Scripts\activate
```

---

## Step 4: Install Required Libraries

### Install all at once
```bash
pip install numpy pandas scikit-learn matplotlib seaborn jupyter tensorflow keras xgboost lightgbm
```

### Or install from requirements.txt
```bash
pip install -r requirements.txt
```

**requirements.txt:**
```
numpy==1.24.3
pandas==2.0.3
scikit-learn==1.3.0
matplotlib==3.7.2
seaborn==0.12.2
jupyter==1.0.0
tensorflow==2.13.0
keras==2.13.0
xgboost==2.0.0
lightgbm==4.0.0
statsmodels==0.14.0
scipy==1.11.2
```

---

## Step 5: Launch Jupyter Notebook

```bash
jupyter notebook
```

Opens at: `http://localhost:8888`

---

## Step 6: Verify Installation

Create a test file `test_installation.py`:

```python
import sys
print(f"Python: {sys.version}")

import numpy as np
print(f"NumPy: {np.__version__}")

import pandas as pd
print(f"Pandas: {pd.__version__}")

import sklearn
print(f"Scikit-learn: {sklearn.__version__}")

import matplotlib
print(f"Matplotlib: {matplotlib.__version__}")

import tensorflow
print(f"TensorFlow: {tensorflow.__version__}")

print("\n✅ All libraries installed successfully!")
```

Run:
```bash
python test_installation.py
```

---

## Troubleshooting

### Issue: Python not found
**Solution:** Add Python to PATH
- Windows: Edit environment variables
- macOS/Linux: Check installation in /usr/local/bin/python3

### Issue: pip command not found
**Solution:** Use python -m pip
```bash
python -m pip install package_name
```

### Issue: Permission denied
**Solution:** Use sudo (macOS/Linux) or run PowerShell as admin (Windows)
```bash
sudo pip install package_name
```

### Issue: TensorFlow installation slow
**Solution:** Install CPU version first
```bash
pip install tensorflow-cpu
```

---

## IDE Setup

### VS Code
1. Download [VS Code](https://code.visualstudio.com/)
2. Install Python extension
3. Select Python interpreter (ml_env)
4. Create `.py` files and run

### PyCharm
1. Download [PyCharm Community](https://www.jetbrains.com/pycharm/)
2. Create new project
3. Set interpreter to ml_env

### Jupyter Lab (Advanced)
```bash
pip install jupyterlab
jupyter lab
```

---

## Next Steps

1. Complete [Practical 1](../practicals/practical-1/)
2. Review [Quick Start Guide](quick-start.md)
3. Explore [Python Basics](python-basics.md)

---

[← Back to Resources](index.md)
