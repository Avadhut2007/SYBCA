# 1. Matrix Algebra

Linear Algebra is the branch of mathematics that focuses on the study of vectors, vector spaces, matrices and linear transformations.

- Deals with linear equations, linear functions and their representations through matrices and determinants.
- Used in quantum mechanics, computer graphics and optimization
- Build a strong base for advanced subjects such as Machine Learning, Data Science, and Computer Graphics.

## Why Learn Linear Algebra?

- Machine Learning & AI: Every neural network, regression model and dimensionality reduction algorithm (PCA, SVD) is built on linear algebra operations.
- Computer Graphics: Rotations, scaling and 3D projections in games and animation are all matrix transformations.
- Physics & Engineering: Quantum mechanics, structural analysis and control systems all rely on eigenvalues and vector spaces.
- Data Science: Working with high-dimensional datasets, covariance matrices and feature transformations requires fluency in linear algebra.

## Foundations of Linear Algebra

Linear algebra builds on a small set of core ideas; scalars, vectors, matrices and the equations that connect them.

- Vectors
- Matrices
- Determinants
- Linear Equations
- Eigenvalues and Eigenvectors

One of the best real-life examples of Linear Algebra in Computer Vision is Face Recognition-the technology used to unlock smartphones or identify people in photographs.

![](1%20Matrix%20Algebra/imagesb366c259-1b05-4d8d-9d6b-cce59629bba4-005_598_744_218_162.jpg)

![](1%20Matrix%20Algebra/imagesb366c259-1b05-4d8d-9d6b-cce59629bba4-005_598_737_218_916.jpg)

![](1%20Matrix%20Algebra/imagesb366c259-1b05-4d8d-9d6b-cce59629bba4-005_582_520_224_1683.jpg)

## Example: Face Recognition in Smartphones

Suppose you unlock your phone using Face ID.
Step 1: Image as a Matrix
When the camera captures your face, it stores it as a matrix of pixel values.
For example, a small grayscale image might look like:

$$
\left[\begin{array}{lll}
120 & 125 & 130 \\
118 & 122 & 128 \\
115 & 120 & 126
\end{array}\right]
$$

A real image may have over a million pixels, so it becomes a very large matrix.

Step 2: Face as a Vector
The image matrix is converted into a long vector.
For example,

$$
\left[\begin{array}{c}
120 \\
125 \\
130 \\
118 \\
122 \\
128 \\
\vdots
\end{array}\right]
$$

Each face is now represented mathematically.

Step 3: Feature Extraction using Eigenvalues and Eigenvectors
Instead of comparing millions of pixels, the system extracts the most important facial features using Principal Component Analysis (PCA).

PCA relies on eigenvalues and eigenvectors, which are key topics in Linear Algebra.
The resulting features capture:

- Distance between the eyes
- Nose shape
- Jawline
- Face width
- Forehead height

These are called Eigenfaces.

Step 4: Compare Faces
The system computes the distance between your current face vector and the stored face vector.
If the distance is very small,

◯ Phone unlocks.

Otherwise,

◯ Access is denied.

Where Linear Algebra is Used

| Linear Algebra Concept | Application in Face Recognition |
| --- | --- |
| Matrix | Store digital images |
| Vector | Represent facial features |
| Matrix Multiplication | Transform image data |
| Eigenvalues | Identify significant facial characteristics |
| Eigenvectors | Create Eigenfaces |
| Distance between Vectors | Compare two faces |
| Orthogonality | Remove redundant information |
| Linear Transformation | Rotate, resize, and normalize images |

## In a nutshell……

Whenever a computer needs to work with large amounts of data-whether it’s images, videos, recommendations, maps, or AI-it first converts that data into numbers arranged as vectors and matrices.
Linear Algebra provides the mathematical tools to process those numbers efficiently, enabling technologies like face recognition, recommendation systems, image editing, robotics, and artificial intelligence.
It is one of the core building blocks of modern computing.

| Application | Linear Algebra Used For |
| --- | --- |
| Google Maps | Finding shortest routes, transformations |
| Google Photos | Face recognition |
| Instagram | Image filters |
| Snapchat | Face filters |
| ChatGPT | Al models represent words and images as vectors and perform matrix operations |
| Netflix | Movie recommendations |
| Spotify | Music recommendations |
| Amazon | Product recommendations |
| Self-driving Cars | Computer vision and object detection |
| Medical Imaging | MRI and CT scan reconstruction |
| Robotics | Motion planning and navigation |
| Games | Character movement, rotation, and 3D graphics |

## Matrices - Introduction

Matrix algebra has at least two advantages:

- Reduces complicated systems of equations to simple expressions
- Adaptable to systematic method of mathematical treatment and well suited to computers

Definition:
A matrix is a set or group of numbers arranged in a square or rectangular array enclosed by two brackets

$$
\left[\begin{array}{ll}
1 & -1
\end{array}\right] \quad\left[\begin{array}{cc}
4 & 2 \\
-3 & 0
\end{array}\right] \quad\left[\begin{array}{ll}
a & b \\
c & d
\end{array}\right]
$$

## Matrices - Introduction

Properties:

- A specified number of rows and a specified number of columns
- Two numbers (rows x columns) describe the dimensions or size of the matrix.

Examples:

$$
\begin{aligned}
& 3 \times 3 \text { matrix } \\
& 2 \times 4 \text { matrix } \\
& 1 \times 2 \text { matrix }
\end{aligned} \quad\left[\begin{array}{ccc}
1 & 2 & 4 \\
4 & -1 & 5 \\
3 & 3 & 3
\end{array}\right]\left[\begin{array}{cccl}
1 & 1 & 3 & -3 \\
0 & 0 & 3 & 2
\end{array}\right]\left[\begin{array}{ll}
1 & -1
\end{array}\right]
$$

## Matrices - Introduction

A matrix is denoted by a bold capital letter and the elements within the matrix are denoted by lower case letters e.g. matrix $[\mathbf{A}]$ with elements $\mathrm{a}_{\mathrm{ij}}$

$$
\underset{\substack{\text { m } \\
{ }_{\mathrm{m}} \mathbf{A}^{\mathrm{n}}}}{ }=\left[\begin{array}{cccc}
a_{11} & a_{12} \ldots & a_{i j} & a_{i n} \\
a_{21} & a_{22} \ldots & a_{i j} & a_{2 n} \\
\boxtimes & \boxtimes & \boxtimes & \boxtimes \\
a_{m 1} & a_{m 2} & a_{i j} & a_{m n}
\end{array}\right]
$$

i goes from 1 to m j goes from 1 to n

## Matrices - Introduction

## TYPES OF MATRICES

1. Column matrix or vector:

The number of rows may be any integer but the number of columns is always 1

$$
\left[\begin{array}{l}
1 \\
4 \\
2
\end{array}\right] \quad\left[\begin{array}{c}
1 \\
-3
\end{array}\right] \quad\left[\begin{array}{l}
a_{11} \\
a_{21} \\
\boxtimes \\
a_{m 1}
\end{array}\right]
$$

## Matrices - Introduction

TYPES OF MATRICES
2. Row matrix or vector

Any number of columns but only one row

$$
\begin{aligned}
& {\left[\begin{array}{lll}
1 & 1 & 6
\end{array}\right] \quad\left[\begin{array}{llll}
0 & 3 & 5 & 2
\end{array}\right]} \\
& {\left[\begin{array}{llll}
a_{11} & a_{12} & a_{13} & a_{1 n}
\end{array}\right]}
\end{aligned}
$$

## Matrices - Introduction

## TYPES OF MATRICES

1. Rectangular matrix

Contains more than one element and number of rows is not equal to the number of columns

$$
\begin{array}{cc}
{\left[\begin{array}{cc}
1 & 1 \\
3 & 7 \\
7 & -7 \\
7 & 6
\end{array}\right]} & {\left[\begin{array}{lllll}
1 & 1 & 1 & 0 & 0 \\
2 & 0 & 3 & 3 & 0
\end{array}\right]} \\
m \neq n
\end{array}
$$

## Matrices - Introduction

## TYPES OF MATRICES

1. Square matrix

The number of rows is equal to the number of columns (a square matrix A has an order of m)
m × m

$$
\left[\begin{array}{ll}
1 & 1 \\
3 & 0
\end{array}\right]\left[\begin{array}{lll}
1 & 1 & 1 \\
9 & 9 & 0 \\
6 & 6 & 1
\end{array}\right]
$$

The principal or main diagonal of a square matrix is composed of all elements $\mathrm{a}_{i j}$ for which $i=j$

## Matrices - Introduction

## TYPES OF MATRICES

1. Diagonal matrix

A square matrix where all the elements are zero except those on the main diagonal

$$
\left[\begin{array}{lll}
1 & 0 & 0 \\
0 & 2 & 0 \\
0 & 0 & 1
\end{array}\right] \quad\left[\begin{array}{llll}
0 & 3 & 0 & 0 \\
0 & 0 & 5 & 0 \\
0 & 0 & 0 & 9
\end{array}\right]
$$

i.e. $\mathrm{a}_{i j}=0$ for all $i \neq j$$\mathrm{a}_{i j} \neq 0$ for all $i=j$

## Matrices - Introduction

## TYPES OF MATRICES

1. Unit or Identity matrix - I

A diagonal matrix with ones on the main diagonal

$$
\left[\begin{array}{llll}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1
\end{array}\right] \quad\left[\begin{array}{ll}
1 & 0 \\
0 & 1
\end{array}\right] \quad\left[\begin{array}{cc}
a_{i j} & 0 \\
0 & a_{i j}
\end{array}\right]
$$

i.e. $\mathrm{a}_{i j}=0$ for all $i \neq j$$\mathrm{a}_{i j}=1$ for some or all $i=j$

## Matrices - Introduction

## TYPES OF MATRICES

1. Null (zero) matrix - 0

All elements in the matrix are zero

$$
\begin{aligned}
& {\left[\begin{array}{l}
0 \\
0 \\
0
\end{array}\right] \quad\left[\begin{array}{lll}
0 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 0
\end{array}\right]} \\
& { }_{i j}=0 \quad \text { For all } i, j
\end{aligned}
$$

## Matrices - Introduction

## TYPES OF MATRICES

## 8. Triangular matrix

A square matrix whose elements above or below the main diagonal are all zero

$$
\left[\begin{array}{lll}
1 & 0 & 0 \\
2 & 1 & 0 \\
5 & 2 & 3
\end{array}\right]\left[\begin{array}{lll}
1 & 0 & 0 \\
2 & 1 & 0 \\
5 & 2 & 3
\end{array}\right]\left[\begin{array}{lll}
1 & 8 & 9 \\
0 & 1 & 6 \\
0 & 0 & 3
\end{array}\right]
$$

## Matrices - Introduction

## TYPES OF MATRICES

8a. Upper triangular matrix
A square matrix whose elements below the main diagonal are all zero

$$
\left[\begin{array}{ccc}
a_{i j} & a_{i j} & a_{i j} \\
0 & a_{i j} & a_{i j} \\
0 & 0 & a_{i j}
\end{array}\right]\left[\begin{array}{lll}
1 & 8 & 7 \\
0 & 1 & 8 \\
0 & 0 & 3
\end{array}\right]\left[\begin{array}{llll}
1 & 7 & 4 & 4 \\
0 & 1 & 7 & 4 \\
0 & 0 & 7 & 8 \\
0 & 0 & 0 & 3
\end{array}\right]
$$

i.e. $\mathrm{a}_{i j}=0$ for all $i>j$

## Matrices - Introduction

## TYPES OF MATRICES

8b. Lower triangular matrix
A square matrix whose elements above the main diagonal are all zero

$$
\left[\begin{array}{ccc}
a_{i j} & 0 & 0 \\
a_{i j} & a_{i j} & 0 \\
a_{i j} & a_{i j} & a_{i j}
\end{array}\right] \quad\left[\begin{array}{lll}
1 & 0 & 0 \\
2 & 1 & 0 \\
5 & 2 & 3
\end{array}\right]
$$

i.e. $\mathrm{a}_{i j}=0$ for all $i<j$

## Matrices - Introduction TYPES OF MATRICES

1. Scalar matrix

A diagonal matrix whose main diagonal elements are equal to the same scalar

A scalar is defined as a single number or constant

$$
\begin{aligned}
& {\left[\begin{array}{ccc}
a_{i j} & 0 & 0 \\
0 & a_{i j} & 0 \\
0 & 0 & a_{i j}
\end{array}\right]\left[\begin{array}{lll}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{array}\right]\left[\begin{array}{llll}
6 & 0 & 0 & 0 \\
0 & 6 & 0 & 0 \\
0 & 0 & 6 & 0 \\
0 & 0 & 0 & 6
\end{array}\right]} \\
& \mathrm{a}_{i j}=0 \text { for all } i \neq j
\end{aligned}
$$

$\mathrm{a}_{i j}=\mathrm{a}$ for all $i=j$

# Matrices

Matrix Operations

## Matrices - Operations

EQUALITY OF MATRICES

- Two matrices are said to be equal only when all corresponding elements are equal
- their size or dimensions are equal as well

$$
\mathbf{A}=\left[\begin{array}{lll}
1 & 0 & 0 \\
2 & 1 & 0 \\
5 & 2 & 3
\end{array}\right] \quad \mathbf{B}=\left[\begin{array}{lll}
1 & 0 & 0 \\
2 & 1 & 0 \\
5 & 2 & 3
\end{array}\right] \quad \mathbf{A}=\mathbf{B}
$$

## Matrices - Operations

Some properties of equality:
IIf $\mathbf{A}=\mathbf{B}$, then $\mathbf{B}=\mathbf{A}$ for all $\mathbf{A}$ and $\mathbf{B}$
IIf $\mathbf{A}=\mathbf{B}$, and $\mathbf{B}=\mathbf{C}$, then $\mathbf{A}=\mathbf{C}$ for all $\mathbf{A}, \mathbf{B}$ and $\mathbf{C}$

$$
\mathbf{A}=\left[\begin{array}{lll}
1 & 0 & 0 \\
2 & 1 & 0 \\
5 & 2 & 3
\end{array}\right] \quad \mathbf{B}=\left[\begin{array}{lll}
b_{11} & b_{12} & b_{13} \\
b_{21} & b_{22} & b_{23} \\
b_{31} & b_{32} & b_{33}
\end{array}\right]
$$

If $\mathbf{A}=\mathbf{B}$ then $\quad a_{i j}=b_{i j}$

## Matrices - Operations

ADDITION AND SUBTRACTION OF MATRICES

The sum or difference of two matrices, A and B of the same size yields a matrix C of the same size

$$
c_{i j}=a_{i j}+b_{i j}
$$

Matrices of different sizes cannot be added or subtracted

## Matrices - Operations

Commutative Law:

$$
\mathbf{A}+\mathbf{B}=\mathbf{B}+\mathbf{A}
$$

Associative Law:

$$
\mathbf{A}+(\mathbf{B}+\mathbf{C})=(\mathbf{A}+\mathbf{B})+\mathbf{C}=\mathbf{A}+\mathbf{B}+\mathbf{C}
$$

$$
\left[\begin{array}{ccc}
7 & 3 & -1 \\
2 & -5 & 6
\end{array}\right]+\left[\begin{array}{ccc}
1 & 5 & 6 \\
-4 & -2 & 3
\end{array}\right]=\left[\begin{array}{ccc}
8 & 8 & 5 \\
-2 & -7 & 9
\end{array}\right]
$$

$\mathbf{A}$$2 \times 3$
B
$2 \times 3$
C
$2 \times 3$

## Matrices - Operations

$$
\mathbf{A}+\mathbf{0}=\mathbf{0}+\mathbf{A}=\mathbf{A}
$$

$\mathbf{A}+(-\mathbf{A})=\mathbf{0}$ (where $-\mathbf{A}$ is the matrix composed of $-\mathrm{a}_{i j}$ as elements)

$$
\left[\begin{array}{lll}
6 & 4 & 2 \\
3 & 2 & 7
\end{array}\right]-\left[\begin{array}{lll}
1 & 2 & 0 \\
1 & 0 & 8
\end{array}\right]=\left[\begin{array}{ccc}
5 & 2 & 2 \\
2 & 2 & -1
\end{array}\right]
$$

## Matrices - Operations

SCALAR MULTIPLICATION OF MATRICES

Matrices can be multiplied by a scalar (constant or single element)

Let k be a scalar quantity; then

$$
\mathbf{k A}=\mathbf{A k}
$$

Ex. If $\mathrm{k}=4$ and

$$
A=\left[\begin{array}{cc}
3 & -1 \\
2 & 1 \\
2 & -3 \\
4 & 1
\end{array}\right]
$$

## Matrices - Operations

$$
4 \times\left[\begin{array}{cc}
3 & -1 \\
2 & 1 \\
2 & -3 \\
4 & 1
\end{array}\right]=\left[\begin{array}{cc}
3 & -1 \\
2 & 1 \\
2 & -3 \\
4 & 1
\end{array}\right] \times 4=\left[\begin{array}{cc}
12 & -4 \\
8 & 4 \\
8 & -12 \\
16 & 4
\end{array}\right]
$$

Properties:

- $\mathrm{k}(\mathbf{A}+\mathbf{B})=\mathrm{k} \mathbf{A}+\mathrm{k} \mathbf{B}$
- $(\mathrm{k}+\mathrm{g}) \mathbf{A}=\mathrm{k} \mathbf{A}+\mathrm{g} \mathbf{A}$
- $\mathrm{k}(\mathbf{A B})=(\mathrm{kA}) \mathbf{B}=\mathbf{A}(\mathrm{k}) \mathbf{B}$
- $\mathrm{k}(\mathrm{gA})=(\mathrm{kg}) \mathbf{A}$

## Matrices - Operations

## MULTIPLICATION OF MATRICES

The product of two matrices is another matrix
Two matrices A and B must be conformable for multiplication to be possible
i.e. the number of columns of A must equal the number of rows of B

Example.

$$
\begin{array}{ccc}
\mathbf{A} & \mathbf{x} & \mathbf{B}
\end{array}=\frac{\mathbf{C}}{(1 \times 3)} \quad(3 \times 1) \quad(1 \times 1)
$$

## Matrices - Operations

B x A = Not possible!
$(2 \times 1)(4 \times 2)$

Ax B = Not possible!
$(6 \times 2) \quad(6 \times 3)$

Example
$\mathrm{A} \quad \mathrm{X} \quad=\quad \mathbf{C}$$(2 \times 3) \quad(3 \times 2) \quad(2 \times 2)$

## Matrices - Operations

$$
\left[\begin{array}{lll}
a_{11} & a_{12} & a_{13} \\
a_{21} & a_{22} & a_{23}
\end{array}\right]\left[\begin{array}{ll}
b_{11} & b_{12} \\
b_{21} & b_{22} \\
b_{31} & b_{32}
\end{array}\right]=\left[\begin{array}{ll}
c_{11} & c_{12} \\
c_{21} & c_{22}
\end{array}\right]
$$

$$
\begin{aligned}
& \left(a_{11} \times b_{11}\right)+\left(a_{12} \times b_{21}\right)+\left(a_{13} \times b_{31}\right)=c_{11} \\
& \left(a_{11} \times b_{12}\right)+\left(a_{12} \times b_{22}\right)+\left(a_{13} \times b_{32}\right)=c_{12} \\
& \left(a_{21} \times b_{11}\right)+\left(a_{22} \times b_{21}\right)+\left(a_{23} \times b_{31}\right)=c_{21} \\
& \left(a_{21} \times b_{12}\right)+\left(a_{22} \times b_{22}\right)+\left(a_{23} \times b_{32}\right)=c_{22}
\end{aligned}
$$

Successive multiplication of row $i$ of $\mathbf{A}$ with column $j$ of B - row by column multiplication

## Matrices - Operations

$$
\begin{aligned}
{\left[\begin{array}{lll}
1 & 2 & 3 \\
4 & 2 & 7
\end{array}\right]\left[\begin{array}{ll}
4 & 8 \\
6 & 2 \\
5 & 3
\end{array}\right] } & =\left[\begin{array}{ll}
(1 \times 4)+(2 \times 6)+(3 \times 5) & (1 \times 8)+(2 \times 2)+(3 \times 3) \\
(4 \times 4)+(2 \times 6)+(7 \times 5) & (4 \times 8)+(2 \times 2)+(7 \times 3)
\end{array}\right] \\
& =\left[\begin{array}{ll}
31 & 21 \\
63 & 57
\end{array}\right]
\end{aligned}
$$

Remember also:

$$
\mathbf{I A}=\mathbf{A}
$$

$$
\left[\begin{array}{ll}
1 & 0 \\
0 & 1
\end{array}\right]\left[\begin{array}{ll}
31 & 21 \\
63 & 57
\end{array}\right]=\left[\begin{array}{ll}
31 & 21 \\
63 & 57
\end{array}\right]
$$

## Matrices - Operations

Assuming that matrices A, B and C are conformable for the operations indicated, the following are true:

1. $\mathbf{A I}=\mathbf{I A}=\mathbf{A}$
2. $\mathbf{A}(\mathbf{B C})=(\mathbf{A B}) \mathbf{C}=\mathbf{A B C} \quad-\quad($ associative law $)$
3. $\mathbf{A}(\mathbf{B}+\mathbf{C})=\mathbf{A B}+\mathbf{A C}$ - (first distributive law)
4. $(\mathbf{A}+\mathbf{B}) \mathbf{C}=\mathbf{A C}+\mathbf{B C}-$ (second distributive law)

Caution!

1. AB not generally equal to BA, BA may not be conformable
2. If $\mathbf{A B}=\mathbf{0}$, neither A nor B necessarily $=\mathbf{0}$
3. If $\mathbf{A B}=\mathbf{A C}, \mathbf{B}$ not necessarily $=\mathbf{C}$

## Matrices - Operations

AB not generally equal to BA, BA may not be conformable

$$
\begin{aligned}
& T=\left[\begin{array}{ll}
1 & 2 \\
5 & 0
\end{array}\right] \\
& S=\left[\begin{array}{ll}
3 & 4 \\
0 & 2
\end{array}\right] \\
& T S=\left[\begin{array}{ll}
1 & 2 \\
5 & 0
\end{array}\right]\left[\begin{array}{ll}
3 & 4 \\
0 & 2
\end{array}\right]=\left[\begin{array}{cc}
3 & 8 \\
15 & 20
\end{array}\right] \\
& S T=\left[\begin{array}{ll}
3 & 4 \\
0 & 2
\end{array}\right]\left[\begin{array}{ll}
1 & 2 \\
5 & 0
\end{array}\right]=\left[\begin{array}{cc}
23 & 6 \\
10 & 0
\end{array}\right]
\end{aligned}
$$

## Matrices - Operations

If $\mathbf{A B}=\mathbf{0}$, neither A nor B necessarily $=\mathbf{0}$

$$
\left[\begin{array}{ll}
1 & 1 \\
0 & 0
\end{array}\right]\left[\begin{array}{cc}
2 & 3 \\
-2 & -3
\end{array}\right]=\left[\begin{array}{ll}
0 & 0 \\
0 & 0
\end{array}\right]
$$

## Matrices - Operations

TRANSPOSE OF A MATRIX

If :

$$
A={ }_{2} A^{3}=\left[\begin{array}{lll}
2 & 4 & 7 \\
5 & 3 & 1
\end{array}\right]
$$

Then transpose of A , denoted $\mathrm{A}^{\mathrm{T}}$ is:

$$
\begin{gathered}
A^{T}={ }_{2} A^{3^{T}}=\left[\begin{array}{ll}
2 & 5 \\
4 & 3 \\
7 & 1
\end{array}\right] \\
a_{i j}=a_{j i}^{T} \quad \text { For all } i \text { and } j
\end{gathered}
$$

## Matrices - Operations

To transpose:
Interchange rows and columns
The dimensions of $\mathbf{A}^{\mathrm{T}}$ are the reverse of the dimensions of $\mathbf{A}$

$$
\begin{array}{ll}
A={ }_{2} A^{3}=\left[\begin{array}{lll}
2 & 4 & 7 \\
5 & 3 & 1
\end{array}\right] & 2 \times 3 \\
A^{T}={ }_{3} A^{T^{2}}=\left[\begin{array}{ll}
2 & 5 \\
4 & 3 \\
7 & 1
\end{array}\right] & 3 \times 2
\end{array}
$$

## Matrices - Operations

Properties of transposed matrices:

1. $(\mathbf{A}+\mathbf{B})^{\mathrm{T}}=\mathbf{A}^{\mathrm{T}}+\mathbf{B}^{\mathrm{T}}$
2. $(\mathbf{A B})^{\mathrm{T}}=\mathbf{B}^{\mathrm{T}} \mathbf{A}^{\mathrm{T}}$
3. $(\mathrm{k} \mathbf{A})^{\mathrm{T}}=\mathrm{k} \mathbf{A}^{\mathrm{T}}$
4. $\left(\mathbf{A}^{\mathrm{T}}\right)^{\mathrm{T}}=\mathbf{A}$

## Matrices - Operations

1. $(\mathbf{A}+\mathbf{B})^{\mathrm{T}}=\mathbf{A}^{\mathrm{T}}+\mathbf{B}^{\mathrm{T}}$

$$
\begin{aligned}
& {\left[\begin{array}{ccc}
7 & 3 & -1 \\
2 & -5 & 6
\end{array}\right]+\left[\begin{array}{ccc}
1 & 5 & 6 \\
-4 & -2 & 3
\end{array}\right]=\left[\begin{array}{ccc}
8 & 8 & 5 \\
-2 & -7 & 9
\end{array}\right] \rightarrow\left[\begin{array}{cc}
8 & -2 \\
8 & -7 \\
5 & 9
\end{array}\right]} \\
& {\left[\begin{array}{cc}
7 & 2 \\
3 & -5 \\
-1 & 6
\end{array}\right]+\left[\begin{array}{cc}
1 & -4 \\
5 & -2 \\
6 & 3
\end{array}\right]=\left[\begin{array}{cc}
8 & -2 \\
8 & -7 \\
5 & 9
\end{array}\right]}
\end{aligned}
$$

## Matrices - Operations

$$
\begin{aligned}
& (\mathbf{A B})^{\mathrm{T}}=\mathbf{B}^{\mathrm{T}} \mathbf{A}^{\mathrm{T}} \\
& \quad\left[\begin{array}{lll}
1 & 1 & 0 \\
0 & 2 & 3
\end{array}\right]\left[\begin{array}{l}
1 \\
1 \\
2
\end{array}\right]=\left[\begin{array}{l}
2 \\
8
\end{array}\right] \Rightarrow\left[\begin{array}{ll}
2 & 8
\end{array}\right] \\
& \quad\left[\begin{array}{lll}
1 & 1 & 2
\end{array}\right]\left[\begin{array}{ll}
1 & 0 \\
1 & 2 \\
0 & 3
\end{array}\right]=\left[\begin{array}{ll}
2 & 8
\end{array}\right]
\end{aligned}
$$

## Symmetric and Skew-Symmetric Matrices

- Transposition gives rise to two useful classes of matrices.
- Symmetric matrices are square matrices whose transpose equals the matrix itself.
- Skew-symmetric matrices are square matrices whose transpose equals minus the matrix.

$$
\mathbf{A}^{\top}=\mathbf{A} \quad\left(\text { thus } a_{k j}=a_{j k}\right), \quad \mathbf{A}^{\top}=-\mathbf{A} \quad\left(\text { thus } a_{k j}=-a_{j k}, \text { hence } a_{j j}=0\right)
$$

## Symmetric and Skew-Symmetric Matrices

$\mathbf{A}=\left[\begin{array}{rrr}20 & 120 & 200 \\ 120 & 10 & 150 \\ 200 & 150 & 30\end{array}\right] \quad$ is symmetric, and $\quad \mathbf{B}=\left[\begin{array}{rrr}0 & 1 & -3 \\ -1 & 0 & -2 \\ 3 & 2 & 0\end{array}\right] \quad$ is skew-symmetric.

## Some Applications of Matrix Multiplication

## Computer Production. Matrix Times Matrix

Supercomp Ltd produces two computer models PC1086 and PC1186. The matrix A shows the cost per computer (in thousands of dollars) and B the production figures for the year 2010 (in multiples of 10,000 units.) Find a matrix C that shows the shareholders the cost per quarter (in millions of dollars) for raw material, labor, and miscellaneous.

$$
\mathbf{A}=\left[\begin{array}{ll}
1.2 & 1.6 \\
0.3 & 0.4 \\
0.5 & 0.6
\end{array}\right] \begin{aligned}
& 1 \\
& \text { Raw Components } \\
& \text { Labor } \\
& \text { Miscellaneous }
\end{aligned} \quad \mathbf{B}=\left[\begin{array}{cccc}
3 & 8 & 6 & 9 \\
6 & 2 & 4 & 3
\end{array}\right] \begin{aligned}
& \text { PC1086 } \\
& \text { PC1186 }
\end{aligned}
$$

Solution.

$$
\mathbf{C}=\mathbf{A B}=\begin{array}{ccrr}
1 & 2 & 3 & 4 \\
{\left[\begin{array}{rrrr}
13.2 & 12.8 & 13.6 & 15.6 \\
3.3 & 3.2 & 3.4 & 3.9 \\
5.1 & 5.2 & 5.4 & 6.3
\end{array}\right]} & \begin{array}{l} 
\\
\text { Raw Components } \\
\text { Labor } \\
\text { Miscellaneous }
\end{array}
\end{array}
$$

Since cost is given in multiples of $\$ 1000$ and production in multiples of 10,000 units, the entries of $\mathbf{C}$ are multiples of $\$ 10$ millions; thus $c_{11}=13.2$ means $\$ 132$ million, etc. $\square$

## Weight Watching. Matrix Times Vector

Suppose that in a weight-watching program, a person of 185 lb burns $350 \mathrm{cal} / \mathrm{hr}$ in walking ( 3 mph ), 500 in bicycling (13 mph), and 950 in jogging (5.5 mph). Bill, weighing 185 lb, plans to exercise according to the matrix shown. Verify the calculations ( $\mathrm{W}=$ Walking, $\mathrm{B}=$ Bicycling, $\mathrm{J}=$ Jogging).

$$
\begin{aligned}
& \\
& \mathrm{MON} \\
& \mathrm{WED} \\
& \mathrm{FRI} \\
& \mathrm{SAT}
\end{aligned} \quad\left[\begin{array}{lll}
1.0 & 0 & 0.5 \\
1.0 & 1.0 & 0.5 \\
1.5 & 0 & 0.5 \\
2.0 & 1.5 & 1.0
\end{array}\right]\left[\begin{array}{l}
350 \\
500 \\
950
\end{array}\right]=\left[\begin{array}{r}
825 \\
1325 \\
1000 \\
2400
\end{array}\right] \begin{aligned}
& \mathrm{MON} \\
& \mathrm{WED} \\
& \mathrm{FRI} \\
& \mathrm{SAT}
\end{aligned}
$$

$\square$

## Matrices - Operations

SYMMETRIC MATRICES
A Square matrix is symmetric if it is equal to its transpose:

$$
\begin{aligned}
\mathbf{A} & =\mathbf{A}^{\mathrm{T}} \\
A & =\left[\begin{array}{ll}
a & b \\
b & d
\end{array}\right] \\
A^{T} & =\left[\begin{array}{ll}
a & b \\
b & d
\end{array}\right]
\end{aligned}
$$

## Matrices - Operations

When the original matrix is square, transposition does not affect the elements of the main diagonal

$$
\begin{aligned}
& A=\left[\begin{array}{ll}
a & b \\
c & d
\end{array}\right] \\
& A^{T}=\left[\begin{array}{ll}
a & c \\
b & d
\end{array}\right]
\end{aligned}
$$

The identity matrix, I, a diagonal matrix D, and a scalar matrix, K, are equal to their transpose since the diagonal is unaffected.

## Matrices - Operations

DETERMINANT OF A MATRIX

To compute the inverse of a matrix, the determinant is required Each square matrix A has a unit scalar value called the determinant of A, denoted by $\operatorname{det} \mathbf{A}$ or $|\mathbf{A}|$

$$
\begin{aligned}
& \text { If } \quad A=\left[\begin{array}{ll}
1 & 2 \\
6 & 5
\end{array}\right] \\
& \text { then } \quad|A|=\left[\left.\begin{array}{ll}
1 & 2 \\
6 & 5
\end{array} \right\rvert\,\right.
\end{aligned}
$$

## Matrices - Operations

If $\mathbf{A}=[\mathbf{A}]$ is a single element (1×1), then the determinant is defined as the value of the element

Then $|\mathbf{A}|=\operatorname{det} \mathbf{A}=\mathrm{a}_{11}$
If $\mathbf{A}$ is ( $\mathrm{n} \times \mathrm{n}$ ), its determinant may be defined in terms of order (n-1) or less.

## Matrices - Operations

MINORS

- In matrices, a minor is the determinant of a smaller matrix obtained by deleting one row and one column from the original square matrix.
- The minor of an element $a_{i j}$ is denoted by $M_{i j}$.

To find $M_{i j}$ :

- Locate the element $a_{i j}$.
- Delete its row and column.
- Find the determinant of the remaining matrix.

## Why are minors important?

Minors are used to find:

- Cofactors
- Adjoint (Adjugate) of a matrix
- Inverse of a matrix
- Determinants using cofactor expansion

## Application of Minors and Cofactors

Minors and Cofactors are used in the calculation of the following terms:

- Adjoint of Matrix
- Inverse of Matrix

Adjoint of Matrix

Step 1: Calculate the cofactors of each element of a given matrix.
Step 2: Construct the matrix from the cofactor of elements.
Step 3: Calculate the Transpose of the resultant matrix in Step 2.
Step 4: Resulting matrix of Step 3 is the adjoint of the given matrix.

Example: Find the adjoint of the following matrix A;

$$
\mathbf{A}=\left[\begin{array}{lll}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{array}\right]
$$

Step 1: Compute the cofactors of each element in $A$

$$
\begin{aligned}
& C_{11}=5 \times 9-6 \times 8=-3 \\
& C_{12}=-(4 \times 9-6 \times 7)=6 \\
& C_{13}=4 \times 8-5 \times 7=-3 \\
& C_{21}=-(2 \times 9-3 \times 8)=6 \\
& C_{22}=1 \times 9-3 \times 7=-6 \\
& C_{23}=-(1 \times 8-2 \times 7)=3 \\
& C_{31}=2 \times 6-3 \times 5=-3 \\
& C_{32}=-(1 \times 6-3 \times 4)=6 \\
& C_{33}=1 \times 5-2 \times 4=-3
\end{aligned}
$$

Step 2: Construct the matrix of cofactors.
Matrix of cofactors, $C=\left[\begin{array}{ccc}-3 & 6 & -3 \\ 6 & -6 & 3 \\ -3 & 6 & -3\end{array}\right]$
Step 3: Transpose the matrix of cofactors.

$$
C^{\prime}=\left[\begin{array}{ccc}
-3 & 6 & -3 \\
6 & -6 & 6 \\
-3 & 3 & -3
\end{array}\right]
$$

Step 4: The resulting matrix is the adjoint of $A$.

$$
\operatorname{adj}(A)=C^{\prime}=\left[\begin{array}{ccc}
-3 & 6 & -3 \\
6 & -6 & 6 \\
-3 & 3 & -3
\end{array}\right]
$$

## Inverse of Matrix

- In matrices, a minor is the determinant of a smaller matrix obtained by deleting one row and one column from the original square matrix.
- The minor of an element $a_{i j}$ is denoted by $M_{i j}$.

To find $M_{i j}$ :
-Locate the element $a_{i j}$.
-Delete its row and column.
-Find the determinant of the remaining matrix.

Example: Find the inverse of the following matrix A:

$$
\mathbf{A}=\left[\begin{array}{ccc}
2 & -1 & 0 \\
-1 & 2 & -1 \\
0 & -1 & 2
\end{array}\right]
$$

Solution:
Step 1: Find the determinant of $A$.

$$
\begin{aligned}
& \operatorname{det}(A)=2(2 \times 2-(-1) \times(-1))-(-1)((-1) \times 2-(-1) \times 0)+0 \\
& \Rightarrow \operatorname{det}(A)=6-2=4
\end{aligned}
$$

Step 2: Calculate the adjoint of $A$ using the steps mentioned in the previous example.

$$
\begin{aligned}
& C_{11}=4-1=3 \\
& C_{12}=-(-2-0)=2 \\
& C_{13}=1-0=1 \\
& C_{21}=-(-2-0)=2 \\
& C_{22}=4-0=4 \\
& C_{23}=-(-2-0)=2 \\
& C_{31}=(1-0)=1 \\
& C_{32}=-(-2-0)=2 \\
& C_{33}=4-1=3
\end{aligned}
$$

Matrix of cofactors,

$$
C=\left[\begin{array}{lll}
3 & 2 & 1 \\
2 & 4 & 2 \\
1 & 2 & 3
\end{array}\right]
$$

Transpose of matrix of cofactors,

$$
\operatorname{adj}(A)=C^{\prime}=\left[\begin{array}{lll}
3 & 2 & 1 \\
2 & 4 & 2 \\
1 & 2 & 3
\end{array}\right]
$$

Step 3: Multiply the adjoint of $A$ by the reciprocal of the determinant.

$$
\begin{aligned}
& A^{-1}=\frac{\operatorname{adj}(A)}{4}=\frac{1}{4} \times\left[\begin{array}{lll}
3 & 2 & 1 \\
2 & 4 & 2 \\
1 & 2 & 3
\end{array}\right] \\
& \Rightarrow A^{-1}=\left[\begin{array}{lll}
\frac{3}{4} & \frac{2}{4} & \frac{1}{4} \\
\frac{2}{4} & \frac{4}{4} & \frac{2}{4} \\
\frac{1}{4} & \frac{2}{4} & \frac{3}{4}
\end{array}\right] \\
& \Rightarrow A^{-1}=\left[\begin{array}{lll}
\frac{3}{4} & \frac{1}{2} & \frac{1}{4} \\
\frac{1}{2} & 1 & \frac{1}{2} \\
\frac{1}{4} & \frac{1}{2} & \frac{3}{4}
\end{array}\right]
\end{aligned}
$$

## Matrices - Operations

eg.

$$
A=\left[\begin{array}{lll}
a_{11} & a_{12} & a_{13} \\
a_{21} & a_{22} & a_{23} \\
a_{31} & a_{32} & a_{33}
\end{array}\right]
$$

Each element in A has a minor
Delete first row and column from A.
The determinant of the remaining 2 x 2 submatrix is the minor of $\mathbf{a}_{\mathbf{1 1}}$

$$
m_{11}=\left|\begin{array}{ll}
a_{22} & a_{23} \\
a_{32} & a_{33}
\end{array}\right|
$$

## Matrices - Operations

Therefore the minor of $\mathrm{a}_{12}$ is:

$$
m_{12}=\left|\begin{array}{ll}
a_{21} & a_{23} \\
a_{31} & a_{33}
\end{array}\right|
$$

And the minor for $\mathrm{a}_{13}$ is:

$$
m_{13}=\left|\begin{array}{ll}
a_{21} & a_{22} \\
a_{31} & a_{32}
\end{array}\right|
$$

Minors and Co-factors

![](1%20Matrix%20Algebra/imagesb366c259-1b05-4d8d-9d6b-cce59629bba4-061_1223_1966_418_234.jpg)

$$
|A|=\left\lvert\, \begin{array}{lll}
1 & 2 & 3 \\
2 & 0 & 1 \\
5 & 3 & 6
\end{array}\right.
$$

## Matrices - Operations

COFACTORS

The cofactor $\mathrm{C}_{i j}$ of an element $\mathrm{a}_{i j}$ is defined as:

$$
C_{i j}=(-1)^{i+j} m_{i j}
$$

When the sum of a row number $i$ and column $j$ is even, $\mathrm{c}_{i j}=\mathrm{m}_{i j}$ and when $i+j$ is odd, $\mathrm{c}_{i j}=-\mathrm{m}_{i j}$

$$
\begin{aligned}
& c_{11}(i=1, j=1)=(-1)^{1+1} m_{11}=+m_{11} \\
& c_{12}(i=1, j=2)=(-1)^{1+2} m_{12}=-m_{12} \\
& c_{13}(i=1, j=3)=(-1)^{1+3} m_{13}=+m_{13}
\end{aligned}
$$

## Matrices - Operations

DETERMINANTS CONTINUED

The determinant of an $\mathrm{n} \times \mathrm{n}$ matrix $\mathbf{A}$ can now be defined as

$$
|A|=\operatorname{det} A=a_{11} c_{11}+a_{12} c_{12}+\boxtimes+a_{1 n} c_{1 n}
$$

The determinant of $\mathbf{A}$ is therefore the sum of the products of the elements of the first row of A and their corresponding cofactors.
(It is possible to define $|\mathbf{A}|$ in terms of any other row or column but for simplicity, the first row only is used)

## Matrices - Operations

Therefore the $2 \times 2$ matrix :

$$
A=\left[\begin{array}{ll}
a_{11} & a_{12} \\
a_{21} & a_{22}
\end{array}\right]
$$

Has cofactors :

$$
c_{11}=m_{11}=\left|a_{22}\right|=a_{22}
$$

And:

$$
c_{12}=-m_{12}=-\left|a_{21}\right|=-a_{21}
$$

And the determinant of $\mathbf{A}$ is:

$$
|A|=a_{11} c_{11}+a_{12} c_{12}=a_{11} a_{22}-a_{12} a_{21}
$$

## Matrices - Operations

Example 1:

$$
\begin{gathered}
A=\left[\begin{array}{ll}
3 & 1 \\
1 & 2
\end{array}\right] \\
|A|=(3)(2)-(1)(1)=5
\end{gathered}
$$

## Matrices - Operations

For a $3 \times 3$ matrix:

$$
A=\left[\begin{array}{lll}
a_{11} & a_{12} & a_{13} \\
a_{21} & a_{22} & a_{23} \\
a_{31} & a_{32} & a_{33}
\end{array}\right]
$$

The cofactors of the first row are:

$$
\begin{aligned}
& c_{11}=\left|\begin{array}{ll}
a_{22} & a_{23} \\
a_{32} & a_{33}
\end{array}\right|=a_{22} a_{33}-a_{23} a_{32} \\
& c_{12}=-\left|\begin{array}{ll}
a_{21} & a_{23} \\
a_{31} & a_{33}
\end{array}\right|=-\left(a_{21} a_{33}-a_{23} a_{31}\right) \\
& c_{13}=\left|\begin{array}{ll}
a_{21} & a_{22} \\
a_{31} & a_{32}
\end{array}\right|=a_{21} a_{32}-a_{22} a_{31}
\end{aligned}
$$

## Matrices - Operations

The determinant of a matrix A is:

$$
|A|=a_{11} c_{11}+a_{12} c_{12}=a_{11} a_{22}-a_{12} a_{21}
$$

Which by substituting for the cofactors in this case is:

$$
|A|=a_{11}\left(a_{22} a_{33}-a_{23} a_{32}\right)-a_{12}\left(a_{21} a_{33}-a_{23} a_{31}\right)+a_{13}\left(a_{21} a_{32}-a_{22} a_{31}\right)
$$

## Matrices - Operations

Example 2:

$$
A=\left[\begin{array}{ccc}
1 & 0 & 1 \\
0 & 2 & 3 \\
-1 & 0 & 1
\end{array}\right]
$$

$$
|A|=a_{11}\left(a_{22} a_{33}-a_{23} a_{32}\right)-a_{12}\left(a_{21} a_{33}-a_{23} a_{31}\right)+a_{13}\left(a_{21} a_{32}-a_{22} a_{31}\right)
$$

$$
|A|=(1)(2-0)-(0)(0+3)+(1)(0+2)=4
$$

Example: Use the above steps to compute the determinant of $3 \times 3$ matrix

$$
A=\left[\begin{array}{lll}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{array}\right] .
$$

Solution:

$$
\begin{aligned}
& \operatorname{det} A=1(\text { co-factor of } 1)+2(\text { co-factor of } 2)+3(\text { co-factor of } 3) \\
& =1 \\
& =1[5(9)-6(8)]-2[4(9)-6(7)]+3[4(8)-5(7)] \\
& =1(-3)-2(-6)+3(-3) \\
& =-3+12-9 \\
& =0
\end{aligned}
$$

## Matrices - Operations

ADJOINT MATRICES

A cofactor matrix C of a matrix A is the square matrix of the same order as $\mathbf{A}$ in which each element $\mathrm{a}_{i j}$ is replaced by its cofactor $\mathrm{c}_{i j}$.

Example:
If

$$
A=\left[\begin{array}{cc}
1 & 2 \\
-3 & 4
\end{array}\right]
$$

The cofactor C of A is $\quad C=\left[\begin{array}{cc}4 & 3 \\ -2 & 1\end{array}\right]$

## Matrices - Operations

The adjoint matrix of $\mathbf{A}$, denoted by $\operatorname{adj} \mathbf{A}$, is the transpose of its cofactor matrix

$$
\operatorname{adj} A=C^{T}
$$

It can be shown that:

$$
\mathbf{A}(\operatorname{adj} \mathbf{A})=(\operatorname{adj} \mathbf{A}) \mathbf{A}=|\mathbf{A}| \mathbf{I}
$$

Example:

$$
\begin{aligned}
& A=\left[\begin{array}{cc}
1 & 2 \\
-3 & 4
\end{array}\right] \\
& |A|=(1)(4)-(2)(-3)=10 \\
& \operatorname{adj} A=C^{T}=\left[\begin{array}{cc}
4 & -2 \\
3 & 1
\end{array}\right]
\end{aligned}
$$

## Matrices - Operations

$$
\begin{aligned}
& A(\operatorname{adj} A)=\left[\begin{array}{cc}
1 & 2 \\
-3 & 4
\end{array}\right]\left[\begin{array}{cc}
4 & -2 \\
3 & 1
\end{array}\right]=\left[\begin{array}{cc}
10 & 0 \\
0 & 10
\end{array}\right]=10 \mathrm{I} \\
& (\operatorname{adj} A) A=\left[\begin{array}{cc}
4 & -2 \\
3 & 1
\end{array}\right]\left[\begin{array}{cc}
1 & 2 \\
-3 & 4
\end{array}\right]=\left[\begin{array}{cc}
10 & 0 \\
0 & 10
\end{array}\right]=10 \mathrm{I}
\end{aligned}
$$

## Find Minors and Cofactors of the Elements of the Determinant

Problem 1: In the given matrix:

231
$\mathrm{A}=457$
689

## Find:

1. Find the minor $\mathrm{M}_{11}$ of the element $\mathrm{a}_{11}=2$.
2. Find the Cofactor $\mathrm{C}_{11}$ of the element $\mathrm{a}_{11}=2$.
3. Find the minor $\mathrm{M}_{11}$ of the element $\mathrm{a}_{11}$

To find Minor $M_{11}$ delete the first row and first column of the given matrix $A$, and we will get:

$$
\begin{aligned}
& {\left[\begin{array}{ll}
5 & 7 \\
8 & 9
\end{array}\right]} \\
& M_{11}=\operatorname{det}\left[\begin{array}{ll}
5 & 7 \\
8 & 9
\end{array}\right]=(5 \times 9)-(8 \times 7)=45-56=-11
\end{aligned}
$$

1. Find the Cofactor $\mathrm{C}_{11}$ of the element $\mathrm{a}_{11}$

Using the formula for finding the cofactor;

$$
\begin{aligned}
& C_{i j}=(-1)^{i+j} M_{i j} \\
& C_{11}=(-1)^{1+1} \times(-11)=-11
\end{aligned}
$$

## Matrices - Operations

USING THE ADJOINT MATRIX IN MATRIX INVERSION
Since

$$
\mathbf{A} \mathbf{A}^{-1}=\mathbf{A}^{-1} \mathbf{A}=\mathbf{I}
$$

and

$$
\mathbf{A}(\operatorname{adj} \mathbf{A})=(\operatorname{adj} \mathbf{A}) \mathbf{A}=|\mathbf{A}| \mathbf{I}
$$

then

$$
A^{-1}=\frac{\operatorname{adj} A}{|A|}
$$

## Matrices - Operations

Example

$$
\begin{gathered}
\mathbf{A}=\left[\begin{array}{cc}
1 & 2 \\
-3 & 4
\end{array}\right] \\
A^{-1}=\frac{1}{10}\left[\begin{array}{cc}
4 & -2 \\
3 & 1
\end{array}\right]=\left[\begin{array}{cc}
0.4 & -0.2 \\
0.3 & 0.1
\end{array}\right]
\end{gathered}
$$

To check

$$
\mathbf{A} \mathbf{A}^{-1}=\mathbf{A}^{-1} \mathbf{A}=\mathbf{I}
$$

$$
\begin{aligned}
& A A^{-1}=\left[\begin{array}{cc}
1 & 2 \\
-3 & 4
\end{array}\right]\left[\begin{array}{cc}
0.4 & 0.2 \\
0.3 & 0.1
\end{array}\right]=\left[\begin{array}{ll}
1 & 0 \\
0 & 1
\end{array}\right]=I \\
& A^{-1} A=\left[\begin{array}{cc}
0.4 & -0.2 \\
0.3 & 0.1
\end{array}\right]\left[\begin{array}{cc}
1 & 2 \\
-3 & 4
\end{array}\right]=\left[\begin{array}{ll}
1 & 0 \\
0 & 1
\end{array}\right]=I
\end{aligned}
$$

## Matrices - Operations

Example 2

$$
A=\left[\begin{array}{ccc}
3 & -1 & 1 \\
2 & 1 & 0 \\
1 & 2 & -1
\end{array}\right]
$$

The determinant of $\mathbf{A}$ is

$$
|\mathbf{A}|=(3)(-1-0)-(-1)(-2-0)+(1)(4-1)=-2
$$

The elements of the cofactor matrix are

$$
\begin{array}{lll}
c_{11}=+(-1), & c_{12}=-(-2), & c_{13}=+(3), \\
c_{21}=-(-1), & c_{22}=+(-4), & c_{23}=-(7), \\
c_{31}=+(-1), & c_{32}=-(-2), & c_{33}=+(5),
\end{array}
$$

## Matrices - Operations

The cofactor matrix is therefore

$$
C=\left[\begin{array}{ccc}
-1 & 2 & 3 \\
1 & -4 & -7 \\
-1 & 2 & 5
\end{array}\right]
$$

so

$$
\operatorname{adj} A=C^{T}=\left[\begin{array}{ccc}
-1 & 1 & -1 \\
2 & -4 & 2 \\
3 & -7 & 5
\end{array}\right]
$$

and

$$
A^{-1}=\frac{\operatorname{adj} A}{|A|}=\frac{1}{-2}\left[\begin{array}{ccc}
-1 & 1 & -1 \\
2 & -4 & 2 \\
3 & -7 & 5
\end{array}\right]=\left[\begin{array}{ccc}
0.5 & -0.5 & 0.5 \\
-1.0 & 2.0 & -1.0 \\
-1.5 & 3.5 & -2.5
\end{array}\right]
$$

## Matrices - Operations

The result can be checked using

$$
\mathbf{A} \mathbf{A}^{-1}=\mathbf{A}^{-1} \mathbf{A}=\mathbf{I}
$$

The determinant of a matrix must not be zero for the inverse to exist as there will not be a solution

Nonsingular matrices have non-zero determinants
Singular matrices have zero determinants

# Matrix Inversion

## Simple 2 × 2 case

## Simple 2 × 2 case

Let

$$
A=\left[\begin{array}{ll}
a & b \\
c & d
\end{array}\right] \quad \text { and } \quad A^{-1}=\left[\begin{array}{ll}
w & x \\
y & z
\end{array}\right]
$$

Since it is known that

$$
\mathbf{A} \mathbf{A}^{-1}=\mathbf{I}
$$

then

$$
\left[\begin{array}{ll}
a & b \\
c & d
\end{array}\right]\left[\begin{array}{ll}
w & x \\
y & z
\end{array}\right]=\left[\begin{array}{ll}
1 & 0 \\
0 & 1
\end{array}\right]
$$

## Inverse of a Matrix

$$
\begin{gathered}
A=\left[\begin{array}{ll}
a & b \\
c & d
\end{array}\right] \\
A^{-1}=\left[\begin{array}{ll}
a & b \\
c & d
\end{array}\right]_{\text {Click to enlarge }}^{-1}=\frac{1}{a d-b c}\left[\begin{array}{cc}
d & -b \\
-c & a
\end{array}\right]
\end{gathered}
$$

Note: This formula only works on Square matrices.

## Adjoint of 2 * 2 Matrix

- In matrices, a minor is the determinant of a smaller matrix obtained by deleting one row and one column from the original square matrix.
- The minor of an element $a_{i j}$ is denoted by $M_{i j}$.
To find $M_{i j}$ :
    
    $$
    \operatorname{adj}(A)=\left[\begin{array}{cc}
    d & -b \\
    -c & a
    \end{array}\right]
    $$
    
- Locate the element $a_{i j}$.
- Delete its row and column.
- Find the determinant of the remaining matrix.

## Simple 2 × 2 case

So that for a $2 \times 2$ matrix the inverse can be constructed in a simple fashion as

$$
A^{-1}=\left[\begin{array}{ll}
w & x \\
y & z
\end{array}\right]=\left[\begin{array}{cc}
\frac{d}{|A|} & \frac{b}{|A|} \\
\frac{-c}{|A|} & \frac{a}{|A|}
\end{array}\right]=\frac{1}{|A|}\left[\begin{array}{cc}
d & -b \\
-c & a
\end{array}\right]
$$

- Exchange elements of main diagonal
- Change sign in elements off main diagonal
- Divide resulting matrix by the determinant

## Simple 2 × 2 case

Example

$$
\begin{aligned}
& A=\left[\begin{array}{ll}
2 & 3 \\
4 & 1
\end{array}\right] \\
& A^{-1}=-\frac{1}{10}\left[\begin{array}{cc}
1 & -3 \\
-4 & 2
\end{array}\right]=\left[\begin{array}{cc}
-0.1 & 0.3 \\
0.4 & -0.2
\end{array}\right]
\end{aligned}
$$

Check inverse

$$
\begin{aligned}
& \mathbf{A}^{-1} \mathbf{A}=\mathbf{I} \\
& -\frac{1}{10}\left[\begin{array}{cc}
1 & -3 \\
-4 & 2
\end{array}\right]\left[\begin{array}{ll}
2 & 3 \\
4 & 1
\end{array}\right]=\left[\begin{array}{ll}
1 & 0 \\
0 & 1
\end{array}\right]=I
\end{aligned}
$$

## Reinforcement Learning Questions

- In matrices, a minor is the determinant of a smaller matrix obtained by deleting one row and one column from the original square matrix.
- The minor of an element $a_{i j}$ is denoted by $M_{i j}$.

To find $M_{i j}$ :
-Locate the element $a_{i j}$.
-Delete its row and column.
-Find the determinant of the remaining matrix.

Which of the following statements is FALSE?

1. Every identity matrix is a diagonal matrix.
2. Every diagonal matrix is a scalar matrix.
3. Every scalar matrix is a diagonal matrix.
4. Every zero matrix is a diagonal matrix.

Which of the following matrices is NOT possible?

1. A matrix that is both upper triangular and lower triangular.
2. A matrix that is both symmetric and skew-symmetric.
3. A matrix that is both diagonal and scalar.
4. A matrix that is both rectangular and square.

Which of the following statements is ALWAYS true?

1. Every identity matrix is a scalar matrix.
    1. Every scalar matrix is an identity matrix.
    2. Every symmetric matrix is diagonal.
    3. Every diagonal matrix is an identity matrix.
- In matrices, a minor is the determinant of a smaller matrix obtained by deleting one row and one column from the original square matrix.
- The minor of an element $a_{i j}$ is denoted by $M_{i j}$.

To find $M_{i j}$ :

- Locate the element $a_{i j}$.
-Delete its row and column.
-Find the determinant of the remaining matrix.

Find $x$ such that:

$$
\left[\begin{array}{ll}
x & 1
\end{array}\right]\left[\begin{array}{ll}
1 & 2 \\
2 & 1
\end{array}\right]\left[\begin{array}{l}
1 \\
1
\end{array}\right]=6
$$

A. $x=2$
B. $x=1$
C. $x=3$
D. $x=0$

Example 1: If the determinant of matrix $\left[\begin{array}{cc}2 x & 9 \\ 2 & x\end{array}\right]$ is 0 , then find the possible value(s) of x.

Example 2:
Let

$$
A=\left(\begin{array}{lll}
2 & 1 & 3 \\
4 & 1 & 5
\end{array}\right) .
$$

Find $A X$ for each of the following values of $X$.
(a) $X=\left(\begin{array}{l}1 \\ 0 \\ 0\end{array}\right)$
(b) $X=\left(\begin{array}{l}0 \\ 1 \\ 1\end{array}\right)$
(c) $X=\left(\begin{array}{l}0 \\ 0 \\ 1\end{array}\right)$

Find the value of $x$ in the matrix below if its determinant has a value of -12 .

$$
\left[\begin{array}{cc}
-4 & 2 \\
-8 & x
\end{array}\right]
$$

If first row of a matrix is entirely zero, then the determinant is

1. 1
2. Depends on the matrix
3. 0
4. Cannot be found

The determinant of an identity matrix of order 5 is

1. 0
2. 1
3. 5
4. 25

The adjoint of a matrix is obtained by

1. Transposing the original matrix
2. Taking transpose of the cofactor matrix
3. Taking transpose of the minor matrix
4. Finding the inverse directly
- In matrices, a minor is the determinant of a smaller matrix obtained by deleting one row and one column from the original square matrix.
- The minor of an element $a_{i j}$ is denoted by $M_{i j}$.

To find $M_{i j}$ :

- Locate the element $a_{i j}$.
- Delete its row and column.
- Find the determinant of the remaining matrix.

If a matrix has determinant equal to 1 , then

1. Inverse does not exist.
2. Inverse equals adjoint.
3. Adjoint equals transpose.
4. Inverse equals original matrix.
- In matrices, a minor is the determinant of a smaller matrix obtained by deleting one row and one column from the original square matrix.
- The minor of an element $a_{i j}$ is denoted by $M_{i j}$.

To find $M_{i j}$ :

- Locate the element $a_{i j}$.
- Delete its row and column.
- Find the determinant of the remaining matrix.

Arrange the following steps in the correct order for finding the inverse of a matrix.

1. Find determinant
2. Find adjoint
3. Find cofactors
4. Find minors
5. Divide by determinant
6. 1, 4, 3, 2, 5
7. 4, 3, 2, 1, 5
8. 1, 3, 4, 2, 5
9. 3, 4, 2, 1, 5
- In matrices, a minor is the determinant of a smaller matrix obtained by deleting one row and one column from the original square matrix.
- The minor of an element $a_{i j}$ is denoted by $M_{i j}$.

To find $M_{i j}$ :

- Locate the element $a_{i j}$.
- Delete its row and column.
- Find the determinant of the remaining matrix.
- In matrices, a minor is the determinant of a smaller matrix obtained by deleting one row and one column from the original square matrix.
- The minor of an element $a_{i j}$ is denoted by $M_{i j}$.

To find $M_{i j}$ :

- Locate the element $a_{i j}$.
- Delete its row and column.
- Find the determinant of the remaining matrix.
- In matrices, a minor is the determinant of a smaller matrix obtained by deleting one row and one column from the original square matrix.
- The minor of an element $a_{i j}$ is denoted by $M_{i j}$.

To find $M_{i j}$ :

- Locate the element $a_{i j}$.
-Delete its row and column.
-Find the determinant of the remaining matrix.