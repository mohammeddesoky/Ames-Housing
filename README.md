# 📘 Linear Regression Models Comparison

This project demonstrates and compares different types of **Linear Regression models** using Python and scikit-learn.  
It includes data preprocessing, model training, evaluation (using R² and RMSE), and performance comparison for all models.

---

## 🚀 Models Covered

### 1️⃣ Simple Linear Regression
- **Description:** Models the relationship between a single independent variable (X) and a dependent variable (y).
- **Formula:** `y = b0 + b1*x`
- **Regularization:** ❌ None  
- **Use Case:** When there is only one feature affecting the target variable.

---

### 2️⃣ Multiple Linear Regression
- **Description:** Extends simple linear regression to multiple features.
- **Formula:** `y = b0 + b1*x1 + b2*x2 + ... + bn*xn`
- **Regularization:** ❌ None  
- **Use Case:** When several independent variables influence the target.

---

### 3️⃣ Ridge Regression (L2 Regularization)
- **Description:** A linear model that adds a penalty equal to the **square of the magnitude of coefficients**.  
- **Penalty Term:** `α * Σ(bi²)`
- **Effect:** Shrinks large coefficients but does **not** make them zero.  
- **Regularization:** ✅ L2  
- **Use Case:** When the dataset has multicollinearity or risk of overfitting.

---

### 4️⃣ Lasso Regression (L1 Regularization)
- **Description:** Adds a penalty equal to the **absolute value of the magnitude of coefficients**.  
- **Penalty Term:** `α * Σ|bi|`
- **Effect:** Can shrink some coefficients completely to **zero**, effectively performing **feature selection**.  
- **Regularization:** ✅ L1  
- **Use Case:** When you want both regularization and automatic feature selection.

---

### 5️⃣ Elastic Net Regression
- **Description:** Combines both L1 (Lasso) and L2 (Ridge) penalties.  
- **Penalty Term:** `α * (l1_ratio * Σ|bi| + (1 - l1_ratio) * Σ(bi²))`
- **Effect:** Balances between Ridge’s stability and Lasso’s feature selection.  
- **Regularization:** ✅ L1 + L2  
- **Use Case:** When features are correlated and both shrinkage & selection are important.

---

## ⚙️ Workflow

1. **Data Preprocessing**
   - Handle missing values (`dropna`, `fillna`)
   - Remove outliers using boxplots
   - Encode categorical variables (One-Hot Encoding)
   - Feature scaling (`StandardScaler`)

2. **Model Training**
   - Train each regression model separately using scikit-learn.

3. **Evaluation Metrics**
   - **R² Score:** Measures how well the model explains the variance in data.
   - **RMSE (Root Mean Squared Error):** Measures prediction error magnitude.

4. **Comparison**
   - Display R² and RMSE results for all models in a single table to compare performance.

---

## 🧪 Experiment Results

The models were trained and evaluated on the **House Prices (Diabetes/Custom)** dataset using the same preprocessing and train-test split.  
Below are the actual performance results obtained from this project:

### 📊 Performance Comparison

| Model | R² Score | RMSE |
|--------|-----------|--------|
| Linear Regression | 0.894077 | 29,141.76 |
| Ridge Regression | 0.894491 | 29,084.80 |
| Lasso Regression | 0.894816 | 29,039.89 |
| Elastic Net Regression | **0.894855** | **29,034.49** |

### 🧠 Interpretation
- All models performed quite similarly, showing a strong linear relationship.  
- **Elastic Net Regression** achieved the **highest R² Score** and the **lowest RMSE**, indicating slightly better performance.  
- The improvement margins are small, suggesting the dataset fits well with standard Linear Regression, but **regularization** still helps fine-tune stability and reduce overfitting.

---

## 🧠 Key Takeaways
- **Ridge** helps reduce overfitting.
- **Lasso** can remove irrelevant features.
- **Elastic Net** combines both advantages.
- Always **scale your data** before applying any regularized regression model.

---

## 🧩 Technologies Used
- Python 🐍  
- pandas, numpy  
- scikit-learn  
- matplotlib, seaborn  

---
