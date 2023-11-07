# credit-risk-classification

## Overview of the Analysis

The purpose of this analysis was to develop machine learning models capable of predicting credit risk for a lending company. The objective was to identify which borrowers are likely to be high-risk (default on their loan) versus those who are low-risk (will repay their loan). This differentiation is critical for the company to manage its financial risk effectively.

The dataset comprised historical financial information from a peer-to-peer lending services company. The key variable to predict was the loan status, categorized into '0' for healthy loans and '1' for high-risk loans. The `value_counts` of the original dataset revealed a significant imbalance between the two categories, which was crucial since it could skew the predictive performance of our models.

During the machine learning process, the following stages were undertaken:
1. Data Preprocessing: Handling missing values, encoding categorical variables, and splitting the data into training and testing sets.
2. Model Selection: Choosing Logistic Regression for its efficacy in binary classification problems.
3. Resampling: Applying the `RandomOverSampler` method to address the imbalance in the dataset and create an even distribution of the two classes.
4. Model Training: Fitting the Logistic Regression model to both the original imbalanced dataset and the oversampled dataset.
5. Model Evaluation: Assessing model performance through metrics such as balanced accuracy, precision, and recall.

## Results

* Machine Learning Model 1:
  * The first model, trained on the original imbalanced dataset, had a certain level of accuracy but showed limitations in recall for the minority class (high-risk loans).

* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores:
      * Balanced Accuracy Score: 0.99
      * Precision for Healthy Loans (0): 1.00
      * Recall for Healthy Loans (0): 0.99
      * Precision for High-Risk Loans (1): 0.84
      * Recall for High-Risk Loans (1): 0.99

## Summary

Upon reviewing the results, it appears that Machine Learning Model 2, which was trained on the oversampled dataset, outperforms Model 1 in terms of balanced accuracy and recall for both classes. This model demonstrates a particularly strong ability to correctly identify the high-risk loans, which is crucial for a lending company to minimize financial loss.

Considering the company's needs, the performance of a model in this context might depend on the specific financial implications of false negatives (failing to identify a high-risk loan) versus false positives (mistakenly identifying a healthy loan as high-risk). Generally, the high recall of high-risk loans in Model 2 suggests it would be the preferred model, as it minimizes the risk of lending to borrowers who are likely to default.

Therefore, Model 2 (the Logistic Regression model trained on oversampled data) is recommended for use. It exhibits a higher accuracy and recall score, suggesting that it is more reliable for classifying both healthy and high-risk loans correctly. This model is less likely to cause financial loss due to defaulted loans and will enable the lending company to make more informed and safer lending decisions.
