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

Methodology:
Preprocessing:

Missing values were handled by dropping rows or imputing them as required.
The dataset was standardized using StandardScaler to ensure all features have zero mean and unit variance, which is critical for models sensitive to scaling.
Encoded categorical variables (e.g., Gender) for use in regression models.
Model Training: Six regression models were trained and evaluated:

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
