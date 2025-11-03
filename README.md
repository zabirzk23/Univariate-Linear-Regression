# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```

import numpy as np
X= np.array(eval(input()))
Y= np.array(eval(input()))
X_mean=np.mean(X)
Y_mean=np.mean(Y)
num=0
denom=0
for i in range(len(X)):
  num+=(X[i]-X_mean)*(Y[i]-Y_mean)
  denom=(X[i]-X_mean)**2
  m=num/denom
  c=Y_mean-m*X_mean
  print(m,c)
  Y_pred=m*X+c
  print(Y_pred)

  import matplotlib.pyplot as plt
  plt.scatter(X,Y,color='RED')
  plt.plot(X,Y_pred,color='blue')
  plt.show()


```
## Output
</br>
<img width="682" height="607" alt="image" src="https://github.com/user-attachments/assets/2c342125-c1d3-4afc-8d31-d5cd4e298de2" />


</br>
<img width="683" height="554" alt="image" src="https://github.com/user-attachments/assets/9404a72e-5c73-402e-b86c-38e2d1f14d27" />

</br>
<img width="715" height="556" alt="image" src="https://github.com/user-attachments/assets/4b08c49e-c2e7-4a6d-a5cb-e974547f4984" />

</br>

<img width="692" height="556" alt="image" src="https://github.com/user-attachments/assets/5d231880-9f00-481b-a2c0-a5993f404b05" />

<br>
<img width="678" height="554" alt="image" src="https://github.com/user-attachments/assets/3182530c-2c5b-49f7-8946-a0a196b0643f" />


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
