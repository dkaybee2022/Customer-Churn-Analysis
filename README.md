# Churn Prediction
## Project Overview

This project aims to predict customer churn using the Telco Customer Churn dataset from Kaggle. The objective is to build a machine learning model to classify whether a customer will churn (stop using a service) based on historical data.

## Table of Contents
Installation
Dataset
Correlation heatmap
Results and Insights

## Installation

To get started, clone the repository and install the required dependencies.

sh
Copy code
git clone (https://github.com/dkaybee2022/Customer-Churn-Analysis/blob/main/Customer_Churn_Project.ipynb)
cd customer-churn-prediction
pip install -r requirements.txt
Dataset

 [Telco Customer Churn dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)



# Correlation heatmap
plt.figure(figsize=(12, 8))
numeric_data = data.select_dtypes(include=['number'])
sns.heatmap(numeric_data.corr(), annot=True, fmt=".2f")
plt.show()




<img width="514" alt="image" src="https://github.com/dkaybee2022/Customer-Churn-Analysis/assets/147632964/99dc43ab-8775-477f-9901-975ba6eddf91">



<img width="507" alt="image" src="https://github.com/dkaybee2022/Customer-Churn-Analysis/assets/147632964/dd793a69-8a90-4ab3-b536-6cf618070e97">

## Results and insights 

1.	High Specificity (65.08%): The model is relatively good at identifying negative instances correctly. This means it is effective in reducing false alarms (false positives) for negative cases.
2.	Moderate Sensitivity (15.83%): The model’s ability to correctly identify positive instances is lower. This indicates that the model is missing a significant portion of positive cases, leading to a higher number of false negatives (10.65%).
3.	False Positive Rate (8.45%): While this rate is relatively low, it indicates some instances are incorrectly classified as positive when they are actually negative.
4.	False Negative Rate (10.65%): The model has a considerable rate of false negatives, meaning it fails to identify some positive instances correctly. This could be critical depending on the application, especially if missing positive cases has significant consequences.
   
Overall Assessment

•	The model has a strong performance in identifying negative instances (high specificity), which is good for applications where reducing false positives is crucial.
•	The lower sensitivity suggests that the model struggles to correctly identify all positive instances. This is a concern if correctly identifying positive cases is important.
•	Depending on the context of the classification problem, the balance between specificity and sensitivity might need adjustment. For example, in medical diagnostics, a high false negative rate can be more problematic than a high false positive rate.
