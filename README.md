# CGPA Prediction using Regression Models Based on Mental Health Effects
Objective:
The aim of this project is to predict a student's CGPA (Cumulative Grade Point Average) based on features related to their mental health, academic engagement, and personal habits.

Dataset:
The dataset includes 1000 rows and 14 columns with the following features:

Independent Variables (Predictors):
Gender: Encoded as binary values (0 for Male, 1 for Female).
Age: Student's age.
YearOfStudy: Encoded as integers (e.g., 1, 2, 3, 4).
Mental Health Metrics: Includes Depression, Anxiety, Panic Attacks, and whether they have received Specialist Treatment.
Lifestyle Metrics: Sleep Quality, Study Stress Level, Study Hours Per Week, and Symptom Frequency in the Last 7 Days.
Academic Engagement: Encoded values reflecting involvement in academic activities.
Dependent Variable (Target):
CGPA: Continuous label representing the student's academic performance.

Data Preprocessing:
Handle Missing Values:

Identify Missing Values: Use methods like .isnull() in pandas to identify missing values in the dataset.
Impute Missing Values:
For numerical columns, you can fill missing values with the mean, median, or mode.
For categorical columns, the mode (most frequent value) is often used for imputation.
Use advanced techniques like KNN imputation or interpolation when appropriate.
Remove Rows/Columns with Missing Values: If missing values are too many, you may decide to drop rows or columns with missing data using .dropna().
Handle Special Cases: For instance, if the missing data is significant (e.g., in time-series data), you might choose to backfill or forward-fill the missing entries.
Handle Duplication:

Detect Duplicates: Use .duplicated() in pandas to check for duplicate rows.
Remove Duplicates: Use .drop_duplicates() to eliminate duplicate rows from your dataset.
Data Transformation:

Scaling: Normalize or standardize data if needed, particularly for algorithms sensitive to scale (e.g., KNN, SVM).
Use StandardScaler() for standardization (zero mean, unit variance).
Use MinMaxScaler() for normalization (scales data between 0 and 1).

Exploratory Data Analysis (EDA):
Descriptive Statistics:

Central Tendency: Compute mean, median, and mode to understand the center of your data.
Dispersion: Measure the spread of data using variance, standard deviation, and interquartile range (IQR).
Skewness and Kurtosis: Check for data symmetry and tails using skewness and kurtosis.
Correlation: Calculate correlation coefficients (Pearson, Spearman) to understand the relationship between numeric variables.
Outliers: Identify potential outliers using statistical methods or visualization techniques like boxplots.
Data Distribution:

Histograms: Use histograms to visualize the frequency distribution of numerical features.
Boxplots: Plot boxplots to check for skewness and identify outliers.
Pair Plots/Correlation Heatmap: Use pair plots or a correlation heatmap to visualize relationships between variables.
Density Plots: These provide a smooth estimate of the distribution of a numerical variable.

Regression Models:

Linear Regression: To understand the linear relationships between features and CGPA.
Random Forest Regressor: To capture complex, non-linear relationships using an ensemble of decision trees.
XGBoost: A gradient-boosted framework for high-performance regression.
Support Vector Regressor (SVR): For modeling non-linear relationships with kernel functions.
K-Nearest Neighbors (KNN) Regressor: To explore instance-based learning effects.
MLPRegressor (Neural Network): To model highly complex relationships using multi-layered perceptrons.
Evaluation Metrics:

Mean Absolute Error (MAE): Average of absolute errors.
Mean Squared Error (MSE): Average of squared errors, sensitive to outliers.
Root Mean Squared Error (RMSE): Square root of MSE, representing error in the same unit as CGPA.
R-squared (R²): Explained variance to measure model performance.
Learning Curves and Predictions:

Plotted loss curves for MLPRegressor and learning curves for all models.
Evaluated predictions on test data, comparing model outputs to actual CGPA values.

Result:

Random Forest Regressor:

MAE: 0.1270
MSE: 0.0388
RMSE: 0.1970
R²: 0.9422
Best overall performance, with the lowest MAE, MSE, and RMSE, and the highest R².
Support Vector Regressor (SVR):

MAE: 0.1468
MSE: 0.0387
RMSE: 0.1967
R²: 0.9424
Very similar to Random Forest, with slightly better R², but a slightly higher MAE.
XGBoost:

MAE: 0.1427
MSE: 0.0496
RMSE: 0.2227
R²: 0.9261
Slightly higher MAE and MSE compared to Random Forest and SVR but still a strong model with good R².
K-Nearest Neighbors (KNN):

MAE: 0.1396
MSE: 0.0500
RMSE: 0.2236
R²: 0.9255
Performs similarly to XGBoost, with slightly higher MAE and MSE, and slightly lower R².
Multilayer Perceptron (MLP) Regressor:

MAE: 0.1761
MSE: 0.0530
RMSE: 0.2303
R²: 0.9210
Performs the least well among the models, with the highest MAE and RMSE and the lowest R².
Linear Regression:

MAE: 0.2087
MSE: 0.0628
RMSE: 0.2506
R²: 0.9065
The simplest model with the highest MAE and RMSE, and the lowest R², indicating it is outperformed by other models.

Summary:
Best performing model: Random Forest Regressor with the lowest MAE, MSE, RMSE, and the highest R².
Consistent high performers: Support Vector Regressor (SVR) and XGBoost, with only slight variations in performance.
Underperforming models: Linear Regression and MLP Regressor with higher errors and lower R² scores.
