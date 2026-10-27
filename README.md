# Student Score Prediction

Predicting students' exam scores from study habits and background factors using regression models.

## Problem
Can we predict a student's final exam score, and which factors matter most?

## Dataset
[Student Performance Factors](https://www.kaggle.com/datasets/lainguyn123/student-performance-factors) (Kaggle): 6,607 students, 20 features.

## Approach
1. Loaded the data and checked missing values and duplicates
2. Visualized study hours vs. exam score
3. Split the data into 80% training and 20% testing
4. Trained a Linear Regression model on study hours
5. Evaluated with MAE, RMSE and R²
6. Bonus: tried Polynomial Regression and different feature combinations

## Results

| Model | MAE | RMSE | R² |
|---|---|---|---|
| Linear (Hours only) | 2.45 | 3.29 | 0.232 |
| Polynomial degree 2 | 2.44 | 3.29 | 0.233 |
| Polynomial degree 3 | 2.44 | 3.29 | 0.233 |
| Linear (6 numeric features) | 1.27 | 2.25 | 0.642 |
| Linear (all features) | 0.45 | 1.80 | 0.770 |

## Key Findings
- Study hours alone explain only about 23% of score variation.
- Polynomial regression did not help, so the relationship is close to linear.
- Adding features such as attendance, previous scores and sleep hours raised R² from 0.23 to 0.77.

## Tech Stack
Python, Pandas, Matplotlib, Scikit-learn

## How to Run
1. Clone the repo
2. Install dependencies: `pip install pandas matplotlib scikit-learn`
3. Open `student_score_prediction.ipynb` in Jupyter or Google Colab and run all cells
