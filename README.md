# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
```
1.IMport the numpy module to use the built_in functions for calculation.
2.Import sys module to use the built_in functions.
3.Get the input from the user for number of rows and add it by 1 for number of columns.
4.Using np.zeros() set the matrix as null matrix .
5.Using nested for loop get input from the user for each element in the matrix.
6.Using nested for loop input find the ration and perform the elementary row operations and find the final matrix.
7.Use back substituion method to find the value of the variable and print it.
8.End the program.
```
## Program:
```
/*
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: M.suren.
RegisterNumber: 23005055
'''
import sys
import numpy as np
n=int(input())
matrix=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range (n+1):
        matrix[i][j]=int(input())
for i in range(n):
    if matrix[i][i]==0.0:
        sys.exit("Divide by zero error")
    for j in range(i+1,n):
        ratio=matrix[j][i]/matrix[i][i]
        for k in range(n+1):
            matrix[j][k]=matrix[j][k]-ratio*matrix[i][k]
x[n-1]=matrix[n-1][n]/matrix[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=matrix[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-matrix[i][j]*x[j]
    x[i]=x[i]/matrix[i][i]
for i in range(n):
    print("X%d = %0.2f"%(i,x[i]),end=" ")

```

## Output:

![image](https://github.com/Msuren48106/Gaussian/assets/150503875/be105c0e-53e0-4cfe-b177-5502d7daf9dc)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

