# Practical 11: Time Series Forecasting

## Objective
Build time series forecasting models for temporal data prediction.

## Duration
**4-5 hours**

## Prerequisites
- Practicals 1-10 completed

---

## What You'll Learn
- ✅ Understand time series components
- ✅ Check for stationarity (ADF test)
- ✅ Build ARIMA models
- ✅ Evaluate forecasts
- ✅ Visualize time series and predictions

---

## 📋 Tasks

### 1. Time Series Exploration
```python
import pandas as pd
from statsmodels.tsa.stattools import adfuller

# Plot time series
plt.plot(ts_data)
plt.show()

# ADF test for stationarity
result = adfuller(ts_data)
print(f'ADF Statistic: {result[0]:.4f}')
```

### 2. ARIMA Model
```python
from statsmodels.tsa.arima.model import ARIMA

model = ARIMA(ts_data, order=(1, 1, 1))
fitted = model.fit()
forecast = fitted.forecast(steps=10)
```

### 3. Evaluate Forecast
```python
from sklearn.metrics import mean_squared_error, mean_absolute_error

mae = mean_absolute_error(test_data, forecast)
rmse = np.sqrt(mean_squared_error(test_data, forecast))
print(f"MAE: {mae:.4f}, RMSE: {rmse:.4f}")
```

---

## 📊 Learning Outcomes
- [ ] Analyze time series data
- [ ] Check stationarity
- [ ] Build ARIMA models
- [ ] Evaluate forecast accuracy
- [ ] Visualize forecasts

---

[Next: Practical 12 →](../practical-12/) | [← Back to Practicals](../)
