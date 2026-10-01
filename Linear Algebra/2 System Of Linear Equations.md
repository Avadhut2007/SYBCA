# 2. System Of Linear Equations

## Linear Equations

Linear equations are common and important for survey problems

Matrices can be used to express these linear equations and aid in the computation of unknown values

Example
$n$ equations in $n$ unknowns, the $\mathrm{a}_{i j}$ are numerical coefficients, the $\mathrm{b}_{i}$ are constants and the $\mathrm{x}_{j}$ are unknowns

$$
\begin{aligned}
& a_{11} x_{1}+a_{12} x_{2}+\boxtimes+a_{1 n} x_{n}=b_{1} \\
& a_{21} x_{1}+a_{22} x_{2}+\boxtimes+a_{2 n} x_{n}=b_{2} \\
& \\
& a_{n 1} x_{1}+a_{n 2} x_{2}+\boxtimes+a_{n n} x_{n}=b_{n}
\end{aligned}
$$

## Linear Equations

The equations may be expressed in the form

$$
\mathbf{A X}=\mathbf{B}
$$

where

$$
\begin{gathered}
A=\left[\begin{array}{lll}
a_{11} & a_{12} & a_{1 n} \\
a_{21} & a_{22} & a_{2 n} \\
\boxtimes & \boxtimes & \boxtimes \\
a_{n 1} & a_{n 1} & a_{n n}
\end{array}\right], X=\left[\begin{array}{l}
x_{1} \\
x_{2} \\
\boxtimes \\
x_{n}
\end{array}\right], \text { and } \quad B=\left[\begin{array}{l}
b_{1} \\
b_{2} \\
\boxtimes \\
b_{n}
\end{array}\right] \\
\mathrm{n} \times \mathrm{n}
\end{gathered}
$$

Number of unknowns = number of equations $=\mathrm{n}$

## Augmented Matrix

- An augmented matrix is a matrix formed by combining the coefficient matrix of a system of linear equations with the column matrix of constants. It provides a compact way to represent and solve linear equations using matrix operations.

![](2%20System%20Of%20Linear%20Equations/images9b9eabbd-1713-4a78-97ba-0128e64a5d82-04_884_774_987_864.jpg)

- Example: Find the augmented matrix of the system of equations. $\left\{\begin{array}{l}-x-4 y-9 z=-7 \\ -3 x-4 y-5 z=-4 \\ -2 x-3 y-6 z=-3\end{array}\right.$

Solution:
Coefficient Matrix: $\left[\begin{array}{ccc}-1 & -4 & -9 \\ -3 & -4 & -5 \\ -2 & -3 & -6\end{array}\right]$
Constant Matrix: $\left[\begin{array}{l}-7 \\ -4 \\ -3\end{array}\right]$
Required Augmented Matrix:

$$
\left[\begin{array}{cccc}
-1 & -4 & -9 & -7 \\
-3 & -4 & -5 \mid & -4 \\
-2 & -3 & -6 \mid & -3
\end{array}\right]
$$

## Linear Equations - Matrix Inversion Method

If the determinant is nonzero, the equation can be solved to produce n numerical values for x that satisfy all the simultaneous equations

To solve, premultiply both sides of the equation by $\mathbf{A}^{-1}$ which exists because $|\mathbf{A}| \neq \mathbf{0}$

$$
\mathbf{A}^{-1} \mathbf{A} \mathbf{X}=\mathbf{A}^{-1} \mathbf{B}
$$

Now since

$$
\mathbf{A}^{-1} \mathbf{A}=\mathbf{I}
$$

We get

$$
\mathbf{X}=\mathbf{A}^{-1} \mathbf{B}
$$

So if the inverse of the coefficient matrix is found, the unknowns, X would be determined

- Example: Find the augmented matrix of the system of equations. $\quad\left\{\begin{array}{r}-x-4 y-9 z=-7 \\ -3 x-4 y-5 z=-4 \\ -2 x-3 y-6 z=-3\end{array}\right.$
- Example: Find the augmented matrix of the system of equations. $\left\{\begin{array}{l}-x-4 y-9 z=-7 \\ -3 x-4 y-5 z=-4 \\ -2 x-3 y-6 z=-3\end{array}\right.$
- Example: Find the augmented matrix of the system of equations. $\left\{\begin{array}{l}-x-4 y-9 z=-7 \\ -3 x-4 y-5 z=-4 \\ -2 x-3 y-6 z=-3\end{array}\right.$
- Example: Find the augmented matrix of the system of equations. $\left\{\begin{array}{l}-x-4 y-9 z=-7 \\ -3 x-4 y-5 z=-4 \\ -2 x-3 y-6 z=-3\end{array}\right.$
- Example: Find the augmented matrix of the system of equations. $\left\{\begin{array}{l}-x-4 y-9 z=-7 \\ -3 x-4 y-5 z=-4 \\ -2 x-3 y-6 z=-3\end{array}\right.$
- Example: Find the augmented matrix of the system of equations. $\left\{\begin{array}{l}-x-4 y-9 z=-7 \\ -3 x-4 y-5 z=-4 \\ -2 x-3 y-6 z=-3\end{array}\right.$

? Example: Find the augmented matrix of the system of equations. $\left\{\begin{array}{l}-x-4 y-9 z=-7 \\ -3 x-4 y-5 z=-4 \\ -2 x-3 y-6 z=-3\end{array}\right.$

## Linear Equations - Matrix Inversion Method

Example

$$
\begin{aligned}
& 3 x_{1}-x_{2}+x_{3}=2 \\
& 2 x_{1}+x_{2}=1 \\
& x_{1}+2 x_{2}-x_{3}=3
\end{aligned}
$$

The equations can be expressed expressed in the form $\mathbf{A X}=\mathbf{B}$

$$
\left[\begin{array}{ccc}
3 & -1 & 1 \\
2 & 1 & 0 \\
1 & 2 & -1
\end{array}\right]\left[\begin{array}{l}
x_{1} \\
x_{2} \\
x_{3}
\end{array}\right]=\left[\begin{array}{l}
2 \\
1 \\
3
\end{array}\right]
$$

## Linear Equations - Matrix Inversion Method

When $\mathbf{A}^{-1}$ is computed the equation becomes

$$
X=A^{-1} B=\left[\begin{array}{ccc}
0.5 & -0.5 & 0.5 \\
-1.0 & 2.0 & -1.0 \\
-1.5 & 3.5 & -2.5
\end{array}\right]\left[\begin{array}{l}
2 \\
1 \\
3
\end{array}\right]=\left[\begin{array}{c}
2 \\
-3 \\
7
\end{array}\right]
$$

Therefore

$$
\begin{aligned}
& x_{1}=2, \\
& x_{2}=-3, \\
& x_{3}=-7
\end{aligned}
$$

## Linear Equations - Matrix Inversion Method

The values for the unknowns should be checked by substitution back into the initial equations

$$
\begin{array}{ll}
x_{1}=2, & 3 x_{1}-x_{2}+x_{3}=2 \\
x_{2}=-3, & 2 x_{1}+x_{2}=1 \\
x_{3}=-7 & x_{1}+2 x_{2}-x_{3}=3
\end{array}
$$

$$
\begin{aligned}
& 3 \times(2)-(-3)+(-7)=2 \\
& 2 \times(2)+(-3)=1 \\
& (2)+2 \times(-3)-(-7)=3
\end{aligned}
$$

## Row Echelon Form

- A matrix is in row echelon form if it is obtained as the result of Gaussian Elimination on the rows of that matrix. This form of the matrix must satisfy some conditions which are discussed below:
    - The leading (non-zero) entry or pivot must be to the right of the leading entry of the row above it.
    - Any row consisting entirely of zeros comes at the bottom of the matrix.
    - In each row the number of zeroes must be more than the previous row
        
        $$
        \left[\begin{array}{rrrr}
        1 & 2 & -1 & 4 \\
        0 & 1 & 0 & 3 \\
        0 & 0 & 1 & 2
        \end{array}\right]
        $$
        

For example, the following matrix is in row echelon form, and its leading entries are shown in red:

$$
\left[\begin{array}{cccc}
0 & 2 & 1 & -1 \\
0 & 0 & 3 & 1 \\
0 & 0 & 0 & 0
\end{array}\right] .
$$

It is in echelon form because the zero row is at the bottom and the leading entry of the second row (in the third column) is to the right of the leading entry of the first row (in the second column).

![](2%20System%20Of%20Linear%20Equations/images9b9eabbd-1713-4a78-97ba-0128e64a5d82-18_1362_765_509_799.jpg)

Which of the following matrices is in row echelon form?

$$
\left[\begin{array}{ll}
0 & 1 \\
1 & 0 \\
0 & 0
\end{array}\right]\left[\begin{array}{ll}
1 & 2 \\
0 & 1 \\
0 & 0
\end{array}\right]\left[\begin{array}{ll}
1 & 2 \\
0 & 1 \\
0 & 1
\end{array}\right]\left[\begin{array}{ll}
1 & 0 \\
0 & 0 \\
0 & 1
\end{array}\right]
$$

A
B
C
D

1. Matrix A
2. Matrix B
3. Matrix C
4. Matrix D
5. None of the above

Solution

The correct answer is (B), since it satisfies all of the requirements for a row echelon matrix.

## Steps of Gaussian Elimination

- Form the Augmented Matrix: Represent the system as an augmented matrix combining coefficients and constants.
- Forward Elimination: Use row operations-swapping rows, scaling rows, or adding multiples of one row to another-to convert the matrix into row echelon (upper triangular) form.
- Back-Substitution: Solve the resulting triangular system from the bottom up to find the values of the variables.

## Elementary Row Operations for Matrices

- Interchange of two rows
- Addition of a constant multiple of one row to another row
- Multiplication of a row by a nonzero constant $c$

## Gauss Elimination: The Three Possible Cases of Systems

When solving a system of linear equations using the Gaussian Elimination Method, there are three possible outcomes after converting the augmented matrix into Row Echelon Form (REF).

| Case | Condition | Result |
| --- | --- | --- |
| Case 1 | No contradictory row and every variable has a pivot | Unique Solution |
| Case 2 | One or more rows become all zeros | Infinitely Many Solutions |
| Case 3 | A contradictory row appears | No Solution (Inconsistent System) |
- Example: Find the augmented matrix of the system of equations. $\left\{\begin{array}{l}-x-4 y-9 z=-7 \\ -3 x-4 y-5 z=-4 \\ -2 x-3 y-6 z=-3\end{array}\right.$
’ Example: Find the augmented matrix of the system of equations. $\left\{\begin{array}{l}-x-4 y-9 z=-7 \\ -3 x-4 y-5 z=-4 \\ -2 x-3 y-6 z=-3\end{array}\right.$
- Example: Find the augmented matrix of the system of equations. $\left\{\begin{array}{l}-x-4 y-9 z=-7 \\ -3 x-4 y-5 z=-4 \\ -2 x-3 y-6 z=-3\end{array}\right.$
- Example: Find the augmented matrix of the system of equations. $\left\{\begin{array}{l}-x-4 y-9 z=-7 \\ -3 x-4 y-5 z=-4 \\ -2 x-3 y-6 z=-3\end{array}\right.$
- Example: Find the augmented matrix of the system of equations. $\left\{\begin{array}{c}-x-4 y-9 z=-7 \\ -3 x-4 y-5 z=-4 \\ -2 x-3 y-6 z=-3\end{array}\right.$

$$
x=1, \quad y=2, \quad z=3
$$

## Reduced Row-Echelon Form

- Reduced Row-Echelon Form (RREF) is a special form of a matrix in which each leading entry is 1 and is the only non-zero entry in its column.
- All the entries above/below each pivot must be a zero.
- The leading 1 in the rows is always right of the leading 1 of the first row
- If there are any rows containing all zeros, they should be at the bottom of the matrix.
    
    $$
    \left[\begin{array}{lll}
    1 & 0 & 0 \\
    0 & 1 & 0 \\
    0 & 0 & 0
    \end{array}\right]
    $$
    

## Gauss-Jordan method

- The Gauss-Jordan method is an algorithmic technique used to solve systems of linear equations and find matrix inverses by transforming an augmented matrix into reduced row echelon form (RREF).
- Steps:
    - Augmented Matrix: Write the linear system as a matrix combining the coefficients and constants.
    - Row Operations: Apply three allowed actions-swap two rows, multiply a row by a non-zero number, or add a multiple of one row to another.
    - Target Form: Reduce the left side into an identity matrix (1s on the diagonal, 0s everywhere else).
    - Solution Reading: Read the final values directly from the rightmost column

## RREF - Gauss Jordon Elimination

Row Operation 1:

![](2%20System%20Of%20Linear%20Equations/images9b9eabbd-1713-4a78-97ba-0128e64a5d82-30_265_347_604_506.jpg)

multiply the 1st row by 1/2

$\begin{array}{lll}1 & 0 & 2 \\ 9 & 2 & 3\end{array}$

Row Operation 2:

![](2%20System%20Of%20Linear%20Equations/images9b9eabbd-1713-4a78-97ba-0128e64a5d82-30_261_347_902_506.jpg)

add -9 times the 1st row to the 2nd row 2:

![](2%20System%20Of%20Linear%20Equations/images9b9eabbd-1713-4a78-97ba-0128e64a5d82-30_261_404_906_1862.jpg)

Row Operation 3:

![](2%20System%20Of%20Linear%20Equations/images9b9eabbd-1713-4a78-97ba-0128e64a5d82-30_265_400_1266_506.jpg)

multiply the 2nd row by 1/2

![](2%20System%20Of%20Linear%20Equations/images9b9eabbd-1713-4a78-97ba-0128e64a5d82-30_400_392_1200_1650.jpg)

## Gauss Jordon Elimination

- $x+5 y=7$
- $-2 \mathrm{x}-7 \mathrm{y}=-5$

Step 1: Convert the equation into coefficient matrix form. In other words, just take the coefficient for the numbers and forget the variables for now:

$$
\left[\begin{array}{rrr}
1 & 5 & 7 \\
-2 & -7 & -5
\end{array}\right]
$$

Step 2: Turn the numbers in the bottom row into positive by adding 2 times the first row:

$$
\left[\begin{array}{lll}
1 & 5 & 7 \\
0 & 3 & 9
\end{array}\right]
$$

Step 3: Multiply the second row by 1/3. This gives you your second leading 1:

$$
\left[\begin{array}{lll}
1 & 5 & 7 \\
0 & 1 & 3
\end{array}\right]
$$

Step 4: Multiply row 2 by -5 , and then add this to row 1 :

$$
\left[\begin{array}{rrr}
1 & 0 & -8 \\
0 & 1 & 3
\end{array}\right]
$$

Suppose the goal is to find and describe the set of solutions to the following system of linear equations:

$$
\begin{array}{rr}
2 x+y-z=8 & \left(L_{1}\right) \\
-3 x-y+2 z=-11 & \left(L_{2}\right) \\
-2 x+y+2 z=-3 & \left(L_{3}\right)
\end{array}
$$

Solution
is $z=-1$,

$$
y=3,
$$

and $x=2$

| System of equations | Row operations | Augmented matrix |
| --- | --- | --- |
| $\begin{aligned} 2 x+y-z & =8 \\ -3 x-y+2 z & =-11 \\ -2 x+y+2 z & =-3 \end{aligned}$ |  | $\left[\begin{array}{rrr\|r}2 & 1 & -1 & 8 \\ -3 & -1 & 2 & -11 \\ -2 & 1 & 2 & -3\end{array}\right]$ |
| $\begin{aligned} 2 x+y-z & =8 \\ \frac{1}{2} y+\frac{1}{2} z & =1 \\ 2 y+z & =5 \end{aligned}$ | $\begin{aligned} L_{2}+\frac{3}{2} L_{1} & \rightarrow L_{2} \\ L_{3}+L_{1} & \rightarrow L_{3} \end{aligned}$ | $\left[\begin{array}{rrr\|r}2 & 1 & -1 & 8 \\ 0 & \frac{1}{2} & \frac{1}{2} & 1 \\ 0 & 2 & 1 & 5\end{array}\right]$ |
| $\begin{aligned} 2 x+y-z & =8 \\ \frac{1}{2} y+\frac{1}{2} z & =1 \\ -z & =1 \end{aligned}$ | $L_{3}+-4 L_{2} \rightarrow L_{3}$ | $\left[\begin{array}{rrr\|r}2 & 1 & -1 & 8 \\ 0 & \frac{1}{2} & \frac{1}{2} & 1 \\ 0 & 0 & -1 & 1\end{array}\right]$ |
| The matrix is now in row echelon form (also called triangular form) |  |  |
| $\begin{aligned} 2 x+y & =7 \\ \frac{1}{2} y & =\frac{3}{2} \\ -z & =1 \end{aligned}$ | $\begin{aligned} L_{1}-L_{3} & \rightarrow L_{1} \\ L_{2}+\frac{1}{2} L_{3} & \rightarrow L_{2} \end{aligned}$ | $\left[\begin{array}{rrr\|r}2 & 1 & 0 & 7 \\ 0 & \frac{1}{2} & 0 & \frac{3}{2} \\ 0 & 0 & -1 & 1\end{array}\right]$ |
| $\begin{aligned} 2 x+y & =7 \\ y & =3 \\ z & =-1 \end{aligned}$ | $\begin{aligned} 2 L_{2} & \rightarrow L_{2} \\ -L_{3} & \rightarrow L_{3} \end{aligned}$ | $\left[\begin{array}{rrr\|r}2 & 1 & 0 & 7 \\ 0 & 1 & 0 & 3 \\ 0 & 0 & 1 & -1\end{array}\right]$ |
| $\begin{aligned} x & =2 \\ y & =3 \\ z & =-1 \end{aligned}$ | $\begin{aligned} L_{1}-L_{2} & \rightarrow L_{1} \\ \frac{1}{2} L_{1} & \rightarrow L_{1} \end{aligned}$ | $\left[\begin{array}{rrr\|r}1 & 0 & 0 & 2 \\ 0 & 1 & 0 & 3 \\ 0 & 0 & 1 & -1\end{array}\right]$ |
| The matrix is now in reduced row echelon form |  |  |

| Gaussian Elimination | Gauss-Jordan Elimination |
| --- | --- |
| Stops at Row Echelon Form (REF) | Continues to Reduced Row Echelon Form (RREF) |
| Requires back substitution | No back substitution required |
| Faster for solving equations | Gives the solution directly |

Note: After reaching REF, you continue eliminating the entries above each pivot until the matrix reaches RREF.

Solve the following system by the Gauss-Jordan method.

$$
\begin{aligned}
2 x+y+2 z & =10 \\
x+2 y+z & =8 \\
3 x+y-z & =2
\end{aligned}
$$

Solution
We write the augmented matrix.

$$
\left[\begin{array}{ccc|c}
2 & 1 & 2 & 10 \\
1 & 2 & 1 & 8 \\
3 & 1 & -1 & 2
\end{array}\right]
$$

$$
\begin{array}{lll}
{\left[\begin{array}{ccc|c}
1 & 2 & 1 & 8 \\
2 & 1 & 2 & 10 \\
3 & 1 & -1 & 2
\end{array}\right]} & \text { we interchanged } \\
{\left[\begin{array}{ccc|c}
1 & 2 & 1 & 8 \\
0 & -3 & 0 & -6 \\
3 & 1 & -1 & 2
\end{array}\right]} & -2 R 1+R 2 \\
{\left[\begin{array}{ccccc}
1 & 2 & 1 & 8 \\
0 & -3 & 0 & -6 \\
0 & -5 & -4 & -22
\end{array}\right]} & -3 R 1+R 3
\end{array}
$$

$$
\begin{array}{lcc|c}
{\left[\begin{array}{cccc}
1 & 2 & 1 & \mid \\
0 & 1 & 0 & \mid \\
0 & -5 & -4 & 2 \\
-22
\end{array}\right]} & \mathrm{R} 2 \div(-3) \\
{\left[\begin{array}{ccc|c}
1 & 0 & 1 & 4 \\
0 & 1 & 0 & 1 \\
0 & 0 & -4 & 2 \\
-12
\end{array}\right]} & -2 R 2+R 1 \text { and } 5 R 2+R 3 \\
{\left[\begin{array}{lllll}
1 & 0 & 1 & \mid & 4 \\
0 & 1 & 0 & \mid & 2 \\
0 & 0 & 1 & \mid & 3
\end{array}\right]} & R 3 \div(-4) \\
{\left[\begin{array}{lllll}
1 & 0 & 0 & \mid & 1 \\
0 & 1 & 0 & \mid & 2 \\
0 & 0 & 1 & \mid & 3
\end{array}\right]} & -\mathrm{R} 3+\mathrm{R} 1
\end{array}
$$

Clearly, the solution reads $x=1, y=2$, and $z=3$.

## Vectors

- A vector is a mathematical way of representing multiple related pieces of information together.
- In Data Science, almost everything eventually becomes a vector of numbers.
- A vector can be represented as: $\quad \mathbf{x}=\left[\begin{array}{l}2 \\ 5 \\ 3\end{array}\right]$
- Think of this as one data record with three features.
- Data has to be converted into numerical representations before most machine-learning algorithms can process it.
- Vectors are the basic format in which machine-learning models receive information.
- A typical ML problem looks like:
- x→ Machine Learning Model → ŷ

where:

$$
\begin{aligned}
& \mathbf{x}=\text { feature vector } \\
& \mathbf{y}=\text { target/output } \\
& \hat{\mathbf{y}}=\text { predicted output }
\end{aligned}
$$

- Vectors are the basic format in which machine-learning models receive information.
- In school mathematics, we often think of a vector as an arrow. In Data Science, think of a vector as a numerical description of an object, observation, or data point.

## Vectors - Language of representing data

A vector is a mathematical object that has both magnitude (size) and direction.

- Think of a vector as an arrow.
    - The length of the arrow represents its magnitude.
    - The direction in which it points represents its direction.
- For example:
    - An arrow pointing 5 units to the right is a vector.
    - An arrow pointing north with a length of 10 km is also a vector.

![](2%20System%20Of%20Linear%20Equations/images9b9eabbd-1713-4a78-97ba-0128e64a5d82-38_458_1257_1342_29.jpg)

$$
\vec{w}=a \vec{u}+b \vec{v}
$$

![](2%20System%20Of%20Linear%20Equations/images9b9eabbd-1713-4a78-97ba-0128e64a5d82-38_474_491_1332_1943.jpg)

![](2%20System%20Of%20Linear%20Equations/images9b9eabbd-1713-4a78-97ba-0128e64a5d82-39_1768_2129_49_164.jpg)

- Example: Find the augmented matrix of the system of equations. $\left\{\begin{array}{l}-x-4 y-9 z=-7 \\ -3 x-4 y-5 z=-4 \\ -2 x-3 y-6 z=-3\end{array}\right.$

## Vectors to Vector Equation

- Example: Find the augmented matrix of the system of equations. $\left\{\begin{array}{l}-x-4 y-9 z=-7 \\ -3 x-4 y-5 z=-4 \\ -2 x-3 y-6 z=-3\end{array}\right.$

## Vector Equations

- Example: Find the augmented matrix of the system of equations. $\left\{\begin{array}{c}-x-4 y-9 z=-7 \\ -3 x-4 y-5 z=-4 \\ -2 x-3 y-6 z=-3\end{array}\right.$
- Example: Find the augmented matrix of the system of equations. $\left\{\begin{array}{l}-x-4 y-9 z=-7 \\ -3 x-4 y-5 z=-4 \\ -2 x-3 y-6 z=-3\end{array}\right.$
- Example: Find the augmented matrix of the system of equations. $\left\{\begin{array}{l}-x-4 y-9 z=-7 \\ -3 x-4 y-5 z=-4 \\ -2 x-3 y-6 z=-3\end{array}\right.$

## How does this become a System of Equations?

- Example: Find the augmented matrix of the system of equations. $\left\{\begin{array}{l}-x-4 y-9 z=-7 \\ -3 x-4 y-5 z=-4 \\ -2 x-3 y-6 z=-3\end{array}\right.$

## Span of vectors

- Example: Find the augmented matrix of the system of equations. $\left\{\begin{array}{c}-x-4 y-9 z=-7 \\ -3 x-4 y-5 z=-4 \\ -2 x-3 y-6 z=-3\end{array}\right.$

: Example: Find the augmented matrix of the system of equations. $\left\{\begin{array}{l}-x-4 y-9 z=-7 \\ -3 x-4 y-5 z=-4 \\ -2 x-3 y-6 z=-3\end{array}\right.$

$$
\mathbf{u} \in \operatorname{Span}\left\{\mathbf{v}_{1}, \mathbf{v}_{2}\right\} .
$$

## Q4. Does

$$
\mathbf{w}=\left[\begin{array}{l}
5 \\
7
\end{array}\right]
$$

belong to the span of

$$
\left[\begin{array}{l}
1 \\
0
\end{array}\right],\left[\begin{array}{l}
0 \\
1
\end{array}\right] ?
$$

We need:

$$
a\left[\begin{array}{l}
1 \\
0
\end{array}\right]+b\left[\begin{array}{l}
0 \\
1
\end{array}\right]=\left[\begin{array}{l}
5 \\
7
\end{array}\right]
$$

This gives:

$$
\left[\begin{array}{l}
a \\
b
\end{array}\right]=\left[\begin{array}{l}
5 \\
7
\end{array}\right]
$$

Therefore:

$$
a=5, \quad b=7
$$

So:

$$
\mathbf{w}=5 \mathbf{u}+7 \mathbf{v}
$$

- Example: Find the augmented matrix of the system of equations. $\left\{\begin{array}{l}-x-4 y-9 z=-7 \\ -3 x-4 y-5 z=-4 \\ -2 x-3 y-6 z=-3\end{array}\right.$

$$
\mathbf{u}=\left[\begin{array}{l}
1 \\
2
\end{array}\right], \quad \mathbf{v}=\left[\begin{array}{l}
3 \\
6
\end{array}\right]
$$

1. Are they collinear?

Observe:

$$
\mathbf{v}=3 \mathbf{u}
$$

because:

$$
3\left[\begin{array}{l}
1 \\
2
\end{array}\right]=\left[\begin{array}{l}
3 \\
6
\end{array}\right]
$$

Therefore, they are collinear.
Yes
2. Are they linearly independent?

No. Since:

$$
\mathbf{v}=3 \mathbf{u}
$$

one vector can be obtained from the other.

- A vector belongs to the span of a set of vectors if it can be expressed as a linear combination of those vectors.”

For example, $\mathrm{w}=3 \mathrm{u}-2 \mathrm{v}$, means w belongs to $\boldsymbol{\operatorname { s p a n }} \boldsymbol{\{} \mathbf{u}, \mathbf{v} \boldsymbol{\}}$.

- Span means all possible linear combinations of the given vectors.
- It tells you which vectors can be generated from a set of vectors.
- If the vectors are linearly independent, they span a larger space.
- If the vectors are linearly dependent, some vectors are redundant and do not increase the span.

## Linear Independence and Dependence of Vectors

- Given any set of $m$ vectors $\mathbf{a}(1) \ldots . \mathbf{a}(m)$ (with the same number of components), a linear combination of these vectors is an expression of the form

where $c 1, c 2 \ldots \ldots c m$ are any scalars.
    
    $$
    c_{1} \mathbf{a}_{(1)}+c_{2} \mathbf{a}_{(2)}+\cdots+c_{m} \mathbf{a}_{(m)}
    $$
    
- Now consider the equation
    
    $$
    c_{1} \mathbf{a}_{(1)}+c_{2} \mathbf{a}_{(2)}+\cdots+c_{m} \mathbf{a}_{(m)}=\mathbf{0} .
    $$
    
- Clearly, this vector equation (1) holds if we choose all ’s zero, because then it becomes
- . If this is the only $m$tuple of scalars for which (1) holds, then our vectors
- are said to form a linearly independent set or, more briefly, we call them
- linearly independent. Otherwise, if (1) also holds with scalars not all zero, we call these
- vectors linearly dependent. This means that we can express at least one of the vectors

## Row Echelon Form and Information From It

- At the end of the Gauss elimination the form of the coefficient matrix, the augmented matrix, and the system itself are called the row echelon form.
- In it, rows of zeros, if present, are the last rows, and, in each nonzero row, the leftmost nonzero entry is farther to the right than in the previous row.
    
    $$
    \left[\begin{array}{rrr}
    3 & 2 & 1 \\
    0 & -\frac{1}{3} & \frac{1}{3} \\
    0 & 0 & 0
    \end{array}\right] \quad \text { and } \quad\left[\begin{array}{rrr:r}
    3 & 2 & 1 & 3 \\
    0 & -\frac{1}{3} & \frac{1}{3} & -2 \\
    0 & 0 & 0 & 12
    \end{array}\right] .
    $$
    
- At the end of the Gauss elimination (before the back substitution), the row echelon for of the augmented matrix will be

The original system of $m$ equations in $n$ unknowns
    
    ![](2%20System%20Of%20Linear%20Equations/images9b9eabbd-1713-4a78-97ba-0128e64a5d82-53_554_862_580_708.jpg)
    

Here, and all entries in the blue triangle and blue rectangle are zero. The number of nonzero rows, $r$, in the row-reduced coefficient matrix $\mathbf{R}$ is called the rank of $\mathbf{R}$ and also the rank of $\mathbf{A}$.

Reinforcement Learning Questions

- Example: Find the augmented matrix of the system of equations. $\left\{\begin{array}{l}-x-4 y-9 z=-7 \\ -3 x-4 y-5 z=-4 \\ -2 x-3 y-6 z=-3\end{array}\right.$

Q. Gaussian Elimination uses:

1. Forward elimination only
2. Forward elimination followed by back substitution
3. Back substitution only
4. Matrix inversion only

Q. Which of the following best describes the difference between Gaussian Elimination and Gauss-Jordan Elimination?
A) Both methods always produce the same intermediate matrices.
B) Gaussian Elimination stops at REF and uses back substitution, while Gauss-Jordan Elimination continues to RREF, allowing the solution to be read directly.
C) Gaussian Elimination can only solve 2 × 2 systems.
D) Gauss-Jordan Elimination cannot solve systems with three variables.
Q. Which of the following is not necessarily true for REF?

1. Leading entries move to the right as you go down the rows.
2. Rows containing all zeros are at the bottom.
3. Every pivot is 1 .
4. Entries below each pivot are zero.
- Example: Find the augmented matrix of the system of equations. $\quad\left\{\begin{array}{c}-x-4 y-9 z=-7 \\ -3 x-4 y-5 z=-4 \\ -2 x-3 y-6 z=-3\end{array}\right.$

From the final reduced row-echelon form (RREF),

$$
x=\frac{34}{13}, \quad y=\frac{11}{13}, \quad z=\frac{33}{13}
$$

## Solve by Gauss Jordon method

Q1. A bowl of corn flakes, a cup of milk, and an egg provide 16 grams of protein. A cup of milk and two eggs provide 21 grams of protein. Two bowls of corn flakes with two cups of milk provide 16 grams of protein. How much protein is provided by one unit of food?

Q2. Two apples and four bananas cost $2.00 and three apples and five bananas cost $\$ 2.70$. Find the price of each.