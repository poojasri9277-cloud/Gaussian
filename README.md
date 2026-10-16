# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Start and read the order n and the elements of the augmented matrix A.
2. Perform forward elimination to convert the augmented matrix into an upper triangular matrix by eliminating the elements below the main diagonal.
3. Perform back substitution to calculate the unknown values X1,X2,....Xn
4. 4. Display the solutions of the unknowns up to two decimal places and Stop.
 

## Program:
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: 
RegisterNumber: 
### import os 
### os.environ["OPENBLAS_NUM_THREADS"]="1"
### import numpy as np
### import sys

### Reading number of unknowns
### n = int(input())

### Making numpy array of n x n+1 size and initializing
### to zero for storing augmented matrix 
### a = np.zeros((n,n+1))

### Making numpy array of n size and initializing
### to zero for storing solution vector 
### x = np.zeros(n)

### Reading augmented matrix coefficients
### for i in range(n):
  ### for j in range(n+1):
    ### a[i][j] = float(input())

### Applying Gauss Elimination
### for i in range(n):
  ### if a[i][i] == 0.0:
  ### sys.exit('Divide by zero detected!')
    
  ### for j in range(i+1,n): 
    ### ratio = a[j][i]/a[i][i]
    
    ### for k in range(n+1):
     ### a[j][k] = a[j][k]-ratio*a[i][k]
   
### Back Substitution
### x[n-1]=a[n-1][n] / a[n-1][n-1]

### for i in range(n-2,-1,-1):
  ### x[i] = a[i][n]
  
  ### for j in range(i+1,n):
    ### x[i] = x[i]-a[i][j]*x[j]
     
  ### x[i] = x[i]/a[i][i]
### Displaying solution
### for i in range(n):
    ###  print('X%d = %0.2f'% (i,x[i]),end=' ')

## Output:
<img width="898" height="825" alt="image" src="https://github.com/user-attachments/assets/32b2064d-860b-45e6-9745-c3f00256b4ec" />


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

