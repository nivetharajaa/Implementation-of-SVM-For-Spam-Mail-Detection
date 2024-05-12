# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:

To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:

1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

### step 1.

Start

### step 2.

Import the required packages.

### step 3

Import the dataset to operate on.

### step 4.

Split the dataset.

### step 5.

Predict the required output.

### step 6.

Stop

## Program:
```
Program to implement the SVM For Spam Mail Detection..
Developed by: 
RegisterNumber:  

Program to implement the SVM For Spam Mail Detection..
Developed by: VIKAASH K S
RegisterNumber:  212223240179
import pandas as pd
data=pd.read_csv('/content/spam.csv',encoding='Windows-1252')
from sklearn.model_selection import train_test_split
data
data.shape
x=data['v2'].values
y=data['v1'].values
x.shape
y.shape
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.35,random_state=0)
x_train
x_train.shape
from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)
from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred
from sklearn.metrics import accuracy_score,confusion_matrix,classification_report 
accuracy=accuracy_score(y_test,y_pred)
accuracy
con=confusion_matrix(y_test,y_pred)
print(con)
cl=classification_report(y_test,y_pred)
print(cl)
```

## Output:

### data:

![image](https://github.com/nivetharajaa/Implementation-of-SVM-For-Spam-Mail-Detection/assets/120543388/ee260634-5224-44d7-9c08-1ee7f33e67f6)

### data.shape:

![329567625-46019e0a-abd4-45ac-9793-ad85d5fc4f81](https://github.com/nivetharajaa/Implementation-of-SVM-For-Spam-Mail-Detection/assets/120543388/017994f4-19b6-46d1-8423-25397525d303)

### x.shape:

![329567862-cdbf779c-5abe-426a-9a43-06fabd253930](https://github.com/nivetharajaa/Implementation-of-SVM-For-Spam-Mail-Detection/assets/120543388/7e73d47e-1c9d-473d-8c68-80de5e3eeadc)

### y.shape:

![329567862-cdbf779c-5abe-426a-9a43-06fabd253930](https://github.com/nivetharajaa/Implementation-of-SVM-For-Spam-Mail-Detection/assets/120543388/ad2be537-ca15-4187-a7d2-e894367fa18e)

### x_train:

![329567724-c5d76edd-4d65-4b34-94c8-bd14e53e21e3](https://github.com/nivetharajaa/Implementation-of-SVM-For-Spam-Mail-Detection/assets/120543388/f8642d23-8b40-4758-9b6e-20ea182e9337)

### x_train.shape:

![329567953-0a132e17-a840-4ae2-955e-b866efcfd4ae](https://github.com/nivetharajaa/Implementation-of-SVM-For-Spam-Mail-Detection/assets/120543388/7f6b4662-dbfb-4df7-8c09-ca80c0def28d)


### y_pred:

![329568013-f3edd0ee-06fb-4594-b99e-06a761fe9956](https://github.com/nivetharajaa/Implementation-of-SVM-For-Spam-Mail-Detection/assets/120543388/d6b605b6-abd7-42ad-919c-5e9d44af20c6)


### Accuracy:

![329568044-55accff0-f33c-4575-9b70-ab39e7ca51d4](https://github.com/nivetharajaa/Implementation-of-SVM-For-Spam-Mail-Detection/assets/120543388/46e7e2d6-c9f5-4547-ba78-ded5dfb2c991)

### confusion_matrix:

![329567542-0196f78d-660e-4592-9b61-165c43dd281d](https://github.com/nivetharajaa/Implementation-of-SVM-For-Spam-Mail-Detection/assets/120543388/e9c9de16-ce26-405c-9892-b8a5947d2926)


### classification_report:

![329568557-02df2736-a171-4c0d-8a81-4fd5ce0f2c73](https://github.com/nivetharajaa/Implementation-of-SVM-For-Spam-Mail-Detection/assets/120543388/e0ea302a-d684-465d-9caf-b8eaa71e243b)


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
