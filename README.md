# Credit-Risk-Modelling
Revising the current credit lending strategy of bank using machine learning

📌 Credit Risk Modeling & EPS Prediction
Overview
This project implements an end-to-end machine learning solution for credit risk assessment and EPS (Earnings Per Share) prediction in the banking sector.
It covers data cleaning, feature engineering, model building, hyperparameter tuning, and web deployment using Flask, allowing users to input financial metrics and instantly receive EPS predictions.

Project Workflow
Data Understanding & Preparation

Merged Bureau Dataset and Internal Product Dataset using a common identifier.

Handled missing values, outliers, and invalid entries.

Removed low-quality features based on missing thresholds.

Performed categorical feature analysis using Chi-square test and numerical feature selection using ANOVA & Variance Inflation Factor (VIF).

Feature Engineering

Label encoded ordinal variables such as Education Level.

One-Hot encoded nominal categorical variables (Gender, Marital Status, Product Enquiries).

Applied scaling for numerical variables like Age, Income, Time with Employer.

Model Building

Implemented Random Forest, XGBoost, and Decision Tree classifiers to predict credit risk tiers (P1, P2, P3, P4).

Tuned hyperparameters using GridSearchCV for optimal accuracy.

Evaluated models on accuracy, precision, recall, and F1-score for all classes.

Selected XGBoost as the best performer based on multi-class metrics.

EPS Prediction Web App

Built a Flask application to serve the trained EPS prediction model (eps_v1.sav).

Designed a user-friendly HTML form for entering key financial metrics (ROCE, CASA, Operating Profit, Expenses, etc.).

Deployed locally to provide instant EPS predictions.

Deployment & Feedback

Configured model to be retrainable with new data/feedback.

Designed workflow for continuous improvement based on real-time user interaction.

Tech Stack
Languages: Python

Libraries: Pandas, NumPy, Matplotlib, Scikit-Learn, XGBoost, SciPy, Statsmodels

Model Serving: Flask

Frontend: HTML, CSS

Data Storage: Excel

Other Tools: GridSearchCV for hyperparameter tuning, Pickle for model serialization

Key Features
✅ End-to-end ML pipeline — from raw banking data to deployment
✅ Multi-class classification for credit risk segmentation
✅ EPS prediction via interactive web form
✅ Strong feature selection using statistical tests (Chi-square, ANOVA, VIF)
✅ Scalable architecture for retraining and model updates

How to Run the Project
Clone the Repository

bash
Copy
Edit
git clone https://github.com/yourusername/CreditRisk_EPS_Prediction.git
cd CreditRisk_EPS_Prediction
Install Dependencies

bash
Copy
Edit
pip install -r requirements.txt
Run the Flask App

bash
Copy
Edit
python deploy.py
