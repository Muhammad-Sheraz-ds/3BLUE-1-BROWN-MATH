# 3Blue1Brown Essence of Linear Algebra Lecture Notes

- [3Blue1Brown Essence of Linear Algebra Lecture Notes](#3blue1brown-essence-of-linear-algebra-lecture-notes)
    - [3](#3)
    - [4](#4)
    - [5](#5)
    - [6](#6)
        - [Right Hand Axes](#right-hand-axes)
        - [Determinant Calculation](#determinant-calculation)
    - [7 Inverse Matrices, Column Space and Null Space uQhTuRlWMxw](#7-inverse-matrices-column-space-and-null-space-uqhturlwmxw)
    - [8 Nonsquare Matrices as Transformations Between Dimensions](#8-nonsquare-matrices-as-transformations-between-dimensions)
    - [9 Dot Products and Duality](#9-dot-products-and-duality)
    - [10 Cross Products](#10-cross-products)
        - [Treat Cross Products as Values](#treat-cross-products-as-values)
        - [Treat Cross Products as 3D Vectors](#treat-cross-products-as-3d-vectors)
    - [11 Cross Products in the Light of Linear Transformations](#11-cross-products-in-the-light-of-linear-transformations)
    - [12 Cramer's Rule, Explained Geometrically](#12-cramers-rule-explained-geometrically)

Playlist: <https://www.youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab>

## 3

Source: <https://www.youtube.com/watch?v=kYB8IZa5AuE>

**Linear transformation** in layman's terms: after a linear transformation, lines remain lines, and the origin stays fixed.
In other words, keep grid lines parallel and evenly spaced.

Linear transformation in formulae:

![Linear Transformation Limits](3_files/linear_transformation_formulae.jpg)

Linear transformations can be described using matrix multiplication.

Affine transformation: Same as linear transformation, except that the origin moves (linear transformation + translation).

## 4

**Composition** of multiple transformations `A @ B @ P`:

- Matrix multiplication of those individual transformation matrices
- The transformation of the rightward matrix `B` get applied first

## 5

Again, 3D transformation matrix's columns: new locations of the new unit vectors.

## 6

**Determinant** of a transformation: area (2D)/volume (3D) scaling factor.

Area scaling factor can be calculated by using square (0, 0, 1, 1):

- All squares have the same scaling factor
- Any area can be *approximated* by small enough squares

Values:

- 0 determinant ->
    - **reduce dimension**
    - Columns are linearly dependent
- Negative determinant -> "invert"/"flip" space

`det(AB) = det(A)det(B)`

### Right Hand Axes

![Right Hand Axes](6_files/right_hand_axes.png)

Can no longer use right hand axes after the transformation: determinant < 0

### Determinant Calculation

![2x2 matrix](6_files/determinant_2_2.png)

![3x3 matrix](6_files/determinant_3_3.png)

## 7 Inverse Matrices, Column Space and Null Space uQhTuRlWMxw

![Linear System of Equations](7_files/linear_system_of_equations.jpg)

![Linear System of Equations to Matrix Multiplication](7_files/linear_system_of_equations_to_matrix_multiplication.jpg)

Identity transformation: `inverse(A) @ A == I`

![Solve variables](7_files/solve_x.jpg)

`det(A) == 0`: Not inversible.
Solutions don't exist if the 2 equations contradict:

![Determinant 0 Solutions](7_files/det_0_solutions.jpg)

Rank: New dimensionality.
"full rank"

**Null space**/**kernel**: The set of vectors that lands on the origin after the transformation.
Describes solutions of `A @ x == [[0], [0]]`.

## 8 Nonsquare Matrices as Transformations Between Dimensions

![2D to 3D space](8_files/2d_to_3d_space.jpg)

Example: 2D vector to 3D vector

Column space: a plane in 3D space

![Column space](8_files/columns.jpg)

## 9 Dot Products and Duality

Dot product calculation using numbers:

![Basic Method](9_files/basic_method.jpg)

Dot product calculation using projection: `len(w's projection on v) * len(v)`

![Projection and Multiplication](9_files/projection_and_multiplication.jpg)

- If `w`'s projection is opposite to `v`, the dot product is negative
- Perpendicular vector: dot product is 0

Projection is symmetric: `v . w == w . v`

Dot product usage: check if 2 vectors point in roughly the same direction.

Consider one of the vectors as a transformation matrix:

![Transformation](9_files/vector_and_transformation.jpg)

**Duality**: natural but surprising correspondence between 2 things.

Dual vector: likes the dot product, maps a 2D vector onto an 1D line.

## 10 Cross Products

### Treat Cross Products as Values

Basic definition: area of parallelogram

![Basic Definition](10_files/numeric_value.jpg)

Asymmetric: `v ✖️ w == - w ✖️ v`

- ![Positive Cross Product](10_files/numeric_positive.jpg)
- ![Negative Cross Product](10_files/numeric_negative.jpg)

Basically, the unit vectors' placement introduces positive cross products:

![Positive with Unit Vectors](10_files/numeric_positive_with_unit_vectors.jpg)

That is because: cross products can be calculated using determinants:

![Calculation with Determinants](10_files/numeric_calculation_determinant.jpg)

Cross products are scalable:

![Scalability](10_files/numeric_scalability.jpg)

### Treat Cross Products as 3D Vectors

The length of 3D cross products equals the area/determinant calculated above.

Direction of cross products: use right hand rule:

![Right Hand Rule](10_files/right_hand_rule.jpg)

Calculation:

![Calculation](10_files/vector_calculation.jpg)

## 11 Cross Products in the Light of Linear Transformations

![Cross Product Facts](11_files/cross_product_facts.jpg)

![Calculation as Part of Determinant](11_files/calculation_determinant_fashion.jpg)

Cross product is the **dual vector** of `v` and `w`.
That it, it is a 3D to 1D linear transformation.

![Linearity](11_files/calculation_determinant_linear.jpg)

![Dual Vector](11_files/dual_vector.jpg)

The dual vector equals the cross product vector:

![Dual Vector and Cross Product Vector](11_files/dual_vector_and_cross_product.jpg)

Dual vector characteristics:

![Dual Vector Characteristics](11_files/dual_vector_characteristics.jpg)

## 12 Cramer's Rule, Explained Geometrically

The solution for linear systems of equations (Cramer's Rule):

![Cramer's Rule 1](12_files/cramers_rule_1.jpg)

![Cramer's Rule 2](12_files/cramers_rule_2.jpg)

This is not the fastest solution.
E.g. [Gaussian Elimination](https://en.wikipedia.org/wiki/Gaussian_elimination) will always be faster.

Dot products before and after a transformation usually do not equal:
`v . w > 0` does not mean that `T(v) . T(w) > 0`.

Orthonormal transformation: rotation.

![Orthonormal Transformation](12_files/orthonormal_transformation.jpg)

Axes in determinants:

![Axes in 2D Determinants](12_files/determinant_axis_2d.jpg)

![Axes in 3D Determinants](12_files/determinant_axis_3d.jpg)

Areas are scaled by the transformation matrix by the same amount.

![Cramer's Rule Proof 1](12_files/cramers_rule_proof_1.jpg)

![Cramer's Rule Proof 2](12_files/cramers_rule_proof_2.jpg)
