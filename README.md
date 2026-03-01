# 🎓 Student Performance Analysis & Prediction

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white"/>
  <img src="https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white"/>
</p>

---

## 📌 Project Overview

Understanding what drives student success is essential for improving educational outcomes.

This project analyzes **6,600+ student records** to uncover the key factors influencing academic performance and builds **predictive models** to estimate final exam scores.

The workflow follows a complete **data science pipeline**, from data cleaning and exploratory analysis to model building and evaluation.

---

## 🎯 Objectives

- 🔍 **Analyze Relationships**  
  Explore how factors like study habits, attendance, and past performance impact student outcomes.

- 📊 **Identify Key Drivers**  
  Determine the most influential features affecting exam scores.

- 🤖 **Build Predictive Models**  
  Compare multiple regression algorithms to identify the most accurate model.

---

## ⚙️ Data Preprocessing & Cleaning

Ensuring high-quality data was a critical first step:

- ✅ **Target Cleaning**  
  Removed unrealistic records where `Exam_Score > 100`.

- 🧹 **Handling Missing Values**  
  Categorical features such as:
  - `Teacher_Quality`
  - `Parental_Education_Level`
  - `Distance_from_Home`  
  were imputed using the **mode** to preserve distribution.

- 🔍 **Data Integrity Checks**  
  Verified that no duplicate records exist.

---

## 📈 Exploratory Data Analysis (EDA)

Key patterns were identified through visualization and statistical analysis:

- 📊 **Score Distribution**  
  Most students score between **60–70**.

- 🔗 **Feature Relationships**
  - **Attendance** → strongest positive correlation (~0.58)
  - **Hours Studied** → second strongest (~0.45)
  - **Previous Scores** → strong linear relationship with final scores

- 📉 **Outliers & Trends**  
  Boxplots and correlation heatmaps were used to detect anomalies and patterns.

---

## 🤖 Model Performance: Exam Score Prediction

Models were evaluated using **R² (coefficient of determination)** to measure how well they explain variance in exam scores.

| Model | R² Score | Insights |
|------|--------|---------|
| **Linear Regression** | **0.83** | Best performer; captures dominant linear relationships |
| **Ridge Regression** | 0.83 | Regularization had no effect due to stable features |
| **ElasticNet** | 0.78 | Slight drop due to coefficient shrinkage |
| **Random Forest** | 0.73 | Captures non-linearity but underperforms |
| **Random Forest (Tuned)** | 0.73 | More stable, but no significant improvement |
| **XGBoost** | 0.70 | Slight overfitting, fails to outperform linear models |

---

## 🔍 Key Insights

### 1️⃣ Linearity Dominates
Features such as **Attendance, Hours Studied, and Previous Scores** have strong linear relationships with exam performance, making linear models highly effective.

### 2️⃣ Simpler Models Win
Complex models like Random Forest and XGBoost do not provide additional value because the dataset lacks strong non-linear patterns.

### 3️⃣ Regularization Impact
Ridge and ElasticNet help prevent overfitting, but do not improve performance in this case.

### 4️⃣ Feature Scaling
Scaling (StandardScaler) changes coefficient values but **does not affect model accuracy**.

---

## 📊 Business / Educational Impact

This analysis can help:

- 🎯 Identify **at-risk students** early  
- 📚 Improve **study strategies**  
- 🏫 Support **data-driven educational decisions**  
- 📈 Enhance overall **academic performance**

---

## ✅ Conclusion

For this dataset, **Linear Regression** is the most effective model due to the strong linear relationships between features.

📌 **Key takeaway:**  
Student success is primarily driven by **consistent attendance and dedicated study time**.

---

## 🛠️ Tech Stack

- 🐍 Python  
- 📊 Pandas & NumPy  
- 📈 Matplotlib & Seaborn  
- 🤖 Scikit-Learn  
- 🚀 XGBoost  


1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/student-performance-analysis.git
