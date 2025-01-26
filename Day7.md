# Linear Algebra Notes

## Linear Independence
- **Basis**: A set of linearly independent vectors that span a vector space.
  - **Key Points**:
    - A basis cannot be created from other vectors in the space.
    - The basis can be changed.

## Distance Calculation
- **Lp Norm**:
  - **L1 Norm (Manhattan Distance)**: Sum of absolute differences between points.
  - **L2 Norm (Euclidean Distance)**: Square root of the sum of squared differences (most common).
  - **L3 Norm**: Similar to L2, but raised to the power of 3.
  
## Unit Vector
- A unit vector is a vector with a magnitude of 1, often used to indicate direction in space.

## Dot Product
- **Dot Product of Vectors**: A measure of how much two vectors point in the same direction.
  - **Orthogonal Vectors**: The dot product is 0 when vectors are 90° to each other.
  - **Opposite Vectors**: The dot product is negative.
  - **Parallel Vectors**: The dot product is positive and maximized when vectors are in the same direction.
  
- **Key Applications**:
  - Represent lines, planes, hyperplanes using dot products.

## Representation of Geometric Objects Using Dot Product
- **Line (1D)**: 
  - Equation: `y = mx + c`
  - General form: `w1*x1 + w2*x2 + ... + wk*xk = 0`
  - `x1, x2, ..., xk` are dimensions/variables, and `w1, w2, ..., wk` are weights/coefficients.
  - If `c = 0`, the line passes through the origin.
  
- **Plane (2D)** and **Hyperplane (3D)**: Similar equations can represent planes and hyperplanes.

## Types of Matrices
- **Inverse**: Only invertible (non-singular) matrices have an inverse.
- **Determinant**: A scalar value that can be computed from the elements of a square matrix, indicating the matrix's invertibility.
  
## Projection of a Vector onto Another Vector
- **Dimensionality Reduction**: Used to project high-dimensional data to lower dimensions with some data loss.
- **Properties**:
  - Projection is not possible if vectors are parallel (dot product = 0).
  - Maximum projection occurs when vectors are in the same direction.

## Distance of a Point from a Line
- The perpendicular distance from a point to a line can be calculated using vector projection.

## Eigenvalues and Eigenvectors
- **Eigenvectors**: Vectors that do not change direction after a linear transformation.
  - They only get scaled by the corresponding eigenvalue.
  
- **Eigenvalue**: A scalar that represents the scaling factor applied to the eigenvector during transformation.

- **Applications**: Eigenvalues and eigenvectors are crucial in many fields, such as in Principal Component Analysis (PCA) for dimensionality reduction.

## Matrix Factorization
- A technique that decomposes a matrix into the product of three matrices (often used in data compression, recommendation systems, etc.).
