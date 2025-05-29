# 🌾 MLP Crop Yield Forecasting

This project implements a **multilayer perceptron (MLP)** model to forecast **next-year crop yields** using satellite-derived environmental and land cover data. Developed as part of a Machine Learning coursework project, it predicts yields at a country–crop level based on soil moisture, temperature, vegetation, precipitation, and other geospatial features.

> 📍 **Final RMSE:** 2,683.83 | **MAE:** 1,030.73 | **Pearson r:** 0.985  
> ✅ Trained and evaluated using temporally split data (2010–2021) for realistic forecasting.

---

## 🔍 Key Features

- **Neural Network:** 2 hidden layers (64, 64) with ReLU activations
- **Inputs:** Annual summaries of soil moisture, temperature, vegetation, precipitation, snow, land cover, and previous yield
- **Temporal Generalization:** Train–val–test split by year (train: 2010–2017, val: 2018–2019, test: 2020–2021)
- **Grid Search:** 216 model configurations tested with 3-fold CV
- **Regularisation:** L2 weight decay, early stopping, and dropout-free stable training
- **Evaluation Metrics:** RMSE, MAE, Pearson correlation on hold-out test data

---

## 📊 Results

| Metric      | Value    |
| ----------- | -------- |
| RMSE        | 2,683.83 |
| MAE         | 1,030.73 |
| Pearson's r | 0.985    |
| Mean Yield  | 9,800.8  |

- Most predictions fall within 10% of actual yield.
- Minimal bias and tight residual distribution.
- Highest predictive accuracy for maize, wheat, and soybean crops.

---

## 🧠 Model Details

- **Framework**: scikit-learn `MLPRegressor`
- **Optimizer**: Adam
- **Activation**: ReLU / Tanh
- **Loss Function**: Mean Squared Error (MSE) + L2 penalty
- **Early Stopping**: Monitors validation loss (patience: 20)

---

## 📦 Dependencies

```bash
scikit-learn
numpy
pandas
matplotlib
seaborn


```
