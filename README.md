# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.Get the matrix from user.

2.Using "from numpy as np sys" to import numpy (Ge).

3.Print the result matrices (Gaussian Elimination).

4.End the program.

## Program:
```
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: K.Madhava Reddy
RegisterNumber: 212223240064
'''
import numpy as np
import sys
n=int(input())
matrix=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        matrix[i][j]=int(input())
for i in range(n):
    if matrix[i][j]==0.0:
        sys.exit("Divide by zero error")
    for j in range(i+1,n):
        ratio=matrix[j][i]/matrix[i][i]
        for k in range(n+1):
            matrix[j][k]=matrix[j][k]-ratio*matrix[i][k]
#Back substitution 
x[n-1]=matrix[n-1][n]/matrix[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=matrix[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-matrix[i][j]*x[j]
    x[i]=x[i]/matrix[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,x[i]),end=" ")
```          

## Output:
![image](https://github.com/Madhavareddy09/Gaussian/assets/145742470/54a1d267-87f6-4919-bf52-72c6f24be7f4)




## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

