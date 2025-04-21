# 📊 Linear Regression Analysis in R

This project demonstrates a **Linear Regression Analysis** performed in R using a dataset related to advertising spend and product sales. The goal is to understand how different types of marketing (TV, Social Media, and Radio) affect **Sales**, and to evaluate the model's performance using metrics like RMSE, MAE, and regression accuracy.

---

### 🔧 Technologies Used
- R
- RStudio / Jupyter Notebook
- Packages: `dplyr`, `caTools`, `ggplot2`, `broom`

---

### 📁 Dataset
The dataset (`Dummy Data HSS.csv`) contains the following columns:
- `TV` – advertising budget spent on TV
- `Social.Media` – budget on social media platforms
- `Radio` – radio ad spend
- `Sales` – resulting product sales

---

### 📈 Workflow
1. **Data Preprocessing**: Loaded CSV data and checked for null values.
2. **Data Splitting**: Split data into training and testing sets using `caTools`.
3. **Model Building**:
   - Simple Linear Regression: `Sales ~ TV`
   - Multiple Linear Regression: `Sales ~ TV + Social.Media + Radio`
4. **Model Evaluation**:
   - RMSE: `3.0365`
   - MAE: `2.4315`
   - Regression Accuracy: `98.19984` *(calculated using MAPE)*

---

### 📌 Accuracy Calculation (Regression)
Although accuracy is more common in classification, here it's estimated using **MAPE**:

```r
mape <- mean(abs((predictions - actuals) / actuals)) * 100
accuracy <- 100 - mape
```

---

### 📊 Conclusion
The multiple linear regression model shows a decent performance with RMSE and MAE within acceptable limits. Further improvements can be made by exploring feature engineering or using regularization techniques like Ridge/Lasso.

---

### 📂 How to Run
1. Open the notebook in RStudio or Jupyter.
2. Make sure the CSV file is in the same directory.
3. Run all cells to see outputs and evaluation metrics.

---
