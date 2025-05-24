# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import required libraries for encoding detection, data handling, text processing, machine learning, and evaluation.

2.Open the dataset file (spam.csv) in binary mode and detect its character encoding using chardet.

3.Load the CSV file into a pandas DataFrame using the detected encoding (e.g., 'windows-1252').

4.Display the dataset using head(), info(), and check for any missing values with isnull().sum().

5.Assign the label column (v1) to variable x and the message text column (v2) to variable y.

Split the dataset into training and testing sets using an 80-20 split with train_test_split().

Convert the text data into numerical format using CountVectorizer to prepare for model training.

Initialize the Support Vector Machine classifier (SVC) and train it on the vectorized training data.

Predict the labels of the test set using the trained SVM model.

Evaluate the model’s performance by calculating and printing the accuracy score using accuracy_score().

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: HARITHA RAMESH
RegisterNumber:  212223100011
import chardet
file='spam.csv'
with open (file,'rb') as rawdata:
    result = chardet.detect(rawdata.read(100000))
result
import pandas as pd
data=pd.read_csv("spam.csv",encoding='windows-1252')
data.head()
data.info()
data.isnull().sum()
x=data["v2"].values
y=data["v1"].values
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)
from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
*/
```

## Output:
![Screenshot 2025-05-24 190322](https://github.com/user-attachments/assets/cdb19ba8-653e-4ee3-b308-5a09640e8c99)


![Screenshot 2025-05-24 190330](https://github.com/user-attachments/assets/b8bcc992-4b88-45a6-bd7a-dc341952e7b3)
![Screenshot 2025-05-24 190337](https://github.com/user-attachments/assets/9ef0273d-4396-4632-aaa4-c7823f88d0e3)
![Screenshot 2025-05-24 190352](https://github.com/user-attachments/assets/dd0b4beb-b600-45c0-b3df-2f58627eb017)
![Screenshot 2025-05-24 190403](https://github.com/user-attachments/assets/839ceef9-e91e-4ad3-8b39-0c8bc891a480)


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
