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
Developed by: 
RegisterNumber:  
*/
```

## Output:
![SVM For Spam Mail Detection](sam.png)


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
