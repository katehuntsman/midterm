# ml-04-midterm

# Mushroom Classification Project

## Overview
This project focuses on classifying mushrooms as either edible or poisonous based on a variety of features. The dataset contains multiple categorical features describing the physical characteristics of the mushrooms, such as cap shape, odor, and gill size. The goal of this project is to build predictive models to classify mushrooms with high accuracy. The dataset has been pre-processed, and two classification models, Decision Tree and Random Forest, are trained to predict whether a mushroom is edible or poisonous.

## What's Included
- **Mushroom Dataset**: Pre-processed and encoded data, where categorical features are converted into numerical format for machine learning models.
- **Two Classification Models**: 
  - **Decision Tree**: A simple but effective model for classification tasks.
  - **Random Forest**: An ensemble of decision trees that improves performance by aggregating the predictions from multiple trees.
- **Visualizations**:
  - Distributions of features (e.g., histograms, count plots)
  - Confusion matrix heatmaps to visualize model performance.
- **Performance Evaluations**:
  - Metrics like accuracy, precision, recall, and F1-score for both models.
  - Class-wise precision, recall, and F1-score for better understanding of the model's behavior.
- **Reflections for Each Step**: Insights into data cleaning, feature engineering, model training, and evaluation.

## Key Results
- **Best Model**: Random Forest, which provided superior classification accuracy.
- **Accuracy**: Both models (Decision Tree and Random Forest) achieved approximately 1.0% accuracy, indicating a perfect classification.
- **Key Predictive Features**:
  - **Odor**: Strongly correlated with the target class, where "foul" or "almond" odors often corresponded to poisonous mushrooms.
  - **Gill Size** and **Spore Print Color** were also strong predictors.

## Files
- **`classification_huntsman.ipynb`**: The main Jupyter notebook containing the full analysis pipeline, including data exploration, preprocessing, model training, and evaluation.
- **`data/mushrooms.csv`**: The dataset used for the classification task, which includes various attributes of mushrooms.
- **`peer_review.md`**: A document with a detailed review of a classmate's work on a similar project, focusing on strengths and areas for improvement.

## Create and Activate Virtual Environment
```
python3 -m venv .venv
source .venv/bin/activate
```

## Install Required Dependencies
```
pip install -r requirements.txt
```


## Project Outline
### Section 1. Import and Inspect the Data
- 1.1 Load the dataset and display the first 10 rows.
- 1.2 Check for missing values and display summary statistics.

Reflection 1: What do you notice about the dataset? Are there any data issues?

Missing Data: The dataset contained missing values in the stalk-root feature (about 30% of the rows). After considering the impact of missing data, we chose to impute the missing values with the most frequent category (mode), as this was the most reasonable choice given the categorical nature of the feature.

Feature Removal: We identified that odor was highly correlated with the target class. Given that it could easily overfit the model, we decided to remove it to make the classification problem more realistic and challenging.

### Section 2. Data Exploration and Preparation
- 2.1 Explore data patterns and distributions
  - Create histograms, boxplots, and count plots for categorical variables (as applicable).
  - Identify patterns, outliers, and anomalies in feature distributions.
  - Check for class imbalance in the target variable (as applicable).
- 2.2 Handle missing values and clean data
  - Impute or drop missing values (as applicable).
  - Remove or transform outliers (as applicable).
  - Convert categorical data to numerical format using encoding (as applicable).
- 2.3 Feature selection and engineering
  - Create new features (as applicable).
  - Transform or combine existing features to improve model performance (as applicable).
  - Scale or normalize data (as applicable).

Reflection 2: What patterns or anomalies do you see? Do any features stand out? What preprocessing steps were necessary to clean and improve the data? Did you create or modify any features to improve performance?

Feature Distribution: We explored the distribution of the categorical features using count plots. Several features had dominant categories (e.g., "w" for cap-color, "p" for gill-color), while others had rare categories. This gave insights into which features were more informative for classification and which could potentially be dropped.

Class Imbalance: The class distribution between edible and poisonous mushrooms was relatively balanced, so no oversampling or undersampling was needed.

Encoding Categorical Variables: To convert the categorical data into a numerical format suitable for machine learning models, we applied label encoding. For each feature, we mapped each unique category to a numerical label.

Feature Engineering: We did not create or modify any features, but we carefully selected the relevant features based on their distributions and importance to the target variable.


### Section 3. Feature Selection and Justification
- 3.1 Choose features and target
  - Select two or more input features (numerical for regression, numerical and/or categorical for classification)
  - Select a target variable (as applicable)
    - Regression: Continuous target variable (e.g., price, temperature).
    - Classification: Categorical target variable (e.g., gender, species).
    - Clustering: No target variable.
  - Justify your selection with reasoning.
- 3.2 Define X and y
  - Assign input features to X
  - Assign target variable to y (as applicable)

Reflection 3: Why did you choose these features? How might they impact predictions or accuracy?

Model Comparison: We trained both a Decision Tree and a Random Forest model. Both models performed excellently, achieving near-perfect accuracy. However, Random Forest showed superior performance by leveraging an ensemble approach.

Confusion Matrix: The confusion matrix showed no misclassifications, with both models accurately identifying edible and poisonous mushrooms. This confirms the effectiveness of the models with the pre-processed data.

Performance Metrics: Precision, recall, and F1-scores for both models were all 1.0, indicating perfect classification on both classes.


### Section 4. Train a Model (Classification: Choose 1: Decision Tree, Random Forest, Logistic Regression)
- 4.1 Split the data into training and test sets using train_test_split (or StratifiedShuffleSplit if class imbalance is an issue).
- 4.2 Train model using Scikit-Learn model.fit() method.
- 4.3 Evalulate performance, for example:
  - Regression: R^2, MAE, RMSE (RMSE has been recently updated)
  - Classification: Accuracy, Precision, Recall, F1-score, Confusion Matrix
  - Clustering: Inertia, Silhouette Score

Reflection 4: How well did the model perform? Any surprises in the results?

Accuracy: Both models performed with an accuracy of 1.0%, which is an excellent result given the simplicity of the classification task. However, this may be a result of overfitting, particularly due to the strong predictive power of the odor feature (which was later removed).

Surprises: The most surprising result was how well both models performed despite the limited number of features and the lack of complex feature engineering. Random Forest, in particular, handled the data well by aggregating multiple decision trees.


### Section 5. Improve the Model or Try Alternates (Implement a Second Option)
- 5.1 Train an alternative classifier (e.g., Decision Tree, Random Forest, Logistic Regression) OR adjust hyperparameters on the original model.
- 5.2 Compare performance of all models across the same performance metrics.

Reflection 5: Which model performed better? Why might one classifier be more effective in this specific case?

### Section 6. Final Thoughts & Insights
- 6.1 Summarize findings.
- 6.2 Discuss challenges faced.
- 6.3 If you had more time, what would you try next?

Reflection 6: What did you learn from this project?
