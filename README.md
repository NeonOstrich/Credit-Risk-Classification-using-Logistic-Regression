# Credit-Risk-Classification-using-Logistic-Regression

## Purpose
The purpose of this analysis is to generate a model that will be able to correctly identify 'healthy loan' and 'high risk loan' applicants based on application factors which include loan size, interest rate, borrower income, debt to income ratio, number of accounts, pre-defined derogetory marks, and total debt. We will then test this model to determine how effective it is at classifying both categories.

## Process
For this analysis, I generated and tested two models. 
The first model was generated with original data. This dataset was highly imbalanced with a significant majority of 'healthy loans' (75,036) compared to 'high risk loans' (2,500). I split this model into Training and Test sets and generated a Logistic Regression model. I then generated confucion matrices and tested its accuracy, precision and recall for both the training and test sets.

<img width="562" alt="Model 1 Confusion Matrix" src="https://github.com/NeonOstrich/Polling-and-Banking-Data-Analysis-in-Python/assets/119632669/0b26c071-f4cc-458a-8e57-e2da40950db4">
<img width="601" alt="Model 1 Classification Report" src="https://github.com/NeonOstrich/Polling-and-Banking-Data-Analysis-in-Python/assets/119632669/066e34ad-5612-49a3-a3cc-da7f5665eafa">

For the second model, I used resampled data instead of original data. This allowed me to have a dataset with an equal number of 'healthy loans' and 'high risk loans' with which to train my model. There were 56,271 of each type in the resampled dataset. I split this model into Training and Test sets and generated a Logistic Regression model. I then generated confucion matrices and tested its accuracy, precision and recall for both the training and test sets.

<img width="583" alt="Model 2 Confusion Matrix" src="https://github.com/NeonOstrich/Polling-and-Banking-Data-Analysis-in-Python/assets/119632669/c3d1dbef-b84b-499c-8f77-10eb12bae809">
<img width="617" alt="Model 2 Classification Report" src="https://github.com/NeonOstrich/Polling-and-Banking-Data-Analysis-in-Python/assets/119632669/3eb9bcc7-08e0-415c-b311-779d464c2169">

## Results

Machine Learning Model 1 (with original data):
  * Test Data Balanced Accuracy: 99%
  * Test Data Precision for 'healthy loans': 100%
  * Test Data Precision for 'high risk loans': 85%
  * Test Data Recall for 'healthy loans': 99%
  * Test Data Recall for 'high risk loans': 91%
  
Machine Learning Model 2 (with resampled data):
  * Test Data Balanced Accuracy: 99%
  * Test Data Precision for 'healthy loans': 99%
  * Test Data Precision for 'high risk loans': 99%
  * Test Data Recall for 'healthy loans': 99%
  * Test Data Recall for 'high risk loans': 99%
  
## Summary

The first Logistic Regression model, using original data, does very well at predicting 'healthy loans' with accuracy, precision and recall close to 100%. It still does well, but performs noticably worse at identifying high-risk loans where it has a precision of 85% and a recall of 91%. This suggests that this model is less able to classify high risk loans than healthy loans. This is likely related to the skew in the data that was provided, with only about 3 percent of the sample being in the high risk loans category.
The second Logistic Regression model that uses resampled data, performs noticably better at identifying high risk loans in addition to identifying healthy loans. The overall prediction rate is consistent across precision, recall, and accuracy.
We would recommend utilizing the second model because of its heightened ability to detect 'high risk loans' accurately. This is especially important given how much it can cost a loan provider to misidentify and lend money to a 'high risk loan' applicant, and the minimal cost of misidentifying a 'healthy loan' applicant. The first model is slightly better at identifying 'healthy loan' applicants, but this is less important than correctly identifying 'high risk loan' applicants, which is accomplished better with the second model.
