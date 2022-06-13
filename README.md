# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: R.vijay
RegisterNumber:  212221230121
*/
```
~~~
import pandas as pd
data=pd.read_csv("/content/spam.csv",encoding='latin-1')
data.head()
data.info()
data.isnull().sum()
x=data["v1"].values
y=data["v2"].values
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()          #CountVectorizer is a method to convert text to numerical data.The text is transformed to sparse matrix.
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
~~~

## Output:
## Data head:
![pic 1](https://github.com/vijay21500269/Implementation-of-SVM-For-Spam-Mail-Detection/blob/main/Data%20head.png)
## Data information:
![pic 2](https://github.com/vijay21500269/Implementation-of-SVM-For-Spam-Mail-Detection/blob/main/data%20info.png)
## Data isnull:
![pic 3]()


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
