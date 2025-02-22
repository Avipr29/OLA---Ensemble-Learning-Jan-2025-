# 🚖 Ola Driver Attrition Prediction - Ensemble Learning

## 📌 Problem Statement
Ola faces a high **driver churn rate**, where drivers frequently leave the platform or switch to competitors like Uber. Acquiring new drivers is costly, and frequent attrition affects operational stability.  

This project aims to **predict driver attrition** using historical performance data, demographics, and tenure details. The goal is to identify **key factors influencing churn** and provide **actionable insights** to improve retention strategies.

---

## 📂 Dataset
**Dataset Name:** `ola_driver.csv`  

**Key Attributes:**
- **Demographics:** City, age, gender, education level
- **Tenure:** Joining date, last working date
- **Performance Metrics:** Quarterly rating, total business value, monthly income, grade

---

## 🧠 Concepts Applied
- **Ensemble Learning:** Bagging & Boosting
- **KNN Imputation:** Handling missing values
- **Class Imbalance Treatment:** Addressing skewed churn data
- **Feature Engineering:** Creating informative variables  
- **Standardization & Encoding:** Preprocessing for model training  
- **Model Evaluation:** ROC AUC, Classification Report  

---

## 📊 Data Preprocessing Steps
1. **Exploratory Data Analysis (EDA)**  
   - Identified patterns in churn behavior  
   - Visualized distributions and correlations  

2. **Feature Engineering**
   - Created target variable (`1` if the driver left, else `0`)
   - Derived quarterly rating change indicator  
   - Designed income growth flag  

3. **Missing Value Handling**
   - Applied **KNN Imputation** for numerical variables  

4. **Class Imbalance Treatment**
   - Implemented **SMOTE** to balance churn vs. non-churn classes  

5. **Encoding & Scaling**
   - One-hot encoding for categorical variables  
   - Standardized numerical features  

---

## 🤖 Model Development
| Model | Train Accuracy | Test Accuracy | ROC-AUC |
|--------|--------------|-------------|---------|
| **Random Forest (Imbalanced Data)** | 87.34% | 82.39% | 0.84 |
| **Random Forest + GridSearchCV** | 97.58% | 87.21% | 0.86 |
| **Balanced Random Forest** | 86.71% | 81.97% | 0.85 |
| **Gradient Boosting** | 93.14% | 87.42% | 0.88 |
| **XGBoost Classifier** | 98.11% | 88.05% | 0.87 |
| **LGBM Classifier (Best Model)** | 98.69% | 88.68% | 0.88 |

🏆 **Best Model:** `LightGBM Classifier` - Achieved **highest accuracy (88.68%)** with balanced precision & recall.

---

## 🔍 Key Insights
- **68% of drivers churned**, with low income growth as a major factor.
- **Quarterly rating impacts churn**, but no drivers received a 5-star rating.
- **City C22 outperforms** all other cities; further analysis needed.
- **Higher education level ≠ lower churn**, suggesting job dissatisfaction.
- **Female drivers are underrepresented** – increasing representation could improve safety and customer satisfaction.

---

## 📢 Recommendations
✅ **Implement Reward Programs:** Incentives for high-performing drivers.  
✅ **Enhance Training Modules:** Focus on customer service & time management.  
✅ **Improve Ratings System:** Capture non-driver factors (app performance, support).  
✅ **Targeted Driver Recruitment:** Prioritize cities & demographics with lower churn.  
✅ **Quarterly Model Updates:** Monitor churn trends and retrain models accordingly.  

---

## 🏗 Future Scope
- Incorporate **real-time telematics data** to improve predictions.  
- Integrate **external economic factors** (fuel prices, traffic patterns).  
- Deploy a **real-time churn monitoring dashboard** for proactive intervention.  

---
