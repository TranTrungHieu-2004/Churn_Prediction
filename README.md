
# Telecom Customer Churn Prediction Project

## 📊 Project Overview

This project builds a complete data analysis and machine learning pipeline to understand customer behavior and predict potential churners in a telecom company using SQL, Power BI, and Python.

It includes:

- SQL for data cleaning and preparation
- Power BI for customer profiling and churn visualization (You can quickly access the dashboard online here: Churn_Analysis_Dashboard )
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
   - Split data into two datasets:  
     - `vw_ChurnData`: Churned & Stayed Customers (used for training)  
     - `vw_JoinData`: Newly Joined Customers (used for prediction)

2. **Data Visualization with Power BI**  
   - Build a dashboard showing the overview of customer demographics, services, payment, and churn

3. **Churn Prediction with Python**
   - Trained a Random Forest model on `vw_ChurnData`
   - Predicted churn on `vw_JoinData`
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

Output: 301 newly Joined customers are predicted to be churned over 411  newly joined customers in total

### 🔍 Top 5 Important Features
1. Contract Type  
2. Total Revenue  
3. Payment Method - Credit Card  
4. Internet Type - Fiber Optic  
5. Total Charges  

---

## 📈 Key Insights (From Dashboard)
- High churn with fiber-optic users (41.1%)
- Month-to-month contract holders churn at 46%
- 70–80% churn among users of Internet, Phone, Paperless Billing, and Unlimited Data services
- Major churn reasons: competitor offers (44%) and dissatisfaction (34%)
  

---

## ⚙️ Dependencies
- pandas 
- numpy 
- matplotlib.pyplot
- seaborn
- RandomForestClassifier
- OneHotEncoder
- joblib
- TargetEncoder
- CatBoostEncoder
- SMOTE

---
📂 Repository Contents
- `Customer_Data.csv`: Raw dataset
- `Churn_Prediction.csv`: Dataset used in modeling (with sheet 1 is Churn customer, sheet 2 is newly joint customer) 
- `Random Forest.ipynb`: Python notebook for model training and evaluation
- `Prediction1.csv`: Final output table of newly joined customers predicted to churn
- `Churn Analysis.pbix`: Power BI dashboard file
- `README.md`: Project documentation



---


