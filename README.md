🏠 California Housing Price Prediction
📌 Project Overview

This project focuses on predicting California housing prices using various regression algorithms, including Ridge Regression, Lasso Regression, and Random Forest Regression.
The dataset, obtained from the California Housing dataset in Scikit-learn, includes demographic and geographic data such as median income, house age, average rooms, and latitude/longitude.

The primary objective is to build and compare multiple regression models to identify which algorithm delivers the best predictive accuracy.

🧠 Key Objectives

Perform exploratory data analysis (EDA) to understand housing trends.

Train and evaluate multiple regression models.

Optimize hyperparameters using cross-validation and grid search.

Compare model performance based on the R² score and prediction error distribution.

📂 Dataset Information

Dataset: California Housing (from sklearn.datasets.fetch_california_housing)

Number of Instances: 20,640
Number of Features: 8 numeric predictive attributes
Target Variable: Median House Value (in $100,000s)

Feature	Description
MedInc	Median income in block group
HouseAge	Median house age in block group
AveRooms	Average number of rooms per household
AveBedrms	Average number of bedrooms per household
Population	Block group population
AveOccup	Average number of household members
Latitude	Block group latitude
Longitude	Block group longitude
🔍 Project Workflow

Data Loading and Preparation – Load the California housing dataset and create a DataFrame with appropriate column names.

Exploratory Data Analysis (EDA) – Explore relationships among variables, visualize distributions, and understand data patterns.

Data Preprocessing –

Split the data into training and testing sets (70:30 ratio).

Standardize numerical features using StandardScaler to normalize the dataset.

Model Building –

Implement Ridge Regression to control multicollinearity through L2 regularization.

Implement Lasso Regression to perform both regularization and feature selection using L1 regularization.

Implement Random Forest Regression as a nonlinear ensemble method for improved accuracy.

Hyperparameter Tuning – Use GridSearchCV to find optimal values for α (lambda) in Ridge and Lasso models.

Model Evaluation –

Evaluate all models using R² score and Mean Squared Error (MSE).

Visualize prediction error distributions with KDE plots.

Model Comparison – Compare all three models based on their predictive accuracy and interpretability.

📊 Model Performance Summary
Model	Best Parameters	Cross-Validation MSE	R² Score on Test Data
Ridge Regression	α = 10	-0.5268	0.5959
Lasso Regression	α = 0.001	-	0.5964
Random Forest Regression	n_estimators = 200	-	0.8067

Key Insight:

Random Forest Regression provided the best performance with an R² score of approximately 0.81, significantly outperforming linear models.

Ridge and Lasso Regression performed similarly, with R² scores around 0.59–0.60, indicating moderate linear relationships between features and housing prices.

💡 Insights and Learnings

Median income (MedInc) is the most important predictor of house value in California.

Regularization in Ridge and Lasso helps prevent overfitting by penalizing large coefficients.

Increasing the regularization parameter (λ) in Ridge causes the coefficients to shrink, stabilizing learning and reducing variance.

Random Forest captures complex nonlinear relationships that simple linear models cannot.

⚙️ Technologies Used

Python

NumPy

Pandas

Scikit-learn

Seaborn

Matplotlib

📈 Evaluation Metrics

R² Score (Coefficient of Determination): Measures how well the model explains the variance in target values.

Mean Squared Error (MSE): Evaluates average squared differences between actual and predicted values.

Residual Distribution Analysis: Ensures predictions are symmetrically distributed around zero.

🚀 Future Improvements

Experiment with XGBoost or Gradient Boosting Regressor for enhanced performance.

Incorporate feature importance analysis and interpretability metrics (e.g., SHAP values).

Use geospatial visualization to map housing price variations across California.

Develop a web-based dashboard for interactive prediction and visualization.

👤 Author

Your Name : Awais Qarni
📧 Email: qarni4126@gmail.com

🌐 GitHub: qarni4126-ui
