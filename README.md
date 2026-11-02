# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries and create a dataset containing students' CGPA and placement status.
2. Separate the input feature and target variable, then split the dataset into training and testing sets.
3. Train the Logistic Regression model using the training data.
4. Predict the placement status of students and display the model's accuracy.

## Program:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: Anitha P
RegisterNumber:  212225040022


import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import accuracy_score

data = {
    'CGPA': [6.1, 7.2, 5.8, 8.5, 6.9, 9.1, 7.8, 5.5, 8.2, 6.4,
             9.3, 7.5, 5.9, 8.8, 7.1, 6.7, 9.0, 5.6, 8.0, 7.7],
    'Placement': [0, 1, 0, 1, 1, 1, 1, 0, 1, 0,
                  1, 1, 0, 1, 1, 0, 1, 0, 1, 1]
}

df = pd.DataFrame(data)

X = df[['CGPA']]
y = df['Placement']

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.3, random_state=42, stratify=y
)

model = LogisticRegression()
model.fit(X_train, y_train)

y_pred = model.predict(X_test)

print("Student Placement Prediction")
print("Actual Placement Status:", list(y_test))
print("Predicted Placement Status:", list(y_pred))
print("Accuracy:", round(accuracy_score(y_test, y_pred) * 100, 2), "%")

student_cgpa = pd.DataFrame({'CGPA': [7.5]})
result = model.predict(student_cgpa)

if result[0] == 1:
    print("Placement Prediction for CGPA 7.5: Placed")
else:
    print("Placement Prediction for CGPA 7.5: Not Placed")
*/
```

## Output:
<img width="1180" height="132" alt="image" src="https://github.com/user-attachments/assets/0f9a49bf-661a-4b34-a233-d0b58ede8b18" />

## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
