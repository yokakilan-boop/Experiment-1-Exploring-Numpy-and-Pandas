# Experiment 1: Exploring NumPy and Pandas

## Aim

To understand the use of NumPy and Pandas for performing basic data
manipulation and analysis in Python.

## Algorithm

1.  Import the NumPy library for matrix and numerical operations.
2.  Define a two-dimensional square matrix `A` and a vector `b`.
3.  Compute the transpose of matrix `A` to interchange rows and columns.
4.  Calculate the inverse of matrix `A` using `np.linalg.inv(A)` (ensure
    `A` is non-singular).
5.  Solve the linear equation `A × x = b` using `np.linalg.solve(A, b)`.
6.  Perform eigen decomposition to find eigenvalues and eigenvectors
    using `np.linalg.eig(A)`.
7.  Display the results for the matrix, transpose, inverse, solution
    vector, and eigenvalues.
8.  End the program.
    
## Formulas / Theory

-   **Transpose:** `Aᵀ` --- interchange rows and columns.
-   **Inverse:** `A⁻¹ = adj(A) / |A|`, provided `det(A) ≠ 0`.
-   **Linear system:** `A × x = b  ⇒  x = A⁻¹b`.
-   **Eigen decomposition:** `A v = λ v`, where `λ` is an eigenvalue and
    `v` is an eigenvector.

## Coding

# Step 1: Import libraries
import numpy as np
import pandas as pd

# Step 2: Define matrix A and vector b
A = np.array([[2, 1, 1],
              [1, 3, 2],
              [1, 0, 0]])

b = np.array([4, 5, 6])

# Step 3: Display original matrix
print("Original Matrix A:")
print(A)

# Step 4: Calculate transpose
print("\nTranspose of Matrix A:")
print(np.transpose(A))

# Step 5: Calculate inverse
print("\nInverse of Matrix A:")
print(np.linalg.inv(A))

# Step 6: Solve linear equation Ax = b
print("\nSolution of Linear Equation:")
print(np.linalg.solve(A, b))

# Step 7: Calculate eigenvalues and eigenvectors
eigenvalues, eigenvectors = np.linalg.eig(A)

print("\nEigenvalues:")
print(eigenvalues)

print("\nEigenvectors:")
print(eigenvectors)

# Step 8: Create Pandas DataFrame
data = {'Name': ['Akilan', 'Arun', 'Kumar'],
        'Marks': [85, 90, 80]}

df = pd.DataFrame(data)

print("\nPandas DataFrame:")
print(df)

# Display basic information
print("\nStatistical Description:")
print(df.describe())


## Output
Original Matrix A:
[[2 1 1]
 [1 3 2]
 [1 0 0]]

Transpose of Matrix A:
[[2 1 1]
 [1 3 0]
 [1 2 0]]

Inverse of Matrix A:
[[ 0.  0.  1.]
 [-2.  1.  3.]
 [ 3. -1. -5.]]

Solution of Linear Equation:
[  6.  15. -23.]

Eigenvalues:
[ 3.91222918  1.28646207 -0.19869124]

Eigenvectors:
[[-0.51233387 -0.51118241 -0.17058945]
 [-0.84874276  0.76210326 -0.48349198]
 [-0.13095702 -0.39735522  0.85856551]]

Pandas DataFrame:
     Name  Marks
0  Akilan     85
1    Arun     90
2   Kumar     80

Statistical Description:
       Marks
count    3.0
mean    85.0
std      5.0
min     80.0
25%     82.5
50%     85.0
75%     87.5
max     90.0

## Result
Thus, the NumPy and Pandas libraries were successfully used to perform matrix operations, solve linear equations, calculate eigenvalues and eigenvectors, and create a DataFrame for basic data analysis.
