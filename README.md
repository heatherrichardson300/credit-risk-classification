# credit-risk-classification

## Overview of the Analysis

The purpose of this analysis was to evaluate the creditworthiness of loan borrowers. Various machine learning techniques were used to analyze a historical dataset from a peer-to-peer lending services company. Two loan types were evaluated: **high-risk loans** and **healthy loans**. 

To achieve predictions, a **machine learning pipeline** was performed. The dataset was split into **training** and **test sets** using `sklearn`. A **logistic regression model** was used to fit the training data, and predictions were made using the testing data. After completing this process, the model’s performance was evaluated using `sklearn`'s `confusion_matrix` and `classification_report` functions.

## Results

**Outcome of Confusion Matrix:**
```plaintext
[[18673,    86],
 [   32,   593]]
```
**Explanation of Output:**
- **18673 True Negatives:** The model correctly identified **18,673** healthy loans (0).
- **86 False Positives:** The model incorrectly classified **86** healthy loans as high-risk.
- **593 True Positives:** The model correctly identified **593** high-risk loans (1).
- **32 False Negatives:** The model incorrectly classified **32** high-risk loans as healthy.

These results indicate that the model is very effective at identifitying **healthy loans**. The model performs relatively well at **high-risk loans** with few false negatives.However, the accuracy for **high-risk loans** may present a slightly greater chance of inaccuracy.

### Logistic Regression Model Performance:

```plaintext
           Precision    Recall  F1-Score   Support

           0       1.00      1.00      1.00     18759
           1       0.87      0.95      0.91       625

    Accuracy                           0.99     19384
   Macro Avg       0.94      0.97      0.95     19384
Weighted Avg       0.99      0.99      0.99     19384
```

### Explanation of Performance Metrics:

- **Accuracy (99%)**: The model correctly predicts loan risk **99% of the time**.
- **Precision (1.00 for healthy loans, 0.87 for high-risk loans):** 100% of predicted healthy loans were actually healthy, while **87%** of predicted high-risk loans were truly high-risk.
- **Recall (1.00 for healthy loans, 0.95 for high-risk loans):** The model correctly identified **100% of healthy loans** and **95% of high-risk loans**.
- **F1-Score (1.00 for healthy loans, 0.91 for high-risk loans):** A strong balance between precision and recall.
- **Support:** Indicates the number of actual occurrences of each class in the dataset (**18,759 healthy loans and 625 high-risk loans**).


## Summary

Overall the logistic regression model performed the best. With an overall accuracy of 99%, this would be the recommended model for predicting loans. This model performs incredibly well and accurately based on the precision and recall scores. This model incredibly reliable. 
