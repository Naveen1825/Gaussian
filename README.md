# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.First, we have to import numpy, then import sys, assume a variable.
2.or gaussian elimination method, we have to make 2nd and 3rd column zero.
3.For that we have to make a range according to our program output.
4.Then print the program with correct form then the output will display.
## Program:
```
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: Naveenkanthan L
RegisterNumber: 23007705
'''
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
        sys.exit()
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
    print('X%d = %0.2f' %(i,x[i]),end=" ")
```

## Output:

<img width="740" alt="290120183-f5c33270-d4dd-44d9-a278-17713cdb7efc" src="https://github.com/Naveen1825/Gaussian/assets/138969868/e403d09c-8b17-430c-a5a3-19dee22c4103">

## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

