# Module 12 Report Template

## Overview of the Analysis

Lending companies lend money or properties to borrowers with the expectation that the borrower will either return the asset or repay the lender. Credit Risk is the risk the lender is taking when the borrower might not return the asset or repay the loan back.In this analysis we will use Machine Learning to measure credit risk by analyziing a dataset of historical lending activity to build a model that can identify which borrowers are the best candidates. 

Using the machine learning model, I will determine which loans are healthy (low-risk) or non-healthy (high-risk) based on the loan status provided by the lending company. Which is why the Logistic Regression Algorithm is the best tool to use for our model since it is widely used to predict the probability of a target variable in classification problems.

According to the confusion matrix in Step 3 "Generate a confusion matrix for the model with Original Imbalanced Data":

Out of the 18,765 loan status's that are healthy (low-risk), the model predicted 18,663 as healthy correctly and 102 that is healthy incorrectly.

Out of the 619 loan status's that are non-healthy (high-risk), the model predicted 563 as non-healthy correctly and 56 that is non-healthy incorrectly.

<img width="989" alt="Screenshot 2024-03-14 at 7 29 56 PM" src="https://github.com/kimrodriguezFINTECH/CHALLENGE_12/assets/152752672/4aee6a5e-4a69-470c-a780-e42d0e07fee2">


According to the confusion matrix in step 3 "Generate a confusion matrix for the model with Resampled(oversampled) Data":

Out of the 18,765 loan status's that are healthy, the model predicted 18,649 as healthy correctly and 116 as healthy incorrectly.

Out of the 619 loan status's that are non-healthy (high-risk), the model predicted 615 as non-healthy correctly and 4 as non-healthy incorrectly.

<img width="994" alt="Screenshot 2024-03-14 at 7 30 16 PM" src="https://github.com/kimrodriguezFINTECH/CHALLENGE_12/assets/152752672/74850eb7-e7de-4dff-9b9f-5e0031a812f0">


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:

The Logistic Regression model fitted with the Imbalanced DataSet predicted healthy loans 100% of the time and predicted non-healthy loans 85% of the time.

According to the models recall scores, the model made 1% of mistakes when predicting healthy loans and made 9% of mistakes when predicted non-healthy loans.

The model generated an accuracy score of 95% but it could be improved. 

<img width="665" alt="Screenshot 2024-03-14 at 7 36 20 PM" src="https://github.com/kimrodriguezFINTECH/CHALLENGE_12/assets/152752672/d5a2da39-5f07-42a4-a6f4-104d1c4e4f2d">

<img width="399" alt="Screenshot 2024-03-14 at 7 38 45 PM" src="https://github.com/kimrodriguezFINTECH/CHALLENGE_12/assets/152752672/faf8b0ad-8682-4b94-a611-c73c90da3514">


* Machine Learning Model 2:

The Logistic Regression model fitted with the OverSampled DataSet predicted healthy loans 100% of the time and predicted non-healthy loans 84% of the time.

According to the models recall scores, the model made 1% of mistakes when predicting healthy loans and made 1% of mistakes when predicted non-healthy loans.

The model generated an accuracy score of 99%. 

<img width="661" alt="Screenshot 2024-03-14 at 7 40 06 PM" src="https://github.com/kimrodriguezFINTECH/CHALLENGE_12/assets/152752672/9595600b-3b44-43c9-a3c6-09b3b81b7e24">

<img width="430" alt="Screenshot 2024-03-14 at 7 40 01 PM" src="https://github.com/kimrodriguezFINTECH/CHALLENGE_12/assets/152752672/4230fa6b-9a64-48e4-9cc1-1a75618602d8">


## Summary

A lending company would want a model that requires classifying healthy loans and non-healthy loans correctly most of the time because healthy loans being identified as a non-healthy loan can cost the lending company a massive loss to the lenders and its customers.

The Logistic Regression model fitted with OverSampled data performed much better than the model fitted with Imbalanced data due to the data being balanced and generating a higher accuracy score and a higher recall, indicating that the model will make extremely fewer mistakes when classifying non-healthy loans. However, a lending company would most likely want fewer False Positives due to the high possibility of a lender losing provided funds when classifying non-healthy loans as healthy. 

Imbalanced Data (Model):

56 (FALSE POSITIVES): The actual value is healthy and the predicted value is non-healthy

102 (FALSE NEGATIVES): The actual value is non-healthy and the predicted value is healthy


Balanced Data (Model):

4 (FALSE POSITIVES): The actual value is healthy and the predicted value is non-healthy

116 (FALSE NEGATIVES): The actual value is non-healthy and the predicted value is healthy

Based off of this analysis, I would recommend using Model 2 (Logistic Regression Model fitted with Balanced (oversampled) data.
