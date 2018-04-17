# Mashable Online News Sharing Data
# Goal
1. Predict the number of shares an article will accumulate.
2. Understand what makes an article popular.

Response (Y) = number of shares,
Predictors (X) = article qualities,
Observations (n) = 39644,
Variables (p) = 59.

# Categorical Examples
Data channel (Tech, Lifestyle, etc.)
(6 categories),
Day of week published
(8 categories - Was it on Weekend?).

# Continuous Examples
Stop/non-stop word count,
Image/video count,
Text subjectivity,
Word polarity.

# Data Pre-processing
1. Removed 6 unrelated predictors.
2. 0 near-zero variance predictors.
3. 2 highly correlated predictors (cutoff = 0.90).
4. Center, scale, and Box-Cox.
5. LGOCV resampling.

# Classification Approach
1. Originally treated data as continuous (counts ranging from 1 to 843300).
2. Poor model performance - Linear (PLS) Rsquared = 0.13, Nonlinear (SVM) Rsquared = 0.15.
3. Ease model expectations by switching to classification.
4. Split number of shares into low, medium, and high classes.
5. Still indicates what features lead to popular articles.
6. More valuable model.
7. Low: 1 - 947, Medium: 948 - 3398, High: 3399 and above.

