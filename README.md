# credit-risk-classification

By employing machine learning methods, an examination was performed on a dataset containing past lending transactions from a peer-to-peer lending company. The goal was to develop a model capable of evaluating borrowers' creditworthiness.

Overview of the Analysis: The analysis considered various factors including: 
- Loan size 
- Interest rate 
- Borrower's income 
- Debt-to-income ratio 
- Number of borrower's accounts 
- Derogatory marks against the borrower 
- Total debt

The dataset, consisting of 77,536 data points, was split into training and testing sets. The training set was utilized to build an initial logistic regression model (referred to as Logistic Regression Model 1), employing the LogisticRegression module from scikit-learn. Following this, Logistic Regression Model 1 was applied to the testing dataset to classify borrower loans as either low- or high-risk.

Initially, the model was trained on a dataset comprising 75,036 low-risk loan data points and 2,500 high-risk data points. To balance the number of data points available for logistic regression modeling, the training set data underwent resampling using the RandomOverSampler module from imbalanced-learn. This resampling technique generated 56,277 data points for both low-risk (0) and high-risk (1) loans, maintaining the original dataset's proportions.

The resampled data was then used to develop a new logistic regression model (referred to as Logistic Regression Model 2), aimed at determining the risk level (low or high) of loans to borrowers within the testing set. The subsequent results are detailed below:

Results: 
Logistic Regression Model 1: 
- Precision: 93% (average precision) 
- Accuracy: 94% 
Recall: 95% (average recall)

Logistic Regression Model 2: 
- Precision: 93% (average precision) 
- Accuracy: 100% 
- Recall: 100%

Summary:
Logistic Regression Model 2 demonstrates a lower probability of generating false negative predictions. However, upon comparing the confusion matrices of both models, it becomes evident that Logistic Regression Model 2 produced marginally more false positives (identifying loans as low-risk when they were indeed high-risk).

Neither model attains precision scores exceeding 90% when targeting the identification of high-risk loans. Nonetheless, Logistic Regression Model 2 showcases fewer erroneous predictions overall on the testing dataset, making it the favored model due to its superior accuracy and recall rates.