
# Telecom Customer Churn Prediction Project

## 📊 Project Overview

This project builds a complete data analysis and machine learning pipeline to understand customer behavior and predict potential churners in a telecom company using SQL, Power BI, and Python.

It includes:

- SQL for data cleaning and preparation
- Power BI for customer profiling and churn visualization
- Python and Random Forest for churn prediction
- An interactive dashboard for visualizing predicted churners

---

## 📁 Dataset Summary

The dataset consists of customer information from a telecom company with the following key features:

- **Demographic & Geographic**: `Gender`, `Age`, `Married`, `State`
- **Referrals & Services**: `Number_of_Referrals`, `Tenure_in_Months`, `Internet_Service`, `Phone_Service`, `Streaming_TV`, etc.
- **Payment & Revenue**: `Payment_Method`, `Monthly_Charge`, `Total_Charges`, `Total_Revenue`
- **Target Column**: `Customer_Status` (`Stayed`, `Churned`, `Joined`), `Churn_Category`, `Churn_Reason`
- Unique identifier: `Customer_ID`

---

## 🎯 Project Goals

1. Analyze customer data at different levels:
   - Demographic
   - Geographic
   - Payment & Account Info
   - Services Used

2. Study churner profiles and identify potential focus areas for marketing

3. Build a churn prediction model to forecast future churners

### 📌 Key Metrics Tracked

- Total Customers  
- Total Churn & Churn Rate  
- Number of New Joiners  

---

## 🔁 Workflow

1. **ETL with SQL**  
   - Load and clean the raw dataset  
   - Handle missing values  
   - Split data into two tables:  
     - `Table 1`: Churned & Stayed Customers (used for training)  
     - `Table 2`: Newly Joined Customers (used for prediction)

2. **Data Visualization with Power BI**  
   - Build dashboard showing overview of customer demographics, services, payment, and churn

3. **Churn Prediction with Python**
   - Trained a Random Forest model on `Table 1`
   - Predicted churn on `Table 2`
   - Exported results of predicted churners for dashboarding

4. **Predicted Churner Dashboard**
   - Visualized model-predicted churners using Power BI for business insights

---

## ✅ Model Results

Using a Random Forest Classifier on the training data:

- **Accuracy**: 0.83  
- **Precision**: 0.88 (Stayed), 0.70 (Churned)  
- **Recall**: 0.87 (Stayed), 0.72 (Churned)  
- **F1 Score**: 0.88 (Stayed), 0.71 (Churned)

### 🔍 Top 5 Important Features
1. Contract Type  
2. Total Revenue  
3. Payment Method - Credit Card  
4. Internet Type - Fiber Optic  
5. Total Charges  

---

## 📈 Key Insights (From Dashboard)

- Majority of churners are associated with **Fiber Optic Internet** and **Month-to-Month contracts**
- Customers who had **high total revenue and monthly charges** were more likely to churn
- Some churners cited **network reliability** and **product dissatisfaction** as reasons

### 💡 Recommendations

- Offer **loyalty plans** or **discounted contracts** to Fiber Optic users
- Investigate service quality in states with higher churn rates
- Improve onboarding and after-sales support to reduce early churn

---

## ⚙️ Dependencies

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import classification_report, confusion_matrix
from sklearn.preprocessing import OneHotEncoder
import joblib
from category_encoders import TargetEncoder, CatBoostEncoder
from sklearn.model_selection import train_test_split, KFold
from imblearn.over_sampling import SMOTE
import warnings

warnings.filterwarnings('ignore')
```

---

## 📂 Repository Contents

- `telecom_churn_analysis.ipynb`: Python notebook for model training and evaluation
- `churn_prediction.csv`: Final output table of newly joined customers predicted to churn
- `Customer_Churn_Dashboard.pbix`: Power BI dashboard files (2 versions: Overview + Prediction)
- `README.md`: Project documentation

---

## 📎 How to Use

1. Clone the repository
2. Open the `.ipynb` file to explore the machine learning process
3. Open `.pbix` files in Power BI Desktop to interact with dashboards
4. View predictions in the `churn_prediction.csv` file

---

## 👨‍💻 Author

*Your Name Here* — Data Analyst | Passionate about turning data into action  
📫 [Your Email or LinkedIn]
