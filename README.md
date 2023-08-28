# TextClassification_Survey
#### Brief survey of text classification methods and models

### Background Info:
- 20newsgroup dataset from scikit-learn is used in all tests
- all tests pre-processed with TF/IDF vectorizer
- For some tests, lemmatization is applied to the text data (will be noted)
- hyper-parameter tuning techniques will be explicated for each test

## Models Tested

### 1. BinomialNB #1
Out-of-box model without lemmatization or additional hyper-parameter tuning. 
### 2. BinomialNB #2
Model includes a grid search.
### 3. BinomialNB #3
Model includes grid search and lemmatized text data
### 4. Logistic Regression #1
Out-of-box model
### 5. Logistic Regression #2
Model includes grid search
### 6. KNN #1
Out-of-box
### 7. KNN #2
Model with grid search
### 8. XGBoost #1
Out-of-box
### 9. XGBoost #2
Model with random search and lemmatization
### 10. Random Forest #1
Out-of-box
### 11. Random Forest #2
Model with random search and lemmatization
### 12. Pytorch NN #1
Out-of-box
### 13. Pytorch NN #2
Model with Optuna hyperparameter tuning
### 14. Pytorch NN #3
Model with Optuna and lemmatized text data

## Results

Model | #1 | #2 | #3 | #4 | #5 | #6 | #7 | #8 | #9 | #10 | #11 | #12 | #13 | #14
--- | --- | --- | --- |--- |--- |--- |--- |--- |--- |--- |--- |--- |--- |---
Weighted F1 Score | 0.77873 | 0.84537 | 0.85476 | 0.81662 | 0.81662 | 0.41976 | 0.44363 | 0.79292 | 0.81329 | 0.75822 | 0.80902 | 0.39065 | 0.84101 | 0.85501

## Conclusions
- Pytorch NN with lemmatization and Optuna tuning performed the best
- Out-of-box Pytorch NN performed the worst
- KNN had generally poor performance, while MultinomialNB had generally good performance
- Lemmatization boosted F1 score every time it was used
