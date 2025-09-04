# 📡 Customer Churn Prediction in the Telecom Sector  

![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)
![Python](https://img.shields.io/badge/Python-3.10+-blue?style=flat-square)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Enabled-orange?style=flat-square)

---

## 🧠 Problem Understanding  

In the highly competitive **telecom industry**, **customer churn**—when a customer stops using a company’s services—is a major business challenge.  
Acquiring new customers is expensive, so **retaining existing ones** is crucial for profitability.  

This project aims to:  
- 🔍 **Predict which customers are most likely to churn**  
- 📊 **Analyze key factors influencing churn**  
- 🛡️ Help telecom companies **implement proactive retention strategies**  

---

## 📂 Dataset Overview  

- **Rows**: 3,333 customers  
- **Features**: 20 attributes + churn label  
- **Target variable**: `Churn` *(1 = customer churned, 0 = retained)*  
- **No missing values** ✅  

| **Feature**                | **Description**                                |
|---------------------------|-----------------------------------------------|
| `State`                   | Customer’s state of residence               |
| `Account length`          | Duration of the customer account            |
| `Area code`              | Area code assigned to the customer          |
| `International plan`     | Whether the customer has an international plan |
| `Voice mail plan`        | Whether the customer has a voicemail plan    |
| `Number vmail messages`  | Number of voicemail messages                |
| `Total day minutes`      | Total minutes used during the day           |
| `Total day charge`       | Charges for daytime usage                   |
| `Total eve minutes`      | Total minutes used during evenings          |
| `Total eve charge`       | Charges for evening usage                   |
| `Total night minutes`    | Total minutes used at night                 |
| `Total night charge`     | Charges for night usage                     |
| `Total intl minutes`     | Total international minutes                |
| `Total intl charge`      | Charges for international calls             |
| `Customer service calls` | Number of calls to customer service         |
| `Churn`                  | Target variable                            |

---

## 🔍 Exploratory Data Analysis (EDA)  

- 📊 **Distribution analysis** of numerical & categorical features  
- 🔗 **Correlation heatmap** → highlight strongest predictors  
- 📉 **Churn imbalance**: dataset is imbalanced, requiring strategies like resampling or model weighting  
- 📦 **Feature importance**:  
    - **Total day charge** → strong positive correlation with churn  
    - **Total day minutes** → significant impact  
    - **Customer service calls** → high churn when customers frequently call  


---

## ⚙️ Data Preparation  

- **Encoding categorical variables** → One-hot encoding for `State`, `International plan`, and `Voice mail plan`
- **Standardization** of numerical features  
- **Train-test split**: 80% train, 20% test  
- **Addressing churn imbalance** using stratified sampling  

---

## 🤖 Modeling & Evaluation  

We tested multiple classification models and compared their performance using **Accuracy**, **ROC AUC**, and **F1-score**:

| **Model**             | **Accuracy** | **ROC AUC** | **F1-Score** |
|----------------------|--------------|-------------|--------------|
| Logistic Regression  | 77%          | 0.77        | 0.74         |
| SVM                  | 82%          | 0.82        | 0.78         |
| Random Forest        | 85%          | 0.86        | 0.81         |
| **XGBoost** ✅        | **88%**      | **0.88**    | **0.85**     |

📌 **Best Model → XGBoost** 🎯  

---



## 📌 Key Insights  

- Customers with an **International Plan** have a **higher churn probability** ⚠️  
- Frequent **customer service calls** are a strong churn indicator 📞  
- High **daytime usage** and **charges** correlate with churn 📊  
- XGBoost outperforms other models, making it the **recommended choice** ✅  

---

## 🛠️ Tech Stack  

- **Language**: Python 🐍  
- **Libraries**:  
  - `pandas`, `numpy` → Data manipulation  
  - `matplotlib`, `seaborn`, `plotly` → Visualization  
  - `scikit-learn` → Model training & evaluation  
  - `xgboost` → Best-performing model  
- **Tools**: Jupyter Notebook  


