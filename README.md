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
![Screenshot 2024-10-16 203247](https://github.com/user-attachments/assets/48986289-536a-4e40-b4f6-b68845533c5e)
![Screenshot 2024-10-16 204016](https://github.com/user-attachments/assets/a4d8dac1-4800-49f5-b735-acd899049180)
![Screenshot 2024-10-16 204029](https://github.com/user-attachments/assets/2aa60f66-f675-4a71-b763-3e67abe1b91b)
![Screenshot 2024-10-16 203141](https://github.com/user-attachments/assets/95ff71a5-2efa-45d3-9b8c-95d9451bcf85)



## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
