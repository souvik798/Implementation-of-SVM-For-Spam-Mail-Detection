# Ex 09 -  Implementation-of-SVM-For-Spam-Mail-Detection
## AIM:
To write a program to implement the SVM For Spam Mail Detection.
## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1. Import the necessary packages.
2. Read the given csv file and display the few contents of the data.
3. Assign the features for x and y respectively.
4. Split the x and y sets into train and test sets.
5. Convert the Alphabetical data to numeric using CountVectorizer.
6. Predict the number of spam in the data using SVC (C-Support Vector Classification) method of SVM (Support vector machine) in sklearn library.
7. Find the accuracy of the model.


## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: souvik kundu
RegisterNumber:  2122221230105

import chardet
file='/content/spam (1).csv'
with open(file, 'rb') as rawdata:
     print('Result output')
    result = chardet.detect(rawdata.read(10000))
result
import pandas as pd
data=pd.read_csv("/content/spam (1).csv",encoding="windows-1252")
print("Data Head ")
data.head()
print("data info")
data.info()
print("data.isnull()")
data.isnull().sum()
x=data["v1"].values
y=data["v2"].values
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
print("y_pred")
y_pred
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
print("accuracy")
accuracy
*/
```

## Output:

1. data.head():

![1s](https://github.com/souvik798/Implementation-of-SVM-For-Spam-Mail-Detection/assets/94752764/6f6e0a91-e552-4bb1-82c8-9da1b7f08bb5)

2. data.info():

![2s](https://github.com/souvik798/Implementation-of-SVM-For-Spam-Mail-Detection/assets/94752764/37170388-6ea4-41ad-9c2b-29dd8de02332)

3.data.isnull().sum():

![3s](https://github.com/souvik798/Implementation-of-SVM-For-Spam-Mail-Detection/assets/94752764/f2ed53ea-ebdc-4450-9d9d-baea83097aec)



4. Y_prediction Value:
   
![4s](https://github.com/souvik798/Implementation-of-SVM-For-Spam-Mail-Detection/assets/94752764/eeeb19ba-2576-467b-83fe-209463e56008)



5. Accuracy Value:

![5s](https://github.com/souvik798/Implementation-of-SVM-For-Spam-Mail-Detection/assets/94752764/bef25bab-42a9-43e0-954f-af61e7d8267b)




## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
