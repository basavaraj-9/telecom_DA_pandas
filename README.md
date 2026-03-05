Telecom Customer Churn Analysis
📌 Project Overview

This project analyzes a telecom customer dataset to identify factors that influence customer churn. The goal is to clean, preprocess, and explore the dataset to understand customer behavior and help telecom companies reduce churn.

📊 Dataset

The dataset contains customer information such as:

Customer ID

Gender

Tenure

Monthly Charges

Total Charges

Contract Type

Internet Service

Payment Method

Churn status

🛠 Technologies Used

Python

Pandas

NumPy

Matplotlib

Seaborn

Jupyter Notebook

⚙️ Project Workflow
1. Data Loading

The dataset is loaded using Pandas.

telecom_data = pd.read_csv("Telco_Customer_Churn_Dataset.csv")
2. Data Exploration

Basic dataset information is explored using:

head()

info()

shape

isnull()

3. Data Cleaning

Steps performed:

Converted TotalCharges to numeric

Handled missing values using median

Removed unnecessary columns like customerID

telecom_data["TotalCharges"] = pd.to_numeric(telecom_data["TotalCharges"], errors="coerce")
telecom_data["TotalCharges"] = telecom_data["TotalCharges"].fillna(telecom_data["TotalCharges"].median())
4. Data Visualization

Missing values and patterns are visualized using Seaborn heatmaps.

sns.heatmap(telecom_data.isnull(), yticklabels=False, cmap="viridis")
5. Feature Encoding

Categorical variables are converted into numeric values using One-Hot Encoding.

📈 Objectives

Understand customer churn patterns

Identify key factors affecting churn

Prepare the dataset for machine learning models

🚀 Future Improvements

Apply machine learning models for churn prediction

Compare different classification algorithms

Build a churn prediction dashboard

📂 Project Structure
Telecom-Churn-Analysis
│
├── telecom_data.ipynb
├── Telco_Customer_Churn_Dataset.csv
└── README.md
