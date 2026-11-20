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
# Experiment 1: Matrix Operations Using NumPy

# Step 1: Import NumPy library
import numpy as np

# Step 2: Create matrix A
A = np.array([[2.0, 1.0], [1.0, 3.0]])

# Step 3: Create array b
b = np.array([1.0, 2.0])

# Step 4: Display matrix A
print("Matrix A:\n", A)

# Step 5: Calculate and display transpose of A
print("\nTranspose A^T:\n", A.T)

# Step 6: Calculate and display inverse of A
print("\nInverse A^-1:\n", np.linalg.inv(A))

# Step 7: Calculate eigenvalues and eigenvectors
eigvals, eigvecs = np.linalg.eig(A)
print("\nEigenvalues:", np.round(eigvals, 4))
print("\nEigenvectors:\n", np.round(eigvecs, 4))

# Step 8: Solve the linear equation Ax = b
x = np.linalg.solve(A, b)
print("\nSolve A x = b --> x:", np.round(x, 4))

```

## Output
```text
Matrix A:
 [[2. 1.]
 [1. 3.]]

Transpose A^T:
 [[2. 1.]
 [1. 3.]]

Inverse A^-1:
 [[ 0.6 -0.2]
 [-0.2  0.4]]

Eigenvalues: [1.382 3.618]

Eigenvectors:
 [[-0.8507 -0.5257]
 [ 0.5257 -0.8507]]

Solve A x = b --> x: [0.2 0.6]
```

## Result
The program was successfully executed using Python and the NumPy library. The transpose and inverse of the matrix were calculated, the linear equation was solved, and the eigenvalues and eigenvectors were obtained successfully. Thus, the experiment demonstrated basic matrix operations and numerical computations using NumPy.
