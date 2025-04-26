🏠 California Housing Price Prediction (Regression Models Comparison)
📋 Project Overview
This project explores predicting California housing prices using regression models.
We apply Linear Regression, Ridge Regression, and Lasso Regression to the dataset and compare their performances based on cross-validated Mean Squared Error (MSE).

Additionally, we perform a detailed univariate, bivariate, and multivariate analysis to understand feature relationships with the target variable.

📚 Dataset
Features:

MedInc, HouseAge, AveRooms, AveBedrms, Population, AveOccup, Latitude, Longitude

Target:

price

Shape: (20640, 9)

📊 Exploratory Data Analysis (EDA)
🔹 Univariate Analysis
Studied distribution of individual features using histograms.

Observed patterns like skewness and spread in MedInc, HouseAge, etc.

🔹 Bivariate Analysis
Explored relationships between each feature and price.

Used scatterplots and correlation checks.

🔹 Multivariate Analysis
Analyzed how multiple features together influence the target.

Observed combined effects like MedInc + Latitude on price.

🤖 Model Building and Cross-Validation
➡️ Models Implemented:
Linear Regression (Baseline model)

Ridge Regression (L2 Regularization)

Lasso Regression (L1 Regularization)

➡️ Model Evaluation:
Used 5-Fold Cross-Validation to calculate Mean Squared Error (MSE) for each model.

Used cross_val_score with scoring='neg_mean_squared_error' (inverted to positive MSE for reporting).

➡️ Best Model Selection:
Compared models based on average MSE.

Visualized comparison using a bar plot.

📈 Results Summary

Model	Mean MSE
Linear Regression	~0.558
Ridge Regression	~0.558
Lasso Regression	~0.662
Ridge Regression performed slightly better than Lasso.

Linear Regression and Ridge Regression performed similarly in this dataset.

Lasso Regression showed slightly higher error, indicating possible underfitting due to feature elimination.

📊 Final Visualization
Bar chart comparing MSE across Linear, Ridge, and Lasso models.

Lower MSE indicates better model performance.

🚀 Key Learnings
Importance of cross-validation to avoid biased train-test splits.

Understanding the behavior of regularization techniques (Ridge vs Lasso).

Visual comparison gives clear intuition on model selection.

EDA (univariate, bivariate, multivariate) is critical for feature understanding before modeling.

📎 How to Run
bash
Copy
Edit
# Install requirements
pip install pandas scikit-learn matplotlib numpy

# Run the Python notebook or script
