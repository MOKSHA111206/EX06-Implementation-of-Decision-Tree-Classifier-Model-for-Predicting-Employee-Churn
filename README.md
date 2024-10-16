# EX 6 Implementation of Decision Tree Classifier Model for Predicting Employee Churn
## DATE:
## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.import the employee churn dataset

2.if the dataset has missing values handel them using techiniques such as mean

3.convert categorical variables into numerical format using techniques such as noe_hot encoding

4.scale features if necessary using standardscaler
 

## Program:
```
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: AMMINENI MOKSHASREE
RegisterNumber:  2305001001

import pandas as pd
from sklearn.tree import DecisionTreeClassifier,plot_tree
from sklearn.preprocessing import LabelEncoder
import matplotlib.pyplot as plt
df=pd.read_csv('/content/Employee_EX6.csv')
data = pd.read_csv('/content/Employee_EX6.csv')
data = df.copy()
data
le = LabelEncoder()
data['salary'] = le.fit_transform(data['salary'])
data
X = data.drop(['Departments','left'],axis=1)
Y = data['left']
clf = DecisionTreeClassifier()
clf.fit(X,Y)
plt.figure(figsize=(80,80))
plot_tree(clf, feature_names=X.columns,class_names=['LEFT','"NOT LEFT"'],filled=True,fontsize=14)
plt.show()
```

## Output:
![image](https://github.com/user-attachments/assets/9424b790-fa21-4e72-a1bf-36ae0df84e10)
![image](https://github.com/user-attachments/assets/30b48a18-24ca-4ac6-8cd0-c8db7d16d2a9)
![image](https://github.com/user-attachments/assets/17c14be7-e511-4af5-a12c-e66678eb78d5)
![image](https://github.com/user-attachments/assets/2021987c-5a41-4dd7-9d6d-3f4800b54b94)



## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
