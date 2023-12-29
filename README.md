# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm

## step 1
Convert the matrix to a NumPy array.
## step 2
Apply Gaussian Elimination to make elements below the diagonal zero.
## step 3
Normalize the diagonal elements to 1.
## step 4
Perform back-substitution to find the solution.
## step 5
The resulting array contains the solutions to the system of equations.

## Program:
```

Program to find the solution of a matrix using Gaussian Elimination.

Developed by: vinodini .k
RegisterNumber: 23013556

import numpy as np
n=int(input())
arr=np.zeros((n,n+1))
res=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        arr[i][j]=int(input())
for i in range(n):
    for j in range(i+1,n):
        ratio=arr[j][i]/arr[i][i]
        for k in range(n+1):
            arr[j][k]=arr[j][k]-ratio*arr[i][k]
res[n-1]=arr[n-1][n]/arr[n-1][n-1]
for i in range(n-1,-1,-1):
    res[i]=arr[i][n]
    for j in range(i+1,n):
        res[i]=res[i]-arr[i][j]*res[j]
    res[i]=res[i]/arr[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,res[i]),end=" ")
```

## Output:
![gau out](https://github.com/vinodhini-17/Gaussian/assets/145742741/fb420138-f277-4bbc-9286-072424c9f88b)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

