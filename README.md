# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: Abishek P
RegisterNumber:  24901317
*/
import numpy as np
import matplotlib.pyplot as plt
x= np.array(eval(input()))
y=np.array(eval(input()))
X_mean=np.mean(x)
Y_mean=np.mean(y)
num=0
denom=0
for i in range(len(x)):
    num+=(x[i]-X_mean)*(y[i]-Y_mean)
    denom+=(x[i]-X_mean)**2
m=num/denom
b=Y_mean-m*X_mean
print("Slope:",m)
print("y_intercept :",b)
y_predicted = m*x+b
print("y_predicted:",y_predicted)
plt.scatter(x,y)
plt.plot(x,y_predicted,color='red')
plt.show()
```

## Output:
## X and Y values:
![image](https://github.com/user-attachments/assets/f4be992c-bf75-4b2e-9841-74a0dceb096b)
## Slope:
![image](https://github.com/user-attachments/assets/29d92eee-a160-406a-a148-a4b752b0f97f)
## Y_intercept:
![image](https://github.com/user-attachments/assets/1bc2b2c1-cd7d-43ad-ba38-b37bf67f752b)
## Y_Predicted value:
![image](https://github.com/user-attachments/assets/ba74411c-21d1-4ba5-ad44-d41316ef7742)
## Graph:
![image](https://github.com/user-attachments/assets/38da0aeb-eb44-43ad-a11d-803536d57138)




## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
