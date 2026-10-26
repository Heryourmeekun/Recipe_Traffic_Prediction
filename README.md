# 🍳 Recipe Traffic Prediction

A machine-learning project that predicts whether a recipe is likely to generate high website traffic based on its nutritional information, category, and serving size. The goal is to help a recipe website make data-informed decisions about which recipes to feature.

## 🎯 Project Objectives

- Predict whether a recipe will generate high or low website traffic.
- Identify recipe characteristics associated with higher traffic.
- Compare multiple classification algorithms.
- Improve model precision through hyperparameter tuning.
- Translate model results into actionable business recommendations.

## 🛠️ Technologies Used

- **Python** — model development and data analysis
- **Pandas & NumPy** — data cleaning and manipulation
- **SciPy** — Yeo-Johnson transformation
- **Matplotlib & Seaborn** — exploratory data analysis and visualisation
- **Scikit-learn** — preprocessing, classification, evaluation, cross-validation, and hyperparameter tuning
- **LightGBM & XGBoost** — gradient-boosting classifiers

## 📊 Data Preparation and Exploration

The dataset initially contained 947 recipe records and eight columns, including nutritional information, recipe category, serving size, and the traffic label.

The preprocessing workflow included:

- Inspecting data types, missing values, and category distributions.
- Standardising recipe categories and cleaning serving-size values.
- Converting the target variable into a binary classification label.
- Handling missing nutritional values.
- Exploring numerical features and recipe categories to identify patterns associated with traffic.
- Applying the Yeo-Johnson transformation to address skewed numerical features.

After removing records with missing nutritional values, 895 records remained for modelling.

## 🤖 Machine-Learning Models

I implemented and compared seven classification algorithms:

1. Gaussian Naive Bayes
2. Logistic Regression
3. Decision Tree
4. Random Forest
5. Support Vector Machine (SVM)
6. LightGBM
7. XGBoost

The models were evaluated using an 80/20 train-test split. Evaluation metrics included accuracy, precision, recall, F1-score, and confusion matrices.

## 🔬 Hyperparameter Tuning and Results

Gaussian Naive Bayes was selected for further optimisation. I used `GridSearchCV` with three-fold cross-validation to tune its `var_smoothing` parameter, using precision as the optimisation metric.

**Key result:** Test precision improved from **0.88 to approximately 0.905** after tuning, with the best parameter value of `var_smoothing = 1e-11`.

This experiment demonstrated the value of systematic hyperparameter tuning and selecting evaluation metrics according to the project's business objectives.

## 💡 Business Insights

The exploratory analysis suggested that recipe category can help inform content decisions. The project identified Vegetable, Potato, and Pork recipes as categories associated with higher traffic, while Beverages tended to attract lower traffic in the analysed dataset.

These findings can help guide decisions about recipe promotion, although they should be validated against future website traffic data before being used as production rules.

## 📚 What I Learned

- Preparing real-world data for machine-learning workflows.
- Comparing multiple classification algorithms using consistent evaluation metrics.
- Applying cross-validation and hyperparameter optimisation.
- Interpreting confusion matrices and the trade-offs between precision and recall.
- Translating predictive results into practical business recommendations.

## 🔗 Project Repository

[**View the complete project on GitHub**](https://github.com/Heryourmeekun/Recipe_Traffic_Prediction)

