# Linear Algebra Notes

## Linear Independence
- **Basis**: A set of linearly independent vectors that span a vector space.
  - **Key Points**:
    - A basis cannot be created from other vectors in the space.
    - The basis can be changed.
---

## Distance Calculation
- **Lp Norm**:
  - **L1 Norm (Manhattan Distance)**: Sum of absolute differences between points.
  - **L2 Norm (Euclidean Distance)**: Square root of the sum of squared differences (most common).
  - **L3 Norm**: Similar to L2, but raised to the power of 3.
 --- 
 
## Unit Vector
- A unit vector is a vector with a magnitude of 1, often used to indicate direction in space.
---
## Dot Product
- **Dot Product of Vectors**: A measure of how much two vectors point in the same direction.
  - **Orthogonal Vectors**: The dot product is 0 when vectors are 90° to each other.
  - **Opposite Vectors**: The dot product is negative.
  - **Parallel Vectors**: The dot product is positive and maximized when vectors are in the same direction.
  
- **Key Applications**:
  - Represent lines, planes, hyperplanes using dot products.

## Representation of Geometric Objects

### General equation of a hyperplane

##### $$ w1*x1 + w2 * x2 + .... + wk * xk = 0 $$
 - `x1, x2, ..., xk` are dimensions/variables, and `w1, w2, ..., wk` are weights/coefficients.
---

### Line
- In **2D space** (i.e k = 2 )):
  - The equation $$w1 * x1 + w2 * x2 = 0 simplifies to $$w1 * x + w2 * y = 0 $$, which represents a **line passing through the origin**.
  - On adding a constant  'c', the equation becomes $$w1 * x + w2 * y + c = 0 $$, which is the **general equation of a line in 2D**.

---

### Plane
A flat, 2-dimensional surface in 3-dimensional space.
- In 2D space: The "plane" is the entire space itself because there's only two dimensions.
- In 3D space: A plane is a 2D surface, like a sheet of paper or a tabletop.
  - Example: Imagine a flat sheet of paper that extends infinitely in two directions. This is a plane in 3D space.
- In **3D space** (i.e k = 3):
  - The equation $$w1 * x1 + w2 * x2 + w3 * x3 = 0 $$ represents a **plane passing through the origin**.
  - Adding a constant 'c' gives $$w1 * x1 + w2 * x2 + w3 * x3 + c = 0 $$ , the **general equation of a plane in 3D**.

---

### Hyperplane
A general term used to describe a flat subspace in any dimensional space. The dimension of a hyperplane is always one less than the space it resides in.
  - In 3D space, a hyperplane is a 2D surface (like a flat plane).
  - In 4D space, a hyperplane is a 3D subspace/a 3D volume (it can be visualized as a "volume" in 4D space).
  - In 5D space, a hyperplane would be a 4-dimensional subspace (a "4D volume").
  - In 6D space, a hyperplane would be a 5-dimensional subspace (a "5D volume").
  - Similarly, in n-dimensional space, a hyperplane is a (n-1)-dimensional subspace.
- In **k-dimensional space**, the equation $$w1 * x1 + w2 * x2 + ... + wk * xk = 0 $$ defines a **hyperplane**, which is a flat subspace of dimension (k-1) in k-dimensional space.

---
## Types of Matrices
- Row Matrix: A matrix with only one row.
- Column Matrix: A matrix with only one column.
- Square Matrix: A matrix with the same number of rows and columns.
- Diagonal Matrix: A square matrix where all off-diagonal elements are zero.
- Identity Matrix: A diagonal matrix where all diagonal elements are 1.
     -Represents the multiplicative identity in matrix multiplication.
- Symmetric Matrix: A square matrix that is equal to its transpose.
- Skew-Symmetric Matrix: A square matrix where the transpose of the matrix is equal to the negative of the original matrix.
- Upper Triangular Matrix: A square matrix where all elements below the main diagonal are zero.
- Lower Triangular Matrix: A square matrix where all elements above the main diagonal are zero.
- Zero Matrix (Null Matrix): A matrix where all elements are zero.
- Sparse Matrix: A matrix with mostly zero elements.
- Dense Matrix: A matrix with a significant number of non-zero elements.

## Matrix operations
- **Inverse**: Only invertible (non-singular) matrices have an inverse.
- **Determinant**: A scalar value that can be computed from the elements of a square matrix, indicating the matrix's invertibility.

## How does determinant relate to invertibility?

The determinant tells us whether a matrix is **invertible** (non-singular) or **non-invertible** (singular):

1. If $$\text{det}(A) = 0 $$
   - The matrix is **singular** and **not invertible**.
   - A determinant of 0 means the matrix does not have full rank (its rows or columns are linearly dependent), so the system of equations represented by the matrix cannot have a unique solution.

2. If $$\text{det}(A) \neq 0 $$
   - The matrix is **non-singular** and **invertible**.
   - A non-zero determinant indicates that the rows and columns are linearly independent, meaning the system of equations represented by the matrix has a unique solution.

---

## Visual interpretation of $$\text{det}(A) = 0 $$ 

When the determinant is 0:
- The matrix is **degenerate**, meaning it "collapses" into a lower-dimensional space.
- For example:
  - In 2D: A matrix might represent a parallelogram, and if $$\text{det}(A) = 0 $$, the parallelogram collapses into a line or a point (it has no area).
  - In 3D: The determinant represents the volume of a parallelepiped. If $$\text{det}(A) = 0 $$, the parallelepiped collapses into a plane or line (it has no volume).

---
  
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
