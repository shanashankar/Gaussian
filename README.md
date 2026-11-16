# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. import nump as np
2. prepare the lists from each linear equations and assign in np.array() 
3. using the np.linalg(, we get the results
4. end the program

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: Sahana Shanakar
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
<img width="1920" height="1080" alt="ex 06 op (2)" src="https://github.com/user-attachments/assets/9b2a2f73-f90d-42e5-9f12-11a4a0665529" />
<img width="1920" height="1080" alt="ex 06 op (3)" src="https://github.com/user-attachments/assets/d63645bf-0bd7-4b95-9a8e-342f942a5035" />


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

