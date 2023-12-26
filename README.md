# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. get the input
2. loop through each row and column
3. use nested loops to perform Gaussian Elimination.
4. print the result

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: Roshini.S
RegisterNumber: 
*/
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: 
RegisterNumber: 
'''
import numpy as np
n=int(input())
arr=np.zeros((n,n+1))
result=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        arr[i][j]=int(input())
for i in range(n):
    for j in range(i+1,n):
        ratio=arr[j][i]/arr[i][i]
        for k in range(n+1):
            arr[j][k]=arr[j][k]-ratio*arr[i][k]
result[n-1]=arr[n-1][n]/arr[n-1][n-1]
for i in range(n-1,-1,-1):
    result[i]=arr[i][n]
    for j in range(i+1,n):
        result[i]=result[i]-arr[i][j]*result[j]
    result[i]=result[i]/arr[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,result[i]),end=" ")

```

## Output:
![gaussian elimination]()

![image](https://github.com/23008859/Gaussian/assets/139117979/900aea23-3c0c-4a80-a440-a901377beaeb)

Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

