# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required libraries.

2.Upload and read the dataset.

3.Check for any null values using the isnull() function.

4.From sklearn.tree import DecisionTreeClassifier and use criterion as entropy.

5.Find the accuracy of the model and predict the required values by importing the required module from sklearn.

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: Deepika R
RegisterNumber: 212224230054

import pandas as pd
from sklearn.tree import DecisionTreeClassifier,plot_tree
data=pd.read_csv("Employee.csv")
data.head()
data.info()
data.isnull().sum()
data["left"].value_counts()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()
x = data[["satisfaction_level", "last_evaluation", "number_project", "average_montly_hours",
          "time_spend_company", "Work_accident", "promotion_last_5years", "salary"]]
x.head() #no departments and no left
y=data["left"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
dt.predict([[0.5,0.8,9,260,6,0,1,2]])
plt.figure(figsize=(15,10))
plot_tree(dt,feature_names=x.columns,class_names=['stayed','left'],filled=True)
*/
```

## Output:
<img width="1506" height="244" alt="image" src="https://github.com/user-attachments/assets/653815a7-cfc2-4400-968c-fcf45224c464" />

<img width="1500" height="350" alt="image" src="https://github.com/user-attachments/assets/cd5cee8f-a70c-4ad5-ae9e-ac4bba9cd299" />

<img width="1504" height="436" alt="image" src="https://github.com/user-attachments/assets/9ea63d4b-9d9f-4d41-a8e4-b3b967ccc3a9" />

<img width="1503" height="218" alt="image" src="https://github.com/user-attachments/assets/29678490-855c-4e10-a403-fa0a5efc05dd" />

<img width="1509" height="305" alt="image" src="https://github.com/user-attachments/assets/1c592afa-1758-4295-8552-5c33e56a8862" />

<img width="1501" height="305" alt="image" src="https://github.com/user-attachments/assets/184b4083-d259-48b1-95b4-ca55e8c00b32" />

<img width="1504" height="283" alt="image" src="https://github.com/user-attachments/assets/923d490a-e2aa-48ea-a4f5-b276a3d9fcc2" />

<img width="1504" height="117" alt="image" src="https://github.com/user-attachments/assets/578af19d-9570-4235-bab0-570ca8dd8065" />

<img width="1509" height="104" alt="image" src="https://github.com/user-attachments/assets/d05299f2-e20a-41af-9877-95f282e73d17" />

<img width="1792" height="786" alt="Screenshot 2025-09-27 141210" src="https://github.com/user-attachments/assets/f4fc5727-8b01-450f-9fa0-6ae665338502" />


## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
