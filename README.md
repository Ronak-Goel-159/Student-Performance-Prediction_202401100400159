# Predicting Exam Scores using Linear Regression

This project demonstrates the use of linear regression to predict exam scores based on three features: study hours, prior grades, and study method. The dataset is synthetically generated using random values to simulate real-world conditions. The linear regression model is trained and evaluated to predict exam scores and assess model performance.

## Table of Contents
1. Data Creation
2. Data Visualization
3. Model Training
4. Model Evaluation
5. Predictions vs Actual

### Data Creation
In this section, we create a synthetic dataset using random values for the following features:
- Study Hours: Simulated as a normal distribution with a mean of 5 hours and a standard deviation of 1.5 hours.
- Prior Grades: Simulated as a normal distribution with a mean of 70 and a standard deviation of 10.
- Study Method: A categorical variable, randomly assigned one of three values: 1 (self-study), 2 (group study), or 3 (online courses).

The target variable, Exam Scores, is generated using a linear combination of these features plus some random noise. The relationship is as follows:

    Exam Scores = (Study Hours * 3) + (Prior Grades * 0.4) + (Study Method * 5) + Noise

A pandas DataFrame is created with these values, and the first few rows of the dataset are displayed.

### Data Visualization
We use matplotlib to visualize the relationship between Study Hours and Exam Scores. A scatter plot is generated to help understand how increasing study hours might correlate with higher exam scores.

```python
plt.scatter(data['Study Hours'], data['Exam Scores'], color='blue')
plt.title("Study Hours vs Exam Scores")
plt.xlabel("Study Hours")
plt.ylabel("Exam Scores")
plt.show()
