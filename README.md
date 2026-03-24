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
from sklearn.datasets import load_iris
from sklearn.linear_model import SGDClassifier
from sklearn.model_selection import train_test_split
from sklearn.metrics import accuracy_score,confusion_matrix

iris = load_iris()

df = pd.DataFrame(iris.data, columns=iris.feature_names)
df['target'] = iris.target
print(df.head())

X = df.drop('target', axis=1)
y = df['target']

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

sgd_clf = SGDClassifier(max_iter = 1000, tol = 1e-3)
sgd_clf.fit(X_train, y_train)



y_pred = sgd_clf.predict(X_test)
accuracy = accuracy_score(y_test, y_pred)
print(f"Accuracy: {accuracy:.3f}")


cm = confusion_matrix(y_test, y_pred)
print("Confusion Matrix:")
print(cm)

```

## Output:/>
<img width="1218" height="532" alt="image" src="https://github.com/user-attachments/assets/548f7b69-c521-4441-9f2a-95c48f03b160" />
<img width="1218" height="532" alt="image" src="https://github.com/user-attachments/assets/cdadf2b9-5b99-4b62-8ea0-d2b91e23c66d" />
<img width="1218" height="532" alt="image" src="https://github.com/user-attachments/assets/839723c2-7131-4caf-b7c3-53cf18acbda6" />








## Result:
Thus, the program to implement the prediction of the Iris species using SGD Classifier is written and verified using Python programming.
