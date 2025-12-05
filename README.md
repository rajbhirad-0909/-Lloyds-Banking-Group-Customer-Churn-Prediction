📊 Lloyds Banking Group — Customer Churn Prediction

A Data Science & Analytics Virtual Experience Project (Forage)
By Raj Bhirad

📝 Project Overview

This project is part of the Lloyds Banking Group: Data Science & Analytics Virtual Experience Program by Forage.
The goal is to:

Analyse customer behaviour

Identify churn patterns

Build predictive machine learning models

Provide actionable insights for customer retention

This repository includes:

✔ Data exploration
✔ Data cleaning & preprocessing
✔ Visualisations
✔ Machine learning models (Logistic Regression, Random Forest, XGBoost)
✔ Insights and recommendations

📂 Project Structure
📁 Lloyds-Churn-Prediction/
│
├── Task1_EDA.ipynb          # Full EDA notebook
├── Task2_Modelling.ipynb    # Model training and evaluation
├── cleaned_customer_data.csv
├── figures/                 # All saved plots (PNG)
│   ├── churn_distribution.png
│   ├── correlation_heatmap.png
│   ├── login_boxplot.png
│   ├── total_spent_hist.png
│
└── README.md                # This file

🔍 1. Exploratory Data Analysis (EDA)
Churn Distribution

Churners: 20.4%

Non-churners: 79.6%
➡ Highly imbalanced dataset, influencing model performance.

Key Visualizations

Churn distribution

Correlation heatmap

Days since last login vs churn (Box plot)

Total spent (Histogram)

Key Findings

Churners have significantly lower login activity

Spending is skewed—most customers are low spenders

No single feature strongly predicts churn → churn is multi-factor

🧹 2. Data Cleaning & Preprocessing

Steps completed:

Verified and handled missing values

Encoded categorical features

Scaled numerical variables

Removed inconsistencies and validated data types

Prepared train/test split with stratification

🤖 3. Machine Learning Models

Trained and compared:

1️⃣ Logistic Regression

Baseline model

ROC-AUC: 0.39

Performs poorly due to nonlinear patterns

2️⃣ Random Forest

Tuned with GridSearchCV

ROC-AUC: 0.49

Model predicts mostly non-churn due to class imbalance

3️⃣ XGBoost (Baseline)

ROC-AUC: 0.43

Handles non-linearity better

4️⃣ XGBoost (Balanced using scale_pos_weight)

Best CV ROC-AUC: 0.5883

Test ROC-AUC ≈ 0.50

Best-performing model overall

📈 Model Comparison
Model	CV ROC-AUC	Test ROC-AUC	Recall (Churn)	Notes
Logistic Regression	0.5189	0.3985	0.39	Weak baseline
Random Forest	0.5698	0.4958	0.02	Biased toward non-churn
XGBoost	0.5826	0.4324	0.22	Better feature learning
XGBoost (Balanced)	0.5883	≈0.50	Moderate	Best overall

🧠 4. Key Insights

Customer churn is driven by inactivity, especially fewer logins and transactions.

Spending behaviour also impacts churn risk—low spenders churn more.

No single factor determines churn → multi-dimensional behaviour.

Class imbalance is the biggest challenge for modelling.

💡 5. Recommendations for Lloyds Banking Group
📌 Improve customer engagement

Automated reminders for inactive customers

Personalized login streak rewards

Triggered notifications based on inactivity thresholds

📌 Enhance customer value

Offer cashbacks for low spenders

Tailored product bundles

Loyalty programs

📌 Data improvements

Collect detailed interaction history

Transaction-level time-series data

Add digital activity metrics (app usage, clickstream)

🧾 6. Tools & Technologies Used

Python

Pandas, NumPy

Scikit-learn

XGBoost

Matplotlib, Seaborn

Jupyter Notebook

👨‍💻 7. About the Author

Raj Bhirad
Data Analyst | AI Learner | Aspiring Machine Learning Engineer
Skilled in data analysis, EDA, modeling, and AI-powered problem solving.

⭐ If you like this project, consider giving the repository a star!
