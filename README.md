# SGD-Classifier
## AIM:
To write a program to predict the type of species of the Iris flower using the SGD Classifier.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required libraries.

2.Upload and read the dataset.

3.Check for any null values using the isnull() function.

4.From sklearn.tree import DecisionTreeClassifier and use criterion as entropy.

5.Find the accuracy of the model and predict the required values by importing the required module from sklearn
## Program:
```
/*
Program to implement the prediction of iris species using SGD Classifier.
Developed by: Kamaleshwaran S 
RegisterNumber: 212225040165
*/
import pandas as pd
from IPython.display import display


data = pd.read_csv("Employee.csv")
print("===== DATA HEAD (5 ROWS) =====")
display(data.head())

print("\n===== DATA INFO =====")
print(data.info())

print("\n===== MISSING VALUES =====")
display(data.isnull().sum().to_frame("Missing Values"))

from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
data["salary"] = le.fit_transform(data["salary"])
print("\n===== X HEAD (5 ROWS) =====")
display(x.head())

from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test = train_test_split(
    x, y, test_size=0.2, random_state=100
)

from sklearn.tree import DecisionTreeClassifier
dt = DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train, y_train)


y_pred = dt.predict(x_test)

from sklearn import metrics
accuracy = metrics.accuracy_score(y_test, y_pred)
print("\n===== MODEL ACCURACY =====")
print("Accuracy:", accuracy)

# Prediction for new employee record
print("\n===== PREDICTION =====")
print(dt.predict([[0.5, 0.8, 9, 260, 6, 0, 1, 2]]))
```

## Output:
<img width="1424" height="284" alt="image" src="https://github.com/user-attachments/assets/d6429a7c-81cf-4776-8b36-51126b39d557" />
<img width="585" height="423" alt="image" src="https://github.com/user-attachments/assets/c13baa34-d5b9-4ce3-b138-a1b36746b2fe" />
<img width="441" height="428" alt="image" src="https://github.com/user-attachments/assets/c78cb501-7c5a-4e10-ab85-fa74ff039896" />
<img width="469" height="77" alt="image" src="https://github.com/user-attachments/assets/bfce5270-ef0c-4133-964e-f3dae0c9575a" />
<img width="1266" height="266" alt="image" src="https://github.com/user-attachments/assets/7a68b41a-f6ce-4a42-a21f-cc1f93ca965a" />
<img width="385" height="142" alt="image" src="https://github.com/user-attachments/assets/33fce426-453b-44e9-bfaf-d7f4d70c2429" />






## Result:
Thus, the program to implement the prediction of the Iris species using SGD Classifier is written and verified using Python programming.
