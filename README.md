# Student Performance Analytics and Prediction Using Machine Learning

## Project Overview

This project explores student academic performance using data analysis and machine learning techniques. It uses demographic, family, social, and academic-related information to predict students' final mathematics grades.

Two regression algorithms, Linear Regression and Random Forest Regression, are implemented and evaluated to compare their predictive performance.

## Objectives

- Explore and analyse student performance data.
- Identify patterns and relationships between student characteristics and final grades.
- Apply data preprocessing techniques to prepare the dataset.
- Train regression models to predict final mathematics grades.
- Evaluate and compare model performance using regression metrics.
- Identify features that contribute to the Random Forest model's predictions.

## Dataset

**Source:** [UCI Student Performance Dataset](https://archive.ics.uci.edu/dataset/320/student+performance)

The project uses the Mathematics subset (`student-mat.csv`).

| Dataset detail | Value |
|---|---:|
| Total records | 395 |
| Original columns | 33 |
| Input features used | 30 |
| Training records | 316 |
| Testing records | 79 |
| Target variable | G3 |

The target variable `G3` represents the student's final mathematics grade, on a scale from 0 to 20.

The previous-period grades `G1` and `G2` were excluded to explore prediction using other available student characteristics.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab

## Project Workflow

1. **Data Collection:** Downloaded and loaded the Mathematics dataset.
2. **Data Exploration:** Examined the dataset structure, descriptive statistics, and feature types.
3. **Data Cleaning:** Checked for missing values and duplicate records.
4. **Exploratory Data Analysis:** Visualised grade distributions, study time, absences, and numerical correlations.
5. **Feature Selection:** Selected 30 input features and the final grade (`G3`) as the target.
6. **Data Preprocessing:** Applied StandardScaler to numerical features and OneHotEncoder to categorical features.
7. **Train-Test Split:** Divided the dataset into 80% training data and 20% testing data.
8. **Model Training:** Trained Linear Regression and Random Forest Regression models.
9. **Evaluation:** Compared the models using MAE, RMSE, and R².
10. **Feature Importance:** Examined the most influential features in the Random Forest model.

## Machine Learning Models

### 1. Linear Regression

A regression algorithm used to model relationships between input features and the target variable.

### 2. Random Forest Regression

An ensemble learning algorithm that combines multiple decision trees to generate predictions.

The Random Forest model was configured with 200 estimators.

## Model Evaluation Results

The models were evaluated using the same test dataset.

| Evaluation Metric | Linear Regression | Random Forest |
|---|---:|---:|
| MAE | 3.3953 | **2.9938** |
| RMSE | 4.1957 | **3.7508** |
| R² Score | 0.1415 | **0.3139** |

Random Forest performed better across all three evaluation metrics.

Its R² score indicates that it explained approximately 31.4% of the variation in final grades in the test set.

## Feature Importance

The five highest feature-importance scores from the Random Forest model were:

| Feature | Importance |
|---|---:|
| Absences | 0.1896 |
| Failures | 0.1445 |
| Health | 0.0493 |
| Going out | 0.0483 |
| Age | 0.0372 |

These scores represent the model's predictive feature importance and should not be interpreted as evidence of causation.

## Key Learnings

Through this project, I gained practical experience with:

- Data exploration and statistical summaries.
- Handling categorical and numerical features.
- Feature selection.
- Data preprocessing and encoding.
- Training regression models.
- Evaluating machine learning models.
- Visualising model predictions.
- Interpreting feature importance.

## Limitations

- The dataset contains only 395 mathematics student records.
- The data originates from two Portuguese schools and may not represent other student populations.
- Previous-period grades were excluded from the prediction features.
- The model demonstrates moderate predictive performance.
- Feature importance does not establish causal relationships.

The predictions should be treated as exploratory estimates, not definitive assessments of individual students.

## Future Improvements

- Experiment with additional regression algorithms.
- Perform hyperparameter tuning.
- Compare models against a baseline predictor.
- Explore alternative feature-selection techniques.
- Develop an interactive application for student grade prediction.

## Author

**Shreya K.**

B.Sc. Artificial Intelligence and Machine Learning Student

GitHub: [shreyakannappan4-pixel](https://github.com/shreyakannappan4-pixel)

---

*This project was developed as a hands-on learning project to understand the end-to-end machine learning workflow, from data exploration to model evaluation.*
