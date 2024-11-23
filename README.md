## DATE:
## Gaussian Elimination
## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import nump and sys.
2. Get the values from the user.
3. Find the empty agumented marix and apply gauss elimination.
4. Solve the marix to get the answer.

## Program:
```
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: J AANKARSH
RegisterNumber: 24013602

import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][j]==0.0:
        sys.exit('Divide by zero detected')
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f'%(i,x[i]),end=' ')


```

## Output:

![Screenshot 2024-11-23 144347](https://github.com/user-attachments/assets/d9f0231b-d22c-4ae8-83f7-bcbad2636bde)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

