# Student Performance Analytics and Prediction Using Machine Learning

A machine learning project that explores student academic performance and predicts final mathematics grades using regression algorithms.

## Project Overview

The objective of this project is to analyse student performance data and develop machine learning models to predict students' final mathematics grades (`G3`) using demographic, family, social and academic features.

Previous-period grades (`G1` and `G2`) were excluded from the input features to explore prediction without relying on earlier examination marks.

## Dataset

- **Dataset:** UCI Student Performance Dataset
- **Subset:** Mathematics (`student-mat.csv`)
- **Total records:** 395 students
- **Input features:** 30
- **Target variable:** G3 (final mathematics grade)
- **Training records:** 316
- **Testing records:** 79
- **Train-test split:** 80:20

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab

## Project Workflow

1. Dataset loading and inspection.
2. Data cleaning and validation.
3. Exploratory Data Analysis (EDA).
4. Numerical and categorical feature identification.
5. Feature preprocessing using StandardScaler and OneHotEncoder.
6. Train-test splitting.
7. Baseline model implementation.
8. Linear Regression model training.
9. Random Forest Regression model training.
10. Model evaluation and comparison.
11. Feature importance analysis.

## Machine Learning Models

Three models were implemented and evaluated:

1. Mean Baseline Model
2. Linear Regression
3. Random Forest Regression

## Model Evaluation

The models were evaluated using three regression metrics:

- **MAE (Mean Absolute Error):** Measures the average absolute difference between actual and predicted grades.
- **RMSE (Root Mean Squared Error):** Measures prediction error while penalising larger errors more heavily.
- **R² Score:** Measures how much variation in the target variable is explained by the model.

### Results

| Model | MAE | RMSE | R² Score |
|---|---:|---:|---:|
| Mean Baseline | 3.6459 | 4.5502 | -0.0097 |
| Linear Regression | 3.3953 | 4.1957 | 0.1415 |
| Random Forest | 2.9938 | 3.7508 | 0.3139 |

Random Forest achieved the best performance among the three models, with the lowest MAE and RMSE and the highest R² score.

Its R² score of approximately 0.314 indicates that it explains around 31.4% of the variation in the test-set grades. The model's predictive performance is moderate and leaves room for improvement.

## Feature Importance

The five most important features identified by the Random Forest model were:

1. Absences
2. Failures
3. Health
4. Going out
5. Age

Feature importance represents predictive contribution within the trained model. It does not establish causal relationships.

## Visualisations

The project includes visualisations such as:

- Final grade distribution.
- Study time versus final grades.
- Numerical feature correlation heatmap.
- Absences versus final grades.
- Actual versus predicted grades.
- Random Forest feature importance.

## Repository Contents

- `Student_Performance_Analytics.ipynb` - Complete Jupyter notebook containing data exploration, preprocessing, model training, evaluation and visualisations.
- `README.md` - Project documentation.
- `requirements.txt` - Required Python libraries.

## Limitations

- The dataset contains only 395 mathematics student records.
- The data was collected from two Portuguese schools, limiting generalisability.
- Previous-period grades G1 and G2 were excluded.
- The model demonstrates moderate predictive performance.
- Predictions should not be treated as definitive assessments of individual students.

## Future Improvements

- Perform hyperparameter tuning.
- Evaluate models using cross-validation.
- Explore additional regression algorithms.
- Develop an interactive student grade prediction interface.

## Author

**Shreya K**

GitHub: https://github.com/shreyakannappan4-pixel

Project Repository: https://github.com/shreyakannappan4-pixel/student-performance-ml-prediction
