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
```python
import numpy as np

# Define a two-dimensional matrix A and vector b
A = np.array([[1, 2],
              [3, 4]])

b = np.array([5, 6])

# Display the original matrix
print("Original Matrix A:")
print(A)

print("\nVector b:")
print(b)

# Calculate the transpose of matrix A
print("\nTranspose of Matrix A:")
print(np.transpose(A))

# Calculate the inverse of matrix A
print("\nInverse of Matrix A:")
print(np.linalg.inv(A))

# Solve the linear equation Ax = b
print("\nSolution of Ax = b:")
print(np.linalg.solve(A, b))

# Calculate eigenvalues and eigenvectors
eigenvalues, eigenvectors = np.linalg.eig(A)

print("\nEigenvalues:")
print(eigenvalues)

print("\nEigenvectors:")
print(eigenvectors)
```

## Output
```text
Original Matrix A:
[[1 2]
 [3 4]]

Vector b:
[5 6]

Transpose of Matrix A:
[[1 3]
 [2 4]]

Inverse of Matrix A:
[[-2.   1. ]
 [ 1.5 -0.5]]

Solution of Ax = b:
[-4.   4.5]

Eigenvalues:
[-0.37228132  5.37228132]

Eigenvectors:
[[-0.82456484 -0.41597356]
 [ 0.56576746 -0.90937671]]
```

## Result
The program was successfully executed using Python and the NumPy library. The transpose and inverse of the matrix were calculated, the linear equation was solved, and the eigenvalues and eigenvectors were obtained successfully. Thus, the experiment demonstrated basic matrix operations and numerical computations using NumPy.
