# 🏠 Ames Housing Price Prediction using Linear & Ridge Regression

## 📌 Project Overview
This project builds a **robust machine learning regression pipeline** to predict house prices using the **Ames Housing dataset**.  
The focus is not just on accuracy, but on **correct ML workflow**, including preprocessing, pipelines, regularization, and cross-validation.

A baseline **Linear Regression** model is first established, followed by a **Ridge Regression model with hyperparameter tuning** to handle multicollinearity and improve generalization.

---

## 🎯 Objective
- Predict house sale prices accurately  
- Compare **baseline Linear Regression** with **regularized Ridge Regression**  
- Apply **industry-standard ML practices**:
  - Pipelines  
  - Proper train–test split  
  - Cross-validation  
  - Hyperparameter tuning  
  - Leakage-free preprocessing  

---

## 📂 Dataset
- **Dataset**: Ames Housing Dataset  
- **Target variable**: `SalePrice`  
- **Features**:
  - Numerical: house size, quality, year built, etc.  
  - Categorical: neighborhood, exterior type, garage features, etc.  

The dataset contains **mixed feature types** and **high multicollinearity**, making it ideal for regularized linear models.

---

## 🛠️ Tools & Libraries
- Python  
- Pandas, NumPy  
- Scikit-learn  
- Jupyter Notebook  

---

## ⚙️ Methodology & Workflow

### 1️⃣ Exploratory Data Analysis (Minimal & ML-Focused)
- Checked data shape, types, and summary statistics  
- Identified numerical and categorical features  
- Analyzed missing values and categorical levels  
- Avoided unnecessary visual EDA  

---

### 2️⃣ Data Preprocessing
- Categorical features handled using **One-Hot Encoding**  
- Numerical features scaled using **StandardScaler**  
- Preprocessing performed using **ColumnTransformer**  
- Entire preprocessing wrapped inside a **Pipeline** to avoid data leakage  

---

### 3️⃣ Train–Test Split
- 80% training, 20% testing  
- Fixed `random_state` for reproducibility  
- Test set used **only once** for final evaluation  

---

### 4️⃣ Baseline Model: Linear Regression
- Built using a full preprocessing pipeline  
- Purpose:
  - Sanity check  
  - Performance benchmark  

**Baseline Performance**
- **R² ≈ 0.89**  
- **RMSE ≈ 28,000**  

This confirms correct preprocessing and strong linear relationships in the data.

---

### 5️⃣ Final Model: Ridge Regression with Cross-Validation
- Ridge regression chosen to handle **multicollinearity**  
- Hyperparameter `alpha` tuned using **GridSearchCV (5-fold CV)**  
- Model selection based only on training data  

**Why Ridge?**
- Stabilizes coefficients  
- Reduces overfitting  
- Improves robustness with correlated features  

---

## 📊 Model Evaluation Metrics
- **R² Score** – goodness of fit  
- **RMSE** – interpretable prediction error in price units  

Ridge regression achieved **comparable or slightly improved performance** compared to the baseline while offering better generalization.

---

## ✅ Final Conclusion
- Linear Regression provided a strong baseline  
- Ridge Regression was selected as the **final model** due to:
  - Regularization  
  - Cross-validated hyperparameter selection  
  - Better stability in the presence of multicollinearity  

> Even when accuracy gains are modest, Ridge Regression is preferred for real-world robustness.

---

## 📁 Project Structure
```
├── Ames_housing_model1.ipynb
├── AmesHousing.csv
├── README.md
```

---

## 🚀 Key Learnings
- Importance of **pipelines** in preventing data leakage  
- Correct usage of **GridSearchCV with pipelines**  
- Why regularization matters even when baseline models perform well  
- Proper evaluation workflow in supervised ML  

---

## 📌 Future Improvements (Optional)
- Try ElasticNet for combined L1/L2 regularization  
- Analyze and interpret top Ridge coefficients  
- Add feature importance stability comparison  
- Deploy model using a simple API  

---

## 👤 Author
**Rahul Maheshwari**  
Aspiring Data Scientist / Machine Learning Engineer
