# Predicting Customer Churn Using Machine Learning

**Author:** Tanu Gera

## Executive Summary

Customer churn is an important challenge for subscription-based businesses because losing existing customers can reduce revenue and increase the cost of acquiring replacement customers.
This project applies machine learning to spot customers who might be at risk of churn and to find out which customer characteristics and behaviors are most closely linked to churn.
Using a publicly available customer churn dataset from Kaggle, I carried out data cleaning, exploratory data analysis (EDA), feature engineering, preprocessing, and machine learning modeling. Logistic Regression, Decision Tree, and Random Forest classifiers were tested, and hyperparameter tuning was done using GridSearchCV.
The analysis showed that payment behavior, customer support interactions, tenure, and usage patterns are key indicators of churn risk.
These findings can help businesses identify at-risk customers earlier and support more targeted customer retention strategies.

## Rationale

Retaining existing customers is important for maintaining revenue and reducing the costs associated with acquiring new customers. If businesses can identify customers who may be at risk of leaving, they can take proactive steps such as targeted outreach, improved customer support, personalized offers, or payment assistance.
The goal of this project is therefore not only to predict customer churn, but also to translate the model findings into practical business insights that can support customer retention decisions.

## Research Question

Can machine learning accurately identify customers who are likely to churn, and which customer characteristics and behaviors are most useful for predicting churn?

## Data Source

This project uses the Customer Churn Dataset obtained from Kaggle.
The dataset contains approximately 64,000 customer records and includes variables such as:

Age

Gender

Tenure

Usage Frequency

Support Calls

Payment Delay

Subscription Type

Contract Length

Total Spend

Last Interaction

Churn (target variable)

## Methodology

The project follows a structured machine learning workflow:

1. Data inspection and quality assessment
2. Data cleaning and preprocessing
3. Exploratory Data Analysis (EDA)
4. Outlier analysis
5. Feature engineering
6. Data visualization
7. Train-test split using stratified sampling
8. Numerical feature scaling and categorical feature encoding
9. Baseline Logistic Regression modeling
10. Decision Tree modeling
11. Random Forest modeling
12. 5-fold cross-validation
13. Hyperparameter tuning using GridSearchCV
14. Model comparison
15. Feature importance analysis
16. Business interpretation and recommendations

Models were evaluated using Accuracy, Precision, Recall, F1-score, and ROC-AUC.

**Recall was selected as the primary evaluation metric** because failing to identify a customer who is likely to churn could result in a missed opportunity for proactive retention.

## Exploratory Data Analysis Findings

The exploratory analysis identified several customer characteristics and behaviors associated with churn.

Key observations included:

- Customers with longer payment delays showed higher churn risk.
- Customers making more support calls were more likely to churn.
- Tenure showed meaningful differences between customers who churned and those who remained.
- Usage frequency was associated with customer retention behavior.
- Total Spend and Age also showed relationships with churn, although their influence was smaller.
These findings provided direction for the machine learning analysis.

## Model Results

Multiple classification models were evaluated.

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 82.70% | 81.37% | 82.34% | 81.85% | 90.30% |
| Decision Tree | 99.89% | 99.82% | 99.95% | 99.89% | 99.89% |
| Random Forest | 99.88% | 99.97% | 99.77% | 99.87% | 100.00% |
| Tuned Decision Tree | 99.84% | 99.71% | 99.95% | 99.83% | 99.93% |
The tree-based models substantially outperformed the Logistic Regression baseline.

Because Recall was the primary evaluation metric, the Decision Tree performed particularly well, identifying approximately **99.95% of customers who churned** in the test dataset.

Five-fold cross-validation also demonstrated strong and consistent performance for the tree-based models.

## Hyperparameter Tuning

GridSearchCV was used to tune the Decision Tree and evaluate different combinations of model hyperparameters.

The tuned Decision Tree achieved a Recall of **99.95%** on the test set. Although tuning did not meaningfully improve test-set performance compared with the original Decision Tree, it demonstrated that strong predictive performance could be maintained while controlling model complexity.

## Feature Importance

Random Forest feature importance was used to better understand which variables contributed most strongly to churn predictions.

The most important features were:

- **Payment Delay:** approximately 43.6%
- **Support Calls:** approximately 16.5%
- **Tenure:** approximately 11.5%
- **Usage Frequency:** approximately 8.4%
- **Total Spend:** approximately 5.2%
- **Age:** approximately 4.1%

Payment Delay was therefore the strongest feature in the Random Forest model.

Feature importance represents predictive contribution and should not be interpreted as evidence that these variables directly cause customer churn.

## Final Model Selection

The **Decision Tree** was selected as the final model for this analysis.

Recall was prioritized because failing to identify an actual churner may result in a missed opportunity for proactive retention. The Decision Tree achieved **99.95% Recall**, while also maintaining strong Accuracy, Precision, F1-score, and ROC-AUC.

Because the tree-based models achieved unusually high predictive performance, additional validation on new or out-of-time customer data would be recommended before using the model for real-world business decisions.

## Business Recommendations

Based on the analysis, businesses could consider the following retention strategies:

- Monitor customers experiencing repeated or increasing payment delays.
- Prioritize follow-up for customers making frequent support calls.
- Consider customer tenure when designing retention strategies.
- Monitor changes or declines in customer usage frequency.
- Use churn-risk predictions to prioritize customers for proactive retention campaigns.

These strategies could allow businesses to identify at-risk customers earlier and focus retention resources where they may provide the greatest benefit.

## Limitations and Next Steps

Although the models demonstrated strong predictive performance, the unusually high results of the tree-based models should be validated further before deployment.

Future work could include:

- Validating the model using new or out-of-time customer data.
- Monitoring model performance over time.
- Exploring additional classification algorithms such as Gradient Boosting.
- Investigating additional feature engineering opportunities.
- Evaluating prediction thresholds based on the cost of false positives and false negatives.
- Testing retention strategies with controlled business experiments.

## Conclusion

This project demonstrates how machine learning can be used to identify customers who may be at risk of churn and translate customer behavioral data into actionable business insights.

Payment Delay, Support Calls, Tenure, and Usage Frequency emerged as important churn indicators. Among the evaluated models, the Decision Tree achieved the strongest performance for the project's primary objective of identifying customers who actually churned.

These insights could help businesses develop more proactive and targeted customer retention strategies while providing a foundation for further model validation and improvement.

## Project Files

- `README.md` — Nontechnical summary of the project, findings, and recommendations
- `customer_churn_eda.ipynb` — Complete analysis, EDA, modeling, evaluation, and interpretation

## Jupyter Notebook

The complete technical analysis is available here:

[Customer Churn Analysis Notebook](customer_churn_eda.ipynb)

## Contact and Further Information

This repository was developed as part of the UC Berkeley Professional Certificate in Machine Learning and Artificial Intelligence Capstone Project.

For questions or feedback, please connect with me through GitHub.
