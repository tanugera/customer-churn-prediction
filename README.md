# Predicting Customer Churn Using Machine Learning

**Author:** Tanu Gera

## Executive summary
Customer churn remains one of the major challenges for subscription-based businesses, since losing current customers has a direct effect on revenue and drives up customer acquisition costs. In this project, machine learning is used to predict customer churn and to pinpoint which customer traits and behaviors are most closely linked to customers deciding to leave a company.

With a publicly available customer churn dataset from Kaggle, I carried out exploratory data analysis (EDA), cleaned and prepared the data, created additional features that are more meaningful for business, and built a baseline Logistic Regression classification model. The aim is to give business stakeholders practical insights that could help strengthen customer retention strategies.

## Rationale
Retaining current customers usually costs significantly less than bringing in new ones. When businesses are able to spot customers who might leave before they actually do, they can step in early with targeted promotions, better customer service, loyalty programs, or more personalized communication.

This project addresses a key business question by pinpointing the main factors that lead to customer churn and showing how machine learning can help guide data-driven decisions for customer retention.

## Research Question
Can machine learning accurately predict which customers are likely to churn, and which customer demographics, behavioral patterns, and account characteristics contribute most to customer attrition?

## Data Sources
This project uses the Customer Churn Dataset obtained from Kaggle.

The dataset contains approximately 64,000 customer records and includes variables such as:

- Age
- Gender
- Tenure
- Usage Frequency
- Support Calls
- Payment Delay
- Subscription Type
- Contract Length
- Total Spend
- Last Interaction
- Churn (target variable)

## Methodology
The project uses a typical machine learning workflow:
1. Data inspection and quality assessment
2. Data cleaning and preprocessing
3. Exploratory Data Analysis (EDA)
4. Outlier analysis
5. Feature engineering
6. Data visualization
7. Data preparation for modeling
8. Baseline Logistic Regression model
9. Model evaluation with Accuracy, Precision, Recall, F1-score, ROC-AUC, and Confusion Matrix
10. Interpretation of model results and recommendations for business

## Results
Exploratory Data Analysis found several variables that seem to be linked with customer churn. Customers who had longer payment delays, made more support calls, and had shorter contract lengths usually showed higher churn rates. On the other hand, customers with higher usage frequency and greater total spending were more likely to stay with the company.

A baseline Logistic Regression model was built to set an initial benchmark for predicting customer churn. The model showed strong predictive performance and indicated that meaningful customer churn patterns are present in the dataset. These findings offer a solid base for comparing more advanced machine learning models in the final capstone project.

## Next steps
Future work will include the following:
- Comparing Logistic Regression with additional classification models such as Decision Trees, Random Forest, and Gradient Boosting.
- Running hyperparameter tuning to try to improve predictive performance.
- Looking at feature importance to better understand which factors most influence customer churn.
- Presenting business recommendations that are supported by model interpretation and visualizations.

## Outline of project
- README.md
- customer_churn_eda.ipynb
- Dataset
- Final Report (Module 24)

## Contact and Further Information
This repository was developed as part of the UC Berkeley Professional Certificate in Machine Learning and Artificial Intelligence Capstone Project.
For questions or feedback, please connect with me through GitHub.