# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. import the numpy module
2. prepare the lists from each linear equations and assign in np.array()
3.perform forward elimination and back substitution 
4. end the program

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: sahana shankar
RegisterNumber: 26002875
*/
```
### import os
### os.environ["OPENBLAS_NUM_THREADS"]="1"
### import numpy as np
### import sys
### n=int(input())
### a=np.zeros((n,n+1))
### x=np.zeros(n)
### for i in range(n):
    for j in range(n+1):
       a[i][j]=float(input())
### for i in range(n):
    if a[i][i]==0.0:
       sys.exit('Divide by zero detected!')
    for j in range(i+1,n):
       ratio=a[j][i]/a[i][i]
       for k in range(n+1):
           a[j][k]=a[j][k]-ratio*a[i][k]
### x[n-1]=a[n-1][n]/a[n-1][n-1]
### for i in range(n-2,-1,-1):
      x[i]=a[i][n]
      for j in range(i+1,n):
          x[i]=x[i]-a[i][j]*x[j]
      x[i]=x[i]/a[i][i]
### for i in range(n):
    print('X%d = %0.2f'%(i,x[i]), end=' ')

## Output:
![gaussian elimination]()

<img width="1920" height="1080" alt="ex 06 op (2)" src="https://github.com/user-attachments/assets/e8aaa882-b630-48ed-9587-3ccc7fed50e6" />

<img width="1920" height="1080" alt="ex 06 op (3)" src="https://github.com/user-attachments/assets/c31bce7a-b458-43a0-87aa-d3c0c1d11429" />


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

