# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import the required packages.

2.Import the dataset to operate on.

3.Split the dataset.

4.Predict the required output.

5.End the program.
## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: Aruru.Sai Bandhavi
RegisterNumber:  212221240006
*/
```
```
import pandas as pd
data=pd.read_csv("spam.csv",encoding='latin-1')
data.head()
data.info()
data.isnull().sum()
x=data["v1"].values
y=data["v2"].values
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
from sklearn.feature_extractiaon.text import CountVectorizer
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
```
## Output:
### Data Head:
![output](https://github.com/Saibandhavi75/Implementation-of-SVM-For-Spam-Mail-Detection/blob/main/91.png?raw=true)

### Data Info:
![output](https://github.com/Saibandhavi75/Implementation-of-SVM-For-Spam-Mail-Detection/blob/main/92.png?raw=true)

### Data isnull():
![output](https://github.com/Saibandhavi75/Implementation-of-SVM-For-Spam-Mail-Detection/blob/main/93.png?raw=true)

### Y_Pred:
![output](https://github.com/Saibandhavi75/Implementation-of-SVM-For-Spam-Mail-Detection/blob/main/94.png?raw=true)

### Accuracy:
![output](https://github.com/Saibandhavi75/Implementation-of-SVM-For-Spam-Mail-Detection/blob/main/95.png?raw=true)
## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
