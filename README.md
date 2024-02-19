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

## RAHUL.B
## 2122222420032
import numpy as np
import matplotlib.pyplot as plt

# Preprocessing Data

X=np.array(eval(input()))
Y=np.array(eval(input()))

# Mean
X_mean = np.mean(X)
Y_mean = np.mean(Y)
num = 0 #for slope
denom = 0 #for slope

# to find sum of (xi-x')&(yi-y')&(xi-x')^2
for i in range(len(X)):
    num+=(X[i]-X_mean)*(Y[i]-Y_mean)
    denom+=(X[i]-X_mean)**2
m=num/denom
print(m)
b=Y_mean - m*X_mean
print(b)
Y_pred=m*X+b
print(Y_pred)
plt.scatter(X,Y)
plt.plot(X,Y_pred,color='red') 
plt.show()

## Output:
![WhatsApp Image 2024-02-17 at 11 48 23 AM](https://github.com/RAHUL-22001882/Find-the-best-fit-line-using-Least-Squares-Method/assets/123528986/2fb3222b-013c-4b26-9b49-1703b586fcc4)





## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
