# Mashable Online News Sharing Data
## Goal
1. Predict the number of shares an article will accumulate.
2. Understand what makes an article popular.

Response (Y) = number of shares,
Predictors (X) = article qualities,
Observations (n) = 39644,
Variables (p) = 59.

## Categorical Examples
Data channel (Tech, Lifestyle, etc.)
(6 categories),
Day of week published
(8 categories - Was it on Weekend?).

## Continuous Examples
Stop/non-stop word count,
Image/video count,
Text subjectivity,
Word polarity.

## Data Pre-processing
1. Removed 6 unrelated predictors.
2. 0 near-zero variance predictors.
3. 2 highly correlated predictors (cutoff = 0.90).
4. Center, scale, and Box-Cox.
5. LGOCV resampling.

## Classification Approach
1. Originally treated data as continuous (counts ranging from 1 to 843300).
2. Poor model performance - Linear (PLS) Rsquared = 0.13, Nonlinear (SVM) Rsquared = 0.15.
3. Ease model expectations by switching to classification.
4. Split number of shares into low, medium, and high classes.
5. Still indicates what features lead to popular articles.
6. More valuable model.
7. Low: 1 - 947, Medium: 948 - 3398, High: 3399 and above.

## Summary

1. Developed a Linear and Non-linear classification models to predict the number of shares an article will accumulate and understand what makes an article popular.
2. Performed pre-processing such as removing the censored data, near-zero variance and highly correlated variables, visualizing missing values using missmap diagram.
3. Transformed the data by centering, scaling and applied Yeo Johnson transformation method.
4. Split the whole dataset into train and test to perform the validation of the models generated and stratified random sampling was used to ensure any training set accurately represented the population distribution to properly generalize models.
5. Implemented leave group out cross-validation (LGOCV) resampling method techniques and calculated the accuracy, AUC to tune the parameters of the model and provide honest estimations of classification performance.
6. Build following 12 linear and non-linear classification models to predict the number of shares.
    • Logistic Regression
    • Linear Discriminant Analysis (LDA)
    • Partial Least Squares Discriminant Analysis (PLSDA)
    • Penalized Model
    • Nearest Shrunken Centroids (NSC)
    • Sparse Linear Discriminant Analysis
    • Neural Network
    • Flexible Discriminant Analysis (FDA)
    • Naive Bayes
    • Support Vector Machines
    • Mixture Discriminant Analysis (MDA)
    • K-Nearest Neighbors
7. The logistic regression, penalized linear model, and flexible discriminant analysis models were found to be the three best performers in terms of accuracy
8. Generated an ensemble model by combining the output of all the above twelve models to achieve 100% accuracy on the test dataset

